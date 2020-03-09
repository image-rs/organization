## Merging PRs

We encourage members to merge pull requests that have been discussed and do not have 
outstanding questions. You are allowed to merge your own PRs as well! This advice 
holds especially if the change does not introduce any SemVer relevant changes. In the 
event of uncertainty, solicit feedback from maintainers. (TODO: we might benefit from
waiting-on-author and waiting-on-discussion tags).

In case there are breaking changes then it need only be made clear to the publish team,
and the author should weigh the benefits to the extra version churn introduced—large
new features are almost always worth it. One strategy we tried out with `image` was also
to create a separate parallel `next` branch to accept and collect breaking changes until
a critical mass has been accumulated to justify the breaking change.

## Release procedure

The following is an description of the current, actual release procedure for those with 
`publish` permissions and for public review in trust. Some justification is given below.

1. Create a new branch with the name `release-<version>`
2. Push any pending meta data changes and the version increment
3. Wait for CI to approve the tip of the branch—not necessarily the PR itself
4. Run `cargo publish` with a clean tree on the commit approved by CI
5. Create a new tag `v<version>` (or `name-v<version>` in workspace repositories).
   The contents of that tag are full or abbreviated change notes and it CAN be signed.
   5.1. Add to the tag description a sha256 hash of the packed crate which was created
        by cargo in `target/package/`. This is optional, signed tags SHOULD include it.
6. Merge the PR on Github
7. Push the new tag

It should be said that the CI checks for merges are somewhat weak. They do not get rerun, 
at least with Travis, when the base branch changes. This is why latest commit of the 
branch should be the deciding factor, not the success of the created merge commit. Recall 
that this is also what goes into the published package.

As has been observed, merging the PR after publishing theoretically runs the risk of 
some intermediate merge having created a merge conflict. This is however no practical
concern at the current rate. If ever, an explicit merge should be created so that the
commit with which the package was published stays in the tree.
