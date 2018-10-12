# Cloud4est - _Community_
- [Instructions](#modifying-the-site) on modifying the site

- [Development guide](#developing-the-site) of the site

- _This site is based on the following theme, its README is attached below:_
> __Landed by HTML5 UP__  
html5up.net | @ajlkn  
Free for personal and commercial use under the CCA 3.0 license (html5up.net/license)  
> A dark, slick, modern, responsive, adjective-drenched design built around an extremely
dynamic landing page (scroll that mofo!). Inspired by Big Picture, another design
of mine with a similarish feel/flow, only this time I took it waaaaaay further and
actually made it multipurpose (versus copping out and making it a one pager like I
did last time ;) Includes multiple pages, a bunch of pre-styled elements, and all
its Sass sources.  
> Demo images* courtesy of Unsplash, a radtastic collection of CC0 (public domain) images
you can use for pretty much whatever.  
> (* = Not included)  
> Feedback, bug reports, and comments are not only welcome, but strongly encouraged :)  
> AJ
aj@lkn.io | @ajlkn  
> Credits:  
> - Demo Images:
	 * Unsplash (unsplash.com)  
> - Icons:
	 * Font Awesome (fontawesome.io)  
> - Other:  
	 * jQuery (jquery.com)
	 * Scrollex (github.com/ajlkn/jquery.scrollex)
	 * Responsive Tools (github.com/ajlkn/responsive-tools)


## __Modifying the site:__

### _Pages_

#### Adding a new page:

You can add a new page by creating a markdown (.md) file in the `_pages` directory. The following metadata should be provided in the front-matter section of the file:  
_(Ticked ones are necessary for proper functioning)_

- [x] `title`: appears in the navbar and on the actual page
- [x] `permalink`:
  - "`/page-permalink/`"
- [x] `ref`: short name used as id
- [x] `lang`: language of current page
  - "`hu`"
  - "`en`"
- [x] `layout`:
  - `default` most of the times
  - (or `home`) used for index page, with sliding sections
- [x] `style`: CSS class of the page
  - `wrapper style1` for pages
- [x] `location`: page link directly on navbar or submenu
	- `navbar`
	- `menu`
- [ ] `description`: appears under the title
- [ ] `order`: numbers starting from 1
- [ ] `sidebar`: location of sidebar
  - `left`
  - `right`
- [ ] `image`: Image shown at the top of page content
  - "`/directory/img.ext`"
- [ ] `icons`: source of posts shown on page
  - `authors`
  - `topics`

Then just write the remaining part of the content following the markdown syntax.

### _Posts_

#### Adding a new post:

Posts are recurring sections on a page, like the sections on the main page, or the author icons on the "authors" subpage. If you add a new post, a new section with the same look as the former ones will show up, but with the values that you have given.  
You can add a new post by creating a (.md) file in the `_posts` directory. The filename should be the following: `YYYY-MM-DD-your-title.md` (date + title). Depending on the type of post you are adding, you should create it in either the `authors`, `sections` or `sidebars` folder.  The following metadata should be provided in the front-matter section of the file:  
_(Ticked ones are necessary for proper functioning)_

- [x] `title`
- [x] `ref`
- [x] `lang`
- [x] `type`: show posts from with given property
	- "`home`" on __homepage__
	- "`author`"
	- "`topic`"
	- "`sidebar`" in sidebars
- [ ] `style`: CSS class of the post (__only__ necessary for __posts__ on the __homepage__)
	- spotlight style1 bottom
	- spotlight style2 right
	- spotlight style3 left
	- _(wrapper style1 special fade-up)_ __removed__ from homepage
	- _(wrapper style2 special fade)_ __removed__ from homepage
- [ ] `description`: appears under the title
- [ ] `order`: numbers starting from 1
- [ ] `image`: image shown as background on __homepage sections__
  - "`/directory/img.ext`"
- [ ] `location`: location of the posts
 - `home` show on __homepage__
 - `{{ page.title }}` the exact title of the page where the __sidebar__ should be
- [ ] `icon`: icons from Font-Awesome in __subpage sections__
  - "`fa-icon-name`"
- [ ] `middle`: if there's a middle text part (like the 1st homepage section)

---

## __Developing the site__

### _Includes_

#### Main includes:

The generally included HTML files are located in the root of the `_includes` folder.

#### Specific includes:

Page and post specific includes are in the folders `pages` and `sections` of the `_includes` folder respectively.

### _Generation process_

A layout is given in the `index.md` file, currently `home`. This layout is found in the `_layouts` folder, `home.html`. This is almost the same as the default (`default.html)` the only difference is the __inclusion__ of `homepage_sections.html` in `home.html`. If you go through the content of the default layout, and its inclusions in order, you can get a picture of how the whole site is constructed.

###  _Data_

Images are currently leftovers from the landed theme, we have yet to replace them. Their location is `/images/` and `/assets/css/images/`. New images are uploaded to the `_uploads` folder. Some images are given in the `_config.yml` file, like the main picture `pic` and `banner`. Predefined strings, - which are also leftovers from the process of transforming the theme to a jekyll site -, are located in `/_data/strings.yml`. In the end we won't need that, as it was only created for the demonstration of the multilingual capability.  
