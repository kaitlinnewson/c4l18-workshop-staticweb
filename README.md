## Code4Lib 2018 Workshop: Getting Started with Static Website Generators

Slides and other materials for the "Getting Started with Static Website Generators" preconference workshop at code4lib 2018. [See the conference page for more details](http://2018.code4lib.org/workshops/getting-started-with-static-website-generators).

The 'docs' directory hosts the built Hugo website from the 'exampleSite' directory. The site is available at [https://kaitlinnewson.github.io/c4l18-workshop-staticweb/](https://kaitlinnewson.github.io/c4l18-workshop-staticweb/).

### Hugo Exercises

* 7 exercises in 45 minutes, about 5 minutes per exercise but it's really go at your own pace
* Instead of going through together a se of instructions of things you can do with Hugo, we're going to take a less traditional format of independent learning, the same way that you might have to figure out a new technology on your own time, but benefitting from other people around to help you
* We'll provide minimal written/verbal instruction. We encourage you to read the Hugo documentation and google/duckduckgo for help!
* If you have questions, ask your neighbour. [Coding learning is social](https://andromedayelton.com/2013/11/25/reflecting-on-introduction-to-python-for-librarians/). If there's still any remaining questions, put up a stickie and one of us will come and help out
* We're going to take up the exercises after 10, 20, and 45 minutes.
* When we take up the exercises, We're going to ask you:
   * Show us how you worked through the problem. What resources did you consult?
   * Provide everyone with a line by line walkthrough of the answer
   * What problems did you run into along the way? Talk about the tiny mistakes you might have made along the way, things like syntax errors, formatting issues, and so on.

#### Exercise 1

Basic Usage - Creating Content 

* Add a new Portfolio page
* Your new Portfolio should have an image on the homepage
* The Portfolio page should be called Dog 7
* Create the page as a draft
* View the page as a draft
* Then, publish it and view it again

#### Exercise 2

Archetypes

* Create and edit the Archetype for Portfolio. Archetypes are files located in the archetypes directory of your project. These files correspond to your website’s content types. It is here that you would put in the front matter variables for your content types. Archetypes facilitate consistent metadata across your website content and allow content authors to quickly generate instances of a content type via the hugo new command.
* If you want to keep working with Archetypes, add another Archetype for Testimonials, create a new Testimonial and view the page.

10 minute mark: Take up 1, 2

#### Exercise 3

List Page Templates

* Create a list page for your Portfolio pages if you were to go to http://localhost:1313/c4l18-test-exercises/portfolio/.
* This page should provide a link to every Portfolio page
* Anytime a new Portfolio page is created it will appear there.
* Create an index page (_index.md) for your Portfolio content type which will appear in your Portfolio list page.

#### Exercise 4

List Page Templates - Summary Page

* Create summaries for your lists instead

20 minute mark: Take up 3, 4

#### Exercise 5

Shortcodes

Shortcodes are simple snippets inside your content files calling built-in or custom templates. You can use them to embed media and other external popular types of content. They're designed to be simple and reusable, without having to repeatedly put in messy html into your markdown files. 

Embed one of the following sources into a new Portfolio page using shortcodes:

* https://www.instagram.com/p/Vo0b44KZhx/
* https://gist.github.com/kimpham54/81f82f576908f245b486a9311f088257
* https://vimeo.com/60188025

#### Exercise 6

Custom CSS

Play around with the styling of the site. Try and do the following:

1. Change the theme's style option from 'sea' to 'pink'
2. Change the "Good Dogs" title in the sidebar to 36px and a different colour
3. Add a box shadow to each dog portfolio image

#### Exercise 7

Custom CSS - overriding existing fonts with web fonts 

Grab a couple of fonts from [Google Fonts](https://fonts.google.com/) and use them to override the fonts on your website. You'll want to edit just the title and body of each dog portfolio post.

#### Exercise 7

Image Metadata
Page Resource
Contact email integration
Create a new page where you get all image resources

45 minute mark: Take up 5, 6, 7

-----------------------------

### Tips

#### Exercise 1

* Find a new image and put it in static/img/dogs/
* You can just create a new .md file and copy over the front matter but you could also use the hugo CLI, hugo new portfolio/work7.md. Note that the metadata is not the same. That's because you haven't specified the archetype.
* Check out https://gohugo.io/commands/hugo_server/ or hugo help

#### Exercise 2

* https://gohugo.io/content-management/archetypes/

For new Archetypes:

* https://gohugo.io/content-management/organization/

While Hugo supports content nested at any level, the top levels (i.e. content/<DIRECTORIES>) are special in Hugo and are considered the content type used to determine layouts etc. To read more about sections, including how to nest them, see sections.

#### Exercise 3

* https://gohugo.io/templates/base/
* https://gohugo.io/templates/lists/
* https://gohugo.io/content-management/organization/

#### Exercise 4

* https://gohugo.io/content-management/shortcodes/

#### Exercise 5

* If you look at the theme README (https://github.com/kishaningithub/hugo-creative-portfolio-theme), this theme provides a style option and the ability to customize your css using a custom.css file. 
* Read https://gohugo.io/themes/customizing/.  Under static/css there is a custom.css file that you can use to override css template files.

#### Exercise 6

Read https://gohugo.io/templates/partials/. You can create a layout/partials folder and create a head.html file to override the themes/hugo-creative-portfolio-theme/layouts/partials/head.html.

In Google Fonts, grab the link href they provide after you select the fonts you want to use.

Other readings:

* https://gohugo.io/templates/base/
* https://gohugo.io/themes/customizing/

#### Exercise 7


ask kaitlin
tables in reveal js
how to create good html in reveal. i used markdown to html, not great
auto prettify after messing around?