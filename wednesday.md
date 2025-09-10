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
