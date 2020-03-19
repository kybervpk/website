# KyberVPK site

A quick introduction to the repository:

## Adding a new profile

* Copy a file `content/people/jauhiainen_juho.md` -> `content/people/yourlastname_yourfirstname.md`
* Edit the content if you are not Juho. Delete the line with `weight` variable if you are not an admin.
* Upload your profile image to `static/images/yourname.jpg`


## Project structure
* `public/` is the static web site root and is where the static site is generated to
* `content/` hosts all the page content that gets built into the template
* `themes/kvpk/` is the root for the page theme and visual elements

## Development

### Relevant paths

* Template skeleton: `themes/kvpk/layouts/_default/baseof.html`
* The different template parts (head, header, footer) can be found in `themes/kvpk/layouts/_default/`
* Main page content: `content/_index.md`
* Main page template: `themes/kvpk/layouts/index.html`
* Single profile view template: `themes/kvpk/layouts/people/single.html`
* Profiles: `content/people/`. These are used to generate the list in the main page as well as the source for the single page profile content.
* Ota yhteyttä page content: `content/contact/_index.md`

### Styling

* The current setup automatically processes and includes CSS version of `assets/main.scss` in the base template (see `head.html` for reference)
* There are page/section specific SCSS partials in `./assets/sass/` to prevent the CSS going full bolognese, please stay organised while styling
* All custom styling efforts should be done in either the `main.scss` file, or preferably in a section/page specific partial that you're working on

### Adding a new page to main level (menus etc)

* Create a new directory `content/newpagename`
* Copy existing `_index.md` file to `content/newpagename/_index.md` for reference
* Edit it. 
* If the page should be hidden from the navigation, change `hidden: true`
* Weight variable can be used to determine the order of menu items

### Installation hugo

* Download hugo for your OS from [https://github.com/gohugoio/hugo/releases](https://github.com/gohugoio/hugo/releases)
* Unarchive the package and place hugo binary on your `$PATH`

### Running development server with liveupdate

In project root:
`hugo serve -D`

This starts a development httpd on http://localhost:1313/

The development server does automatic liveupdate and refreshes the page every time you change content or templating.

### Building static pages

In project root:
`hugo`

## LOL apua

Ping @joona / @joohoi
