# Welcome!


## Who's this documentation for?

<a href="playanalyzer.com">PlayAnalyzer.com</a> is built on top of a RESTful server that processes PML and produces metadata and visualization outputs. While most users can gain insight into a play through the web interface, this documentation exposes the full API for users who want to be able to quickly batch generate insights and analyses of plays.

## How to get started

Most users should use the play analyzer <a href="https://github.com/kevinmkarol/play_analyzer_api_interface">api interface</a> repository to make requests to the server using python.  Just replace the file path parameter and start generating outputs with single python commands.

If you haven't had a chance to mark up your own texts into PML yet, but would like to see what this API can do, a <a href="https://github.com/kevinmkarol/play_analyzer_play_repository">play repository</a> of public domain texts is also available.

## Site Map
The site pages document the following information:<br>
<b>PML Spec:</b> Documents Play Markup Language (PML) syntax and design philosophy<br>
<b>Metadata API:</b> Documents metadata outputs available and the return JSON syntax<br>
<b>Visualization API:</b> Documents requests for play visualizations to generate pngs<br>

## Making API Requests
All requests are POST requests to api.playAnalyzer.com/api_type.  

All API requests require the following fields:<br>
<b>pml_text</b> - the marked up play text as a file<br>
<b>type</b> - the output type to generate<br>

Where appropriate the api often allow the corpous to be refined with the following parameters:<br>
<b>acts</b> - A comma seperated list of acts.  Unspecified means the whole show.<br>
<b>from_scene</b> - The scene in the first listed act to start from.<br>
<b>to_scene</b> - The scene in the last listed act to end with.<br>
<b>characters</b> - A comma seperated list of character names<br>


## Feedback?
If you encounter issues, have suggestions for future visualizations or metadata, or would like to have studies you conduct using this API featured on PlayAnalyzer.com, please contact us <a href="mailto:kevinmkarol+playAnalyzerApi@gmail.com">here.</a>