# Replacing .csv with T-SQL

In your life you undoubtedly have touched a .csv file if your job involves IT.
And even if you consider Microsoft Excel to be your daily bread and butter you might have unknowingly worked with them.

The idea of saving 2 dimensional data in a file by delimiting every column with a separator it genius, although it has its own limits.

Regularly at work we had to import some chunks of data into a customer database.
When I started to work there one of my first tasks was to import a big chunk into that database.
Luckily the software we used offered a tool for importing from a delimited text file.

Normally those imports would range from a few dozen lines to a few hundred lines.
Well when my boss left for vacation he transferred me all the files for an import containing half a million records.
I have to add, that this table in the database at that time was made up of around 1 million datasets, and I would have to add half a million more - CREEPY.
So I tested the import beforehand. I created a backup of that database and tried the import with a dataset of a few dozen rows.

Now imagine anything going wrong and not knowing SQL queries (as I did at that time).
If anything went wrong, we would go into the software and delete/correct all the wrong datasets BY HAND.
I didn't know there is an option for a database-rollback, but at least I was made aware of the backup/restore options, so that was helpful.
So even if I found a field to mark all the entries I was importing I had no way of correcting it as a bulk.
I could find them all, but not correct them.

When you imported the datasets via the import tool you didn't get a detailed log of the import (entries net being inserted, total number of failures, etc.).
But if you created the import profile and started it via the command line you would get the log, but couldn't see how far the import was.
It was either detailed log or status bar.
We definitely needed the log in case anything went wrong, so I didn't know if it was actually doing anything or failing on each and every single dataset one by one.

So there I was, my boss being on vacation (available, sure, but who wants to page his boss from vacation) and I was sitting there as a new employee who has to handle the import.
I prepared the .csv file (yes, I did ONE big import, not a few different chunks, who needs that, right?).
I double checked the delimiter character (we used a | as the delimiter).
I triple checked the delimiter character and the whole file for good measure.
I had checked that the import worked correctly with a smaller dataset.
I did have and idea of how long the import might take, I stopped the time using 100 rows and tried to extrapolate the time it might take though, my estimate was 30 mins.
I went into the cmd and started the import.

Now it was waiting time.
I couldn't just let it import and come back when it was done.
In case I screwed over the whole DB I had to stand by and restore the backup.
To keep it short my estimate was s\*\*\* and it made me nervous.
It took a whole two hours during which I was staring at the screen and trying to find signs in the software that anything had gone wrong.

This occasion made me learn SQL as one of my first languages just to be able to correct things in the database, revert stuff in case something went wrong anf finally being able to skip the import tool as a whole.
You know, to save license cost on the import tool we mostly were using once and then never again for every customer.

Just learn SQL in case you are messing in databases.
