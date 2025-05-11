---
description: >-
  How the modeling of operating assets differs from the modeling of
  pre-construction assets, and how a good model can help your asset management
  and operations teams.
---

# Modeling of Operating Assets (IN PROGRESS)

## Intro

If you were able to attend my talk at PVPMC 2025, this is the long form version of the information presented there.  Feel free to skim to get to the more detailed bits!\


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


<figure><img src="../../.gitbook/assets/image (34).png" alt=""><figcaption><p>Orienting ourselves again</p></figcaption></figure>

### Going Deeper

