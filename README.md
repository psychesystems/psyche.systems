# psyche.systems

Website for [␥the␥psyche␥lab](https://psyche.systems) group.

## Running and building the website

The website is built with [jekyll](https://jekyllrb.com). 

## New members

### User data

Add your user information to as a [YAML](https://yaml.org) file in the [users](_data/users) data directory. The file basename should be your self-assigned `username`. The required keys are:

```yaml
name: Your Full Name
label: Name
```

where `Name` is the part of your name you'd like to appear in member lists associated with collections.

For example

```yaml
Name: Mark James Adams
label: Adams
```

#### Links and social media

Add links and social media links as a list under the key `links:`. Each entry should have a `title:` and `url:` key.

For websites, format the `title` with the domain name and/or path. For example, if the `url:` is `https://domain.tld/path`, the title should be `domain.tld/path`, `domain.tld`, or `path`.

For social media, format the `title:` with your handle as `"@handle"` (in quotes) and use your profile's URL for the `url:`.

### Members page

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