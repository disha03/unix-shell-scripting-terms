# unix-shell-scripting-terms
## Telnet 
is an application protocol used on the Internet or local area network to provide a bidirectional interactive text-oriented communication facility using a virtual terminal connection. User data is interspersed in-band with Telnet control information in an 8-bit byteoriented data connection over the Transmission Control Protocol (TCP).Telnet provided access to a command-line interface on a remote host. However, because of serious security concerns when using Telnet over an open network such as the Internet, its use for this purpose has waned significantly in favor of SSH.
## Cryptography, or cryptology,
is the practice and study of techniques for secure communication in the presence of third parties called adversaries.
## Unix
UNIX is an operating system which was first developed in the 1960s, and has been under constant development ever since. By operating system, we mean the suite of programs which make the computer work. It is a stable, multi-user, multi-tasking system for servers, desktops and laptops.
UNIX systems also have a graphical user interface (GUI) similar to Microsoft Windows which provides an easy to use environment. However, knowledge of UNIX is required for operations which aren't covered by a graphical program, or for when there is no windows interface available, for example, in a telnet session.
## The kernel
The kernel of UNIX is the hub of the operating system: it allocates time and memory to programs and handles the filestore and communications in response to system calls.

As an illustration of the way that the shell and the kernel work together, suppose a user types rm myfile (which has the effect of removing the file myfile). The shell searches the filestore for the file containing the program rm, and then requests the kernel, through system calls, to execute the program rm on myfile. When the process rm myfile has finished running, the shell then returns the UNIX prompt % to the user, indicating that it is waiting for further commands.

## The shell
The shell acts as an interface between the user and the kernel. When a user logs in, the login program checks the username and password, and then starts another program called the shell. The shell is a command line interpreter (CLI). It interprets the commands the user types in and arranges for them to be carried out. The commands are themselves programs: when they terminate, the shell gives the user another prompt (% on our systems).

## The Directory Structure
All the files are grouped together in the directory structure. The file-system is arranged in a hierarchical structure, like an inverted tree. The top of the hierarchy is traditionally called root (written as a slash / )

Unix File Structure

In the diagram above, we see that the home directory of the undergraduate student "ee51vn" contains two sub-directories (docs and pics) and a file called report.doc.

The full path to the file report.doc is "/home/its/ug1/ee51vn/report.doc"
## Commands
### ls 
lists the contents of your current working directory.ls does not, in fact, cause all the files in your home directory to be listed, but only those ones whose name does not begin with a dot (.) Files beginning with a dot (.) are known as hidden files and usually contain important program configuration information. They are hidden because you should not change them unless you are very familiar with UNIX!!!
### ls -a 
lists files that are normally hidden.
### mkdir (make directory)
### cd (change directory)
### cd .
Note: typing cd with no argument always returns you to your home directory. This is very useful if you are lost in the file system.
### pwd (print working directory)
### ls backups
### cd ~	
change to home-directory
### cp (copy)
cp file1 file2 is the command which makes a copy of file1 in the current working directory and calls it file2
firstly you have to reach the directory in which you want to copy then,cp "write full path of file you want to copy" "new name of file"
### mv file1 file2 moves (or renames) file1 to file2(move in existing directoy)
mv /home/diiiiisha/Downloads/mnn mvv
mv "write full path of file you want to copy" "new name of file"
### rm (remove), rmdir (remove directory)
### clear (clear screen) 
### cat (concatenate)
The command cat can be used to display the contents of a file on the screen. cat disha.txt
### less
The command less writes the contents of a file onto the screen a page at a time. Type
% less science.txt
Press the [space-bar] if you want to see another page, and type [q] if you want to quit reading. As you can see, less is used in preference to cat for long files.
### head
The head command writes the first ten lines of a file to the screen.
First clear the screen then type
% head science.txt
### tail
The tail command writes the last ten lines of a file to the screen.
Clear the screen and type
% tail science.txt
### Simple searching using less
Using less, you can search though a text file for a keyword (pattern). For example, to search through science.txt for the word 'science', type
% less science.txt
then, still in less, type a forward slash [/] followed by the word to search
/science
### grep (don't ask why it is called grep)
grep is one of many standard UNIX utilities. It searches files for specified words or patterns. First clear the screen, then type

% grep Science science.txt

The grep command is case sensitive; it distinguishes between Science and science.

To ignore upper/lower case distinctions, use the -i option, i.e. type

% grep -i science science.txt

To search for a phrase or pattern, you must enclose it in single quotes (the apostrophe symbol). For example to search for spinning top, type

% grep -i 'spinning top' science.txt

Some of the other options of grep are:

-v display those lines that do NOT match
-n precede each matching line with the line number
-c print only the total count of matched lines

Try some of them and see the different results. Don't forget, you can use more than one option at a time. For example, the number of lines without the words science or Science is

% grep -ivc science science.txt
### wc (word count)























