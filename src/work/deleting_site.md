# Deleting a whole site in the database

This one is actually one of my favourite stories to tell where Software helped us save a lot of time.
At work we were using a software to manage the physical access control for a huge customer.
One of the sites had to be offboarded and unfortunately it was absolutely massive.
When deleting something out of that software it was required to delete anything that depends on it first, the structure looked something like this:

- Site
  - Access Control Hardware
    - Access Control Card Readers
    - Elevators
    - I/O

Logically there were some more structures that depended on the hardware:

- Clearance Codes containing Elevators and Readers
- Persons were then assigned Clearance Codes to manage where they can get access
- Status Groups for the hardware
- etc.

So when we went to finally delete the site we realized we would have to rip it all out.
There was no option to delete the site and all its dependencies from the software.
That meant removing all the relevant clearance codes from all Persons, then removing all clearance codes, all Readers, all I/O and so on.
We estimated it to take at least 2 weeks to rip it all out because there were not options to to anything automatically and one would have to manually click through all of it.

There must be a better way, right?
And there was, you can delete it all in the database directly.
Creating a script took a few hours but still saved a lot of time in the long run.
Luckily the naming scheme for the sites was consistent, everything was marked with a unique identifier and then it was just figuring out what else needed to be deleted.

So if you think there is no easy way to do something, maybe there is ;)
