# __<span style="color:#D57500">Command Line Application Help</span>__
This topic provides a basic introduction to using software tools that do not have a graphical user interface (GUI) and instead can only be used at the Windows Command Prompt.

### Description
Several of the applications available on this site are command-line only applications. This means that they do not have a graphical user interface (GUI) and, instead, must be run via the Windows Command Prompt. The following discussion is provided to help you run command line applications.

### Identifying Command Line Applications

You will know the program is a command line application if you see one of the following behaviors:

You run the program shortcut (e.g. Start->Programs->PAST Toolkit->Residue Frequency Summarizer) and a black window appears in the background, while a Program Syntax window appears in the foreground (see Figure 1 in CommandLineHelp.pdf, available below)
You navigate to the program's folder in C:\Program Files\ and double click the program executable (e.g. ResidueFrequencySummarizer.exe) and, again, you see a black window in the background and a syntax window in the foreground (see Figure 1 in CommandLineHelp.pdf)
You run the program (either by shortcut or double clicking the .Exe) and a black window appears very briefly and then disappears (see Figure 2 in CommandLineHelp.pdf)

### Running a Command Line Application
In order to properly run a command line application, you will need to follow these steps.  Note that CommandLineHelp.pdf (available below) also includes screenshots for these steps.

1. Go to the Windows command prompt.  One option is to choose Run from the Windows Start menu, type cmd, and click OK
2. Use the "cd" command to change to the folder containing the program you wish to run. You can also use the "dir" command to view the files and folders present.
3. Run the command line program by typing its name and pressing Enter

### Program Switches

When running a command line program, you will typically need to pass some information to the program, e.g. a filename to process or a parameter that specifies a processing option. Windows command line programs typically use the / character (forward slash) for a switch, though sometimes the - character (dash) is used instead. In the example shown in the above figure, the /i switch was used to specify the input file for the program, like this:

`ResidueFrequencySummarizer.exe /i:TestSequences.txt`

Each command line program available on this site should include a Readme.txt file that explains the switches appropriate for the given program. Alternatively, if you run the program without any switches, or with the /? switch, you should see the program syntax, either in a new window or in the command prompt window (as shown in Figures 1 and 2, above).

### Additional Information

You can find numerous web pages that describe the use of the command prompt in Windows. For example, the top hits for googling [using the windows command prompt](http://www.google.com/search?sourceid=navclient&q=using+the+windows+command+prompt) include tutorials at these sites:

* [BleepingComputer.com](http://www.bleepingcomputer.com/tutorials/windows-command-prompt-introduction/)
* [CommandWindows.com](http://commandwindows.com/)
* [Sophos.com](http://www.sophos.com/en-us/support/knowledgebase/13195.aspx)

### Downloads
* [PDF with command line usage tips and screenshots](CommandLineHelp.pdf)
