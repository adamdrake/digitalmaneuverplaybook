---

title: "01 - Measure Progress"

---

In order to achieve a goal it is necessary to determine whether or not progress is being made towards that goal **and** whether or not further progress is worth the additional effort.

In order to do this, having appropriate metrics is a prerequisite to any change management effort, technical or otherwise.

It is important that metrics be representative of the actual goal to be achieved and not some poor proxy thereof.  Focus on creating **few** metrics to measure in order to determine progress since it is easy to tell competing stories as more metrics are added.

By [Goodhart's Law](https://en.wikipedia.org/wiki/Goodhart%27s_law) we know that "When a measure becomes a target, it ceases to be a good measure."  In other words, people are going to game the system and that compromises the integrity of the metric in question.  One way to deal with this is to **choose competing metrics**.  For example, a company might have a metric on profit, while also having a metric on customer satisfaction.  Considering these two metrics together prevents an organization from optimizing profit by cutting expenses severely and also prevents optimizing customer satisfaction at the expense of profit reduction.  Choose few, competing, metrics.

## Technical metrics

In addition to non-technical metrics, it is also important to have proper metrics, monitoring, telemetry, etc. for software.

Keep track of things like memory usage, CPU usage, request time latency (in 99th percentile, not average), and so on.

Average anything is almost always bad for such metrics.  Use either median or 95th/99th percentile in order to get an accurate picture.

There will be two sections here, technical and non-technical.

From a user perspective, consider things like [Usability.gov](https://usability.gov) and the [System Usability Survey](https://www.usability.gov/how-to-and-tools/methods/system-usability-scale.html) and make user metrics one of the top things you consider in the success of your system.  Concepts like Net Promoter Score may also be appropriate, though they have their own flaws and caveats.
