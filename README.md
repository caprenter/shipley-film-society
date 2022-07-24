# shipley-film-society

## About

This is a static site to replace the current site at http://www.shipleyfilmsociety.org.uk/

It is deployed via the gh-pages branch of this repo using Github Pages.

## Adding content
All the data about the films is stored in _data/films.csv

### Film Descriptions
You can use markdown in the csv for the film description

A short description is useful for e.g. the front page where we don't want loads of text.

### Films listings
We parse the data from the CSV file when the site is built, and display information in various places

Front page - next film, and all upcoming films for the season
Films page - all upcoming films and past films

### Home Page
Use a mixture of index.md and _includes/main.md to curate content on the homepage.


## Local Development
To run this locally

Clone the repository
 
	cd shipley-film-society	
	bundle exec jekyll serve
	
## Contributing

Please fork the repo,and make pull requests from your clone to this one.

### Branches

- `main` holds the most recent code
- `gh-pages` holds the current site - it may be behind main
- `(number)-(name)` branches are working branches where (number) is an issue number and (name) is made up, but has some relation to the issue

### Workflow

* Pick (or create an issue)
* Create a branch (from main if practical) - name the branch (issue number)-(suitable name) e.g. 23-fix-the-footer
* Work on the branch. 
* Push to your own fork
* Make a pull request in this repo.
