# Expanding Pelican Origin Monitoring

Fellow: Patrick Brophy  
Mentors: Haoming Meng & Justin Hiemstra  
Fellowship Dates: 06/03 \- 08/23

## Background

The [Pelican Platform](https://pelicanplatform.org) plays a pivotal role in enabling researchers to seamlessly deploy and manage their data across a federated network. At the core of this platform lies the Origin service, a critical component that ensures data accessibility across the federation. The stability and performance of the Origin service are vital; any disruptions or failures could render the data inaccessible, undermining the very purpose of the federation. Consequently, maintaining a robust monitoring framework for the Origin service is not just necessary but essential for the continued success of data federation efforts. Understanding the health and performance metrics of the Origin service is crucial for administrators and users alike who rely on this data for their scientific and research endeavors.

## Project Description

The primary objective of this project was to elevate the monitoring capabilities of the Origin service by introducing new metrics and developing enhanced visualizations. The project was designed with a phased approach, starting with the Origin server and potentially extending to other components like the cache and director servers, depending on the time available. The intention was to provide a more granular view of the service's performance and health, thereby improving observability and aiding administrators in proactive maintenance and troubleshooting. By identifying key performance indicators and implementing new metrics, this project sought to provide a more comprehensive understanding of the service's operations and potential bottlenecks.

## Project Outcome

The project culminated in the development of a new Grafana dashboard tailored specifically for the Origin service, accompanied by several newly created metrics that offer deeper insights into the system's performance. The design and implementation of the dashboard were heavily influenced by feedback gathered through a user study conducted with system administrators from CHTC and OSG. This iterative process ensured that the final product was not only technically sound but also user-centric, addressing the real-world needs of those who manage and rely on the Pelican Platform. The introduction of these new metrics has significantly enhanced the transparency and observability of the Origin service, enabling administrators to detect issues earlier and make more informed decisions.

I also gave a lightning talk at [HTC24](https://agenda.hep.wisc.edu/event/2175/). You can watch it here.
[![My lightining talk](https://img.youtube.com/vi/EeFGRD29fSw/0.jpg)](https://youtu.be/EeFGRD29fSw?si=EIt5mC7xxv8eQZ31&t=972)


Here is a [link](https://github.com/PelicanPlatform/pelican/pulls?q=is%3Apr+is%3Aclosed+author%3Apatrickbrophy) to all my contributions to the Pelican Platform.

## Recommendations for Next Phase of Project

For the next phase of the project, would be to build out dashboards for the other Pelican services. This shouldn’t be a large undertaking but there would be some differences between them. I’d also recommend building out notifications within Pelican for alerting when a federation or any individual service is unhealthy. I would also recommend adding the ability to use an external prometheus service, this is because the way we run Prometheus can cause all sorts of performance issues and also defeats the purpose of having telemetry separate from your application so that you can gain observability when your application is down. Lastly, develop more metrics within XRootD to provide more observability. I also thought that a Prometheus plugin to XRootD could be beneficial for XRootD system admins.

## Lessons Learned

Throughout the fellowship I’ve learned lessons about engineering, design, and the importance of building tools to support science. With engineering, I learned about how Pelican works, the philosophy behind high throughput computing, and the rigor required to build production grade software. On design, I learned that users don’t always know what they want. When designing the origin dashboard, I conducted user studies with system admins, and I took away from those studies that they really don’t know what they need. They have ideas about what may be helpful, but not what they need. Yet, when designing the dashboard, I learned about designing layouts and presenting information meaningfully is important for understanding what is going on within the origin. Lastly, I learned about the importance of building tools to support science. If you squint hard enough, CHTC is like the second derivative of research outcomes, science being the first derivative of research outcomes. Science produces research outcomes and we at CHTC try to accelerate science. Being an accelerator is rewarding because you get very immediate feedback. When acceleration increases so does the velocity and position. In terms of CHTC, more science gets done and more results are developed. As a fellow, I have felt even though my impact may be small, I am thrilled to be a part of the acceleration, pushing science forward.

## Project Material Links and Descriptions

Pelican \- [https://pelicanplatform.org](https://pelicanplatform.org/)  
Prometheus \- [https://prometheus.io/](https://prometheus.io/)  
Grafana \- [https://grafana.com/](https://grafana.com/)  
XRootD \- [https://xrootd.slac.stanford.edu/index.html](https://xrootd.slac.stanford.edu/index.html)
