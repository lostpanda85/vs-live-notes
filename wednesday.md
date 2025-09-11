# Wednesday

Wednesday was more sessions and another keynote.

## I Love YAML! Using Azure DevOps to Build and Release to Azure

* Ben Day

Note: *We're doing this already, only noting new information*

### Agenda

* YAML Pipelines
  * Build, Test, Deploy with Pipelines
  * Pools, Triggers, Variables
  * Docker
  * Multi-Environment Deploys

What is YAML? Yet Another Markup Language. YAML Ain't Markup Language :D :D

### Classic Pipelines

Classic Pipelines have been around a while, use a design to build pipeline. JSON based under the hood.

### YAML Pipelines

* Stored in version control
* Text based
* Builds and Releases are 'stages' in the same pipeline definition.

### Takeaways

* Get good at CLI as pipelines are just running CLI Commands behind the scenes
* Each pipeline step runs in its own process.

## Boiling the Frog: Implementing a modern message-based Architecture without anyone noticing

* Hazel Bohon

(See slides)

### Why Modernize?

* Easier to maintain
* Easier to onboard
* More reliable, more secure, more robust
* Easier to change and deliver business value

### Why messaged-based?

* Decoupled
* Fault tolerance
* Scalability

## Github Action in Action

* Marcel de Vries

### General

* Use GitHub over AzDO
  * GitHub will innovate, AzDO will not.
* 0 Downtime Deployments?!?
* Consider separating CI and CD
  * CI is for Developers
    * Provides fast feedback
  * CD is for release engineers and business
    * Isolates permissions for production environments
* GitHub works by convention.
  * The `.github` folder does a lot automatically when GitHub detects it
* Don't just check for errors to validate deployments, check metrics too
* [Test Examples](https://github.com/vriesmarcel/vslive-hq-2024)

[Example App](https://github.com/vriesmarcel/globoticket)

### Actions

* Can be used to automate most tasks
* Is an workflow engine
* Easy to write and share
* Uses yaml
* Cross-platform
* Containers supported
* Runners can run locally or in the cloud
* Can perform matrix build
  * Multi-targeted build (x86/64, arm, etc)
* Streaming Log
* Built in secret store
* Actions can be found in the GitHub Marketplace
  * Checkmark indicates that the domain is verified, not the action


### Workflow

|Workflow Files|Actions|
|-|-|
|Reference Actions|Modular|
|Exist within the repo|Exist within the repo or in other repos|
|Template for workflows| |

#### Structure of Workflows

Event -> Runner 1 (Job 1..., Step 1...) -> Runner 2 (Job 2..., Step 1...) (Check slides)

For basic syntax, refer to slides.

* Runners define what platform performs the action
* Secrets are encrypted in an isolated container
  * Stamped into the app at build time

### Security

* Scanning is important
  * Ensures that vulnerabilities are not being introduces
  * License checks!
* Built-in Advances Security
  * Dependabot
    * Automates removal of vulnerabilities
  * CodeQL Scanning
    * Analysis for known exploits
    * eg, Clear text passwords discoverable
  * External Tools

### Releases

* Control deployment
* Separate from build pipeline
* Controls versioning
* Targets specific builds for release
* Tags repos

### Deployment Strategies

* Use Slots!
* App needs to be stateless
* Traffic manager
* Observability
* Use Blue/Green Deployment
  * k8s/OpenShift should handle this for us
* Actions can drive traffic changes

#### Ring Based Deployments

* Deploy one ring at a time
* (See slides)
* Choose rings wisely

#### Deployment Slots

* Good for web apps
* Traffic routing is built in
* You can force requests to specific slots
* Divide traffic until confident app is working as expected

#### Observability

* Ready Endpoints
  * DB Connections Checks
  * Integrations Checks
* Live Endpoints
  * Running check
* Consider adding validations to workflow actions

## Database DevOps with Next-Gen SQL Projects

* Brian Randell

DB DevOps, like any other DevOps, is a people problem. Getting people to change habits is hard.

### Database Development

* The Inner Loop
* Needs a way to model data
  * Golden Schema / Migrations
* Need A way to protect work
  * Version Control
* Need A Way to test and validate changes
  * Local DB 'Server'
* Consider setting up a SQL Server Database Project in Visual Studio
  * DACPACs serialize the DB schema into XML
    * Glorified zip file, importable into Visual Studio
  * Can also directly connect to DB by importing it
    * Serialized database into visual studio project objects as sql scripts
    * Doing this gives us both a designer and the database definition language scripting
  * Building the DB in Visual Studio generates a DACPAC
    * Generated DLL and pbd are not needed
  * Publishing deploys to a server
    * Compares whats there versus what is being deployed and incrementally updates
  * Remote changes can be pulled in to sync

### Database DevOps

* The Outer Loop
* A Way to build
  * DACPACs
  * DLLs
  * Scripts
* A way to deploy
  * Automation!
* A Way to validate
  * Database Unit Tests
    * This isn't fun and most orgs don't do it
  * Integration Tests
    * Bare minimum for db testing
* Red Gate software may help here
* GitHub actions can provide CI/CD pipelines

### Containers

* Portable & Lightweight
* Consistent Image of SQL Server for all users
* Efficient
* Static volume contains changes
* Consider Aspire
