# Cloud4est - _Community_
- [Instructions](#modifying-the-site) on modifying the site
  - [Authors](#authors)
  - [Topics](#topics)
  - [Posts](#posts)
  - [Pages](#pages)
- [Development guide](#developing-the-site) of the site
  - [Includes](#includes)
  - [Generation process](#generation-process)
  - [Data](#data)
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
Credits:  
  - Demo Images:
  	 - Unsplash (unsplash.com)  
  - Icons:
  	 - Font Awesome (fontawesome.io)  
  - Other:  
  	 - jQuery (jquery.com)  
  	 - Scrollex (github.com/ajlkn/jquery.scrollex)  
  	 - Responsive Tools (github.com/ajlkn/responsive-tools)


## __Modifying the site:__

### _Authors_

#### Adding a new author:

You can add a new author by creating a (.md) file in the `_authors` directory. The following metadata should be provided in the front-matter section of the file:
*__Ticked__ ones are __necessary__ for functioning, but the __others__ are also __required__ to ensure proper and unified content*

- [x] `title`: appears in the navbar and on the actual page
- [ ] `date`:
- [x] `lang`: language of current page
- `hu`
- `en`
- [ ] `image`: picture to show
- [x] `description`: appears under the title

### _Topics_

#### Adding a new topic:

You can add a new topic by creating a (.md) file in the `_topics` directory. The following metadata should be provided in the front-matter section of the file:
*__Ticked__ ones are __necessary__ for functioning, but the __others__ are also __required__ to ensure proper and unified content*

- [x] `title`: appears in the navbar and on the actual page
- [ ] `date`:
- [x] `lang`: language of current page
- `hu`
- `en`
- [ ] `image`: picture to show
- [x] `description`: appears under the title

### _Posts_

#### Adding a new post:

Posts are recurring sections on a page, like the sections on the main page, or the author icons on the "authors" subpage. If you add a new post, a new section with the same look as the former ones will show up, but with the values that you have given.  
You can add a new post by creating a (.md) file in the `_posts` directory. The filename should be the following: `YYYY-MM-DD-your-title.md` (date + title). The following metadata should be provided in the front-matter section of the file:  
*__Ticked__ ones are __necessary__ for functioning, but the __others__ are also __required__ to ensure proper and unified content*

- [x] `title`
- [ ] `date`: else provided from the filename
- [x] `lang`:
  - en
  - hu
- [x] `style`: CSS class of the post (_direction from which it slides in_)
  - bottom
  - right
  - left
- [ ] `image`: image shown as background
  - `/directory/img.ext`
- [ ] `description`: appears under the title
- [ ] `is-featured`: show post on main page
- [ ] `author`
- [ ] `topic`

### _Pages_

#### Adding a new page:

You can add a new page by creating a markdown (.md) file in the `_pages` directory. The following metadata should be provided in the front-matter section of the file:  
*__Ticked__ ones are __necessary__ for functioning, but the __others__ are also __required__ to ensure proper and unified content*

- [x] `title`: appears in the navbar and on the actual page
- [x] `lang`: language of current page
- `hu`
- `en`
- [x] `description`: appears under the title
- [ ] `permalink`: path of the subpage
- [ ] `location`: if you'd like your page to appear in the navbar
- `navbar`
- [ ] `icons`: source of posts shown on page
- `authors`
- `topics`

---

## __Developing the site__

### _Includes_

#### Main includes:

The generally included HTML files are located in `_includes/general/`.

#### Specific includes:

Page and section specific includes are in the folders `pages` and `sections` of the `_includes` folder respectively. By sections here I mean recurring parts of the site, such as the icon layout on the authors page or the sliding posts.

### _Generation process_

There are only 2 layouts used in this concept. One is `flowing` and the other is `default`. The `flowing` one is used when the page consists of posts filtered by specific metadata (e.g. author or topic). The default is basically used with all the other pages, like the subpage for showing available topics or authors. If you go through the content of the layouts and see what files are included in order, you can get a picture of how the whole site is constructed.

###  _Data_

Images are uploaded to the `_uploads` folder. Some image paths are given in the `_config.yml` file, like the main picture `pic` and `banner`. Predefined strings, - which are also leftovers from the process of transforming the theme to a jekyll site -, are located in `/_data/strings.yml`. In the end we won't need that, as it was only created for the demonstration of the multilingual capability.  
