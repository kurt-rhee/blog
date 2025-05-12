---
description: >-
  How the modeling of operating assets differs from the modeling of
  pre-construction assets, and how a good model can help your asset management
  and operations teams.
---

# Modeling of Operating Assets (IN PROGRESS)

## Intro

If you were able to attend my talk at PVPMC 2025, this is the long form version of the information presented there.  Feel free to skim to get to the more detailed bits!\
\
As always, this blog is painstakingly written by hand without AI because I like writing things and because AI writing isn't fun to read.\


## Too Long Didn't Read

* The Pro Forma model is often used to determine if an operating asset is under-performing.  But the Pro Forma is a simplification of the actual plant and is also built on assumptions that are not knowable at the time of construction completion.  This means that it is a good financial tool but a poor diagnostic one.

## A Journey into the Iceberg of Under Performance

One way I like to think about performance engineering in the post-construction world is that we performance engineers are like divers on a mission.  We have been hand-picked to go to (technical) depths that others cannot go, with specialized tools and knowledge to help us get there and make sense of what we see.\
\
The question from our superiors, as always, is "can we make more money?"  But that can be translated to "Is this asset under-performing?" and "why is it under-performing?"  \


### The top of the Iceberg

Let's say we have a 300 MWac / 402 MWdc PV project called Hidden Mesa.  At this site there are:

* 2 different tracker manufacturers
* 2 different module families
* 6 different module bins
* 5 different met stations
* DC line losses up to the combiner differ by up to 2%

What might you do first?  Maybe look at the meter power.  I obscured the y-axis here and on a lot of the rest of the charts to not give away any customer data.  I've also used data from a few different sites so that no one site is identifiable.

<figure><img src="https://lh7-rt.googleusercontent.com/slidesz/AGV_vUfl-202ItKo5-mYZ8ZjJw0Jv3E5PVu9ov4BDUdHR7OXoA7IeRfK9vSX8M-EAsihhKQw8uh2tQJypV8oc2KSONzsvU9XzfFjMvDYI-QR36j4Z_CGUsr68XC3HgXtJiTwnNSDHvF0=s2048?key=Bar0iCcOCseUXIr3xR7ZdDoL" alt=""><figcaption><p>Meter Power at Hidden Mesa PV Site</p></figcaption></figure>

Let's say that the peak power here is 259 MW.  That is about 86% of plant AC capacity.  Can we tell if the plant is under-performing?  Probably not, it could be sunny but not bright enough to reach clipping levels.  Let's look at this with POA data included.\


<figure><img src="https://lh7-rt.googleusercontent.com/slidesz/AGV_vUd5byKKrvBEKd9ram-3OVGaf7150AseRWcDaX896M5qABcgh52ErHULGu4-8BLdv7RFmRG3AVB7CDMKVYKI1n3ObIA7gi2eLzRMUtnaMVyuQiDqxWkpL0coVlpn3MgA-0I_oPR9bQ=s2048?key=Bar0iCcOCseUXIr3xR7ZdDoL" alt=""><figcaption><p>Meter Power and POA at Hidden Mesa</p></figcaption></figure>

Let's say POA is 800 W/m^2.  That is 80% of STC.  If you remember that the plant DC capacity is 402 MWdc then we are producing around 64% of peak DC capacity.  Now your ears are ringing.  Something is going on at this site. &#x20;



<figure><img src="../../.gitbook/assets/image (33).png" alt=""><figcaption><p>Orienting ourselves</p></figcaption></figure>

\
\
At this point in our dive we are still above the water.  No specialized tools are needed.  A college student with excel could make these charts.  Let's break the surface now.



### The Surface

The next tool you might reach for if you have it is a performance index (ratio of actual meter power to modeled meter power).  \
\


<figure><img src="https://lh7-rt.googleusercontent.com/slidesz/AGV_vUdf2ROnlomxSWTH11fG7uO9Cx68rko2YT5kWq-XzreJT25K2JoSJGLsp4dfyNmCiy6UBGSmG7p7WIjThL37MT8zE29vkAsYIHb5RVvk2mhTwegfJ6BZ421Oy5OEQgvQIsORZp9ttA=s2048?key=Bar0iCcOCseUXIr3xR7ZdDoL" alt=""><figcaption><p>Performance Index at Hidden Mesa.  Actual meter power in blue, Modeled meter power in orange.</p></figcaption></figure>

Now it is very apparent that something is happening at this site.  Let's say that the asset is under-performing about 15% relative to the modeled site.\
\
Oh and by the way you don't necessarily need a performance index here though I think it is probably the easiest and best tool to use.  In the right hands a performance ratio, temperature corrected performance ratio, a regression model or a ML model would work okay.\
\
I personally like performance index because I find performance ratio's hard to understand without having a lot of experience with the site and some regression / ML models bake in the site's past performance into the model.   If the site has performed correctly less than it has performed badly, then the model expects poor performance, which is kind of  like a machine form of  "learned helplessness."\
\
But, if you have worked on the operational side before, you know that sometimes we don't get the drawing set or the original model to work with, and are often given a large portfolio of projects to monitor.  If you working on hundreds of distributed or commercial sites, making a performance model for each one just isn't practical.  \


<figure><img src="../../.gitbook/assets/image (34).png" alt=""><figcaption><p>Orienting ourselves again</p></figcaption></figure>

### Going Deeper

As we try to determine what is going wrong with the project, there are a few root causes that are easy to rule out.   Let's go through some of them quickly here:\




* Trackers aren't stuck, we would be able to tell in the meter power graph. &#x20;
  * The evening or morning production would be higher if they were stuck east or west.
  * It would look like a fixed tilt single humped graph if they were stuck in the middle.
* Soiling looks minimal
  * ![](<../../.gitbook/assets/image (36).png>)

What about the inverters?  Are any of them offline?\


<figure><img src="../../.gitbook/assets/image (37).png" alt=""><figcaption><p>Real Time Inverter Output at 12:00 P.M. at Hidden Mesa</p></figcaption></figure>

Note that the y-axis has been truncated.  I'll tell you that 16 is offline and 02 and 12 are under-performing seriously.  But what about 19?  It looks lower than its neighbor 18.

<figure><img src="../../.gitbook/assets/image (38).png" alt=""><figcaption><p>Same graph but normalized by DC Input</p></figcaption></figure>

Okay actually, 19 is fine when normalized.  This sort of normalization is even more apparent at the combiner level.\
\


<figure><img src="../../.gitbook/assets/image (39).png" alt=""><figcaption><p>Combiner output before and after normalization by installed capacity</p></figcaption></figure>

People who have worked with data at or below the combiner level are probably angry at this point, because unless you have an enlightened EPC and SCADA team, there is no way that this normalization is going to work.  (If you need a recommendation for an EPC that gets this right, I can pass a name along) You see, one of the problems that is happening right now in our industry is that there is not often good communication between the two groups.  \
\
The problem goes like this, the EPC team comes in and installs all of the combiners and then buries all of the cables underground.  Then the SCADA team comes through and has no idea what cable goes to which combiner.  They just randomly assign numbers and call it a day.  Each combiner has a different amount of DC capacity installed on it and then the denominators of your normalization function are complete trash.

There are two ways to remedy this.  You can turn off combiners one by one and see which ones go offline in your data stream.  Or you can read your live data stream and re-map the data based off of an algorithm.   As far as I know there are two algorithms for doing this, one by Dr. Joe Ranalli which was presented at PVSC 2024 and another by Proximal's own Rob van Haaren.  \
\


<figure><img src="../../.gitbook/assets/image (40).png" alt=""><figcaption><p>van Haaren, R. (2025). Unscrambling combiner box SCADA tags using time series data. In Proceedings of the Photovoltaic Reliability Workshop (PVRW) 2025</p></figcaption></figure>

So, orienting ourselves again, now we are using some pretty specialized tools.  Generally we're comparing the data stream coming off of a device to it's neighbors to see if the device is different in any way.  Sore thumbs and under-performing devices stick out.  Machine Learning tools shine in this layer of analysis.\
\


<figure><img src="../../.gitbook/assets/image (41).png" alt=""><figcaption><p>Very specialized tools required </p></figcaption></figure>

I think this is the point where most available commercial tools stop, at least in 2025.  But I think we can go deeper.  It's actually almost tautological that I think we can go deeper.  Why go work for a startup in a space if you don't believe that you can improve the solutions to some of the problems within that space?\
\
So where can we go from here?\
\
I think we can go pretty far if we could have a unique performance index for each data emitting device in the project.\
\
\


<figure><img src="../../.gitbook/assets/image (42).png" alt=""><figcaption><p>Where I think we can go</p></figcaption></figure>

There is a reason nobody (as far as I know) has gone here yet.  It's trivial from a performance modeling perspective to run a bunch of models, but it's hard from a software engineering perspective to run as many models as you would have to run to get device level performance models.\
\
Imagine this: If you have a 600 MWac project, you'll have about 3000 combiners to model.  If you ran 3000 performance models at a 5 minute interval, that would be 36,000x performance models you would have to run relative to your standard one year of 8760 data at the meter level.\
\
Not only would that take along time, it also takes up a lot of computer memory.  A LOT.  Now imagine you have to do this across a fleet of projects, for every combiner, every five minutes.\
\
Luckily there are tricks in the field of computer science which can help us.  First off, you can use a faster programming language, and most of the software companies that do performance modeling choose to use relatively fast languages.\
\
PVsyst uses object Pascal.\
PlantPredict and SolarFarmer use C#\
SAM uses C++

You can also employ the cloud to parallelize all of these calculations across a bunch of different servers.  PlantPredict already does this by creating new servers when a lot of people are using the application.  Proximal takes it a step further and gives each project it's own dedicated modeling server-lette.  \
\
The final thing you can do is employ algorithms to increase speed and decrease memory usage.  We figured that we could use a common algorithm to compress all unique inputs to a pvlib function, only run pvlib on the absolute most unique inputs and then decompress the result set over all of the devices.  After all, many PV modules may be at the same angle for instance or have the same soiling amounts.  Plus by leveraging pvlib, all of our users know exactly what code is being run and they can contribute to our model at any time.\
\
So we built a custom model chain which compresses and decompresses the inputs and outputs of individual pvlib functions and combines this all into one custom model chain.\


<figure><img src="../../.gitbook/assets/image (43).png" alt=""><figcaption><p>Algorithms for Performance Modeling</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (44).png" alt=""><figcaption><p>docs.proximal.energy</p></figcaption></figure>

So why go through all of this extra work?  \
\
Well, because you get a lot more utility out of your model this way.  You set it up once and reap the rewards over the entire 35 year lifetime of the project.\
\
For example, you have x met stations on your site.  Why not use all x met stations worth of data?  Older models only allow you to have one met file per model.  This lets your have a performance index that is responsive to intermittent and moving clouds at the device level.\
\
You can also see Geo-spatially what is happening at the site, which helps when coordinating with field personnel.\
\


<figure><img src="../../.gitbook/assets/image (45).png" alt=""><figcaption><p>Geo-spatial performance index</p></figcaption></figure>

You can even sort the results by module families.  Imagine if you have two module series A and module series B on site.  You could separate the performance index by the module family and see if one is performing better or worse than another.  \
\


<figure><img src="../../.gitbook/assets/image (46).png" alt=""><figcaption><p>Module Family Level Performance Index</p></figcaption></figure>

This is all powered by the fact that we can run performance models at any arbitrary level of depth.  If you can go as deep as you want, then filtering and grouping by any metric becomes trivial.  \
\
You can even slide and dice by bin class.

<figure><img src="../../.gitbook/assets/image (47).png" alt=""><figcaption><p>Performance Index by Bin Class</p></figcaption></figure>

So what are we left with now.  We have a model that is as transparent as possible because it is literally using pvlib as its engine.  You can set it up once and forget about it.  It makes pretty maps.   I think it is a pretty powerful diagnostic tool and it was relatively simple (6 months-ish?) to build because pvlib is so awesome.  \
\
I hope this blog post was interesting for you, it was fun for me to work on.  If you are interested in how any of this works feel free to reach out, I'm happy to help think about how this might apply to your work even if you don't care about using Proximal at all!\
\


<figure><img src="../../.gitbook/assets/image (48).png" alt=""><figcaption><p>Last slide of the PVPMC Presentation for the laughs</p></figcaption></figure>
