## How GitHub repositories and discussions can serve as CMS

> **Note** TL;DR: Read this only if you want to know how it works, but this not required to contribute to this repository specifically.

This is how GitHub repositories and the _Discussions_ tab can used as [Content Management System](https://en.wikipedia.org/wiki/Content_management_system)s.

## A brief intro into the GitHub discussions and repository system

GitHub has a nice repository permission-based system and it also has a collaborative feature called _Discussions_ (see [Discussions Quickstart](https://docs.github.com/en/discussions/quickstart)).

- A repository have unlimited amount of collaborators and admins.
- Anyone who has a GitHub account can open an discussion but [they can't add _Announcements_ category](https://github.blog/changelog/2021-05-18-github-discussions-labels-and-announcements-category-format/) without an admin permission (useful in a blog to avoid spamming or processing of [untrusted data](https://owasp.org/www-community/Injection_Theory)).
- Some _Discussion_ features:
  - Have an author and can have partipants (those who are commenting/sharing feedback in the discussion).
  - Have multiple labels/tags.
  - Can have feedback through the comments.
  - Have an [integrated markdown editor](https://github.com/byrintt/log/discussions/new?category=Submitted&welcome_text=true), including image hosting (+ drag-and-drop) (max 5mb) support.
  - Have _categories integrated with the repository permission system_.

If we replace _repository_ with _project_ and _discussion_ with _blog post_ we've a collaborative CMS that is based on your GitHub account.

## GitHub repository permission-system

These permissions can be added through the _Settings -> Collaborators -> Add people_.

### Basic _personal accounts_ repository permissions

These are the permissions available on repositories owned by personal GitHub accounts.

- **Outside collaborators**: users that have no permissions in a repository, e.g: I'm a outside collaborator in a repository of yours and vice-versa.
- **Collaborator**: can pull (read) the contents of the repository and push (write) changes to the repository, but they do not have admin permissions as the _Owner_ does, so they can't modify repo settings, add other collaborators or even make use of _Announcements_ discussion category.
- **Owner**: full-access, the repository owner, can not be shared with another personal account.

### Basic _organization_ repository permissions

These roles are available to repositories owned by organizations.

- **Outside collaborators**: users that have no permissions in a repository, e.g: I'm a outside collaborator in a repository of yours and vice-versa.
- **Triage**: can manage issues and pull requests but doesn't have any write access.
- **Maintain**: can do anything in the repository except by adding other maintainers and modifying repository settings (deleting, making public or private, etc.).
- **Admin**: full-access.

## Lets convert it to a blog 

But firstly lets define some high-level requirements:

1. If you're looking for a blog which:

- You are the only one who can publish posts.
- Accept or not external collaboration (post written by outside collaborators).

Then you can use a repository in your personal account or organization, but you should be the only one with _Admin_ or _Owner_ roles (this is required by default on repositories owned by personal accounts).

2. If you are looking for a blog which:

- You + other people choosen by you can publish posts.
- Accept or not external collaboration (post written by outside collaborators).

Then you need to use a repository owned by a organization because of [personal account limitations](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-personal-account-settings/permission-levels-for-a-personal-account-repository) (Ownership permissions can't be shared with another personal account).
