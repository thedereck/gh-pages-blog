---
layout : page
title : Syntax Highlighting
subtitle : You write code. You want to show it off. You want it to look good. Syntax highlighting is here to help.
exclude : true
---

With version 0.3.0 of gh-pages-blog, syntax highlighting is now supported.

### Configuration File ###

Let's starting with the new entries in the \_config.yml configuration file that were added for syntax highlighting.

    syntax-highlighting:
      enabled : true
      css: syntax.css

The enabled entry will determine if the css file is loaded or not. The css entry determines which css file is loaded. The css file needs contain the stylesheet entries needed by the Jekyll to rend the content between the {% raw %}{% highlight text %}{% endraw %} and {% raw %}{% endhightlight %}{% endraw %} tags. Finally, the css file will need to be saved in the css directory.

### Posts and Pages ###

Now, let's talk about adding syntax highlighting to source code contained in posts and pages.

In order to get the soure code to render correctly on your blog post and pages, you'll need to wrap the code in the highlight tags supported by [Jekyll](http://jekyllrb.com).

<pre>{% raw %}{% highlight text %}
code goes here
{% endhighlight %}{% endraw %}</pre>


It's very important to include `text` in the tag, otherwise the GitHub page won't build. Jekyll will render the line breaks and spacing correctly between the highlight tags, so it shouldn't be necessary to do any other formatting. It's not necessary to wrap your code in `<pre><code></code></pre>` when using the highlight tag.

Adding the highlight tags around some sample code would result in the following output:

{% highlight text %}
function code_example() {
  console.log("Showing the plain text rendering of code using gh-pages-blog.");
}
{% endhighlight %}


In order to turn on syntax highlighting for a particular language, you'll also need to include the language in the highlight markup tag by replacing the word `text` with the proper language (for javascript, `{% raw %}{% highlight javascript %}{% endraw %}`).

{% highlight javascript %}
function code_example_with_javascript_syntax_highlights() {
  console.log("Showing the syntax highlighting rendering of code using gh-pages-blog.");
}
{% endhighlight %}


For a complete list of languages with syntax highlight, please see the [lexers](http://pygments.org/docs/lexers/) documentation of the [Pygments](http://pygments.org/) project. Pygments is used by Jekyll, and Jekyll is used by the GitHub:Pages. The rabbit hole can go deeper, but I don't think it's necessary to go there at this time.

If you want to include line numbers in your source code listings, you just need to add `linenos=table` to the `{% raw %}{% highlight javascript linenos=table %}{% endraw %}` tag.

{% highlight javascript linenos=table %}
function code_example_with_line_numbers() {
  console.log("Showing the line number rendering of code using gh-pages-blog.");
}
{% endhighlight %}


You can use `linenos` without the `=table`, but the code output puts the line numbers inline with the text, making it very difficult to copy and share.

### Conclusion ###

That should cover the basic usage of syntax highlight. If you need more indepth undestanding, you'll need to refer to the Jekyll and Pygments documentation.

One final thing. Thanks to [Tom Preston-Werner](https://github.com/mojombo/jekyll) for making the default syntax.css file used by gh-pages-blog available under the MIT License.

Happy blogging.

Dereck
