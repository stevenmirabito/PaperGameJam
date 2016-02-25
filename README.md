CSH Paper Game Jam
==================

This is the public website for the CSH Paper Game Jam. The live website is available at: http://papergamejam.com/

## Build Instructions (Jekyll)
1. Clone this repo
2. Certain assets (Bootstrap and jQuery at the time of writing) are managed by [Bower](http://bower.io/). Update them by running:
```
bower update
```
3. Finally, run the following command to build the site:
```
jekyll build
```

The generated static website will be available in `_site`.

## Modification
The site has been designed to be as modular as possible. Check out the YAML front matter at the top of each page to see the variables and layouts used.

#### To add a new page and have it appear in the navigation bar:
Simply include this front matter at the top of the file:
```
---
layout: framework
group: navigation
order: {ORDER_IN_NAV}
parent: {PARENT_PAGE_TITLE}
icon: {GLYPHICON}
title: {PAGE TITLE}
---
```

* **Order** should be an integer specifying the page's position in the navigation bar
* **Parent** should be the title of the parent page to have this new page appear in a dropdown menu (put **top** to have it appear in the top level)
* **Icon** should be the last part of the Bootstrap Glyphicon class name (e.g. _calendar_ or _book_) of the icon to display next to the navigation button
* **Title** should be the page title


#### To add a new year's worth of submissions:

1. Create a new directory for the year in `archive`, then create `index.html` within that directory. Make sure you include the following two lines in the content, adding the appropriate year:
```
{% assign archive_year = "{YYYY}" %}
{% include archive_page.html %}
```

2. Add the submission pages in the same directory with the following format (replacing variables as required):
```
---
layout: submission
title: {SUBMISSION_TITLE}
year: {YYYY}
image: {IMAGE_FILE_NAME}
team: >
    <li>{TEAM_MEMBER}</li>
    {...}
---
<p>{DESCRIPTION</p>
```