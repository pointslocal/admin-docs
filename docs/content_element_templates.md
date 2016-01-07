# Components / Element Templates

> Element templates represent individual display components for the front end of your site.  From event listings to box scores to stories, the element templates section enables modular design of your pages and works in congress with the stream designer to help you visually design the display of every piece of your site.

## Editing Element Templates
![Venue Selection](img/content_element_templates.png)

## Setting Global Variables In Element Templates
Any value can be set in both element templates using the following syntax:

```@set("name",value)```

This is useful for transferring information from stream components to the template at large, particularly for SEO.  A common example is setting page metadata from within the details of a page:

```@@set("page_title",{{title}})```

Which allows ```<[var:page_title]>``` to be accessed from other components and the overall header/footer stream template.