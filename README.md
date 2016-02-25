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

To add a new year's worth of submissions:

1. Copy the previous year's index.html and update the title and data file name.
2. Add a new data file in `_data`, following the format of the previous years' file.
3. Add the submission pages.