# What is PML?
Most scripts consist of the same key components  PML stands for Play Markup Language.


Over time PML will continue to introduce new metadata types which will expand the types of information that ideas which were previously silowed away will become accessible to the theatrical community and make our work better.

## PML Design Principles

PML was designed with the following goals
1) Human readability:  For PML to be useful non-technical authors need to be able to write it, and the raw text file needs to be readable.  This eliminates the possibility of using something akin to XML or JSON style storage directly as they introduce too much clutter to being able to read the file directly.
2)  Easy to evolve: as the markup becomes more widely used the ability to add additional metadata information is going to be extremely useful.  However, a text that has been marked up once should be able to generate all visualizations and metadata that it can.
3)  Usable over HTTP:  This eliminates the ability to rely on whitespace or line breaks as these are eliminated when sent over a network

A markup line of PML looks like this:
@fieldType{varName:varData, varName:varData}

In PML all lines are either a markup line or a body line.  All data that comes between 2 markup lines is assumed to be related to the first markup line.  As a result, each line of markup describes and provides metadata information about the text that comes next.  This also makes the standard easily extensible - if a new markup line is introduced the new data will simply be ignored by visualizations designed for earlier versions.

## Components of PML

The main components are:
1) @ sign is first character in line.  This allows the reader to easily skip lines that aren’t in the original text
2) a field type identifier.  This identifies what type of data comes after the markup line
3) A dictionary of variableNames to data that provide additional metadata information

## PML V0.1
(Quotes matter)<br>
@play{title: “placeholder”, author: “placeholder”} - information about the play<br>
@v{number: placeholder} - The pml version number<br>


@a{number: placeholder} - new act<br>
@s{number: placeholder} - new scene<br>

@l{name: “placeholder”} - A line of dialogue spoken by a character<br>
@d{}  - A stage direction<br>

@e{names:[“placeholder”, ”placeholder”]} - Character enters<br>
@x{names:[“placeholder”, ”placeholder”]} - Character exits<br>
@c{start: placeholder, stop:placeholder} - A comment or annotation for a line spanning the two listed word numbers<br>

