# Welcome to PlayAnalyzer.com's API Documentation

Most non-technical users can utilize PML and the insights it can provide into a text using the resources on <a href="playanalyzer.com">PlayAnalyzer.com.</a>  However, for the more technically inclined this documentation should provide you insight into the workings

## Site Map
The site pages document the following information:<br>
<li>PML Spec: This page details the specifics of how PML markup works, the principles behind it, and documents the latest PML specification</li>
<li>Metadata API: The api for requesting metadata information derived from the text.</li>
<li>Visualization API: The api for requesting pngs that graphically display properties of the play derived from the text.</li>

## Field Descriptions
All API requests require the following fields:<br>
<b>fieldName</b>:'pmlText' <b>value</b>: the marked up play text
<b>fieldName</b>:'type' <b>value</b>: the vizualization type generate.

Each request type may specify some subset of the fields explained below.  These fields narrow the portions of the text that will be considered part of the corpous to return the metadata from.<br>
<b>None</b> - no additional fields required.<br>
<b>acts</b> - A comma seperated list of acts to use the text from.  Unspecified means the whole show.<br>
<b>fromScene</b> - The scene in the first listed act to start from.<br>
<b>toScene</b> - The scene in the last listed act to end with.<br>
<b>characters</b> - A comma seperated list of characters to use the dialogue of.<br>


## Making API Requests
A collection of <a href="http://kevinmkarol.com">python scripts</a> has been provided to make the process of submitting API requests as easy as possible.

All REST requests should be sent via POST request to api.playAnalyzer.com/api_type.  If you encounter issues using the api, have suggestions for future visualizations or metadata, or would like to have studies you conduct using this API featured on PlayAnalyzer.com, please contact us <a href="mailto:kevinmkarol+playAnalyzerApi@gmail.com">here.</a>


