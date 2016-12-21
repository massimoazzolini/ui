---
layout: page
title: CSS Architecture
permalink: /getting-started/css/
resource: true
categories: Getting Started
---
{% include base.html %}

Aggiungere desc introduttiva
The CSS foundation of this site is built with the Sass [https://sass-lang.com/] preprocessor language.
Using the SASS files (variables, include, ...) (anchor)
Per avere i sorgenti sass devi installare il pacchetto tramite bower (link alla sezione Bower)
Add WFP UI as a dependency to your main SCSS file:
@import "bower_components/wfp-ui/scss/wfpui";
// Import WFP UI + Grid
@import "bower_components/wfp-ui/scss/wfpui+grid";

Global scss variables are defined in bower_components/wfp-ui/scss/_init.scss
Se vuoi customizzare alcune di queste variabili (è consigliabile limitare al minimo gli interventi per non rischiare di allontanarsi dalle branding guidelines) puoi:
copiare questo file nel tuo project’s Sass folder
changing applicable variables values
importing it before the wfpui.scss

TIPS
It's best to compile wfp-ui directly to your SASS main file, in order to benefit from a smaller overall file size, and having a single CSS file to load and render by the web browser. This is because CSS is considered as a render blocking resource.

Using the CSS (anchor)
Se non si ha bisogno di includere il sass e personalizzare le variabili si può anche..
You can also reference a preprocessed WFP UI css directly in your markup, adding link to your <head> element. See Download [link] or CDN [link] section to get more info.
TIPS
Se hai scaricato i files, we recommend you copy dist/css/wfpui.css into your own css directory, if you plan on simply linking it from HTML.

CSS organization and naming conventions (anchor)
Nota: non è indicata da nessuna parte qual è la naming convention di WFP (uso dei prefissi, struttura dei nomi con - o - -, organizzazione dei files…). Il rischio è inventarsi cose che non seguono i loro ragionamenti. La lascerei minimale o vuota...
The WFP approach to class naming is the following:
.wfp-[component]--[variant]
For example: .wfp-table--striped

TIPS
Uses modular CSS for scalable, modular, and flexible code.
Uses nesting when appropriate. Nest minimally with up to two levels of nesting.
Hard-coded magic numbers are avoided and, if necessary, defined in the core/variables scss file.
Media queries are built mobile first.
Spacing units are as much as possible defined as rem or em units so they scale appropriately with text size. Pixels can be used for detail work and should not exceed 5px (For example: 3px borders).
