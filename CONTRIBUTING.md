## Contributing

First off, thank you for considering contributing to this project. It's people like you that make github such a great tool.

### 1. Where do I go from here?

If you've noticed a bug or have a question don't hesitate in opening an [issue][] to see if 
someone else in the community has already created a ticket. If not, go ahead and
[make one][new issue]!

### 2. Fork & create a branch

If this is something you think you can fix, then [fork this project][] and
create a branch with a descriptive name.

A good branch name would be (where issue #325 is the ticket you're working on):

```sh
git checkout -b 325-add-japanese-translations
```
### 3. Did you find a bug?

* **Ensure the bug was not already reported** by [searching all issues][].

* If you're unable to find an open issue addressing the problem,
  [open a new one][new issue]. Be sure to include a **title and clear
  description**, as much relevant information as possible, and a **code sample**
  or an **executable test case** demonstrating the expected behavior that is not
  occurring.

* If possible, use the relevant bug report templates to create the issue.
  Simply copy the content of the appropriate template into a file, make the
  necessary changes to demonstrate the issue, and **paste the content into the
  issue description**:
  * [**Topic** master issues][new issue]

### 4. Implement your fix or feature

At this point, you're ready to make your changes! Feel free to ask for help;
everyone is a beginner at first :smile_cat:

### 5. View your changes

Everything provided by this repo is meant to be used by humans, not cucumbers. So make sure to take
a look at your changes in a browser.

### 6. Get the style right

Your patch should follow the same conventions & pass the same code quality
checks as the rest of the project. 

### 7. Make a Pull Request

At this point, you should switch back to your master branch and make sure it's
up to date with project's master branch:

```sh
git remote add upstream git@github.com:paulushcgcj/daitan-k8s-bootcamp.git
git checkout master
git pull upstream master
```

Then update your feature branch from your local copy of master, and push it!

```sh
git checkout 325-add-japanese-translations
git rebase master
git push --set-upstream origin 325-add-japanese-translations
```

Finally, go to GitHub and [make a pull request][] :D

We care about quality, so your PR won't be merged until everything is OK. It's unlikely,
but it's possible that your changes won't be merged. In that case, comment on the PR and we will revisit it!

### 8. Keeping your Pull Request updated

If a maintainer asks you to "rebase" your PR, they're saying that a lot of code
has changed, and that you need to update your branch so it's easier to merge.

To learn more about rebasing in Git, there are a lot of [good][git rebasing]
[resources][interactive rebase] but here's the suggested workflow:

```sh
git checkout 325-add-japanese-translations
git pull --rebase upstream master
git push --force-with-lease 325-add-japanese-translations
```

### 9. Merging a PR (maintainers only)

A PR can only be merged into master by a maintainer if:

* It is passing the requirements.
* It has been approved by at least one maintainer. If it was a maintainer who
  opened the PR, only one extra approval is needed.
* It has no requested changes.
* It is up to date with current master.

Any maintainer is allowed to merge a PR if all of these conditions are
met.

### 10. Shipping a release (maintainers only)

Maintainers need to do the following to push out a release:

* Make sure all pull requests are in and that changelog is current
* Create a stable branch for that release:

  ```sh
  git checkout master
  git fetch daitan-k8s-bootcamp
  git rebase daitan-k8s-bootcamp/master
  # If the release is 2.1.x then this should be: 2-1-stable
  git checkout -b N-N-stable
  git push daitan-k8s-bootcamp N-N-stable:N-N-stable
  ```

[issue]: https://github.com/paulushcgcj/daitan-k8s-bootcamp/issues?q=something
[new issue]: https://github.com/paulushcgcj/daitan-k8s-bootcamp/issues/new
[fork this project]: https://help.github.com/articles/fork-a-repo
[searching all issues]: https://github.com/paulushcgcj/daitan-k8s-bootcamp/issues?q=
[make a pull request]: https://help.github.com/articles/creating-a-pull-request
[git rebasing]: http://git-scm.com/book/en/Git-Branching-Rebasing
[interactive rebase]: https://help.github.com/articles/interactive-rebase
