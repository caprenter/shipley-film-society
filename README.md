# shipley-film-society

## About

This is a static site to replace the current site at http://www.shipleyfilmsociety.org.uk/

It is deployed via the gh-pages branch of this repo using Github Pages.

## Adding content
All the data about the films is stored in _data/films.csv

Once the data is mapped to a collection in _config.yml
you can generate markdown for each collection entry
by running `bundle exec jekyll pagemaster {collection name}`

This command will generate markdown for views for each item in the collection
under `./_{collection name}`

To update generated markdown delete that directory
as existing files are not updated when pagemaster runs

### Film Descriptions
You can use markdown in the csv for the film description

A short description is useful for e.g. the front page where we don't want loads of text.

### Films listings
We parse the data from the CSV file when the site is built, and display information in various places

Front page - next film, and all upcoming films for the season
Films page - all upcoming films and past films

### Home Page
Use a mixture of index.md and _includes/main.md to curate content on the homepage.

To update the home page to highlight the next film, change the 'our_id' variable in the front matter to match the film id in the CSV file.

### Twitter Cards
The twitter card code should use the latest film image if you're linking to the home page, or a default if there is no next film. The default is defined in _includes/head.html

Individual pages (e.g. about) define a cover image in the front matter which is used for all pages except 'home'

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
