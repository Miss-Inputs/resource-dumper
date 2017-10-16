# resource-dumper
This is a small simple application that runs with MacPython 2.2.3 (maybe other versions but those would be untested). It asks the user for a file and dumps the entire resource fork to a folder containing each resource as a data file. The file type is set to the resource type (so certain things might open inside Mac OS) and the creator is set to ???? so you'll get prompted to find something that can open it, though you'll probably want to use something like FileTyper to set things unless you're just copying the files over to Windows/Linux/etc from a SheepShaver guest or something.

This is intended for ripping the music from old Mac games so you can theoretically listen to stuff on Windows/Linux, but I guess it could be used for other evil purposes too. As an example, if you have a MADH resource that a lot of games seem to use, it will write the creator as PlayerPRO so you can open the file there, and then convert it to .xm or whatever.

TODO list because I can't be stuffed raising issues for myself:
  - Nicer interface, or I should say an interface at all. Just a nice little list of resource types that you can browse through, and when you select one a nice little list of resources of that type appear, and then you have a button to extract selected, which extracts the whole lot if you don't select a resource type, or all resources of a type, or all the resources you have selected or just one. Maybe a button to convert, maybe even a play/view/etc button  
  - Convert some known resource types to more usable formats (but dump the original as well)  
  - Maybe resource injection?
  - Maybe Linux/Windows/etc version that can look in .rsrc folders on BasiliskII/SheepShaver shared drives, or HFS disk images
