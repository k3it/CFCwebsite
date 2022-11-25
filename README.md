Clearview Flying Club Website
=========================

# Install Jekyll

```
gem install bundler jekyll image_optimizer
```

# Run the website

```
bundle exec jekyll serve
```

Visit the site: http://localhost:4000

# Making changes

## Optimize images

There's a built in image optimizer for creating the smallest image sizes possible

_note, you may need to install additional libraries for png and jpeg on your computer_

```
ruby opimize_imgs.rb
```

## Directory Structure

### img

All images should be contained here.

### docs

This directory contains club documents like bylaws, POH's, etc

### newsletters

This directory contains the past newsletters

### \_includes

This directory contains partials to be included in other pages. Jekyll compiles parts of pages in this directory into other static html

### \_layouts

This directory contains all the layouts for various page types. Jekyll uses these layouts to compile down the final pages. A change here will affect all pages that use that layout.


## Special Handling

### cfis.html

The cfis.html page has special handling in the header:

```yaml
cfis: 
  - Tom Henry CFI
  - Brian Corcoran CFI
  - Naomi Schayek CFII
```

The page uses this list to compile the final page. Each row must have the name, certificate type, and email of the CFI in comma delimited format for the compiler to properly handle expansion into the HTML.

### aircraft pages

The aircraft pages use the 'aircraft' layout provided in the \_layouts directory. This layout requires the following items to be set in the head of the page to compile properly:

```yamnl
---
tail: N700ZG
model: 2004 Cirrus SR20 G2
price: $185/hour hobbs*
---
```
Changing these items changes the values on the final page.
