# psyche.systems

Website for [␥the␥psyche␥lab](https://psyche.systems) group.

## Running and building the website

The website is built with [jekyll](https://jekyllrb.com). 

## New members

### User data

Add your user information to the [users](_data/users.yml) data file ([YAML](https://yaml.org) format), following the format of the other entries. The entry starts with your self-assigned `username`. The `member:` field should be the name of your [members](/_members) page.

### Members page

Make a page about yourself in [_members](/_members). The front matter should be:

```yaml
---
name: Full Name
user: username
layout: default
---
```

### Projects

If you are involved with a specific [project](/_projects), add your `username` to the front matter `users:` field.

## Posting

Regular updates and research notes can be added as dated entries in the [posts](/_posts) directory.

## Assets

Images and other binary assets are hosted outside the repository ([ref.psyche.systems](https://ref.psyche.systems)).