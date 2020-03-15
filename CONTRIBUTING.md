# How to contribute to image-rs

Welcome! When you are reading this, chances are, you are wondering about
contributing. The joyful news is that this is easy, and simple. You need not
even have written any line of code.

## Code of Conduct

Follow the [Code of Conduct][COC]. In less elaborate terms, keep the community
welcoming and respectful to all and disagree calmly, encourage productive
experimentation and fresh ideas. **This also applies to the gitter channels**.

[COC]: CODE_OF_CONDUCT.md

## Membership and Teams

There are four basic groups within the organization:

| Group | Permissions | Responsibilities | Requirements |
|:--|:--|:--|:--|
| anyone | A personal [blog page](#blog) and issue administration | - | None, simply [ask to be added][OrgJoin] |
| Collaborator | Write access to repositories, create repos | None, PR help and reviews appreciated | Successfully get a PR merged |
| Publish | Ownership on `crates.io` | Finalizing releases and publishing new versions | Invite only |
| Admin | Managing teams | Ensure PR progress, Resolve conflicts, Arbitrate | Distinguished community member |

[OrgJoin]: https://github.com/image-rs/organization/issues/1

We use the issue tracker for most tasks. We *try* to plan as much as possible
up front and break the tasks down into 'Easy' tasks. You do not necessarily
need to know a lot about Rust to work on the project. Even organizational work,
improved documentation, and planning help greatly in progressing the project.

The most common way of contributing is by creating an issue or PRs. You do not
need write access, you do not have to be added as collaborator.  If you need
write access to a specific repository and you for some reason do not want to
join one of the above teams, people in the Admin group can also invite you as
an outside collaborator.

The `image-rs` project is devised as a community project. In contrast to other
large projects it is not particularly backed by a larger entity. This means
that to ensure progress, **your help** is required but also that each
individual's input is valued. Division into teams is done mostly to manage
risks from a security perspective and to ensure that users of the crates can
have trust in the libraries' integrity. The judgement of experience and
helpfulness is made informally by the people sending the invitation, in cases
of doubt please contact an admin. Membership may be removed without warning
if suspicious activity is discovered.

If, after a successful contribution, you are not added as collaborator, post a
message [here][CollaboratorJoin]. When you are a collaborator you can assign
issues to yourself, make commits and merges to the repository and also create
new projects. Maybe also look around and see if there are unassigned issues
that fit your skill, or even ones that challenge yourself. Offer feedback to
other contributors that seek it.

[CollaboratorJoin]: https://github.com/image-rs/organization/issues/2

## Types of contributions

Feel free to open issues, post comments about progress, questions, new ideas,
brain storming etc. You can edit comments as a way of refining ideas in the
issue tracker. Many issues needs to be broken down into new issues before they
can be implemented. Please add comments like "can copy code from X" that tells
other people how you do it efficiently.

If you have an idea how to make collaboration better, open an issue.

We also have a [blog](https://github.com/image-rs/blog.image-rs.org) and a
[webpage](https://github.com/image-rs/image-rs.github.io) to track our
progress. Any member of the organization is free to contribute! This includes
and encourages personal reports, essays, and notices about usage of the
library, possible future directions or design goals. These will be considered
when progress reports (every ~3 months) or update project focus (every ~1
year).

## A note about code formatting and `rustfmt`

Consistent formatting can make code more legible and reduces contribution
overhead. Unfortunately, the `rustfmt` tool does not always perform
particularly well in this regard, especially for large projects. Therefore, it
can sometimes even be a roadblock as small changes may affect disproportionate
amounts of code which then leads to discussions on syntax that it was supposed
to help avoid. [You can read more in-depth opinions in the internals thread][fmt-internals].

So what's the policy? When a project is small enough or recent then we'll try
to use `fmt` and add it to CI. But for the large, main `image` project it is
not really a good fit—introducing it would format a seventh of all code and
definitely requires manual review [1][fmt-image]. This may of course change in
the future. If it becomes possible to use it with less aggressive settings,
e.g. to only format and order imports, we'll revise this section and try to
agree on a common configuration file.

[fmt-internals]: https://internals.rust-lang.org/t/forced-rustfmt-is-a-roadblock-to-contributing/11913
[fmt-image]: https://github.com/image-rs/image/pull/1162

## Getting started with coding

Here is how you get started (using the `image` repository as an example):

1. [Fork](https://github.com/image-rs/image/fork) the respective repository.
2. Clone your repository to the local hard drive ([GitHub for Mac](https://mac.github.com/), [Github for Window](https://windows.github.com/)).
3. Open up the Terminal and navigate to the project directory.
4. If you have not installed Rust yet, download it [here](https://rustup.rs/).
5. Type `cargo build` to build the library.

You work against the fork as you would do with personal projects. When you want
review of your code, open up a pull request on Github. *Even if it is just a
small change, a PR makes it easier for other people to follow the changes.*

## Donations

If you feel charitable, your best option at this moment is to support a local
charity of your choice. Should you happen to run across one of the contributors
at a conference you could also offer to buy them a drink or coffee.

