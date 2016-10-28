# Metadata Introduction
Metadata API requests return JSONs which contain information extracted from the text.  This documentation details both the required POST fields and the returned JSON's format.  All POST fields listed must be specified, even if they are specified as empty.

All metadata api requests should be made via POST request to api.playAnalyzer.com/metadata.  

-----
## Character List
### Type: "character_list"<br>

### Description:<br>
Returns all of the characters in the text.

### Fields:<br>
None

### Returns:<br>
{"characters": [array of characters]}

-----
## Most Common Words
### Type: "most\_common_words"<br>

### Description:<br>
Returns an ordered array of the most commonly used words in the corpous.

### Fields:<br>
acts, fromScene, toScene, characters

### Returns:<br>
[{"word": \_\_\_, "count": \_\_\_}, ...]

-----
## Character Speech Flow
### Type: "character\_speech_flow"<br>

### Description:<br>
Returns an ordered array of the characters that speak after each other most frequently.

### Fields:<br>
acts, fromSecen, toScene, characters

### Returns:<br>
[{"character1": \_\_\_, "character2": \_\_\_, "count": \_\_\_, "percentage": \_\_\_}, ...]

-----
## Parsed Play List
### Type: "parsed\_play_list"<br>

### Description:<br>
Returns a json

### Fields:<br>
NONE

### Returns:<br>
[{"entryType": \_\_\_, ...(entry specific properties)...}, ...]

### PML V0.1 EntryTypes/properties are:<br>
<li>Dialogue: characterName, text</li>
<li>StageDirection: direction</li>
<li>Entrance: characterNames</li>
<li>Exit: characterNames</li>
<li>Comment: startingWord, endingWord, text</li>
<li>Act: actNumber</li>
<li>Scene: sceneNumber</li>
<li>PlayInfo: title, author</li>
<li>VersionNumber: versionNumber</li>
<li>Unknown: entryName, entryParameters, entryBody </li>


