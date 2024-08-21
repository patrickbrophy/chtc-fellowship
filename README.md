# Expanding Pelican Origin Monitoring

Fellow: Patrick Brophy  
Mentors: Haoming Meng & Justin Hiemstra  
Fellowship Dates: 06/03 \- 08/23

## Background

The [Pelican Platform](https://pelicanplatform.org) plays a pivotal role in enabling researchers to seamlessly deploy and manage their data across a federated network. At the core of this platform lies the Origin service, a critical component that ensures data accessibility across the federation. The stability and performance of the Origin service are vital; any disruptions or failures could render the data inaccessible, undermining the very purpose of the federation. Consequently, maintaining a robust monitoring framework for the Origin service is not just necessary but essential for the continued success of data federation efforts. Moreover, it's crucial that groups federating their data have a clear understanding of how their data is being utilized. This transparency is not only important for operational reasons but also for accountability, especially in the context of grant-funded research. Often, these groups must report back to their grant providers, demonstrating the impact and value of their work through comprehensive data visualizations, such as graphs and spreadsheets. These reports are essential for justifying that the funding is being spent effectively and that the research is producing meaningful outcomes. Thus, robust monitoring and reporting tools within the Pelican Platform play a critical role in supporting these administrative and funding-related requirements, further highlighting the importance of understanding the health and performance metrics of the Origin service.


## Project Description

The primary objective of this project was to elevate the monitoring capabilities of the Origin service by introducing new metrics and developing enhanced visualizations. The project was designed with a phased approach, starting with the Origin server and potentially extending to other components like the cache and director servers, depending on the time available. The intention was to provide a more granular view of the service's performance and health, thereby improving observability and aiding administrators in proactive maintenance and troubleshooting. By identifying key performance indicators and implementing new metrics, this project sought to provide a more comprehensive understanding of the service's operations and potential bottlenecks.

## Project Outcome

The project culminated in the development of a new Grafana dashboard tailored specifically for the Origin service, accompanied by several newly-created metrics that offer deeper insights into the system's performance. The design and implementation of the dashboard were heavily influenced by feedback gathered through a user study conducted with system administrators from CHTC and OSG. This iterative process ensured that the final product was not only technically sound but also user-centric, addressing the real-world needs of those who manage and rely on the Pelican Platform. The introduction of these new metrics has significantly enhanced the transparency and observability of the Origin service, enabling administrators to detect issues earlier and make more informed decisions.  Additionally, this work aligns with one of the core principles of CHTC: "Thou shalt engage in translational CS." By translating computer science research into practical tools that have been deployed to address real-world problems, this project exemplifies the commitment to making impactful contributions that go beyond theoretical research. The deployment of these tools within CHTC underscores their practical value, ensuring that they are not only developed but also actively used to support scientific endeavors.

I also gave a lightning talk at [HTC24](https://agenda.hep.wisc.edu/event/2175/). You can watch it here.
[![My lightining talk](https://img.youtube.com/vi/EeFGRD29fSw/0.jpg)](https://youtu.be/EeFGRD29fSw?si=EIt5mC7xxv8eQZ31&t=972)

## Recommendations for Next Phase of Project

The next phase of the project would be to build out dashboards for the other Pelican services. I would recommend starting with Cache service. This service has some noteworthy differences from the Origin service due to its role in a federation. The Cache service is hopefully what users interact with the most and so building out a dashboard for this service is critical so that operators can diagnose issues if or when they arise. The next part of the project requires actually determining the health of a federation or any of individual services. There are obvious instances where a federation may be unhealthy or dead but examining the edge cases of health has been unexplored. Once health is defined, other downstream developments can be made. One of these developments could be building out notifications within Pelican for alerting when a federation or any individual service is unhealthy. I would also recommend adding the ability to use an external prometheus service, this is because the way we run Prometheus can cause all sorts of performance issues and also defeats the purpose of having telemetry separate from your application so that you can gain observability when your application is down. Lastly, develop more metrics within XRootD to provide more observability. I also thought that a Prometheus plugin to XRootD could be beneficial for XRootD system admins.

## Lessons Learned

Throughout the fellowship I’ve learned lessons about engineering, design, and the importance of building tools to support science. With engineering, I learned about how Pelican works, the philosophy behind high throughput computing, and the rigor required to build production-grade software. On design, I learned that users don’t always know what they want. When designing the Origin dashboard, I conducted user studies with system admins, and I took away from those studies that they really don’t know what they need. They have ideas about what may be helpful, but not what they need. Yet, when designing the dashboard, I learned about designing layouts and that presenting information meaningfully is important for understanding what is going on within the Origin. Lastly, I learned about the importance of building tools to support science. If you squint hard enough, CHTC is like the second derivative of research outcomes, science being the first derivative of research outcomes. Science produces research outcomes and we at CHTC try to accelerate science. Being an accelerator is rewarding because you get very immediate feedback. When acceleration increases so does the velocity and position. In terms of CHTC, more science gets done and more results are developed. As a fellow, I have felt even though my impact may be small, I am thrilled to be a part of the acceleration, pushing science forward.

## Project Material Links and Descriptions

- [Pelican](https://pelicanplatform.org/)  
- [My Fork of Pelican](https://github.com/patrickbrophy/pelican/)
- [Prometheus](https://prometheus.io/)  
- [Grafana](https://grafana.com/)  
- [XRootD](https://xrootd.slac.stanford.edu/index.html)
