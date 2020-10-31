# <div align="center">MiniValine</div>

# CONTRIBUTING

First of all, thanks for taking your time to contribute and help make our project even better than it is today! The following is a set of guidelines for contributing to [MiniValine](https://github.com/MiniValine) and its libs submodules. These are mostly guidelines, not rules. Use your best judgment, and feel free to propose changes to this document in a pull request.

## Table Of Contents

[How Can I Contribute?](#how-can-i-contribute)

  * [Before Submitting An Issue](#before-submitting-an-issue)
    * [Read the docs](#read-the-docs)
    * [Quick debug instructions](quick-debug-instructions)
  * [Reporting Bugs](#reporting-bugs)
    * [Reporting Security Bugs](#reporting-security-bugs)
  * [Suggesting Enhancements](#suggesting-enhancements)
  * [Submitting a Pull Request](#submitting-a-pull-request)
  * [Creating Releases](#creating-releases)

[Guides](#guides)

  * [Coding Rules](#coding-rules)
  * [Coding Standards](#coding-standards)
  * [Labels Rules](#labels-rules)
  * [Commit Messages Rules](#commit-messages-rules)

## How Can I Contribute?

### Before Submitting An Issue

#### Read the docs

If you just have a question, you'll get faster results by checking the [FAQs](https://github.com/MiniValine/MiniValine/blob/master/.github/FAQ.md) for a list of common questions and problems

Also, you can perform a [cursory search](https://github.com/MiniValine/MiniValine/search?q=&type=Issues&utf8=%E2%9C%93) to see if the problem has already been reported or solved. You don't want to duplicate effort. You might be able to find the cause of the problem and fix things yourself, or add comments to the existed issue.

#### Quick debug instructions

Before submitting an Issue on GitHub, you can follow the steps below to debug:

* Execute clear the browser cache and disable all CDN services (e.g. Cloudflare Rocket Loader)
* Upgrade MiniValine to the latest version.
* Upgrade Node.js and `npm` to the latest version.
* Uninstall all non-essential plugins, or reinstall all plugins using `npm install --save`.

If you get an error message from your browser, please search in Google / Stackoverflow / GitHub Issues, or report it to us when submitting a new Issue.

If you find a bug in the source code, most importantly, please check carefully if you can reproduce the problem [in the latest release version of MiniValine](https://github.com/MiniValine/MiniValine/releases/latest). Then, you can help us by [Reporting Bugs](#reporting-bugs) or [Suggesting Enhancements](#suggesting-enhancements) to our [Repository](https://github.com/MiniValine/MiniValine). Even better, you can [submit a Pull Request](#submitting-a-pull-request) with a fix.

### Reporting Bugs

Before creating bug reports, please check [this list](#before-submitting-an-issue) as you might find out that you don't need to create one. After you've determined the repository your bug is related to, create an issue on that repository and provide the information as many details as possible by filling in [the required template](ISSUE_TEMPLATE.md).

Following these guidelines helps maintainers and the community understand your report :pencil:, reproduce the behavior, and find related reports:

* Use a clear and descriptive title for the issue to identify the problem.
* Provide more context by answering these questions:
  * Can you reproduce the problem? Can you reliably reproduce the issue? If not, provide details about how often the problem happens and under which conditions it normally happens.
  * Did the problem start happening recently or was this always a problem?
  * If the problem started happening recently, can you reproduce the problem in an older version of MiniValine? What's the most recent version in which the problem doesn't happen? You can download older versions of Next from [the releases page](https://github.com/theme-next/hexo-theme-next/releases).
  * Which version of Node, MiniValine are you using? You can get the exact version by running `node -v` in your terminal, or copy the contents in site's`package.json`.
  * Which packages do you have installed? You can get that list by copying the contents in site's`package.json`.
* Describe the exact steps which reproduce the problem in as many details as possible. When listing steps, don't just say what you did, but explain how you did it, e.g. which command exactly you used. If you're providing snippets in the issue, use [Markdown code blocks](https://help.github.com/articles/creating-and-highlighting-code-blocks/) or [a permanent link to a code snippet](https://help.github.com/articles/creating-a-permanent-link-to-a-code-snippet/), or a [Gist link](https://gist.github.com/).
* Provide specific examples to demonstrate the steps. Include links to files (screenshots or GIFs) or live demo.
* Describe the behavior you observed after following the steps and point out what exactly is the problem with that behavior.
* Explain which behavior you expected to see instead and why.

#### Reporting Security Bugs

If you find a security issue, please act responsibly and report it not in the public issue tracker, but directly to us, so we can fix it before it can be exploited. Please send the related information to thepie@qq.com (desirable with using PGP for e-mail encryption).

We will gladly special thanks to anyone who reports a vulnerability so that we can fix it. If you want to remain anonymous or pseudonymous instead, please let us know that; we will gladly respect your wishes.

### Suggesting Enhancements

Before creating enhancement suggestions, please check [this list](#before-submitting-an-issue) as you might find out that you don't need to create one. After you've determined the repository your enhancement suggestion is related to, create an issue on that repository and provide the information as many details as possible by filling in [the required template](ISSUE_TEMPLATE.md).

Following these guidelines helps maintainers and the community understand your suggestion :pencil: and find related suggestions.

* Use a clear and descriptive title for the issue to identify the suggestion.
* Describe the current behavior and explain which behavior you expected to see instead and Explain why this enhancement would be useful to most users.
* Provide specific examples to demonstrate the suggestion. Include links to files (screenshots or GIFs) or live demo.

### Submitting a Pull Request

Before creating a Pull Request (PR), please check [this list](#before-submitting-an-issue) as you might find out that you don't need to create one. After you've determined the repository your pull request is related to, create a pull request on that repository. The detailed document of creating a pull request can be found [here](https://help.github.com/articles/creating-a-pull-request/).

Following these guidelines helps maintainers and the community understand your pull request :pencil::

* Follow our [Coding Rules](#coding-rules) and [commit message conventions](#commit-messages-rules).
* Use a clear and descriptive title for the issue to identify the pull request. Do not include issue numbers in the PR title.
* Fill in [the required template](PULL_REQUEST_TEMPLATE.md) as many details as possible.
* All features or bug fixes must be tested in all schemes. And provide specific examples to demonstrate the pull request. Include links to files (screenshots or GIFs) or live demo.

### Creating Releases

Releases are a great way to ship projects on GitHub to your users.

1. On GitHub, navigate to the main page of the repository. Under your repository name, click **Releases**. Click **Draft a new release**.
2. Type a version number for your release. Versions are based on [Git tags](https://git-scm.com/book/en/Git-Basics-Tagging).
3. Select a branch that contains the project you want to release. Usually, you'll want to release against your `master` branch, unless you're releasing beta software.
4. Type a title and description that describes your release.
   - Use the version as the title.
   - The types of changes include **Breaking Changes**, **Updates**, **Features**, and **Bug Fixes**. In the section of Breaking Changes, use multiple secondary headings, and use item list in other sections.
   - Use the passive tense and subject-less sentences.
   - All changes must be documented in release notes. If commits happen without pull request (minimal changes), just add this commit ID into release notes. If commits happen within pull request alreay, just add the related pull request ID including all possible commits.
5. If you'd like to include binary files along with your release, such as compiled programs, drag and drop or select files manually in the binaries box.
6. If the release is unstable, select **This is a pre-release** to notify users that it's not ready for production. If you're ready to publicize your release, click **Publish release**. Otherwise, click **Save draft** to work on it later.

## Guides

### Coding Rules

This project and everyone participating in it is governed by the [Code of Conduct](CODE_OF_CONDUCT.md) to keep open and inclusive. By participating, you are expected to uphold this code.

### Coding Standards

We use ESLint and Stylint for identifying and reporting on patterns in JavaScript and Stylus, with the goal of making code more consistent and avoiding bugs. These specifications should be followed when coding.

### Labels Rules

We use "labels" in the issue tracker to help classify Pull requests and Issues. Using labels enables maintainers and users to quickly find issues they should look into, either because they experience them, or because it meets their area of expertise.

If you are unsure what a label is about or which labels you should apply to a PR or issue, look no further!

Issues related:

- By types
  - `Bug`: A detected bug that needs to be confirmed
  - `Feature Request`: An issue that wants a new feature
  - `Question`: An issue about questions
  - `Meta`: Denoting a change of usage conditions
  - `Support`: An issue labeled as support requests
  - `Polls`: An issue that initiated a poll
- By results
  - `Duplicate`: An issue which had been mentioned
  - `Irrelevant`: An irrelevant issue for Next
  - `Invalid`: An issue that cannot be reproduced
  - `Expected Behavior`: An issue that corresponds to expected behavior
  - `Need More Info`: Need more information for solving the issue
  - `Verified`: An issue that has been verified
  - `Solved`: An issue that has been solved
  - `Backlog`: An issue that is to be completed and later compensated
  - `Stale`: This issue has been automatically marked as stale because lack of recent activity

Pull requests related:

- `Breaking Change`: A pull request that makes breaking change
- `Bug Fix`: A pull request that fixes the related bug
- `New Feature`: A pull request that provides a new feature
- `Feature`: A pull request that provides an option or addition to existing feature
- `i18n`: A pull request that makes new languages translation
- `Work in Progress`: A pull request that is still working in progress
- `Skip Release`: A pull request that should be excluded from release note

Both:

- `Roadmap`: An issue / pull request about future development
- `Help Wanted`: An issue / pull request that needs help
- `Discussion`: An issue / pull request that needs to be discussed
- `Improvement`: An issue that needs improvement or a pull request that improves NexT
- `Performance`: An issue / pull request that improves the performance
- `Hexo`: An issue / pull request related to Hexo or Hexo plugins
- `Template Engine`: An issue / pull request related to template engine
- `CSS`: An issue / pull request related to CSS
- `Fonts`: An issue / pull request related to fonts
- `PJAX`: An issue / pull request related to PJAX
- `3rd Party Plugin`: An issue / pull request related to 3rd party plugins & service
- `Docs`: An issue / pull request related to instruction document
- `Configurations`: An issue / pull request related to configurations

### Commit Messages Rules

We have very precise rules over how our git commit messages can be formatted. Each commit message consists of a `type` and a `subject`. This leads to more
readable messages that are easy to follow when looking through the project history.

- `type` describes the meaning of this commit including but not limited to the following items, and capitalize the first letter.
  * `Build`: Changes that affect the build system or external dependencies
  * `Ci`: Changes to our CI configuration files and scripts
  * `Docs`: Documentation only changes
  * `Feat`: A new feature
  * `Fix`: A bug fix
  * `Perf`: A code change that improves performance
  * `Refactor`: A code change that neither fixes a bug nor adds a feature
  * `Style`: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
  * `Revert`: Revert some existing commits
  * `Release`: Commit a release for a conventional changelog project
- The `subject` contains a succinct description of the change, like `Update code highlighting in readme.md`.
  * No dot (.) at the end.
  * Use the imperative, present tense: "change" not "changed" nor "changes".

# CODE_OF_CONDUCT

A CODE_OF_CONDUCT dictates how conversation during code updates, issue communication, and pull requests should happen within [MiniValine](https://github.com/MiniValine/MiniValine) repository.  We expect all users to show respect and courtesy to others through our repositories. Anyone violating these rules will not be reviewed and will be blocked and expelled from our repositories immediately upon discovery.

## Table Of Contents

- [Our Pledge](#our-pledge)
- [Our Responsibilities](#our-responsibilities)
- [Our Standards](#our-standards)
- [Scope](#scope)
- [Enforcement](#enforcement)
- [Contacting Maintainers](#contacting-maintainers)
- [Attribution](#attribution)

## Our Pledge

As contributors and maintainers of this project, we pledge to respect all people who contribute through reporting issues, posting feature requests, updating documentation, submitting pull requests or patches, and other activities.

In the interest of fostering an open and welcoming environment, we are committed to making participation in our community a harassment-free experience for everyone, regardless of level of experience, gender, gender identity and expression, sexual identity and orientation, disability, personal appearance, body size, race, ethnicity, age, religion, or nationality.

## Our Responsibilities

Project maintainers have the right and responsibility to clarify the standards of acceptable behavior and are expected to remove, edit, or reject comments, commits, code, wiki edits, issues, and other contributions that are not aligned to this Code of Conduct, or to block temporarily or permanently any contributor for other behaviors that they deem inappropriate, threatening, offensive, or harmful.

## Our Standards

As a project on GitHub, this project is overed by the [GitHub Community Guidelines](https://help.github.com/articles/github-community-guidelines/). Additionally, as a project hosted on npm, it is covered by [npm Inc's Code of Conduct](https://www.npmjs.com/policies/conduct).

Examples of behavior that contributes to creating a positive environment include:

* Using welcoming and inclusive language.
* Being respectful of differing viewpoints and experiences.
* Gracefully accepting constructive feedback.
* Focusing on what is best for the community.
* Showing empathy and kindness towards other community members.

Examples of unacceptable behavior by participants include:

* The use of sexualized language or imagery and unwelcome sexual attention or advances
* Trolling, insulting/derogatory comments, and personal or political attacks
* Public or private harassment
* Publishing others’ private information, such as a physical or electronic address, without explicit permission
* Other conduct which could reasonably be considered inappropriate in a professional setting

## Scope

This Code of Conduct applies both within project spaces and in public spaces when an individual is representing the project or its community.

Depending on the violation, the maintainers may decide that violations of this code of conduct that have happened outside of the scope of the community may deem an individual unwelcome, and take appropriate action to maintain the comfort and safety of its members.

## Enforcement

If you see a Code of Conduct violation, follow these steps:

1. Let the person know that what they did is not appropriate and ask them to stop and/or edit their message(s) or commits. That person should immediately stop the behavior and correct the issue.
2. If this doesn’t happen, or if you're uncomfortable speaking up, [contact the maintainers](#contacting-maintainers). When reporting, please include any relevant details, links, screenshots, context, or other information that may be used to better understand and resolve the situation.
3. As soon as available, a maintainer will look into the issue, and take further action.

Once the maintainers get involved, they will follow a documented series of steps and do their best to preserve the well-being of project members.

All complaints will be reviewed and investigated and will result in a response that is deemed necessary and appropriate to the circumstances. The project team is obligated to maintain confidentiality with regard to the reporter of an incident. Further details of specific enforcement policies may be posted separately.

Thesehese are the steps maintainers will take for further enforcement, as needed:

1. Repeat the request to stop.
2. If the person doubles down, they will have offending messages removed or edited by a maintainers given an official warning. The PR or Issue may be locked.
3. If the behavior continues or is repeated later, the person will be blocked from participating for 24 hours.
4. If the behavior continues or is repeated after the temporary block, a long-term (6-12 months) ban will be used.

On top of this, maintainers may remove any offending messages, images, contributions, etc, as they deem necessary. Maintainers reserve full rights to skip any of these steps, at their discretion, if the violation is considered to be a serious and/or immediate threat to the well-being of members of the community. These include any threats, serious physical or verbal attacks, and other such behavior that would be completely unacceptable in any social setting that puts our members at risk.

Project maintainers who do not follow or enforce the Code of Conduct in good faith may face temporary or permanent repercussions as determined by other members of the project's leadership.

## Contacting Maintainers

You may get in touch with the maintainer team through any of the following methods:

* Through Email: thepie@foxmail.com

## Attribution

This Code of Conduct is adapted from the [Contributor Covenant](https://www.contributor-covenant.org/) and [WeAllJS Code of Conduct](https://wealljs.org/code-of-conduct).



# CLA

## MiniValine Individual Contributor License Agreement

Thank you for your interest in contributing to open source software projects (“Projects”) made available by MiniValine or its affiliates (“MiniValine”). This Individual Contributor License Agreement (“Agreement”) sets out the terms governing any source code, object code, bug fixes, configuration changes, tools, specifications, documentation, data, materials, feedback, information or other works of authorship that you submit or have submitted, in any form and in any manner, to MiniValine in respect of any of the Projects (collectively “Contributions”). If you have any questions respecting this Agreement, please contact thepie@foxmail.com.


You agree that the following terms apply to all of your past, present and future Contributions. Except for the licenses granted in this Agreement, you retain all of your right, title and interest in and to your Contributions.


**Copyright License.** You hereby grant, and agree to grant, to MiniValine a non-exclusive, perpetual, irrevocable, worldwide, fully-paid, royalty-free, transferable copyright license to reproduce, prepare derivative works of, publicly display, publicly perform, and distribute your Contributions and such derivative works, with the right to sublicense the foregoing rights through multiple tiers of sublicensees.


**Patent License.** You hereby grant, and agree to grant, to MiniValine a non-exclusive, perpetual, irrevocable,
worldwide, fully-paid, royalty-free, transferable patent license to make, have made, use, offer to sell, sell,
import, and otherwise transfer your Contributions, where such license applies only to those patent claims
licensable by you that are necessarily infringed by your Contributions alone or by combination of your
Contributions with the Project to which such Contributions were submitted, with the right to sublicense the
foregoing rights through multiple tiers of sublicensees.


**Moral Rights.** To the fullest extent permitted under applicable law, you hereby waive, and agree not to
assert, all of your “moral rights” in or relating to your Contributions for the benefit of MiniValine, its assigns, and
their respective direct and indirect sublicensees.


**Third Party Content/Rights.** If your Contribution includes or is based on any source code, object code, bug
fixes, configuration changes, tools, specifications, documentation, data, materials, feedback, information or
other works of authorship that were not authored by you (“Third Party Content”) or if you are aware of any
third party intellectual property or proprietary rights associated with your Contribution (“Third Party Rights”),
then you agree to include with the submission of your Contribution full details respecting such Third Party
Content and Third Party Rights, including, without limitation, identification of which aspects of your
Contribution contain Third Party Content or are associated with Third Party Rights, the owner/author of the
Third Party Content and Third Party Rights, where you obtained the Third Party Content, and any applicable
third party license terms or restrictions respecting the Third Party Content and Third Party Rights. For greater
certainty, the foregoing obligations respecting the identification of Third Party Content and Third Party Rights
do not apply to any portion of a Project that is incorporated into your Contribution to that same Project.


**Representations.** You represent that, other than the Third Party Content and Third Party Rights identified by
you in accordance with this Agreement, you are the sole author of your Contributions and are legally entitled
to grant the foregoing licenses and waivers in respect of your Contributions. If your Contributions were
created in the course of your employment with your past or present employer(s), you represent that such
employer(s) has authorized you to make your Contributions on behalf of such employer(s) or such employer
(s) has waived all of their right, title or interest in or to your Contributions.


**Disclaimer.** To the fullest extent permitted under applicable law, your Contributions are provided on an "asis"
basis, without any warranties or conditions, express or implied, including, without limitation, any implied
warranties or conditions of non-infringement, merchantability or fitness for a particular purpose. You are not
required to provide support for your Contributions, except to the extent you desire to provide support.


**No Obligation.** You acknowledge that MiniValine is under no obligation to use or incorporate your Contributions
into any of the Projects. The decision to use or incorporate your Contributions into any of the Projects will be
made at the sole discretion of MiniValine or its authorized delegates.


**Disputes.** This Agreement shall be governed by and construed in accordance with the laws of the State of
New York, United States of America, without giving effect to its principles or rules regarding conflicts of laws,
other than such principles directing application of New York law. The parties hereby submit to venue in, and
jurisdiction of the courts located in New York, New York for purposes relating to this Agreement. In the event
that any of the provisions of this Agreement shall be held by a court or other tribunal of competent jurisdiction
to be unenforceable, the remaining portions hereof shall remain in full force and effect.

**Assignment.** You agree that MiniValine may assign this Agreement, and all of its rights, obligations and licenses
hereunder.











