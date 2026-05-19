# DevOrganizationMaturityLevels
Describes stages that modern software developer organization have to reach to benefit from the latest trends - like SRE/Platform Engineering/AI assisted Ops/Development

## Pre-word
After failed to successfully implement Internal Developer platform and Observability/SRE principles in several organizations I asked why that happened. 
Based on research data available in public internet there are certain stages or level of maturity that software development organization has to go through before it needs and can efficiently implement approaches like Platform Engineering and AI adoption.
And below is a list of oragnization maturity levels may be generalized answer to that.

## Quick ‘local’ examples
 
### IaC separation of concerns
Organization needs a dedicated team (Infra platform) that will maintain and publish for other teams re-usable infrastructure as a code modules - terraform on aws in our case -  with embedded best practices, no critical or high vulnerabilities, before you can implement platform orchestrator (Humanitec or Harness) and quickly create environments with self-service or scaffolding in Backstage.

### Governance
If there is no tool that will check Infrstructure code compliance to pre-defined and agreed by all teams standards, there is no way to enforce or even check compliance that standard. Such tool could be just a step in CI/CD pipeline that checks terraform code and fail pipeline until critical/high issues are fixed or full-fledged orchestration with Policy checks like Hashicorp Cloud Platform with Waypoint or mentioned above Humanitec/Harness.

### Golden path
Organization needs a set of tried and tested tech stack combinations to allow quick creation of GitHub repo, standing up new VPC, Environments, ECR, ECS/EKS clusters and RDS/Secrets/Parameters/Lambdas/S3 buckets and related observability and development artefacts.

### FinOps
Tagging of cloud resources has to be mandatory for every production and non-prod publci cloud resource before you can go and extract FinOps cost data through AWS Cost Explorer API. 

### Standard Compliance
Similar with CI/CD pipeline, before you can measure each repo compliance (and build on top of that team's compliance scorecard) you have to define standard CI/CD pipeline and several standard scalable cluster versions (ECS, EKS, serverless). 

### Reliability/SRE
Similar with DORA metrics - to get insight into reliability/velocity balance of the specific microservice one needs data collected by each deployment/release, incidents, ticketing system (jira in our case). And to measure SLI, error budget SLO has to be defined and downtime measured with some metrics of log collection system (DataDog in our case) and even before that KPI has to be defined at an application requirements development stage (non-functional requirements NFR) and then relevant metrics exposed for pull collection or pushed into observability system.


## Case #1
Organization with obsolete stack (18 years old!) and rigid ITISM setup, that relied on ever-changing 3pv contractor to install, integrate and evolve most of their software products (ERP, POS, Cloud Infra). Mostly cargo cult approach. "We hire SRE and started developing DevQA/DevOps standards and that's defenitely has to fix our reliability  abd availability issues, with no stupid clouds, CI/CD pipelines, automated tested, performance testing, unit tests, or docker containers or orchestrators/cluster, NFR, iterative development approaches."

## Case #2
We need internal developers platform/portal and AI because that might save us from poor engineering practices, no architecture review process, wack-a-mole approach to security. But we still do not maintain IaC terraform modules centrally, we have no SSO in AWS org, we do not have standards,not even minimum observability requirements, SLO/SLI, no deployment stats collections, no platform team, no standard for CI/CD and QA, we use only AWS ECS and believe k8s is too complex for our use-case"


## Levels 0 - 6 

### Level 0 — Heroics / Tribal Knowledge
### Level 1 — Standardization Foundation << but we are only  half-way here
### Level 2 — Measured Automation
### Level 3 — Observability + Reliability Engineering
### Level 4 — Platform Engineering / Internal Developer Platform
### Level 5 — FinOps + Governance Engineering
### Level 6 — AI-Augmented Engineering Organization << Management want us to be here

Organizations fail not because they lack advanced tools, but because they skip foundational operational standardization and telemetry layers.

Modern practices like Platform Engineering, SRE, FinOps, AI-assisted operations, and Internal Developer Portals are not isolated capabilities — they are stacked capabilities. Each maturity layer depends on data, standards, and automation produced by earlier layers.

Recent industry research consistently shows that mature DevOps organizations are dramatically more successful with AI adoption, platform engineering, and operational scaling.

Below is a consolidated maturity model synthesized from:

DORA / Google DevOps research

CNCF Platform Engineering maturity dimensions

Gartner platform engineering guidance

SRE operational models

FinOps operational practice patterns

recent industry/platform engineering reports

real-world operational dependencies observed in enterprise cloud organizations

Software Engineering / DevOps Organizational Maturity Model
Level 0 — Heroics / Tribal Knowledge

Typical characteristics:

Manual deployments

SSH into servers

"Pet" infrastructure

Snowflake environments

No ownership clarity

Monitoring only for infra uptime

Teams depend on specific individuals

At this stage:

AI coding tools create more chaos

Public cloud costs become invisible

SRE is impossible

Platform engineering becomes "another team making YAML"

Missing prerequisites:

Standards

Automation

Metadata

Telemetry

Service ownership

Level 1 — Standardization Foundation

This is the first truly non-skippable stage.

Core capabilities
Standard delivery patterns

Examples:

Standard CI templates

Standard repo structures

Standard containerization

Standard deployment methods

Standard runtime targets:

EKS

ECS

Lambda/serverless

Infrastructure as Code standardization

Usually:

Terraform/OpenTofu modules

Versioned reusable modules

Shared networking/security patterns

Mandatory metadata

Critical example:

ProjectName

Environment

Owner

CostCenter

DataClassification

Without this:

FinOps fails

Governance fails

Security ownership fails

AI context becomes incomplete

Identity and access baseline

SSO

RBAC

centralized IAM patterns

auditability

Centralized observability baseline

logs

metrics

traces

deployment events

Without this:

SRE impossible

DORA impossible

AI Ops impossible

Why this stage cannot be skipped

Your observation is exactly correct:

Before you can build Internal Developer Platforms, you need reusable, standardized primitives.

Platform engineering is not "Backstage installation maturity."

It is:

standardization maturity

reusable automation maturity

governance maturity

Without golden paths:

every service becomes custom

self-service becomes impossible

support burden explodes

This is why many IDP initiatives fail:

they start with portal UI

instead of operational standardization

Recent platform engineering maturity research specifically identifies this transition from ad-hoc scripts to standardized reusable delivery foundations as the key threshold.

Level 2 — Measured Automation

This is where organizations begin collecting reliable engineering data.

Core capabilities
CI/CD maturity

deployment pipelines standardized

automated testing

artifact versioning

rollback support

deployment tracking

Environment consistency

ephemeral environments

immutable infrastructure

policy-as-code

cluster baselines

Deployment telemetry

Every deployment emits:

service name

version

environment

timestamp

commit SHA

deployment actor

Without deployment events:

DORA metrics become inaccurate

incident correlation becomes manual

AI operational analysis weakens

Ticketing/workflow integration

Examples:

Jira linkage

incident linkage

release linkage

Without workflow integration:

change failure rate becomes subjective

reliability analysis becomes anecdotal

Why this stage cannot be skipped

This stage creates the operational data model.

Without structured engineering telemetry:

DORA metrics become vanity metrics

executive dashboards become fiction

AI copilots lack operational context

A recurring industry finding:
many organizations claim "DevOps adoption" while lacking measurable delivery telemetry.

Level 3 — Observability + Reliability Engineering

This is where SRE becomes realistically possible.

Core capabilities
Service ownership model

Each service has:

owner

escalation path

SLO

operational dashboard

runbooks

SLI/SLO/Error Budget model

This is another non-skippable maturity gate.

Without SLOs:

there is no reliability target

there is no error budget

there is no reliability tradeoff framework

Without SLIs:

AI cannot reason about service health properly

incidents remain reactive

platform prioritization becomes political

Full observability

metrics

logs

traces

business KPIs

deployment events

infra telemetry

Incident lifecycle integration

incidents linked to deployments

MTTR measurable

postmortems standardized

Why this stage cannot be skipped

SRE is not "people who manage Kubernetes."

SRE fundamentally requires:

measurable reliability targets

telemetry

operational ownership

feedback loops

Without observability maturity:

error budgets are fake

AI SRE tools hallucinate

auto-remediation becomes dangerous

Recent industry discussions around "AI SRE" repeatedly show this failure mode:
organizations try to automate operations before operational semantics exist.

Level 4 — Platform Engineering / Internal Developer Platform

Only now does IDP truly become scalable.

Core capabilities
Self-service golden paths

Examples:

"Create microservice"

"Provision RDS"

"Deploy service"

"Create namespace"

"Request DNS"

Internal platform as product

Dedicated team:

platform PM

platform roadmap

developer UX

documentation

adoption metrics

Guardrails and policy-as-code

security controls

compliance

budget enforcement

runtime standards

Service catalog

Usually:

Backstage

Port

Compass

internal portals

Why this stage often fails

Organizations skip directly here.

But self-service requires:

reusable IaC

standardized pipelines

standardized observability

metadata consistency

ownership models

Otherwise:

platform team becomes ticket fulfillment team

every onboarding becomes custom consulting

CNCF platform engineering research repeatedly identifies lack of measurement and standardization as the primary blocker to mature platform engineering adoption.

Level 5 — FinOps + Governance Engineering

Now the organization can finally optimize at scale.

Core capabilities
Mandatory tagging governance

Exactly as you described:
Without enforced tags:

no accurate chargeback

no project cost analysis

no environment allocation

no unit economics

Cost observability

cost per service

cost per environment

cost per team

cost per customer

cost anomaly detection

FinOps in delivery pipelines

Examples:

Infracost in PRs

budget policy checks

architectural cost scoring

Reliability vs cost optimization

This is where SRE and FinOps converge:

availability costs money

redundancy costs money

observability costs money

Tradeoffs become measurable.

Why this stage cannot be skipped before AI optimization

AI systems require:

clean metadata

structured telemetry

historical trends

ownership models

governance

Otherwise AI becomes:

expensive autocomplete

hallucinating dashboards

unreliable recommendations

Recent DevOps research strongly indicates AI amplifies existing maturity rather than replacing it.

Level 6 — AI-Augmented Engineering Organization

Only mature organizations reach this stage effectively.

Realistic AI capabilities
AI-assisted operations

incident summarization

RCA assistance

deployment risk analysis

anomaly detection

AI-assisted platform engineering

Terraform generation

policy generation

documentation synthesis

service scaffolding

AI-assisted governance

compliance drift detection

cost optimization recommendations

dependency risk analysis

AI-assisted SDLC

PR analysis

test generation

release notes

operational impact prediction

Critical insight from recent research

The most important pattern emerging across recent DevOps and platform engineering reports:

AI does not replace DevOps maturity.
AI amplifies DevOps maturity.

Organizations with:

strong standards

telemetry

governance

automation

observability

gain enormous leverage from AI.

Organizations without them:

create AI-generated operational entropy.

The Most Common Failed Transformation Pattern

A very common enterprise sequence:

Install Kubernetes

Install Backstage

Buy AI tools

Declare "platform engineering"

But missing:

standard modules

tagging standards

deployment telemetry

SLO ownership

observability maturity

CI/CD consistency

Result:

fragmented clusters

unreliable metrics

unusable FinOps

platform team burnout

AI hallucinating on incomplete data

The Most Important Non-Skippable Dependencies
Before SRE

You need:

observability

deployment telemetry

service ownership

SLO definitions

Before FinOps

You need:

mandatory tagging

standardized environments

resource ownership

Before Platform Engineering

You need:

reusable IaC

standardized pipelines

golden paths

operational standards

Before AI Engineering

You need:

structured telemetry

governance

operational metadata

reliable automation

auditability

A useful mental model

Modern engineering maturity evolves roughly like this:

Standardization
    ↓
Automation
    ↓
Measurement
    ↓
Observability
    ↓
Reliability Engineering
    ↓
Platform Engineering
    ↓
FinOps/Governance
    ↓
AI-Augmented Operations

Trying to skip layers usually creates:

hidden toil

operational chaos

unreliable metrics

AI-generated confusion

platform team overload

rather than true engineering acceleration.
