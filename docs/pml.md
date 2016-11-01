# What is PML?
Play analysis is a centeral part of the production of a play for every playwright, performer and member of the design/production team.  However, the tendancy to rely on physical scripts for practical and logistical reasons throughout much of the production process has meant that these analyses have stayed analogue as well.

Play Markup Language (PML) provides a standard that playwrights can convert their scripts to which will allow many of the tasks that take up the begining of a rehearsal process to be automated.  This allows artists to dive deeper, ask more experimental questions without fear of wasted effort and identify insights and problems before they arrive later in the reharsal process.

This page is the definitive resource for the PML standard as it evolves.  Currently PML markup lines only denote information traditionally found in the text of play, but over time it will continue to evolve to include useful information previously unavailable within theatrical texts.

## PML Design Principles
The central design goal of PML was to maintain human readability of the file while also providing the markup necessary for automated processing.  As a result PML consists of sections of text broken up by single lines of markup.  The text that lies between any two lines of markup is described by the markup line immediately above it.  In practice this means a markup line that indicates a line of dialogue and identifies the character speaking proceeds the line that is spoken, which follows traditional script format.

A markup line of PML looks like this:<br>
<b>@field_type</b>{<b>var_name</b>:var_data, <b>var_name</b>:var_data, ...}<br>

After the field type specifier (which is preceeded by an @ sign to distinguish these lines for human readers) standard JSON format is followed.

## PML V0.1
(Quotes matter)<br>
@play{title: “place_holder”, author: “place_holder”} - information about the play<br>
@v{number: place_holder} - The pml version number<br>

@a{number: place_holder} - new act<br>
@s{number: place_holder} - new scene<br>

@l{name: “place_holder”} - A line of dialogue spoken by a character<br>
@d{}  - A stage direction<br>

@e{names:[“place_holder”, ”place_holder”]} - Character enters<br>
@x{names:[“place_holder”, ”place_holder”]} - Character exits<br>
@c{start: place_holder, stop:place_holder} - A comment or annotation for the preceding line spanning the two listed word numbers.<br>

