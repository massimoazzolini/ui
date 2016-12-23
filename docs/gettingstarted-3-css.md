---
layout: page
title: CSS Architecture
permalink: /getting-started/css/
resource: true
categories: Getting Started
---
{% include base.html %}

This page describes how to use CSS and how to adapt it to your needs. We would also give you some tips to have a better experience.

The CSS foundation of the WFP UI is built with the [Sass](https://sass-lang.com/) preprocessor language.


### Using the CSS

If you just need to use the kit and not to customize WFP UI, you can directly include the CSS stylesheets adding the references into your `<head>` element. In the installation page, see [Download]({{ base }}/getting-started/installation#download), [Bower]({{ base }}/getting-started/installation#bower)  or [CDN]({{ base }}/getting-started/installation#cdn) section to get more info.

**TIPS**

If you downloaded the files, we recommend you copy dist/css/wfpui.css into your own css directory, if you plan on simply linking it from HTML.

### CSS organization and naming conventions

The WFP approach to class naming is the following:
``` .wfp-[component]--[variant]```

For example:
```.wfp-table--striped```

**TIPS**

 * Use modular CSS for scalable, modular, and flexible code.
 * Use nesting when appropriate. Nest minimally with up to two levels of nesting.
 * Media queries are built mobile first.
 * Spacing units are as much as possible defined as rem or em units so they scale appropriately with text size. Pixels can be used for detail work and should not exceed 5px (For example: 3px borders).



### Using the SASS files

First of all you need to get the Sass source code. Download the package following the instructions in the [Bower]({{ base }}/getting-started/installation#bower) section.


You can add _WFP UI_ as a dependency to your main SCSS file:

{% highlight sass %}
// Import WFP UI
@import "bower_components/wfp-ui/scss/wfpui";
// Import WFP UI + Grid
@import "bower_components/wfp-ui/scss/wfpui+grid";
{% endhighlight %}


Global SCSS variables are defined in `bower_components/wfp-ui/scss/_init.scss`.

**TIPS**

 * Pay attention to not customize too much the Sass files, the risk is to no follow the branding guidelines
 * It's best to compile wfp-ui directly to your SASS main file, in order to benefit from **a smaller overall file size**, and **having a single CSS file** to load and render by the web browser. This is because CSS is considered as a render [blocking resource](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css).
