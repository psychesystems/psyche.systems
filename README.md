# psyche.systems

Website for [␥the␥psyche␥lab](https://psyche.systems) group.

## Running and building the website

The website is built with [jekyll](https://jekyllrb.com). Install [ruby](https://www.ruby-lang.org), e.g. via [brew](https://brew.sh):

```sh
brew install chruby ruby-install
ruby-install ruby 3.3.5
chruby 3.3.5
```

Clone the repository, install required gems, and start the local server:
```sh
git clone git@github.com:psychesystems/psyche.systems.git
cd psyche.systems
gem install bundler jekyll
bundle install
bundle exec jekyll serve
```

## Editing the website

The `main` branch of the repository is [protected](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/about-protected-branches). To make an edit, create a new branch (manually or via an issue) and make a [pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request). Pull requests [are reviewed](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/about-protected-branches#require-pull-request-reviews-before-merging) by another member of the team before merging.

## New members

### User data

Add your user information as a [YAML](https://yaml.org) file in the [users](_data/users) data directory. The file basename should be your self-assigned `username`. The required keys are:

```yaml
name: Your Full Name
label: Name
position: Your Position
```

where `label: Name` is the part of your name you'd like to appear in member lists associated with collections. 

For example

```yaml
name: Mark James Adams
label: Adams
position: Senior Research Fellow
```

Then add your username to the [groups](_data/groups.yml) file to specify your role (`staff` or  `student`).

#### Links and social media

Add web and social media links as a list under `links:`. Each entry should have a `title:` and `url:` key.

For websites, format the `title` with the domain name and/or path. For example, if the `url:` is `https://domain.tld/path`, the title should be `domain.tld/path`, `domain.tld`, or `path`.

For social media, format the `title:` with your handle as `"@handle"` (in quotes) and use your profile's URL for the `url:`.

### Member's page

Make a page about yourself in [_members](/_members). The front matter should be:

```yaml
---
user: username
layout: member
---
```

### Projects

If you are involved with a [project](/_projects) or [collaboration](/_collabs), add your `username` to the front matter `users:` field.

## Posting

Regular updates and research notes can be added as dated entries in the [posts](/_posts) directory.

## Assets

Images and other binary assets are hosted outside the repository ([ref.psyche.systems](https://ref.psyche.systems)).
