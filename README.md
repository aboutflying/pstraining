Day 2

1. Variables
   - Syntax
   - How to set
   - Practical example
2. Methods and properties
    - Syntax
    - How to use
    - Practical example
3. How to run commands on remote computers using invoke-commands
    - Syntax
    - How to use
    - Practical example
4. Self-teaching
    - Section 4 (Gathering information) and 5 (Remoting): https://app.pluralsight.com/library/courses/powershell-getting-started/table-of-contents
5. Complete quests after watching the above training

Quest 1

1. Create a branch in your repo called 'feature/day2'
2. Create a directory in your local copy of your repository called 'Day 2'
3. Write a powershell script that locates and outputs information about a specific file from a remote server. The remote server you'll use is ``<redacted>``. 
    Your goal is to locate a file with the following properties, using only powershell scripting:
    - File size is 90614
    - File is located on the C drive
4. Add, commit and push your changes to the remote 'feature/day2' branch

Quest 2

1. On the same server, there is a firewall rule with a display name of the filename of the file you located in Quest 1 minus the file extension (i.e. the filename 'blahblah.txt' = firewall rule name 'blahblah'). 
    Add more code to your powershell script from the previous quest that returns the local port number for this rule.
    - You'll need to modify your existing script from Quest 1 to also store the basename of the file you located in a variable, then use that variable for this quest. Nothing should be set statically.
2. Save  your updated script to your day2 directory
3. Add, commit and push your changes to the remote 'feature/day2' branch

Extra Credit

- Add code to your script to copy the file you located in Quest 1 to your local computer, then commit, push and open a PR to have it reviewed.

Notes/Rules:

- Skip the part in Pluralsight about enabling remote functionality in section 5 "Remoting with Powershell" - it isn't needed
- Set the server name using a variable at the top of your script. Use this variable whenever you would normally type it in statically.
- The path format for a remote computer is ``\\<computername>\<driveletter>$\<path>`` i.e. ``\\<IPOrHostName>\c$\Windows\coolfile.txt``
- Filenames/paths should be discovered and set programatically in your scripts i.e. if you discover that the file path is ``C:\blahblah.txt``, you cannot statically use ``"C:\blahblah.txt"`` in your script
- Output from a command can be captured and assigned to a variable, and reused in  your script i.e. ``${myVar} = Get-Childitem C:\``
- "Length" is the property for file size in Powershell
- The pluralsight training will only get you part of the way there. The rest you will need to figure out using get-help and the online Microsoft documentation/examples. Make sure teo read the command descriptions closely!

something
another thing
