---
layout : post
title : Hello, world!
subtitle : Plus some rambling musings about the origin and current state of gh-pages-blog
category : Version 0.1
tags :
  - initial release
---

Hello, World!

Back at the end of February I decided it was time to start blogging again. In the past I have used [Posterous](http://www.posterous.com) as my blogging platform of choice and I really liked it. Unfortunately, Posterous is closing up shop and shutting the doors at the end of [April](http://blog.posterous.com/thanks-from-posterous).

Bummer. But thank you Posterous for making such a great blogging solution in the first place!

So I looked around and the other free blogging options didn't really appeal to me. And I really wasn't looking for a pay blog, as my blogging volume would most likely be low.

Then I thought, hey [GitHub](http://www.github.com) has [Pages](http://pages.github.com/) for their users and maybe I should just create a blog and manually code all the blog posts as static html pages using a template. So I started down that road.

Luckily, I learned that [Jekyll](https://github.com/mojombo/jekyll) was powering GitHub Pages, and Jekyll was designed to create static blogs.

Jackpot!

I googled for a project that would incorporate a GitHub Pages blog with Bootstrap, because I wanted a responsive website that would work on mobile phones, tablets, and desktop browsers. There were a few projects, but not really all that many. And the ones I found either weren't complete, or they weren't being actively developed.

Ok, no problem. I'll just go ahead and incorporate Bootstrap into my pages. Which was really easy to do. The added bonus is that I'm not really a frontend developer. I did most of my best programming work on the backend. So Bootstrap really fit the bill. (If you want to complain about Bootstrap sites all looking the same, you can get off your soapbox right now and go preach your gospel of hate somewhere else. Or better yet, put in a pull request with better looking boostrap CSS attached.)

I went and added Font Awesome because I liked the look of the fonts, and they scale well.

After Bootstrap and Font Awesome were incorporated, I thought what else could I use to make Jekyll more like a traditional dynamic blogging solution. So other sections began to come about, sections like a brief biography, plus a navlist of blog post archives, and also navlists of blog tags and categories. And since this was to be GitHub hosted, a list of GitHub projects the user to could profile made sense as well.

Somewhere along the line I decided to make this it's own GitHub project that others could use. So I made it so that all the navlists could also be navbar drop menus. And they're all configurable, so they don't have to be displayed at all.

Static pages were also added early on in my coding, and then I started focusing on other things. Finally, I came back around to the static pages again and added an ordering option so that they show up in a specific order in the navbar. The pages configuration needs more options where they can also be a dropdown menu or a navlist.

And although the blogging solution available from Jekyll isn't dynamic, I added some dynamic options in the form of javascript so that when you click on a category or tag in a blog post a page will display all matching values. The javascript I wrote is quite ugly and needs to be cleaned up. But it's functional.

Also, lots of the display elements could use some better CSS instead of things like break tags to provide vertical separation. Again, it's functional, and I'll get these things cleaned up in time.

But right now, I'd like to announce a version 0.1.0 of the [gh-pages-blog](http://www.github.com/thedereck/gh-pages-blog/) software. There's still plenty of work to be done and documentation to be produced, but it's very functional as is and that'll be good enough for now.

Enjoy the blogging.

Dereck
