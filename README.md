# Ember TED Docs

Components for writing docs sites for your open-source projects at TED.

![Demo](https://cloud.githubusercontent.com/assets/2922250/9823883/1663a7c6-5897-11e5-9aeb-ebe94155facf.png)

## Requirements

This is an Ember addon, so it assumes you'll be creating your docs site as an Ember app.

**Documenting an Ember addon**

You already have an Ember app under `/tests/dummy`, so you can just use that for your docs site. There's also [a great addon](https://github.com/poetic/ember-cli-github-pages) that makes it easy to deploy this app to GitHub Pages.

**Documenting another project**

You'll be making a new Ember app for your docs. [Install Ember CLI](http://www.ember-cli.com) if you haven't already. Then, from your project's repo, check out an orphaned branch:

```sh
git checkout --orphan docs
git clean -fd  # this removes the working files in your directory
```

## Installation

Install the following addons:

```sh
ember install ember-cli-sass
ember install ember-cli-bootstrap-sassy
ember install ember-ted-docs
```

and import Bootstrap and TED docs' styles (you may need to rename `app.css` to `app.scss`: 

```
<!-- tests/dummy/app/styles/app.scss -->
@import 'bootstrap';
@import 'ember-ted-docs/styles';
```

Now `ember s` and develop your docs using the components below.

## Usage

In your template you can now use the `<ted-page-header>` component:

```hbs
{{ted-page-header
  subheading='My'
  slim-heading='Awesome'
  strong-heading='Library'
  byline='The best, most amazing thing to happen to anyone, anywhere'}}
```

and here's what you get:

![Demo](https://cloud.githubusercontent.com/assets/2922250/9823883/1663a7c6-5897-11e5-9aeb-ebe94155facf.png)

Now, go forth and document!
