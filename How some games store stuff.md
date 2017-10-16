For my own evil purposes, this is a list of some games, and how they store their data. So you know how to rip them I guess. I just woke up I don't know how to describe things.

## Commmon formats

### MADH
This resource is just a MADH file, which Resource Dumper extracts nicely. You just need to put the data of this resource as the data fork of a new file, change the file type to MADH and the creator to PlayerPRO, and then you can listen to it or convert it.

PlayerPRO is open source and once extracted with Resource Dumper it's just a data fork, so it'd be theoretically possible to make a MADH player on Windows/Linux/etc and you wouldn't need conversion. Nobody's done that though. I think.

### snd resource
I'm not sure of the format, it's not just raw streamed audio as you might think, nor are they just snd files you can put in the System suitcase for use as alert sounds. Brian's Sound Tool can extract them (to WAV/AIFF), but it'll just give you every single sound resource at once. i suppose Resource Dumper would do that too with the way it's currently designed.

### nVir
If you see this resource you have the nVir.A virus! Get rid of it, silly.

--------
## A Day at Work
Unknown. Uses the Cocoa engine (the one that was an engine before Cocoa was an appliction framework. It's okay to be confused, just know that the engine's called Cococa, and there's a DITL resource which credits the "Cocoa Autoplayer Engine" copyright Apple 1998 written by Peter Jensen). CanOpener can't even see anything except a picture of a bird thing on a hoverboard used in that DITL.

## Ares
### Text
The main executable contains the shareware nag dialog in the TEXT/styl resources 900, 901, and 902. 6500 is the credits, which seems to have a few formatting directives in there and doesn't even need to be a styl resource at all.

STR# resource 750 is named "cheats", but they look like garbage. But hey, they could be actual cheat codes, I haven't really played this game.

### Graphics
PICT 900 in the main executable is the Ambrosia logo from the splash screen, and 502 is the title screen.

Ares Sprites logically would contain the sprites, but when you open it up you just get a lot of SMIV resources. The names would suggest these are indeed the sprites, but I don't know the SMIV format yet.

### Music
MADH resources in Ares Sounds (in Ares Data f folder). If you just want to listen to it Ambrosia has mp3s on the game's addons page.

### Sound effects
They're all snd resources inside Ares Sounds.

## Avernum
### Text
There's a lot of interesting things in the STR# resources in the main executable. Spell names and special abilities and whatnot.

### Graphics
The main executable has a bunch of ppat resources which seem to be the tiles used in the game.

Avernum Character Graphics is where it gets fun, as you have a bunch of sprite sheets in PICT resources, divided by a 1 pixel black border. And some big character pictures too. Avernum Graphics also contains a whole bunch of PICTs that are sometimes also divided by black 1px borders, and seems to have all the items and UI elements in the game.

### Music
Opening music is snd resource 20022 in Avernum Sounds.

### Sound effects
All snd resources inside Ares Sounds.

## Bub & Bob
### Music
Stored in the main executable, snd resources 128-132. The fish and death jingles are 134 and 138 respectively.

### Sound effects
snd resources inside main executable.

### Graphics
Title screen is PICT resource 129 in main executable. Game over screen is 130, highscore list header is 151, you get the idea, there's a bunch of UI elements in there.

Tiles are ppat resources inside Bub & Bob Levels. Adorable sprites are cicn resources in Bub & Bob Sprites. Larger graphics like bonus fruit is stored as PICT resources in Bub & Bob Sprites.

### Game data
Levels are LEVL resources in Bub & Bob Levels. I'm not sure of the format but they all seem to have a size of 1090 bytes.

Bub & Bob Dreamland is an alternate level set I think, so it also has LEVL resources (and ppat for the tile graphics).

## Bubble Trouble
### Graphics
PICT resources in the main executable have the Ambrosia logo, the title screen logo, the "By Alex Metcalf & David Wareing" graphic, the "Press Caps Lock to Resume" graphic, and... a poem? Is that unused?

There's a TMPL resource in there which lets you edit Rect resources, which seems to be used for telling the game where to render UI elements to (what size and position).

Super ResEdit says the ppat resources in BT Levels are corrupted, so I guess it's a different format than the usual. Whatever they're used for here.

Sprites would be in BT Sprites, but they're in a weird format. There's some btSP resources which don't seem to be in any particular normal format used by normal people.

Title screen graphics and UI elements are PICT resources in BT Titles. There's also some PICT resources with IDs 9001 and 9002 for green text and yellow text respectively.

### Text
STR# 129 in main executable has a list of names to the other files needed by the game, so I wouldn't touch it, but it's interesting. The other ones are just errors and preferences dialogs text, but what's interesting is 4000, which contains a single string:  
"Heh! Do you really think we'd hide the cheat codes in here?"

### Sound effects
snd resources in BT Sounds.

### Game data
Levels seem to be stored in MAZE resources in BT Levels, which is a format that I'm not quite sure about, but they're also 176 bytes. There's also corresponding LEVL resources which are presumably not the same as Bub & Bob LEVLs, and are all 64 bytes.

### Music
MADH files in the BT Music folder. The creator code is set to PlayerPRO already.

## Captain Bumper

### Music
snd resources in main executable.

### Sound effects
Also snd resources in main executable.

### Graphics
All the title screen graphics and sprites and whatnot are PICT resources in the main executable.

## Where in the World is Carmen Sandiego? Deluxe

### Sound effects
There's some in snd resources in Sound.rsrc (in the misc resources folder), but then there's also Sound2.rsrc which has some csnd resources.

### Music
testsong.rsrc contains some MIDI resources, which are probably just MIDI files in resource form, but I haven't tried dumping them yet. There's also instruments in the snd resources there, plus INST resources which seem to describe the instruments, and a TMPL for editing SONG resources which seem to contain information for how the MIDI engine should play the songs.

### Graphics
Title screen graphics are PICT resources in the main executable.

The animations would be stored in the anims folder, and there's .anX files in each subfolder there, but I'm not sure what that format is. All I can figure out is that there's a STR# resource that seems to contain which sounds are played in that animation, and a clut for the palette. The PBIT resources possibly do something.

picts1.rsrc, picts2.rsrc, picts3.rsrc, and picts3b.rsrc all contain clut resources and PBIT resources. Still dunno what PBIT is.

There's graphics for the phone in phone anim.rsrc, and profiles.rsrc and screen.rsrc have some UI elements. Those are all in PICT resources.

### Text
carmen.rsrc has a whole lot of fun STR# resources, which seems to have UI elements, clues, names of characters... damn well everything.

country.rsrc has a list of countries and cities, and educational information about those countries and cities (cool!), but the STR# resources which have those are unnamed so there doesn't seem to be organization there. There's also some INFO resources, which is a weird binary format, but I can see that each INFO resource has the name of a currency and some colours (colours used in that country's flag I guess?)

## Cave Dig 3
### Music
The Cave Dig Music folder in the Data folder has some QuickTime movies, which are just mp3s in a QuickTime container. You can extract them to actual sound files using QuickTime Player (might need Pro version) by using Export... and then Sound to Wave (or other things depending on what QuickTime components you have). VLC should be able to just open them though if you give them a .mov extension.

### Graphics
Various title screen graphics and what I think is cutscenes and pics of the developers are all in PICT resources in the Cave Dig Classic executable (in the Data folder), but what may be most interesting is PICT 2000, which has all the sprites.

### Sound effects
snd resources in Cave Dig Classic executable.
