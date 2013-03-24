skrollr-pages
=============

Adds a concept of "pages" to [skrollr](https://github.com/Prinzhorn/skrollr). Pages are sub-intervals of the page you are scrolling which are endowed with special page-like behaviour, including "scrollspy" and local navigation. This is a bit tedious to do direclty with skrollr. Specifically:

- Pages should be dom elements with a (default is "page"). The pags should have a unique ID if you want in-page navigation to work.
- Local navigation will be updated to reflect which "page" you scroll to.
- Pagination elements will automatically be wired up to scroll through pages if you create them. Default classes for these are "scroll-page-down", "scroll-page-up", "scroll-page-top", "scroll-page-bottom".

## Example:
My company, [Countable](http://countable.ca) uses this skrollr add-on.

## Usage:

```
<!-- currently requires jQuery. -->
<script src="jquery-1.9.1.min.js"></script>
<script src="skrollr.min.js"></script>
<script src="skrollr-pages.js"></script>

<script>
  $(function(){
    skrollr_instance = skrollrPages()
  });
</script>

<ul>
  <li><a href="#page1">page 1</li>
  <li><a href="#page2">page 2</li>
</ul>

<div class="page" id="page1">
   first page content.
</div>
<div class="page" id="page2">
   2nd page content.
</div>

<style>
  .page {height: 1000px;}
  .active {color: red;}
</style>
```

