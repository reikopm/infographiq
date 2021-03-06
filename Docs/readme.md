# Required Files
1. svg/my_infographic.svg - scalable vector graphic file that defines the image shown in your scene
1. svg_elements.csv       - tells infographiq about the shapes to use from your svg(s)
1. plot_indicators.csv    - defines plots to show in the modal for each svg element

## infographic.svg
Scalable Vector Graphic (SVG) files can be created using the free, cross-platform program Inkscape or exported from Adobe Illustrator. This file format is a human-readable subset of xml. For example files see the [info-demo/svg](https://github.com/USF-IMARS/info-demo/tree/master/svg). 

svg files must be placed in a directory named `svg` in order to be found by infographiq.

## svg_elements.csv

1. Columns needed in svg_elements 
- svg
- svg_id (lower case no spaces - **MUST MATCH** svg_id in plot_indicators.csv)
- label
- status_text
- status_color
- modal_text : optional row specifying location of a caption text to include at the bottom of the modal

Example 

|**svg**   |**svg_id**      |**module_title**       |**status_text**|**status_color**|
|----------|----------------|-----------------------|---------------|----------------|
|corals.svg|sea-turtle      | Sea Turtle (focal)    |               |                |

## plot_indicators.csv

1. Columns needed in plot_indicators.csv 
- svg_id (lower case no spaces - **MUST MATCH** svg_id in svg_elements.csv)
- plot_title (title on plot)
- y_label (y label on plot)
- col_t (calls column from csv_url)
- col_y (calls column from csv_url)
- filter (to filter from csv_url)
- group_by (to group from csv_url)
- csv_url (needs to be in github repository)
- skip_lines

Example: 

| **svg_id** |**plot_title**      |**y_label**       |**col_t**|**col_y**|**filter**|**group_by**|**csv_url**|
|------------|--------------------|------------------|---------|---------|----------|------------|-----------|
|sea-turtle  | Sea Turtle Richness| Species Richness | year    | richness| NA       | NA         | github.com/marinebon/info-fk/blob/master/plot_indicators.csv


