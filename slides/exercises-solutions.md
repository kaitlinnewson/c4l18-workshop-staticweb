# Solutions

#### Exercise 1

* Find a new image and put it in static/img/dogs/
* You can just create a new .md file but you could also use the hugo CLI, hugo new portfolio/work7.md
* Edit the front matter, image = "img/portfolio/dogs/dog7.jpg"

```
---
title: "Dog 7"
date: 2018-02-12T00:27:38-05:00
draft: false
image: "img/portfolio/dogs/dog7.jpg"
---

It's Dog Time!

## Doggy Daycare

Doggo very good spot floofs sub woofer you are doing me a frighten stop it fren very taste wow, big ol pupper heckin long water shoob long bois much ruin diet.

> Doggorino the neighborhood pupper snoot very taste wow, porgo doge, heckin angery woofer long doggo. Heckin extremely cuuuuuute you are doin me a concern he made many woofs long doggo, yapper shoober sub woofer. Extremely cuuuuuute thicc super chub fat boi pats, very taste wow borking doggo.
```

* hugo server --buildDrafts or hugo server -D. Find out by running hugo help.
* hugo server

#### Exercise 2

archetypes/portfolio.md

```
+++
draft = true
image = ""
date = {{ .Date }}
title = ""
showonlyimage = false
weight = 5
+++
```

``` hugo new portfolio/work8.md```

check out work8.md

```
+++
draft = true
image = ""
date = 2018-02-12T01:11:54-05:00
title = ""
showonlyimage = false
weight = 5
+++
```

#### Exercise 3

Add portfolio/_index.md

Taken from themes/hugo-creative-portfolio-theme/layouts/_default/single.html and transplanted into 

layouts/portfolio/list.html

```
{{ define "main" }}
<div class="col-xs-12 col-sm-8 col-md-9 content-column white-background">
  {{ partial "mobile_nav_toggle.html" . }}
  <div class="row">
    <div class="col-lg-8">
      <div class="content-column-content">
         <h1>{{ .Title }}</h1>
         {{ .Content }}
         {{ template "_internal/disqus.html" . }}

         <ul>
    <!-- Ranges through content/post/*.md -->
    {{ range .Data.Pages }}
        <li>
            <a href="{{.Permalink}}">{{.Date.Format "2006-01-02"}} | {{.Title}}</a>
        </li>
    {{ end }}
    </ul>
      </div>
    </div>
  </div>
</div>
{{ end }}
```

### Exercise 4


layouts/portfolio/summary.html

```
<article class="post">
  <header>
    <h2><a href='{{ .Permalink }}'> {{ .Title }}</a> </h2>
    <div class="post-meta">{{ .Date.Format "Mon, Jan 2, 2006" }} - {{ .FuzzyWordCount }} Words </div>
  </header>
  {{ .Summary }}
  <footer>
  <a href='{{ .Permalink }}'><nobr>Read more →</nobr></a>
  </footer>
</article>
```

layouts/portfolio/list.html

```
{{ define "main" }}
<div class="col-xs-12 col-sm-8 col-md-9 content-column white-background">
  {{ partial "mobile_nav_toggle.html" . }}
  <div class="row">
    <div class="col-lg-8">
      <div class="content-column-content">
         <h1>{{ .Title }}</h1>
         {{ .Content }}
         {{ template "_internal/disqus.html" . }}

         <ul>
    <!-- Ranges through content/post/*.md -->
    {{ range .Data.Pages }}
        <!-- <li>
            <a href="{{.Permalink}}">{{.Date.Format "2006-01-02"}} | {{.Title}}</a>
        </li> -->
    <!-- For summary view, enable .Render summary and disable the range method-->
            <p>{{ .Render "summary"}}</p>
    {{ end }}
    </ul>
      </div>
    </div>
  </div>
</div>
{{ end }}
```


#### Exercise 5

```
---
title: "Dog 7"
date: 2018-02-12T00:27:38-05:00
draft: false
image: "img/portfolio/dogs/dog7.jpg"
---

It's Dog Time!

### INSTAGRAM

{{< instagram Vo0b44KZhx >}}


### GIST SAMPLE

{{< gist kimpham54 81f82f576908f245b486a9311f088257 "maps.json" >}}


### VIMEO SAMPLE

{{< vimeo 60188025 >}}

## Doggy Daycare

Doggo very good spot floofs sub woofer you are doing me a frighten stop it fren very taste wow, big ol pupper heckin long water shoob long bois much ruin diet.

> Doggorino the neighborhood pupper snoot very taste wow, porgo doge, heckin angery woofer long doggo. Heckin extremely cuuuuuute you are doin me a concern he made many woofs long doggo, yapper shoober sub woofer. Extremely cuuuuuute thicc super chub fat boi pats, very taste wow borking doggo.
```

#### Exercise 6

Used Developer mode to figure out the tags for the title.

static/css/custom.css

```css
.sidebar-heading a {
	font-size: 36px;
	color: #285d47;
}

.box-masonry .box-masonry-image {
	box-shadow: 0 0 18px 5px black;
}
```

#### Exercise 7

```sh
$ mkdir layouts/partials
$ touch head.html
```

layouts/partials.head.html

1. copy from themes/hugo-creative-portfolio-theme/layouts/partials/head.html

2. next add

```html
<!-- Dog site custom fonts -->
<link href="https://fonts.googleapis.com/css?family=BioRhyme+Expanded|Playfair+Display" rel="stylesheet">
```

static/css/custom.css

```css
.box-masonry h4 a {
	font-family: 'BioRhyme Expanded', serif;
}

.box-masonry p  {
	font-family: 'Playfair Display', sans-serif;
}
```

Other things that were looked at:

* https://discourse.gohugo.io/t/make-font-awesome-icons-locally-available/3903
* https://discourse.gohugo.io/t/how-to-dynamically-use-google-fonts-in-a-hugo-website-config-toml/4423
* https://discourse.gohugo.io/t/cherry-pick-from-fonts-googleapis-com-in-config-toml/10327