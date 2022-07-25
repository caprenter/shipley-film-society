# shipley-film-society

**NB We have two versions at the moment. See "Branches" below**

## About

This is a static site to replace the current site at http://www.shipleyfilmsociety.org.uk/

## Local Development
To run this locally

Clone the repository
 
	cd shipley-film-society	
	bundle exec jekyll serve --baseurl=""
	
## Contributing

Please fork the repo,and make pull requests from your clone to this one.

### Branches

We're working on a new version of the site all that development should treat the `version2` branch like the main branch

So:
- `main` holds the most recent code *for the current site*
- `gh-pages` holds the current site - it may be behind main
- `version2` is the main development branch for the new site
- `(number)-(name)` branches are working branches where (number) is an issue number and (name) is made up, but has some relation to the issue

### Workflow

* Pick (or create an issue)
* Create a branch (from main if practical) - name the branch (issue number)-(suitable name) e.g. 23-fix-the-footer
* Work on the branch. 
* Push to your own fork
* Make a pull request in this repo.
