# .NET Foundation Maturity Ladder Policies

This document describes policies for the [.NET Foundation Maturity Ladder](maturity-ladder.md).

Any .NET open source project is welcome to participate in the maturity ladder program. Registering for the maturity ladder is separate from applying to be member project of the .NET Foundation. This distinction is covered in more detail later.

## Just ask for help

Some aspects of the maturity ladder might be complicated or hard. You can get direct 1 on 1 help to work through problems. You can reach out to the working group (link coming) to ask questions or find someone to work with you.

## Registration

Projects can request to participate in the maturity ladder by pull request on this repository, following this pattern:

* Describe your project using the pattern used in the [project template](projects/_sample.md).
* Hyperlink all relevant text, including GitHub handles. Full names can also be included, potentially with links to other resources (like a blog).
* Name your file according to your project (for example `banana.md` for the "Banana project").
* Add file to the [projects](https://github.com/dotnet/foundation/tree/master/projects) directory.
* All maintainers and trusted successors must separately add their GitHub handle and/or a timestamp beside their handle by git commit. This process demonstrate their acceptance of their respective roles in the project and to participating in the maturity ladder.
* Make a pull request on this repository. The pull request description should make it clear when the working group should start the review process.
* If accepted, the PR will be merged with all commits intact (no squashing).

There is a preference to keeping these project files relatively short and uniform. Supporting information (for example, links to CI) that demonstrate satisfying the ladder requirements should be included in the PR description, or better yet, on a project-owned page (for example, on GitHub). A template can be created for that if there is a demand.

Maintainers must have an active [.NET Foundation personal membership](https://dotnetfoundation.org/become-a-member) to register , which can be established at no cost. This requirement is intended as a light-weight mechanism to ensure that the interests of maintainers and the .NET Foundation are aligned. For example, there may be Foundation membership votes that are of interest to maintainers.

Trusted successors do not need an active .NET Foundation personal membership, although they are invited to create one.

Trusted successors are requested to update the timestamp beside their handle ([example](projects/_sample.md#trusted-successors)) every 90-180 days to validate that they remain available, both generally, and for this this particular role.

Project users cannot register on the behalf of a maintainer. They are free to request maintainers to register (just like they might file a feature request).

## .NET Foundation Project Membership

.NET Foundation Project Membership is separate from the ladder, but integrated in the following way:

* Projects do not need to formally join the Foundation to participate in the ladder.
* Projects are given the option to join the Foundation at level 2.
* Projects must [join the Foundation](https://github.com/dotnet/foundation/blob/master/guidance/new-projects.md) at level 3. Exemptions may be granted by the working group by specific request.

Why link the ladder with Foundation membership? In short, this is how other foundations work, and it is considered a good model for growing projects from incubation to graduation for broad ecosystem benefit. However, the working group sees significant value in making the ladder a more generally applicable definition of quality for the ecosystem to use. That's why Foundation membership is part of the ladder but doesn't start with it. Level 3 was considered a good point to include Foundation membership as a required characteristic.

There are also more practical considerations. Levels 3 and 4 include requirements that require paying for things (like signing certificates). Level 4 includes a requirement to use trusted infrastructure. It is much easier to avoid maintainers having out-of-pocket expenses and to satisfy trust requirements if levels 3 and 4 are limited to .NET Foundation projects. It is also easier to add  potentially costly ($) requirements later on, due to the changing requirements of the industry, if the Foundation simply pays those costs for Foundation projects. For example, the Foundation may upgrade to a higher cost version of static analysis tools and publish that as a new benefit of all level 3 and 4 projects.

## Existing .NET Foundation Projects

Existing .NET Foundation projects are encouraged but not required to participate in the maturity ladder program. A working group member will be made available for projects that need help.

## Forge projects

New projects created in the [project forge](README.md#proposal-project-forge) will be established as .NET Foundation projects. They will be given initial support such that they can satisfy level 2 relatively easily.

## Working group process

The working group will process ladder registration requests regularly. The same model will be used for new projects as well as level promotions. One of the following approaches will be used:

* The working group accepts the registration, possibly with requested improvements.
* The working group rejects the registration, with feedback.
* The working group puts the registration up for a membership vote, and makes a public decision based on the result of the vote. This is more likely for level 3 and 4 candidates.

Ladder level promotions need to be championed by a working group member who agrees to mentor the library, or identifies a community member who can provide mentorship.

## Leaving the program policy

Projects can remove themselves from the [maturity ladder](maturity-ladder.md) program at any time. Project removal needs to be done in a staged way (over 60 days) to give consumers an opportunity to react to changes in policy. Project removals will be announced ahead of time.

The [project forking policy](project-continuation-policies.md#project-forking-policy) may be used for projects that are removed from the program.

## Projects no longer meeting ladder requirements

In some cases, projects may falter in their practices relative to their current ladder level. When this occurs, a mentor will be assigned to help the project get back on track. If the maintainers are unable or unwilling to re-adopt their previous practices, then the project will be removed from the program, with a friendly note that it can re-apply again at another time.

The [project forking policy](project-continuation-policies.md#project-forking-policy) may be used for projects that are removed from the program.

## Maintainer changes license or deletes (goes closed) source

A maintainer may change plans in a way that is incompatible with the program at any time, and not offer the .NET Foundation an opportunity for a graceful exit from the program. When this happens, the project will be removed from the program.

The [project forking policy](project-continuation-policies.md#project-forking-policy) may be used for projects that are removed from the program.

## Maintainer code of conduct violations

It is unlikely but possible that a maintainer might start to violate the code of conduct of their own project. All code of conduct violations are taken seriously by the Foundation.

* Maintainers will be given one code of conduct violation warning, which is considered to last one year.
* Upon a second violation, the project will be removed from .NET Foundation programs, including the maturity ladder.
* Severe violations, such as hate speech, or threats of violence will result in immediate removal.
* Intentional inclusion of malicious code in source or project distributions will result in immediate removal.
* If a project with multiple maintainers wants to prevent project removal, then they can choose to remove the maintainer(s) who violated the policy.

The [project forking policy](project-continuation-policies.md#project-forking-policy) may be used for projects that are removed from the program.
