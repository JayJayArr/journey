# Deploying vs Maintaining

This one will be a story about manpower.
Some of you may have read about the mythical man-month, and it might connect a little here.

Imagine for a moment, that you sell customers a server(It's Windows, I'm sorry) with a software you provide, some workstation clients with the client version of that software(Windows as well) and around 10 enclosures of hardware that you handwire.
From time to time you interconnect some different systems, a customers wants some tweaks here and there, you build some special functionality, etc.
If your company is big enough you would soon have a dedicated team for those products.

And of course most of these companies do not want to maintain their own team of engineers to keep those systems up and running.
Well, most IT teams don't even want to do the patching on those systems.
So they will happily pay you to maintain those systems.
Maybe some quarterly OS patching here, some software updates there, but some customers even decide to not maintain those systems at all.
"Never change a running system" can go well for a long time, but if you do not want to change that system, please at least maintain it.
I encountered some situations where servers came down because of a failing RAID 5 that used to have a hot spare disk.
A RAID taking two month to rebuild? Sure, that's normal.
Sometimes you find a Windows Server 2012 Running somewhere or even a Windows XP if you want.
Of course running a software version that is not supported anymore since the last decade.

So riddle me this:
If you have a small team of engineers who install those new systems, how big should your team be to maintain those systems?

1. one person
2. the same size as the team installing the systems
3. humongous and growing steadily as new systems are onboarded

You know the theoretical answer and how it is in real life could not be further apart.
That might be because of sales (maintained systems do not count when you look at the sales staff), but the situation you have here might be a deadlock.
You have one or two persons who maintain those systems and of course it is a nightmare for them.
Customers will call them every day to get some small things changed, and they will call because if they call they will get it.
But if the customers convert your Maintenance staff into a call center (requesting new things they actually don't pay for) who will do the maintenance?
Well, you would start to reach out to the installation team for anything that can be done remotely and they will demand to plan ahead.

Congratulations! You have just successfully convertet your maintenance team into a permanent call center for hardware related issues.
And at the same time converted the engineering/installation team to an IT team that has to support the maintenance team.
What will happen now?
Well the people working in the maintenance/service team will never again look at a software as they will not be able to keep up with new stuff coming out.
At the same time the installation team will have to handle the software maintenance on hundreds of systems in addition to new projects coming in.
This will first of all slow down your installation team and at the same time degrade the quality of the work they can do as they have to handle aditional tasks.
In the next step the engineering will start to dedicate people to the maintenance topic.
You now have two different teams doing (partially) the same thing badly, and what do you of course do in that case?
Stupid question, move the maintenance staff that was created on the installation team to the overworked maintenance staff in the maintenance team, they are doing the same stuff anyways.
Now we have completed the first full circle.
They will get pulled into the call center work and not be able to keep up with new developments and you start again to offload work to the installation team.

There you go, your maintenance team will have to draft off of the installation team and the installation team has to hire new people.
The people in the installation team will hate the maintenance team for that and vice versa.
And people in the maintenance team will quit because they understandably did not sign up for call center work which will further enhance the problem.

So you hire in the instllation team, force them to work maintenance, move them to maintenance and they will quit there, what a world to live in.
The only solution to this in my opinion is to go full ham on the maintenance team, move a BUNCH of skilled personell there to make it a happy place and overpay them to keep them happy.
And who in their right mind would do that rather then enhancing the installation team (that's where sales is happening, don't forget it).
