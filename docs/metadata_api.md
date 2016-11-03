# Metadata Introduction
Metadata API requests return JSONs which contain information extracted from the text.  This documentation details both the required POST fields and the returned JSON's format.  All POST fields listed must be specified, even if they are specified as empty.

All metadata api requests should be made via POST request to api.playAnalyzer.com/metadata.  

-----
## Character List
### Type: character_list<br>

### Description:<br>
Returns all of the characters in the text.

### Fields:<br>
None

### Returns:<br>
{"characters": [array of characters]}

-----
## Most Common Words
### Type: most\_common_words<br>

### Description:<br>
Returns an ordered array of the most commonly used words in the corpous.

### Fields:<br>
acts, from_scene, to_scene, characters

### Returns:<br>
[{"word": \_\_\_, "count": \_\_\_}, ...]

-----
## Character Speech Flow
### Type: character\_speech_flow<br>

### Description:<br>
Returns an ordered array of the characters that speak after each other most frequently.

### Fields:<br>
acts, from_scene, to_scene, characters

### Returns:<br>
[{"character\_1": \_\_\_, "character\_2": \_\_\_, "count": \_\_\_, "percentage": \_\_\_}, ...]

-----
## Concordance
### Type: concordance<br>

### Description:<br>
Returns every instance of the requested word or phrase in context

### Fields:<br>
acts, from_scene, to_scene, characters, words

### Returns:<br>
String with concordance occurances seperated by newline

-----
## Common context
### Type: common\_contexts<br>

### Description:<br>
Returns a list of words that occur within the same contexts as the requested word.  Submitting more than one word is an and request (words that occur in the context of both) not an or request.

### Fields:<br>
acts, from_scene, to_scene, characters, words

### Returns:<br>
[{"word": \_\_\_, "context": \_\_\_}, ...]

-----
## Parsed Play List
### Type: parsed\_play_list<br>

### Description:<br>
Returns a json

### Fields:<br>
None

### Returns:<br>
[{"entry_type": \_\_\_, ...(entry specific properties)...}, ...]

### PML V0.1 entry_types:properties are<br>
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


