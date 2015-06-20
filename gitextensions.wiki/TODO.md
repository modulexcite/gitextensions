**TODO:**

- Improve Visual Studio integration

- This is kind of a big one, but a radio button to switch from ‘change’ view to ‘tree’ view in the main window would be awesome!  I’m thinking of a tree control showing the repository as it’s currently checked out, with columns indicating the file status, most recent change (author, date and comment) for each file.  Context menus would allow viewing the history of the file, showing the blame results for the file , etc. 

- Another big one, have you seen Perforce’s “time lapse view”?  It’s a view of the file with “blame” markers on the left, a draggable timeline at the top and change details at the bottom.  Dragging the timeline left and forth allows you to “watch” the file change over time.

## PUTTY

It turned out that plink.exe (v 0.53b), contrary to what its usage output
says, doesn't use SSH protocol by default, instead, the protocol selected
depends on the "Default Settings" read from the registry. These settings
can be customized using putty.exe GUI.


Steps to reproduce:

1. Run putty.exe
2. Load "Default Settings" session (select it in the "Saved session"
listbox then click the "Load" button).
3. Change the "Protocol" radiobutton to something other than "SSH" (say,
"Telnet").
4. Click the "Save" button, exit the program.
5. Perform some action with git involving talking to a remote repository
via SSH, see it failing.


I think the problem can be solved in two ways:

1. When plink.exe is used, add the "-ssh" command line option to the list
of arguments to plink. The necessary framework exists as there is already a
workaround for its "-P" option.
2. Let the user choose how to invoke plink: allow GIT_SSH to contain also
arbitrary parameters to plink.exe, not just its path name, and make a note
about broked PuTTY behavior in a README file. This would allow the user to
have a non-SSH defaults in PuTTY's "Default Settings" and set his/her
GIT_SSH to something like
C:\path\to\plink.exe -ssh
or even
C:\path\to\plink.exe -load saved_session_name

You could also set the environment variable PLINK_PROTOCOL=ssh 