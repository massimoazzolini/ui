---
layout: page
title: Installation
permalink: /getting-started/installation/
resource: true
categories: Getting Started
---
{% include base.html %}

The WFP UI is intended to be plug & play, and integrate seamlessly with any front-end framework unobtrusively. Whether you use BootStrap, Foundation, Skeleton, or any other framework, you should easily be able to apply WFP UI styles to your projects.

### Using WFP UI
Here are a few different ways to use the WFP UI within your project. Which one you choose depends on the needs of your project and how you are most comfortable working.

Here are a few notes on what to consider when deciding which installation method to use.

Download the WFP UI if:

*  you are not familiar with npm and Bower.

Use the Bower way if:

*  you are familiar with Bower.
*  you would like to leverage WFP UI Sass files.

Use the CDN way if:
*  you just want to use the WFP kit.


### Download

You can view the kit on [github](https://github.com/wfp/ui).

1. Download the WFP UI (version {{site.version}}) at this URL:
[https://github.com/wfp/ui/archive/{{site.version}}.zip](https://github.com/wfp/ui/archive/{{site.version}}.zip)
2. Unpack it and look for the `dist` folder.
3. It has this folder structure:

  ```
  dist
  ├── assets
  │   ├── favicons
  │   ├── fonts
  │   │   ├── aleo
  │   │   └── lato
  │   ├── icons
  │   │   ├── thematic
  │   │   └── ui
  │   └── logos
  │       ├── dark
  │       │   ├── png
  │       │   └── svg
  │       └── light
  │           ├── png
  │           └── svg
  ├── css
  │   ├── bootstrap-theme.css
  │   ├── wfpui+grid.css
  │   └── wfpui.css
  └── js
  ```

4. Add those folders into a relevant place in your code base — likely a directory where you keep third-party libraries

To use the WFP UI on your project, you’ll need to include the CSS and JavaScript files in each HTML page in your project.

Refer to these files by adding the following `<link>` and `<script>` elements into your HTML pages.

Add this to your `<head>` element to include CSS:

{% highlight html %}
<link rel="stylesheet" href="bower_components/wfp-ui/dist/css/wfpui.css">
{% endhighlight %}

or alternatively use this version that provides also the WFP grid system:

{% highlight html %}
<link rel="stylesheet" href="bower_components/wfp-ui/dist/css/wfpui+grid.css">
{% endhighlight %}

Add this before the closing `</body>` tag to include JavaScript:

{% highlight html %}
<script src="bower_components/wfp-ui/js/responsive-nav.js"></script>
<script src="bower_components/wfp-ui/js/subnav.js"></script>
<script src="bower_components/wfp-ui/js/tools.js"></script>
{% endhighlight %}

We offer a minified version. Use it in a production environment or to reduce the file size of your downloaded assets. The examples above recommend using the minified versions.

Now, you should be set to use the WFP UI.

If you need it, you can also download [any particular release](https://github.com/wfp/ui/releases) of WFP UI from GitHub.

### Bower
WFP UI provides a complete set of tool to help you either quickly tap into the library of user interface components and patterns available in this repo, by extending your project via Bower package.

To install the latest release of WFP UI:
{% highlight bash %}
$ bower install wfp-ui --save
{% endhighlight %}

It's also possible to install any particular release of WFP UI:
{% highlight bash %}
$ bower install wfp-ui#0.7.0 --save
{% endhighlight %}

Files are organized into the `bower_components` folder in this way:

```
bower_components
└── wfp-ui
    └── dist
    │   ├── assets
    │   ├── css
    │   └── js
    ├── icons
    ├── js
    └── scss
```

#### SCSS
You can add _WFP UI_ as a dependency to your main SCSS file:

{% highlight sass %}
// Import WFP UI
@import "bower_components/wfp-ui/scss/wfpui";
// Import WFP UI + Grid
@import "bower_components/wfp-ui/scss/wfpui+grid";
{% endhighlight %}

#### Use WFP UI directly
The resources in `dist` are the ones that you may want to directly include in your page.

Add this to your `<head>` element to include CSS:

{% highlight html %}
<link rel="stylesheet" href="bower_components/wfp-ui/dist/css/wfpui.css">
{% endhighlight %}

or alternatively use this version that provides also the WFP grid system:

{% highlight html %}
<link rel="stylesheet" href="bower_components/wfp-ui/dist/css/wfpui+grid.css">
{% endhighlight %}

Add this before the closing `</body>` tag to include JavaScript:

{% highlight html %}
<script src="bower_components/wfp-ui/js/responsive-nav.js"></script>
<script src="bower_components/wfp-ui/js/subnav.js"></script>
<script src="bower_components/wfp-ui/js/tools.js"></script>
{% endhighlight %}



### CDN
Alternatively, you can load _WFP UI_ from our CDN, denoting a version number (i.e.: `v0.8.0`).

Add this to your `<head>` element to include CSS:

{% highlight html %}
<link rel="stylesheet" href="http://cdn.wfp.org/libraries/wfpui/{{ site.version }}/css/wfpui.css">
{% endhighlight %}

or alternatively use this version that provides also the WFP grid system:

{% highlight html %}
<link rel="stylesheet" href="http://cdn.wfp.org/libraries/wfpui/{{ site.version }}/css/wfpui+grid.css">
{% endhighlight %}

Add this to your `<head>` element to include the fonts:
{% highlight html %}
<link rel="stylesheet" href="http://cdn.wfp.org/libraries/webfonts/lato/lato.css">
<link rel="stylesheet" href="http://cdn.wfp.org/libraries/webfonts/aleo/aleo.css">
{% endhighlight %}

All the graphic resources (icons, favicons, logos, ...) are described in [Graphic Resources]({{ base }}/getting-started/graphic-resources)


### Need installation help?

If you have questions or need help with setup, please open an issue here: https://github.com/wfp/ui/issues
