# Visualization Introduction
Visualization requests generate and return png visualizations of the play according to the specified parameters.  This documentation details the required POST fields for generating images.  All POST fields listed must be specified, even if they are specified as empty.

All metadata api requests should be made via POST request to api.playAnalyzer.com/generate_viz.  

-----
## Scene Rhythm Chart
### Type: scene\_rhythm\_chart<br>

### Description:<br>
Generates a visualization of approximate scene length based on word count to show the overall rhythm of the show.

### Fields:<br>
None

-----
## French Scene Chart
### Type: french\_scene\_chart<br>

### Description:<br>
Generates a chart that marks all french scenes.

### Fields:<br>
None

-----
## Word Occurance Chart
### Type: word\_occurances\_chart<br>

### Description:<br>
Generates a chart that marks all occurances of a comma seperated list of words within the corpous spoken by specified characters.

### Fields:<br>
acts, from_scene, to_scene, characters, words

-----
## Dialogue Shape Chart
### Type: dialogue\_shape\_chart<br>

### Description:<br>
Generates a chart that displays line length based on word count along the y-axis with subsequent lines laid out along the x-axis.  Charaters that are passed in will have their lines highlighted on the chart.

### Fields:<br>
acts, from_scene, to_scene, characters

-----
## Line Shape Chart
### Type: line\_shape\_chart<br>

### Description:<br>
Generates the same style of chart as the Dialogue Shape Chart, however instead of highlighting charcters specfied, it displays only lines by the characters specified.

### Fields:<br>
acts, from_scene, to_scene, characters

-----
## Character Speech Chart
### Type: character\_speech_chart<br>

### Description:<br>
Generates a weighted graph of the connection between characters based on how frequently they speak after each other.

### Fields:<br>
acts, from_scene, to_scene, characters