# .NET Foundation Project Maturity Ladder

This document describes the .NET Foundation project maturity ladder. It is intended as a shared definition of quality for the .NET ecosystem, for use by producers and consumers. It can be used by consumers to increase confidence in their dependencies and by maintainers to make it more straightforward to satisfy consumer needs.

Any project can use the maturity ladder. The registration process for the ladder is described in [.NET Foundation Maturity Ladder Policies](maturity-ladder-policies.md#register). Participating in the ladder is the best way to join the Foundation if that's a goal for a project.

The .NET Foundation will run a badge server so that projects can officially display their participation in the ladder, including on GitHub and NuGet.org.

## Overview

Project maturity level is a signal by the .NET Foundation for project users (including corporations and governments) to use for adopting community projects. Projects increase their maturity by demonstrating their quality and sustainability to the .NET Foundation working group: that they have adoption, a healthy rate of changes, and follow recommended security practices.

The .NET Foundation maturity ladder is analogous to the [Apache Foundation Maturity Model](https://community.apache.org/apache-way/apache-project-maturity-model.html). The primary difference is that the ladder defines a specific progression of characteristics (hence the difference in names). The ladder does not describe all the details of how projects might or should operate, but aims to capture the most important aspects that are expected to be important to project consumers.

The maturity ladder is broken into four levels, starting at level 1 and ending at level 4. Each level adds meaningful and observable value for the project, and can be an acceptable stopping point. The levels are thematic (for example, security practices), with the intention that the project provides most or all of what a consumer would want for that theme. This is as opposed to  progressive improvement across multiple themes, but not sufficiently complete for any of them.

## Requirements

The ladder levels are described in terms of three categories: health, practices, and benefits.

* **Health** -- Qualities that are observable through interacting with a project on GitHub.
* **Practices** -- Qualities that are observable through using the project (like a NuGet library), or mitigate potential risks of using it.
* **Benefits** -- Specific assistance and opportunities that maintainers have available to make their project easier to maintain or somehow improve it.

The health and practices listed for each level are intended as valuable and important, however, projects may be considered to achieve a level without satisfying every single line item. Some of the qualities are critical and others are more supporting (they are listed in order of importance, per category). Assessment of projects is intended to hit the sweet spot between rewarding maintainers for an honest effort to meet the requirements of a level and deliver on a confidence promise to users.

## Level 1 -- Incubator

This level describes a project that is healthy, enabling easy and pleasant interaction and use for consumers. It is intended to be within reach of any project.

* **Health**
  * Uses [MIT](https://opensource.org/licenses/MIT) or other compatible license, and third party contributions are documented in a notice file.
  * Uses the [.NET Foundation CLA bot](https://cla.dotnetfoundation.org/) (or acceptable alternative) to manage contributor copyright.
  * Uses [.NET Foundation code of conduct](https://dotnetfoundation.org/code-of-conduct) (or acceptable alternative).
  * Maintainer(s) respond to and fix issues and encourage community contribution.
  * CI/nightly builds are active, usable and their status is visible (by a badge). The build server must be patched and otherwise be considered secure.
  * Publishes new stable versions regularly (possibly just patch updates), at least once/year, but ideally at least once/quarter.
  * Most code changes are performed via PRs, and open to community feedback and transparent viewing. The specific review and merge process used is a project choice.
  * Versioning and breaking change policy is documented.
  * Roadmap is documented, via formal document and/or an issue query.
  * Build scripts are documented and can be readily used by consumers.
* **Practices**
  * No additional requirements.
* **Benefits**
  * Access to [.NET Foundation CLA bot](https://cla.dotnetfoundation.org/) .
  * Access to the .NET Foundation maturity ladder badge server.
  * Increased project visibility, by being listed on the .NET Foundation projects page (for the maturity ladder).

## Level 2 -- Basic security practices

This level describes a project that has a basic layer of security practices in place, which establishes an important, although narrow, level of trust between producer and consumer.

* **Health**
  * No additional requirements.
* **Practices**
  * 2FA in place for all accounts (GH, DevOps, NuGet, …).
  * Builds are [reproducible](https://github.com/dotnet/sourcelink/tree/master/docs#continuousintegrationbuild), use [sourcelink](https://github.com/dotnet/sourcelink) and publish symbols (portable PDBs) (in-package or as a [symbol package](https://docs.microsoft.com/en-us/nuget/create-packages/symbol-packages-snupkg)).
* **Benefits**
  * Access to .NET Foundation build infrastructure for automated/continuous project builds, testing and publishing.

## Level 3 -- High quality project

This level of project is intended to provide a consumer with a project that has proven to be generally useful (via crowd voting), and that employs a higher-level of practices that demonstrate a strong commitment to continuous improvement and secure software.

* **Health**
  * The ecosystem has adopted this project at a significant scale, demonstrated by one or more key metrics, such as package downloads, number of dependent projects on GitHub, or community activity on the project repo(s).
  * Project documentation is available for users.
  * Documents security vulnerability publishing policy.
  * \>1 project maintainer.
  * [Member project](https://dotnetfoundation.org/projects) of the .NET Foundation.
* **Practices**
  * Complies with [.NET Foundation continuation policy](continuation-policy.md).
  * Stable packages depend on libraries that are at level #2 or higher.
  * Signs packages.
  * Uses static analysis tools to validate pedigree and safety.
  * Applies [.NET API design guidelines](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/framework-design-guidelines-digest.md).
  * Seeks and applies guidance from .NET Foundation design and architecture group.
  * Updates package references regularly to accommodate servicing updates in dependencies.
* **Benefits**
  * Access to .NET Foundation build infrastructure for static analysis and [code signing (extended validation)](https://en.wikipedia.org/wiki/Extended_Validation_Certificate) using the [.NET Foundation Signing Service](https://github.com/dotnet/SignService/blob/master/README.md).
  * Access to a higher level of technical guidance and mentorship.
  * Access to .NET Foundation Enterprise LastPass subscription for storing secrets.
  * Access to the .NET Foundation trademark service.
  * Can use the `dotnet` or `dotnet-foundation` GitHub orgs for project repos.

The recommended set of static analysis tools is TBD. One option is [Security Code Scan](https://security-code-scan.github.io/).

[Dependabot](https://dependabot.com/dotnet/) can be used for automatically updating package references.

## Level 4 -- Trustworthy project

This level of project is intended to provide a consumer with packages that use infrastructure and dependencies that they can trust, primarily due to the build and publishing workflow. These projects are likely the most trustworthy open source dependencies available.

* **Health**
  * No additional requirements.
* **Practices**
  * Stable packages depends on libraries that are at level #4.
  * Uses .NET Foundation certified infrastructure to build, sign and publish official public packages (ensures package is based on public git commit).
  * Pre-disclose .NET Foundation project vulnerabilities that may need coordination from other project maintainers.
* **Benefits**
  * Considered trustworthy project by the ecosystem, and can be used and recommended by organizations that require this level.

.NET Core, .NET Framework or .NET Standard references are considered level 4. No other projects have a pre-defined status, at level 4 or any other level.

Corporate-backed projects can use .NET Foundation infrastructure (as described above) or can choose to self-certify their own infrastructure to build and push packages. If such a project chooses to self-certify their infrastructure, consumer trust should shift from placing value on .NET Foundation-provided infrastructure to the trustworthiness of the specific corporation that backs the project. Corporate-backed project may be given a different color of badge to indicate this difference.

## Caveat emptor

> [Buyer be-aware](https://en.wikipedia.org/wiki/Caveat_emptor) of your dependencies and make informed choices.

The ladder is intended to define and provide major improvements in quality and confidence improvements for project consumers. However, it provides no absolute guarantees. Even when viewed through the lens of "best effort and best intentions" on the part of maintainers, bad things can still happen that cause harm.

Levels 3 and 4 put stronger safeguards in place to mitigate a variety of undesired scenarios. They define a model for building confidence using open source community projects.

Some projects may display badges that do not use the badge server, and therefore are based on self-assessment and may even be intentionally deceptive. This is not expected to be common and will be discouraged. The community may actively discourage maintainers from this practice. On GitHub, it is easy to tell the source of a badge.
