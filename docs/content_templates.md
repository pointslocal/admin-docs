# Create Or Modify Media Streams
> This guide will show you how pages - or "media streams" - are created in Pointslocal.

In order to customize the appearance of various “streams” you will need to create “templates” and , optionally, “Element Templates”. Stream templates are include all of the main design elements of a page while “Element Templates” allow you to customize the styles for individual elements inserted via the “Stream Designer”.

1. Login to the Pointslocal Admin
Pointslocal Step by Step Stream Setup

1. Login - http://sitecode.pointslocal.com/admin:
2. Navigate to files and templates:
3. Click “New Stream Template:
4. Name your template and assign the desired URL rewrite if applicable:
5. Insert your desired HTML:
Note: Header and footer are not both required but provided as many organizations provide “wrappers” in this convention.
6. Within the HTML insert, ```<[content-group:1]>```, ```<[content-group:2]>``` and so on in any location you want to be available for dynamic content in the visual designer:
7. Select “Edit Stream Template” at the bottom of the page to save:

Your template is now saved and available for selection on the creation of new streams. You can modify existing templates by selecting them from the list of available templates, making changes and selecting “Edit Stream Template”

##Creating element templates

1. Navigate to “Element Templates:
2. Select “New Stream Element”:
3. Name your new Element Template:
4. Insert the desired styling you wish to be available for Elements in the Stream Designer:
Note on the right the choice of element types and the wide array of dynamic elements available for inclusion on the Element. Each Element type has different options available for inclusion on the Element Template
5. Save by selecting “Edit Stream Element”:

##Creating a new stream

1. Navigate to “Media Streams”:
2. Select “New Stream”
3. Name your new stream (and modify rewrite if desired) and select the desired template to be attached to the Stream:
4. Select the Stream Designer icon in the row of the stream you wish to create or edit”
5.  You will now see the template you created rendered with dotted boxes in all the locations you made available for dynamic content by including the ```<[content-group:X]>``` tag:
6. To insert content into those boxes simply select the desired type represented by the icons available in the top bar and drag the icon to the desired content group box:

Note: Mousing over the icon will provide explanations of different element types.

7. Each element type has different configuration options with the exception of adding html (which you might use to insert a video widget or ad tag e.g.). 

To configure the element click on the edit element icon

Some recurring options include Ontology, which filters on manual or automatically tagged ontologies and Image Crop Mode, which allows you to specify auto crop options

8. Preview your Stream by electing the preview icon in the upper right:
9. Save your Stream by electing the  save icon:
10. Returning to the list of available Streams you can perform a number of edits that directly bypass the navigation required in creating them.

To edit the content elements in the stream select:

To immediately recache the stream (depending on your requirements streams are set to cache for varying periods by default):

To change the stream name and or template choice:

Or to edit the code in the template or add or change content groups you can select the hyperlinked template name:

3. Create your story by filling in all desired fields and metadata:
