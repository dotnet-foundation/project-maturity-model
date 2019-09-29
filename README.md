# A .NET Foundation project to grow the .NET ecosystem through shared models of Quality, Confidence, and Support

This proposal describes new approaches that we can use to improve the quality and quantity of .NET open source projects, and the .NET ecosystem generally. The .NET ecosystem is strong, but could be stronger still, and there are general challenges in open source projects that we should address in our ecosystem.

The .NET Foundation is a independent foundation created to support .NET Open Source Software. As an independent foundation it's in a unique position to support open source projects to target new clients and to help projects adopt best practices.

> TL;DR: We are proposing three new programs:
>  * Maturity profiles that define project quality.
>  * A training and support program for maintainers
>  * A new project forge that creates new projects for the ecosystem.
>  The goals of these programs are to increase project quality for consumers, increase consumer confidence in and adoption of community libraries, and to fill gaps to make .NET development more efficient and more fun.

The remainder of the document describes the proposed approaches, and references documents that define shared definitions and policies that are critical to making these approaches viable in our ecosystem. This proposal is open for public comment and amendment.

Supporting documents:

* [.NET Foundation Maturity Profiles](maturity-profiles.md)
* [.NET Foundation Maturity Profiles Program](maturity-profiles-policies.md)
* [.NET Foundation Project Continuation Policies](project-continuation-policies.md)

Note: The term "projects" is used throughout as a broad catch-all term. While most open source projects are likely libraries, the proposal equally applies to tools, applications, services and other project varieties.

## Premise

The proposed approaches (detailed below) are based on two ideas:

* Forging new projects at ecosystem scope for ecosystem benefit based on identified gaps or new industry trends will raise the effectiveness of every .NET developer.
* Improving user (person or organization) confidence in open source projects will increase and broaden usage.

Which lead to the aspirational goal of the proposal :

> .NET is a stronger choice for public sector and business software, due to safeguards that help protect open source consumers (and their users), a growing set of projects that lower development costs, and a self-organizing ecosystem that values predictability and quality.

.NET open source projects (including .NET Core) are already used in critical public sector and business software. That's been the case for years. Looking forward, we have an opportunity to define higher value characteristics and build software that incorporates those. Over time (and this has already started), it is expected that maintainers of critical software will require that dependencies deliver higher guarantees around practices. Satisfying these requests will be hard to achieve on an ad-hoc basis, but instead requires a model that operates at ecosystem scale.

We need shared mechanisms that can produce these and other important outcomes and that we all feel ownership and influence over. The [.NET Foundation](https://dotnetfoundation.org/), as a generally accepted, independent, and trusted intermediary, is uniquely suited to fulfill this role of enabling our ecosystem to self-organize for shared benefits.

To that end, the Foundation will do the following:

* Define and publish shared definitions and policies for comment, adoption, and long-term evolution.
* Highlight and improve the free services that are offered to open source projects.
* The .NET Foundation Project Support Action Group will establish a working group that cater to and document/backlog the needs of the primary roles in our ecosystem: maintainers, contributors and consumers. The working groups need to pay attention to the many experiences that overlap across roles.
* The .NET Foundation Technical Review Action Group will establish a working group to implement a new Project Maturity Model as described below.

## Inspiration from other Foundations

This proposal takes inspiration from other software foundations that have analogous programs in place, in particular:

* [Apache Foundation](https://apache.org/) -- See: [Incubator](https://incubator.apache.org/); [Maturity Model](https://community.apache.org/apache-way/apache-project-maturity-model.html); [Projects](https://projects.apache.org/projects.html)
* [Cloud Native Computing Foundation (CNCF)](https://www.cncf.io/) -- See: [Sandbox](https://www.cncf.io/sandbox-projects/); [Projects and Maturity Levels](https://www.cncf.io/projects/); [Graduation Criteria](https://github.com/cncf/toc/blob/master/process/graduation_criteria.adoc)

Apache and CNCF have great structures in place to grow new projects from infancy into graduated projects that operate in reliable and predictable ways. When projects graduate and join the ranks of other mature projects, the foundations do an exceptional job of providing higher levels of visibility. This helps consumers understand "this project is great and has been vetted", making it easy to make good choices selecting projects to use without needing to a do a lot of up-front research.

The proposed .NET Foundation programs are intended to operate in similar ways and deliver similar benefits as Apache and CNCF while being oriented the around the specifics of the .NET ecosystem.

Note: Several ideas and some text came directly from other projects, including Apache and CNCF. We stand on the shoulders of giants, and greatly appreciate the work that has already been done in those communities for the public good.

## Inspiration from other Projects

Community projects are taking on related challenges, such as [ClearlyDefined](https://clearlydefined.io/about), [Code Infrastructure Initiative](https://www.coreinfrastructure.org/programs/badge-program/) and [Software Package Data Exchange (SPDX)](https://spdx.org/). These are great initiatives that are intended to provide transparency related to project licensing, source location for binaries, vulnerabilities, and other concerns. We should define practices and provide tools that make it easy to produce the correct metadata such that consumers of those services can find relevant information about .NET packages.

## Historical Context

> The [.NET Foundation](https://dotnetfoundation.org/) is an independent organization, started by Microsoft in 2014, and is now governed by a community elected board of directors.

The .NET Foundation and .NET Core as an open source project were announced in November 2014. The initial goal was to fully realize .NET as an open source ecosystem, enabling .NET projects to be fully open from top to bottom, including their development stack. Achieving that goal has been a tremendous effort on the part of the community, the Foundation and Microsoft, and it has taken about five years (2014 until now) to make happen.

One can think of that five year period for the Foundation as being narrowly focused on establishing services for heavily used community projects. Similarly, Microsoft has been focused on establishing .NET Core as an open platform. As we look at the next five years, we should aim to improve the .NET ecosystem much more broadly, in important ways.

This proposal was developed by a .NET Foundation working group, based on observed challenges and missed opportunities in the ecosystem. The proposal was further refined with the Technical Steering Group and Advisory Council, with the goal of launching an initial pilot and to solicit feedback from the broader community.

## Proposal: Maturity profiles

> Proposal: Define maturity profiles that projects can use for certification, to increase user confidence and adoption.

Project quality is a tough nut to crack, and can be approached in many ways. For the purpose of this document, project quality is approached exclusively from the vantage point of improving user confidence.

Note: We should use surveys over time to validate that confidence is improving based on this proposal.

When you are building an application, every new dependency you add should *reduce* your confidence unless you have a well-justified reason to trust that dependency. The maturity profiles are intended to help provide project consumers (that take a dependency on a community project) with more information so that they can make more informed choices, and also develop a more accurate sense of safety for their code (which to a large degree is a function of its dependencies).

The maturity profiles attempts to resolve the following real-world challenges:

* What happens if a lone maintainer abandons the project (for example, due to death), and does not have a plan in place for continuation?
* How does the maintainer manage vulnerabilities, both ingestion of fixes from dependencies of the project and disclosing its own vulnerabilities?
* Does the binary describe the git SHA it was built from, and is that accurate, and public?
* Can users have confidence that the project is safe to use, from the perspective of malware, or other dangerous code?

The maturity profiles are fully defined in [.NET Foundation Maturity Profiles](maturity-profiles.md). It references additional policies defined in [.NET Foundation Maturity Profiles Program](maturity-profiles-policies.md) and [.NET Foundation Project Continuation Policy](project-continuation-policies.md).

## Proposal: Project Forge

> Proposal: Forge new projects at ecosystem scope for ecosystem benefit based on identified gaps or new industry trends.

New projects are the lifeblood of any ecosystem. This is particularly important for new industry trends, like microservices, AI, or pick-your-favorite-trendy-topic and equally new innovative ideas that don't yet even have a name. Most promising new projects will come to life in the same way they do today, by a developer that has a great idea, a company that shares a (formerly proprietary) project, or from a student working on a novel research project.

Even with a vibrant ecosystem, some projects don't seem to happen or fail to reach escape velocity, even though everyone knows that the project is important. Maybe the project is hard, requires coordination among a large group of stake-holders or people think that a large corporation is going to lay claim to that space, so everyone stays away. None of those are good outcomes, yet they absolutely exist today.

We need a curation mechanism for new projects -- the project forge -- that enables us, as a community, to lay claim to and start the projects we need. It is a kind of ecosystem self-design.

Projects created through the forge will be encouraged to use the `dotnet` or `dotnet-foundation` GitHub orgs. While forge projects will be controlled by their maintainers, forge projects are intended to be amongst the most community oriented projects in our ecosystem. Hosting them in a neutral space helps to demonstrate and foster that. These projects can publish packages in the `dotnet.` NuGet prefix, as a way of increasing visibility, demonstrating a relationship between forge projects, and as a kind of cousin to `System.` packages.

A new working group will be formed to do the following:

* Identify gaps and industry trends.
* Maintain a public project backlog/board on GitHub.
* Accept new project proposals.
* Encourage the community to vote and provide direct feedback on project proposals.
* Recommend new projects to move forward with, to the community and Foundation board.
* Match the most promising projects with maintainers that have interest in taking them on.

## Proposal: Maintainer "Bench" Program

> Proposal: Grow and support a community of contributors that want to become maintainers.

New maintainers are unlikely to materialize in significant numbers unless we intentionally encourage them as a community. In addition, the project forge concept has a strong dependency on a growing set of maintainers.

The bench program will provide training, guidance and support, to help contributors feel comfortable taking on project maintenance. Mentors will be made available that can help contributors work through challenges, technical, interpersonal, and (critically important) motivational.

Maintainers need vacations! The foundation will provide limited-service backup maintainers (if desired) to ensure a project moves forward while the maintainer is away, per their instructions. It may be as simple as merging Dependabot PRs.

Maintainers may want to move on, and we want to enable new maintainers to take over to help with project continuity.

A new working group will be formed to manage the maintainer bench program within the .NET Foundation. It will:

* Provide docs, and guidance (for self-help).
* Provide training for free Foundation services (for projects).
* Run an ecosystem-wide "up-for-grabs" or "help-wanted" board for projects.
* Match mentors to projects.
* Identify gaps in maintainer/contributor tools that should be proposed as (high priority) projects to the Forge.

## Summary of Benefits

These proposals are intended to provide solutions for challenges in the software industry, for the .NET ecosystem, with the following desired benefits:

* **For maintainers:** increase adoption and contributors, by describing and improving project quality for users according to a shared quality definition (the maturity profiles).
* **For contributors:** improves opportunities and mentorship available for personal growth and community engagement.
* **For users:** improves the security and transparency of the open source software supply chain, by making it easier to select dependencies.
* **For users:** increases the availability of libraries that satisfy important scenarios, by adopting a structured process for matching new projects with maintainers.

As part of developing this proposal, the working group learned that there are an increasing set of industry programs that are addressing related challenges. Most of them include tools that enable looking up a package to learn about licensing, vulnerability and other package/project information. .NET packages don't work well with those tools today, because they do not expose the correct metadata. A major shared benefit of this proposal is that it can be used to better align .NET workflows and developer tools with those industry programs so that the correct metadata is always available, enabling consumers to successfully learn about .NET packages with these industry tools.

## Next Steps

The .NET Foundation will start a pilot program based on this proposal. The pilot will include a small number of projects to validate the fundamentals of the proposal. It will also act as an initial demonstration of the ideas, essentially a proof of concept. While the pilot program will be kept small, any project can register to be included.

While the pilot is running, it is important to get broad community feedback on the proposal. The working group will be seeking feedback from maintainers, contributors, and users. In terms of users, the working group will seek feedback from individuals, companies, public organizations and governments.

Some of the ideas proposed will be controversial, and it isn't expected that everyone will want to participate. That's okay! This is entirely voluntary, and is intended for projects for which it's a good fit.

The initial public feedback period will be open for 60 days. After the proposal has received broad feedback, and appropriately amended, it will be put to a vote with the .NET Foundation board. The board will be given access to community feedback before voting. If the board votes to move forward with the proposal, then the pilot will be expanded to encompass all aspects of the proposal and the .NET Foundation will encourage broad community participation.

Please provide your feedback, via filing an issue in this repo, reaching out to working group by mail, or requesting a conversation or call.
