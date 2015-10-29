# Importing Events and Configuring Scrapers

### Scraping Manifests
> All scraping processes are defined by configuration files called 'manifests.'  These are JSON files that utilize the following structure

```json
{
    "name": "[Name of Import]",
    "method": "[HTTP Method, typically GET or POST]",
    "root-url": "[Starting URL]",
    "encapsulate-element": "[DOM element that matches events on a page]",
    "refine-encapsulate-element": "[DOM element that matches events on a details page]",
    "lookups": [
      {
        "name": "[name of lookup table]",
        "values": [
          {"input":"[text to compare]", "output":"[text to replace]"}
        ]
      }
    ],
    "rules": [
        {
            "field": "[name of field]",
            "element": "[DOM element of field]",
            "attribute": "[If the value is contained in an element's attribute]",
            "refine": "[true/false, whether this represents a link to a detail page]",
            "multiple": "[true/false, whether to retain all matches]",
            "filters": [
                {
                    "type": "[type of filter (see below)]",
                    "options": [
                        {
                        }
                    ]
                }
            ]
        }
    ],
    "refine-rules": [
        {
            "field": "[name of field]",
            "element": "[DOM element of field]",
            "attribute": "[If the value is contained in an element's attribute]",
            "refine": [true/false, whether this represents a link to a detail page],
            "multiple": [true/false, whether to retain all matches],
            "filters": [

            ]
        }
    ]
}
```
### Types of filters
Filters can be stacked and are called in the order they are defined.  As an example, if you have a title element that always matches Title:, you can use a ```textMustMatch``` filter to identify it, then a ```replace``` filter to strip text and a ```trim``` filter to remove space.  Those fields will be called in order.

* ```textMustMatch``` - Will only match elements that contain this text
* ```replace``` - Allows regular expressions
* ```composite``` - Accepts template-based declaration of field values.  In other words, if you had a date element and a time element and wished to combine into a single element, you could use ```{{date}} - {{time}}``` to produce this value.
* ```extract``` - Shorthand regex that allows you to isolate text in a field
* ```appendValue``` - Adds defined text at the end of the field
* ```prependValue``` - Adds defined text at the beginning of a field
* ```html2nl``` - Will replace ```div```, ```br```, ```hr```, ```p``` with newlines
* ```stripHTML``` - Removes HTML
* ```setVar``` - Allows current value of field to be copied into new dynamic field
* ```split``` - Allows turning a field value into an array by splitting by character
* ```javascript``` - Allows manipulation of current data using Javascript.  Current value is accessed by and stored as ```$V```
* ```lookup``` - Converts current value to predefined value using values from lookups