# Astronaut

API documentation template for Jekyll. Forked from `aviator-jekyll-template` by Cloud CMS.

## Develop

Aviator was forked from `aviator-jekyll-template` by Cloud CMS. Built with [Jekyll](http://jekyllrb.com/) version 3.1.6, but should support newer versions as well.

Install the dependencies with [Bundler](http://bundler.io/):

~~~bash
$ bundle install
~~~

Run `jekyll` commands through Bundler to ensure you're using the right versions:

~~~bash
$ bundle exec jekyll serve
~~~

### Usage

* Each section is a different collection, this helps organise your content.
* Set the order of the collections with the position field in collection configuration in `_config.yml`.
* Set the order of the documents inside a collection by setting the position in front matter.

### Search

* Add `excluded_in_search: true` to any documentation page's front matter to exclude that page in the search results.
