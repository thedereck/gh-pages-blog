---
layout : page
title : Getting Started
subtitle : So you want to learn more about using gh-pages-blog? Well, you've come to the right place.
exclude : true
---

gh-pages-blog was designed to be a simple and quick solution to creating a responsive blog and website using the GitHub Pages functionality available to all GitHub accounts and hosted projects.

### Configuration File ###

Start with forking the [gh-pages-blog](http://www.github.com/thedereck/gh-pages-blog) project, then take a gander at the \_config.yml file. The config file has lots of comments that make an effort at making the configuration easier. But to start with, just focus on the first group of options. You'll definitely need to set these to get your site to work correctly. After making the changes you feel are appropriate for your site, upload it to your GitHub Page and see how it looks. Tweek from there.

If you want to change the Bootstrap theme, you can download some from the Bootswatch website. You may need to play around a bit with the gh-pages-blog.css file though to get things just right. But chances are it will work just fine, or well enough.


### Posts ###

Now, let's talk about posts. You can find the example Hello World post in the \_posts directory. You'll need to put all of your posts there. Posts can be either in HTML (.html) or Markdown (.md). Use whatever you are most comfortable with.

The post file names is also the permalink. The GitHub:Page Jekyll backend will parse the name of the post file to figure out the date for ordering of posts. Most recent posts are shown first.

At the top of the post file is something known as front-matter. Here information about the post is contained in what is known as yml format. For the Hello World post, the front matter looks like:

    ---  
    layout : post  
    title : Hello, world!  
    subtitle : Plus some rambling musings about the origin and current state of gh-pages-blog  
    ---  

Any information between the top and bottom three dashes will be treated as post settings, and will not display in the body of the post. The body of the post will be everything below the bottom three dashes of the front-matter.

The three front-matter settings in our example are:

* layout - Layout tells the Jekyll rendering engine which layout to use when generating the website. Keep it simple here, and just use post as the layout option for now. Layout is a mandatory setting.
* title - Title is the title of the post. Title is a mandatory setting.
* subtitle - Subtitle is the subtitle for the post (surprise!). It'll be rendered just below the title in a smaller font. This is an optional setting. You don't have to inclue a subtitle if you don't want to.

Not represented in the Hello World sample are three other front-matter settings you should be aware of:

* description - The description is a brief description of the post. This will be used in the generation of the rss.xml and will also be used when showing all posts with a specific category or tag. This is completely optional, but probably good form if your title and subtitle don't give enough information about the content of the post.
* category - Every post can have at most one category. The categories to use are completely up to you. When categories are displayed, the first letter in the first word is capitalized. Category is an optional setting.
* tags - Tags are basically the important elements of your post summarized into a few words. If your post includes information about specific people, you might make those people the tags of the post. A post can have more than one tag, but tags are completely optional to use. When tags are dispayed, they are displayed in all lowercase.
* author - The optional author tag is used when the author of the post is different than the author of the site. Only one author tag can be included on each post. In the absense of the author tag, then the site author will be used. The post author is displayed on the post, and is also included in the html header meta data of the site.
* author\_email - The optional author\_email tag is used when the author of the post is different than the author of the site. Only one author\_email tag can be included on each post. In the absense of the author\_email tag, the site author email will be used. The author\_email is not displayed on the post page, but is part of the html header meta data.

Just for fun, let's expand the front-matter of the Hello, World example to show all the available elements mentioned here.

    ---  
    layout : post  
    title : Hello, world!  
    subtitle : Plus some rambling musings about the origin and current state of gh-pages-blog  
    description : An introductory message about gh-pages-blog.  
    category : Status Update  
    tags :  
      - Bootstrap  
      - Jekyll  
    ---  

Assuming your \_config.yml file has either the categories or tags navlist or navbar dropdown enabled, the first post that has either a category or tag should cause the either the navlist or the dropdown list to appear. If no posts contain categories or tags, then the navlist and dropdownlist won't be rendered to save some screen real estate.


### Pages ###

You can also add pages to your gh-pages-blog site. Simply create a new file in the gh-pages-blog parent directory with either an HTML (.html) or Markdown (.md) extension.

Created pages are listed on the right side in the navbar at the at the top of the site.

The page you create will also need some front-matter. Here's a good example:

    ---  
    layout : page  
    title : Getting Started  
    subtitle : So you want to learn more about using gh-pages-blog? Well, you've come to the right place.  
    exclude : true  
    ---  

Let's break down the front-matter for the page, but it's very similar to the front-matter for a post described above.

* layout - Layout tells Jekyll which layout to use. For now, just always use page when creating a new page. This is a mandatory setting.
* title - Title is the title for the page. This is an optional setting, but if it is not included, then the site description from the \_config.yml file will be used for the page title.
* subtitle - Subtitle is the optional subtitle for the page. If the subtitle is not defined, there is no default. It just won't be displayed.
* exclude - Exclude is the optional identifier to tell gh-pages-blog to exclude the page from the list of pages displayed in the navbar. If the exclude setting is missing, gh-pages-blog will display the page in the navbar list.
* order - This is a value between 0 and 100. The lower the value, the further left the page will be on the navbar list of pages. This too is an optional setting. But if the order is not included in the front-matter, then page will appear to the right of the ordered pages. Not setting order is the same as saying order of 101. Pages with the same order value will most likely be ordered in a way that appears quite random to the viewer of the website.
* author - The optional author tag is used when the author of the page is different than the author of the site. Only one author tag can be included on each page. In the absense of the author tag, then the site author will be used. The author is not displayed on each page, but is included the html header meta data.
* author\_email - The optional author\_email tag is used when the author of the page is different than the author of the site. Only one author\_email tag can be included on each page. In the absense of the author\_email tag, the site author email will be used. The author\_email is not actually displayed on each page, but is included i the html header meta data.

Like posts, the body of the page is contained after the three bottom dashes in the front-matter.


### Conclusion ###

Well that's it in a nutshell. If you run into a bug or have a request for a new feature, please submit an [issue](https://github.com/thedereck/gh-pages-blog/issues).

Happy blogging.

Dereck