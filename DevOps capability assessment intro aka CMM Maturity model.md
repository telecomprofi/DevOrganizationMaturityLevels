# DevOps Capability Assessment intro

The software development industry is indeed focused on enhancing the efficiency of development teams. Here are some key areas of emphasis:

- **Speed of Delivery**: Reducing the time from defining a new software feature to its deployment in the production environment is crucial. This often involves adopting agile methodologies, continuous integration/continuous deployment (CI/CD) practices, and automation tools.
- **Developer Experience**: Improving the experience of individual developers is essential. Happy developers tend to produce better code. This can be achieved through better tools, streamlined processes, and a supportive work environment.
- **Code Reliability**: Increasing the reliability of delivered code is a priority. This includes implementing thorough testing practices, code reviews, and using static analysis tools to catch issues early in the development process.
- **Production Incident Reduction**: Decreasing the number of production incidents is vital for maintaining user trust and satisfaction. This can be addressed by improving monitoring, logging, and alerting systems, as well as conducting [post-mortem analyses](https://docs.google.com/document/d/1ob0dfG_gefr_gQ8kbKr0kS4XpaKbc0oVAk4Te9tbDqM/edit)to [learn from incidents.](https://rework.withgoogle.com/en/guides/foster-an-innovative-workplace#learn-from-failures)
- **Operational Efficiency**: Making it easier for operations teams to resolve issues quickly is important. This can involve better documentation, improved communication between development and operations (DevOps practices), and the use of incident management tools.

By focusing on these areas, organizations can create a more efficient, reliable, and enjoyable software development process while sticking to Kaizen continuous improvement principle.

One of the approaches to track such team/organization efficiency are so called DORA metrics. [DORA (DevOps Research and Assessment)](https://dora.dev/research/) metrics are a set of key performance indicators (KPIs) that measure the effectiveness of software development and delivery practices. They provide insights into an organization's ability to deliver software quickly and reliably. The four key DORA metrics are:

1. Deployment Frequency
2. Lead Time for Changes
3. Mean Time to Restore (MTTR)
4. Change Failure Rate

Open image-20250331-080936.png

![image-20250331-080936.png](assets/DevOps%20Capability%20Assessment%20intro%20-%20image-20250331-080936.png)

Theses KPI could be measured, assessed and improved.

One of the approaches to start measuring these and identify where Dev team currently is comparing to industry leaders is to perform series of interviews to pinpoint possible areas of improvements.

Model used in such assessments is simplified[CMM - Capability Maturity Model](https://en.wikipedia.org/wiki/Capability_Maturity_Model) (foundation for [https://insights.sei.cmu.edu/library/cmmi-for-development-version-12/](https://insights.sei.cmu.edu/library/cmmi-for-development-version-12/) by [Software Engineering Institute](https://www.sei.cmu.edu/)).

### DevOps Capabilities

There are[~28 different capabilities](https://cloud.google.com/architecture/devops)identified by DORA/Google and they are grouped into the following three groups

## Technical capabilities

- [Cloud infrastructure](https://dora.dev/devops-capabilities/technical/cloud-infrastructure)
- [Code maintainability](https://dora.dev/devops-capabilities/technical/code-maintainability)
- [Continuous delivery](https://dora.dev/devops-capabilities/technical/continuous-delivery)
- [Continuous integration](https://dora.dev/devops-capabilities/technical/continuous-integration)
- [**Test automation**](https://dora.dev/devops-capabilities/technical/test-automation)
- [Database change management](https://dora.dev/devops-capabilities/technical/database-change-management)
- [Deployment automation](https://dora.dev/devops-capabilities/technical/deployment-automation)
- [Empowering teams to choose tools](https://dora.dev/devops-capabilities/technical/teams-empowered-to-choose-tools)
- [Loosely coupled architecture](https://dora.dev/devops-capabilities/technical/loosely-coupled-architecture/)
- [Monitoring and **observability**](https://dora.dev/devops-capabilities/technical/monitoring-and-observability)
- [Shifting left on security](https://dora.dev/devops-capabilities/technical/shifting-left-on-security)
- [**Test data management**](https://dora.dev/devops-capabilities/technical/test-data-management)
- [**Trunk-based development**](https://dora.dev/devops-capabilities/technical/trunk-based-development)
- [Version control](https://dora.dev/devops-capabilities/technical/version-control)

## Process capabilities

- [Customer feedback](https://dora.dev/devops-capabilities/process/customer-feedback)
- [Monitoring systems to inform business decisions](https://dora.dev/devops-capabilities/process/monitoring-systems)
- [**Proactive failure notification**](https://dora.dev/devops-capabilities/process/proactive-failure-notification)
- [Streamlining change approval](https://dora.dev/devops-capabilities/process/streamlining-change-approval)
- [**Team experimentation**](https://dora.dev/devops-capabilities/process/team-experimentation)
- [Visibility of work in the value stream](https://dora.dev/devops-capabilities/process/work-visibility-in-value-stream)
- [Visual management](https://dora.dev/devops-capabilities/process/visual-management)
- [Work in process limits](https://dora.dev/devops-capabilities/process/wip-limits)
- [**Working in small batches**](https://dora.dev/devops-capabilities/process/working-in-small-batches)

## Cultural capabilities

- [**Generative organizational culture**](https://dora.dev/devops-capabilities/cultural/generative-organizational-culture)
- [Job satisfaction](https://dora.dev/devops-capabilities/cultural/job-satisfaction)
- [Learning culture](https://dora.dev/devops-capabilities/cultural/learning-culture)
- [Transformational leadership](https://dora.dev/devops-capabilities/cultural/transformational-leadership)

In proposed simplified DevOps CMM framework capability levels are down from original 5 levels to simple Red-Yellow-Green 3 traffic-light approach (think of a child growing up and learning how to walk)

Individual capabilities are assessed one-by-one during interviews with Dev Team/Leads or self-assessment questionnaire/survey or both. Examples of such survey questions for Dev Teams:

- [DORA DevOps Quick Check](https://dora.dev/quickcheck/) (Program by Google Cloud)
- [Microsoft DevOps Survey](tba)
- [Adidas DevOps Maturity Assessment](https://github.com/adidas/adidas-devops-maturity-framework/blob/master/framework/devops_maturity_framework.md) framework - uses simplified CMM

### Practical application in an Organization

To implement an effective process within a Software Development organization, it is essential to first identify the areas that require improvement. This should be followed by establishing a change cycle and conducting both initial and ongoing assessments to ensure progress and improvement.

#### Time estimates

[Self-assessment](tba) (1.5h) →

Team Lead Interview (2h) →

Recommendations for next cycle (4-5h) with focus on pains, ‘crawl’ underperforming areas aligned with Org goals →

Itemize recommendations into backlog as tasks and prioritize (2h) →

Execute proposed changes (most of the time is spent here) →

Measure results/ refine goals (3-4h) →

Rinse & repeat.

Open image-20250331-084319.png

![image-20250331-084319.png](assets/DevOps%20Capability%20Assessment%20intro%20-%20image-20250331-084319.png)

### References

[![](https://learn.microsoft.com/favicon.ico)Capability Maturity Model Integration (CMMI), background notes - Azure Boards](https://learn.microsoft.com/en-us/azure/devops/boards/work-items/guidance/cmmi/guidance-background-to-cmmi?view=azure-devops)

[Individual DevOps capabilities by Google/DORA](https://cloud.google.com/architecture/devops)

### [![](https://dora.dev/favicon-16x16.png)DORA | Accelerate State of DevOps Report 2024](https://dora.dev/research/2024/dora-report/)

[![](https://www.gstatic.com/cgc/supercloud_favicon.ico)Announcing the 2024 DORA report | Google Cloud Blog](https://cloud.google.com/blog/products/devops-sre/announcing-the-2024-dora-report)

[https://services.google.com/fh/files/misc/2024\_final\_dora\_report.pdf](https://services.google.com/fh/files/misc/2024_final_dora_report.pdf)

[ISO 9001:2018](https://www.iso.org/obp/ui/en/#iso:std:iso-iec-ieee:90003:ed-1:v1:en)

### CMM, CMMI

CMM was developed and is promoted by the Software Engineering Institute (SEI), a research and development center sponsored by the U.S. Department of Defense (DOD) and now part of Carnegie Mellon University. SEI was founded in 1984 to address software engineering issues and, in a broad sense, to advance software engineering methodologies. More specifically, SEI was established to optimize the process of developing, acquiring and maintaining heavily software-reliant systems for the DOD. SEI advocates industry-wide adoption of the CMM Integration (CMMI), which is an evolution of CMM. The CMM model is still widely used as well.

CMM is similar to ISO 9001, one of the ISO 9000 series of standards specified by the International Organization for Standardization. The ISO 9000 standards specify an effective quality system for manufacturing and service industries; ISO 9001 deals specifically with software development and maintenance. The main difference between CMM and ISO 9001 lies in their respective purposes: ISO 9001 specifies a **minimal acceptable quality level** for software processes, while CMM establishes a **framework for continuous process improvement.** It is more explicit than the ISO standard in defining the means to be employed to that end.

CMM's five levels of maturity for software processes There are five levels to the CMM development process. They are the following:

##### _Initial - Level 1_

At the initial level, processes are disorganized, ad hoc and even chaotic. Success likely depends on individual efforts and is not considered to be repeatable. This is because processes are not sufficiently defined and documented to enable them to be replicated.

##### _Repeatable - Level 2_

At the repeatable level, requisite processes are established, defined and documented. As a result, basic project management techniques are established, and successes in key process areas are able to be repeated.

##### _Defined - Level 3_

At the defined level, an organization develops its own standard software development process. These defined processes enable greater attention to documentation, standardization and integration.

##### _Managed (Capable) - Level 4_

At the managed level, an organization monitors and controls its own processes through data collection and analysis.

##### _Optimizing (Efficient) - Level 5_\*

At the optimizing level, processes are constantly improved through monitoring feedback from processes and introducing innovative processes and functionality.

\*Only 12% of organization appraised at this level

#### Capability Im-maturity model, CIMM (Satire)

### Negligent - Level 0

The organization pays lip service, often with excessive fanfare, to implementing engineering processes, but lacks the will to carry through the necessary effort. Whereas CMM level 1 assumes eventual success in producing work, CIMM level 0 organizations generally fail to produce any product, or do so by abandoning regular procedures in favor of [crash programs](https://en.wikipedia.org/wiki/Crash_program).

### Obstructive - Level -1

Processes, however inappropriate and ineffective, are implemented with rigor and tend to obstruct work. Adherence to process is the measure of success in a level −1 organization. Any actual creation of viable product is incidental. The quality of any product is not assessed, presumably on the assumption that such assessment is unnecessary since if the proper process is followed, high quality is guaranteed. This is the most common level achieved by most organizations that pursue CMM ratings.

However, level −1 organizations believe fervently in following defined procedures, but lacking the will to measure the effectiveness of the procedures they rarely succeed at their basic task of creating work. This behavior is inherent in the CMMI evaluation process. Since many government agencies will only award contracts over a certain monetary value to organizations that can pass a CMMI-3 or higher [SCAMPI](https://en.wikipedia.org/wiki/Standard_CMMI_Appraisal_Method_for_Process_Improvement) appraisal, management may be willing to accept inefficiencies to win these lucrative contracts. Government contracting models in which organizations are paid not for the value of their products but by the number of hours spent building them reward organizations for performing non-value-added activities related to CMMI compliance. Thus, government contractors with CMMI ratings may be more profitable than non-CMMI rated companies regardless of the quality of the work they produce.

### Contemptuous - Level -2

The organization's ineffectiveness has become apparent to the marketplace or the larger organization, which ignores or attempts to neutralize these unfavorable perceptions. Measurements are fudged to make the organization look good. Measures of activity (bugs fixed, lines of code written, hours worked) replace measures of productivity (% functions completed, test success rates). Volatility in specifications and schedules is recast as evidence of organizational "agility". Certifications on "best processes" are presented as evidence that the organization is performing optimally; poor results are blamed on factors outside the organization's control. The processes chosen typically omit or shortcut essential components of recognized methods (e.g. "6-week [Six-Sigma](https://en.wikipedia.org/wiki/Six_Sigma)" or "[Lean](https://en.wikipedia.org/wiki/Lean_manufacturing) CMM"), which are flexible and can cover both good and bad practices. The organization becomes committed to ineffective processes, leading to a feedback cycle of increasing disorganization.

### Undermining - Level -3

Undermining organizations routinely work to downplay and sabotage the efforts of rival organizations, especially those successfully implementing processes common to CMM level 2 and higher. This behavior may involve competing for scarce resources, drawing those resources from more effective departments or organizations.
