# Oopsies

This page is dedicated to all the oopsies I did at work.

### Limiting MSSQL-Server RAM to the absolute minimum

One of my worst mistake was definitely reducing the maximum RAM on a MSSQL-Server in production.
I accidentally set it to the absolute minimum (512 MB) and then actually restarted the service.

The question "How did this happen by accident?" will stay my secret.

What happens then you might ask? It does still start, but you cannot connect to it via SSMS as it is lacking suffficient RAM.

After some searching online under time pressure I found out that it is not bricked and can be recovered.
Then only way to connect is via sqlcmd, so that's exactly what we tried.

```cmd
sqlcmd -S. -E
```

Then you wood try to increase the RAM, first of all configure the advance options.

```SQL
sp_configure 'show advanced options', 1;
GO

RECONFIGURE
GO
```

This one worked fine so far, onto the second part:

```SQL
sp_configure 'max server memory', 4096;
GO
RECONFIGURE;
GO
```

The answer to this command was a classic "out of memory" message, the RECONFIGURE failed because of the missing RAM.
So we restarted the service, and no surprise, the memory was still limited to the minimum.

It seems like it is just enough for one RECONFIGURE.
So I retried the action, first one was fine, second one was failing again. It took some time to realize, that the first command does not need to be issued on every reconnect.

And Success!

Stressful hour that was.
