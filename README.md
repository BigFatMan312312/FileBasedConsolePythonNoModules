# FileBasedConsolePythonNoModules
This is just a python console a made, please test and report any bugs you file, want to make a os, but need more feedback to fix bugs in this test build


To Test this copy and paste the code into this website "https://www.online-python.com/online_python_compiler"
If you want to test this is the code:

import math

Files = []
FileLine = []
FileLineName = []

print("This is my Console, the commands are Add File, Change File Name, EditFile, ReadFile. Add File justs adds a file with the name you choose, edit file edits the text inside the file using lines, readfile reads the lines from that current file, changefilename just changes the file name of what ever file you choose")

def Console():
    GetLine = input("Type in your command")
    
    if(GetLine == "Add File"):
        GetFile = input("What is the file name")
        Files.append(GetFile)
        Console()
    if(GetLine == "Change File Name"):
        FileIndex = input("what file do you want to change")
        for x in range(0, len(Files)):
            if(FileIndex == (Files[x])):
                FileName = input("what do you want your new file name to be")
                Files[x] = FileName
                Console()
    if(GetLine == "ReadFile"):
        WhatFile = input("what file you want to read")
        
        for x in range(0, len(Files)):
            if(WhatFile == Files[x]):
                for x in range(0, len(FileLine)):
                    print(FileLineName[x])
                    print(FileLine[x])
                    Console()
    if(GetLine == "EditFile"):
        FileEdit = input("what file do you want to edit")
        for x in range(0, len(Files)):
            if(FileEdit == Files[x]):
                Line = input("Add your line here")
                FileLine.append(Line)
                FileLineName.append(Files[x])
                Continue = input("want to add more y/n")
                if(Continue == "y"):
                    Line = input("Add your line here")
                    FileLine.append(Line)
                    FileLineName.append(Files[x])
                    Continue = input("want to add more y/n")
                if(Continue == "n"):
                    Console()
    
Console()

