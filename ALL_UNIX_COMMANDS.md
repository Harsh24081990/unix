
UNIX COMMANDS
``` shell
1. $ LOGNAME		: It displays the current user information
2. $PWD			: present working directory
3. $DATE			: It displays the system date & time
4. $clear			: To clear the screen
5. $cal			: it current month and year
6. $cal 2000			: Displays the 2000 year calendar
7. $cal 8 2006		: displays the 8th month of 2006
8. $exit or logout		: exit from current user account
9. $ who			: displays the all user in who are currently working on server
10. $finger   			: displays the all user who are currently working on server with more information
11. Who am I   		: displays current user information
12. Which or where   	: displays the location of the given command

My Commands:
Du –sk filename : to find the size of one file
    Du –sk test.txt
Du –sk filename1 filename2 …. : to find size of multiple files
Du –sk test.txt test2.txt
Du –a   ‘Directory name’ : Give the size of all files in that directory.
Du –sk * also can be used to find size of all the files.
Du –a ‘In Bound’  : It List size of all files/Folder size in present directory
Du  -[akhrstx]: Du for folder can be used with any of these characters
But I am getting same result for Du –[trx]
Du –h ‘In Bound’ : consider size of directory while calcualating
E:\files in ds>du -h
      512B ./In Bound/testing_UNIX
   14.50KB ./In Bound
  153.50KB ./Out Bound
  327.00KB .




How to find all the files in all the directories in that folder?
Suppose Files in Ds is the folder which has so many files and also 2 Folders In Bound and Out Bound. We want the files present in In Bound and also Out bound, In that case what needs to be used?
Ls –R


  Syn: $which pwd
13. Cat			: is use to create new files or to open exiting files or to append data to the exiting files
Create: cat >filename
-----------    
-----------cntl+d
Redirect: cat file1 file2 file3 >file4--------→redirect output
Append: cat >>filename--------→ single file        $cat file1 file2 file3 >>EMP------→multi files
-----------    
-----------cntl+d
Open file: cat <filename-----→open single file   $cat file1, file2, file3----------→to open multi files
Cat >.filename---------for hidden files
14. Touch   		: It is used to create an empty file i.e. 0 byte file
SYN: $ touch filename
$ touch file1 file2 file3---------→ create multiple files
15. rm      		: deleting files or directories
EX
rm filename----------------→deleting single file
rm -i filename--------------→deleting files with confirmation
rm file1 file2----------------→deleting multiple files
rmdir dirname--------------→deleting the directory but the directory must be empty
rm  -r dirname-------------→deleting directory recursively (i.e. with tree str)x
rm –ri dirname-------------→remove directory with confirmation
rm *   ---------------------→ it delets all files
rm  -I *--------------------→delets all files with confirmation
rm t* ---------------------→it delets whose file name starts with ‘t’
How to delete the directory which is not empty?
Ex: Rm –r Testing_Unix.
16. mkdir		 : creating directories
Syn: $mkdir dirname
Sys: $Mkdir .dirname------------→hidden directory
17. Cd		: change directory
Sys: $cd abc
$pwd------/home/madhav/abc using above cmd we can come out from abc now we at //home/madhav
cd..---------------------------→to come out from current directory
cd../..------------------------→parent directory
cd/---------------------------→it changes to root directory
cd ~-------------------------→it changes to home directory


18. cp   			:copy source file to target file

Ex
Cp emp1 emp2----------------------→emp1 tp 2 coping
Cp –I m1 m2-------------------------→overwrite confirmation? Y
Cp –R source directory to target directory-------cp –R abc xyz
19. mv			: it is used to rename or move file
Ex: mv exiting filename new filename
    	 Mv emp .emp----------------------→to hide
     	Mv .emp emp--------------------→to unhide
20.ls  			: display, list of all files & directories in a current directory
21.ls|more 		: display, list of all files & directories page by page
22. ls –a		: display, list of all files & directories including hidden files and dirctories also in current directory
23. ls  –r 		: display list of all files & directories revers order in a current directory
24. Ls –R 		: display list of  all files & directories recursively in a current directory
25. Ls –t		 : display list of all files & directories according to date of creation in a current directory
26. Ls –F		 : display all list of files & directories, link files, .exe files in a current directory
27. Ls-x		: display all list of files & directories according to width wise in a current directory
28. Ls-L		: display all list of files & directories in a current directory in a long list i.e. 9 fields
 1) File types
[1) -- For regular file ii) d—for dir file III) L—for link file IV) b—for block of filesV) c— for char files] [here IV, V is device files]
2) File permissions 3) no. of links 4) owner name 5) group name 6) file size in bytes 7) Date 8) time 9) filename

30. cmp 		: it compares two files char by char
Sys: cmp file1 file2 
E:\files in ds\In Bound>cmp type1.txt type2.txt
type1.txt type2.txt differ	r: char 25, line 2       
Ex: a1: Hello Good Morning
     	     a2: Hello Good Evening
    If two lines are same then return nothing
     If two files are are different then it displays line number with character position
31. comm. 		: It display common lines b/w 2 files
  	 Syn: Comm File1 file2
32. diff			: it display different lines b/w 2 files
33. pg			: it display the file contents page by page
     		Syn: $Pg filename
34. more		: it also display the file contents page by page
   		Syn: $more filename
34. head 	:it display the 1st n lines from the file
Sys: $ head –n filename
35. tail		: it display the last n lines from file
   		Syn: tail –n filename
   Tail +n filename----→it indicates nth line to end of the line  
   Ex: tail +30 file (in this file total no of records is 100) it displays the records from 30th to 100
36. wc		: it counts the no of lines, words, chars in a given file.
   		Syn: $wc filename
i) wc –l filename------------------→it gives the no of lines in a given file
ii) wc –w filename---------------→it gives the no of words in a given file
III) wc –c filename---------------→ it gives no. of char in file
iv) wc -lw filename--------------→ it gives the no of lines and character in a given file

37. WILD CARD CHARCTERS or META CHARCTERS
i)	‘*’--------→it matches ‘0’ or more chars
ii)	‘?’ -------→it matches any single chars
iii) [    ] ---→it matches any single chars in the given list
iv)	‘–‘------→it matches any single char in the given range
ls  t*---------------→it list the files starts with ‘t’

ls  *s  -------------→it list the files that ends with ‘S’


ls b*k--------------→it list the files starts with ‘b’ and ends with ‘k’

ls  a?--------------→it list the 2 characters filename 1st later fallowed by ‘a’ and second letter is any one character


ls[bknt]-----------→it list the files starts with ‘b’ or ‘k’ or ‘n’ or ‘t’

ls [abcdefgh] or ls[a-h]*--→list the files, first char b/w ‘a’ to ‘h’


ls [b-k][p-t][d-n]*---------→ it list the files the 1st character ‘b’ to ‘k’ 2nd char ‘p’ to ‘t’ 3rd char ‘d’ to ‘n’ after that any no of characters
ls doesn’t care about Case sensitive 
ex: ls [aeiou]*.txt and ls[AEIOU]*.txt both will give the same result
38. grep		: [globally search a regular expression and print it]
Is used for to search a string or regular expression in a given file(s)
I) Eg: $ grep madhav sample
O/p: 2nd line
5th line
7th line
         		 ii) Eg: $grep madhav a1, a2, a3:
 		a1:------
 		a2:------
a3:------
        		iii) $ grep techno *------→it searches for techno in current dir files (all files)
       	iv) $grep techno soft sample-----→it searches for more than one word 
We kept it in “   “
         v) $grep “techno soft” sample
grep cmd options
$ grep –i techno sample-----------------------→ignore case sensitive
$ grep –c techno sample-----------------------→count no of lines
$grep –n techno sample-----------------------→print along with the line numbers
$grep –l techno *------------------------------→list only file names
$grep –v “techno soft” sample---------------→not matches print the lines
$grep –ci techno sample----------------------→Ignore case sensitive found no of lines
$grep “techno *” sample---------------------→pattern
Regular expression: any string contains wildcard charctor knows as regular expression or pattern
 	These patterns are of 3 types:
Charctor pattern: the default pattern  is char pattern only
i) $grep “techno *” sample
ii) $grep “b [aeiou] ll” sample
iii) $grep “b..d” sample---→i.e. or matches any single charctor
Word pattern :/<    />
  		/< -------→start of the word
		/>------→end of the word
Grep “/<techno/>” sample ------------→o/p: techno
Grep “/<techno” sample----------------→o/p: techno soft
				             -----------------→o/p: techno 123
Grep “techno/>” sample              ----→o/p: hellotechno, abctechno
Grep “/< [0-9][0-9][0-9][0-9]/>” sample--------------→it display 4 digits       (i.e.1234, 4567)

Line pattern: ^----------starts of the file
	          			$----------ends of the file
Ex: grep “^d” sample---------------→it display the line starts with‘d’
     	Grep “^the” sample-----------------→it list the lines start with ‘the’
     	Grep “^/<the/>” simple ----------→sample the line exactly start with ‘the’
     	Grep “t$” simple-------------------→list the line ends with‘t’ or last char is‘t2019
    	 Grep “[0-9] $” sample------------→ display the line ends with 0 to 9 digit
Grep “^ [bkt]” sample------------→list the line starting with ‘b’ or ‘k ‘or’t’
Grep “^ [^bkt]” sample----------→list the line which is not start with ‘b’ or ‘k’ or‘t’
Grep “”^UNIX$” sample ---------→display the line having only word ‘Unix’
Grep “^…. $”----------------------→list the line which contains ‘4’ characters    
(.)----------------------------------→represent single charctor
Grep “^.”------------------------→Sample it list all lines
Grep “/.” Sample: --------------→it lists the line start with (.)
We use \ to search *, $, ^ as a charctor-------→ i.e.\*,|^,\$
Grep “^$” sample--------------→ it list empty lines
Grep –c “^$” sample----------→counts no of empty lines in a file
Grep –v “^$” sample----------→print not matches (i.e. not empty) lines
Grep –v “^$”sample >temp
Mv temp sample-------------------→here both are delete empty files
This command is used to show the After 3 lines when the string is found
Grep –A 3 –i “Chandra” emp.txt
This command is used to show the Before 3 lines when the string is found
Grep –B 3 –I “se” emp.txt
If the no.of lines found are not exactly same as the lines found then it will result the lines that it found.



39. fgrep	: it is used for search multiple strings but it doesn’t allow to search regular expression
     $grep “hello
                >techno
       	>UNIX”sample----------→it searches for hello or techno str UNIX
40. egrep 		: it is combination of grep and fgrep
   $egrep “hello
	  >hello
	>UNIX”sample       $egrep “^$” sample
41. Sed		: to replace a string
$ sed “s/existing string/new string/g” filename--→sed is used to find and replace and grep is for find print
Here g is to state that replace existing string with new string Globally. If we want to replace only second instance then
Sed “s/ existing string/new string/2”
We can use any delimiter to replace the command
Sed “s| existing string| new string |g”
We can replace the string in only one particular line
Sed “3 s| existing string| new string |g”
We can replace range of lines by using below command
Sed “1,3 s| existing string| new string |g”

We can find any no.of lines 2 times by using sed command
Sed  ‘p’ emp.txt -→ This will print all lines 2 times
We can print only particular lines of a file
Sed –n ‘1p;$p’ emp.txt
We can delete lines by usin sed
Sed ‘2 d’ emp.txt →Delete 2 line
Sed  ‘1d; $d ‘ emp.txt  →Delete 1 and last line
Sed  ‘1,5 d’ emp.txt →Delete the line range from 1 to 5.




i) $sed “s/Unix/Linux/gi “madhav: -------------→ ‘i ‘for case sensitive
ii) $sed “s/^Unix/Linux/gi”----------------------→ whatever lines starting with UNIX are replaced by Linux
iii) $sed “s/^$/I like Unix/g I” sample--------→empty string are filled with ‘I like UNIX’’
iv) $Sed “s/Unix//g I” sample-----------------→it search UNIX if found replace with ‘nothing’ (empty)
42. tr			: to translate a charctor
i) tr “a” “p” <s--------------------→ it read data from sample and ‘a’ is replaced by ‘p’
ii) tr “aeiou” “AEIOU”<sample----→replace char by char
iii) tr “,” “lt” <emp----------------→whenever “,” is there replace with tab space
          iv) tr “[a-z]” “[A-Z] <Siva--------→ converts hole file into uppercase
43) Cut   	: it is used for to retrieve required fields and characters from a given file
Ex: madhav is good boy--→18 chars
Cut –f 2-5 madhav---→o/p: adha
Cut –c 1-10 madhav
Cut –c 5-10, 15-20 madhav-------→for every line 5-10, 15-20 characters
Cut –c 1,2,3 emp.txt →Prints 1,2 and 3rd char of each line
Cut –c 1-3,4-6 emp.txt → prints 1 to 3 and 4 to 6 character of each line
Cut –c10- emp.txt  →Print the lines from 10th to end position by using cut command
We can print the lines by using delimiter
Cut –d’,’ –f2 emp.txt →This will print the 2nd word of each line by taking ‘,’ as delimiter.
Cut –d’,’ –f2,3, emp.txt →This will print the 2nd and 3rd words of each line by taking comma as delimiter.

How to get the last field of a file.
Cat emp.txt| rev| cut –d’,’ –f2 |rev

44) Paste	: is used for to join two or more files horizontally by using delimiter
Cat >states					cat >cities            paste –d “:”states cities>tr filename
AP						Hyderabad		AP: Hyderabad		
Tamilnadu					madras		Tamilnadu: madras
Karnataka					Bangalore		Karnataka: Bangalore 	
Kerala						Trivandrum
Maharashtra					Bombay
45) Sort	: it is used for to sort the file content. By default it sorts file contents based on ASCII values-→default is ascending
Sort sample
i) sort –r sample------→displays descending order
ii) sort –u sample-----→it displays unique lines in the given file
iii) sort –n file----→’N” numeric comparisons
iv) sort –nur file 
v) sort sample >temp
$mv temp sample
Sorting the data field by field
+pos--→starting field
-Pos--→ending field (optional)
i) Sort –f +pas1 –pas2 filename
ii) Sort –f +1 -3 filename-----→starting from end before 3
iii) Sort –fn +2 -3 file ------→it gives only numbers
46) Uniq	: it displays unique lines in the given file but the file contents should be in sort order
Ex:file1	i) $ uniq file                  ii) $uniq –u filename--→it eliminates duplicates Aaaaaa 
Aaaaaa	Aaaaaa			ccccc
Aaaaaa	cccccccc		          ddddd	
Ccccccc	dddddd			Ppppp	
Ddddd		hhhhhh			ttttttt		
Hhhhh		pppppp
Hhhhh		ttttttttt
Ppppp
Ttttttt
iii) $ Uniq –d filename----displays only duplicated lines   IV) uniq –c filename-----→it counts how many times lines duplicated
																			              Aaaaaa-----2
							    Cccccccc----1
V) $ uniq –u file >temp
$ mv temp filename
Delete duplicated lines from file			Ddddd-----1
							Hhhhhh---2
							Ppppp-----1
							Ttttttt-----1
47)piping(|)     : it is used for to combine 2 or more cmds |take left side o/p to right side cmd as i/p
i)  $who |wc –l---------→count total no of lines (files) in current directory
ii) $ ls|wc –l------------→displays total no of subdirectories in the current directory
iii) ls –l |grep “^d”----→displays total no of subdirectories who stats with line no‘d’
iV) $head -30 sample|tail +20 sample------→display the the lines from 20 to 30 from given file
v) $ grep UNIX stud | cut –f 2, 3|sort filename -----→display UNIX students names & ph no in ascending order
48) $tee		: it is used to for to write data to the file as well as to the screen
$grep UNIX stud | cut –f 2, 3 |sort |tee file1
49) Shell scripting:
It is group of UNIX commands and shell keywords
The main concept of shell scripting is to handle text files
I) Boune shell----→steave Bourne -----→$--------sh--- (sh as interpreter)
ii) Bash shell (borne again shell) ---same as above--→advanced version of Bourne is BASH (Linux default shell)
iii) Korn shell------David korn----$----------ksh (interpreter) ----→used as AIX default shell
Mostly used shell is korn shell it supports re usability, all shell designed on bourn shell
50) $ksh		: shift to korn shell
51) $echo $0	 	: it displays current child shell name
52) $alias   		 : it lists all alias names
53) Unalias alias names: to delete alias names
54) $ history		  : it displays the previously executed commands
55) Echo			: it display the string on screen (monitor)
File permissions:(xxx/xxx/xxx)
User/owner---permissions 	(first part)
Group permissions 		(second part)
Other permissions 		(third part)
+--- (add permissions to u/g/o but it does not delete exiting permission)
--- (deny permissions)
=---- (assign permissions (add permissions to u/g/o but it  delete exiting permission))
rw-/rw-/r-- ---------→Default permissions for regular files
rwx/rwx/r-x---------→default permission for directories
56) chmod		: it is used for to change file permissions
Syn: $chmod who/ [+/-/=]/
i) ls –l filename-------→rw- rw-   r—
ii) chmod g+x filename-----→rw- rwx  r—
iii) chmod u+x, g-w filename------→rwx r-x r—
iV) chmod g=w filename-----→rwx –w- r—
Octal code
Read------4
Write-----2
Execute—1
$chmod 756 filename-------→rwx r-x rw-
$chmod 642 filename----→rw- r--  -w-
57) chown	  : to change owner name of the file
#chown owner name filename
58) chgrep  	: to change group name of the file
# chgrp group name filename
58) $write	 : it is user for to with the users but the user shxould be logged into the server
	$write techno2		ii) $mesg n--→deny the msg
	Hello 			iii) mesg y-→to allow msges
	Cmtl+d
59) awk/nawk file		: scan for patterns in a file and process the results
60) cat 			: concatenate (list) or file
61) chsh (paawd –e/-s) userlogin_shell: change the user login shell
62) df				: report the summary of disk blocks and nodes free and in use
      	 i) df –k---→it displays the disk space in bytes
      	ii) df –h---→it displays disk space in kilo bytes
     	 iii) df –g---→it displays the disk space in giga bytes
63)du  :it displays the directory wise disk usage in form of blocks each block size is 512 bytes
64)g zip  		:to create a zip file
Ex $gzip filename----→o/p: filename.gz
To Create multiple Zip files to a single Zip file we use below command
>Zip myzip.zip emp*.txt
The above command will zip all the files to Myzip.zip and we can get all files starting with emp.
65) gunzip	 	: to unzip the files
Ex: gunzip filename.gz
66. compress	: it also used for to zip the file---→it used to save with .z format
67) Uncompress	: same as above
Gzip saves more memory than compress
68) zcat 		: it used to displays zip file contents in readable format
$zcat sample.gz

Or
$zcat sample.z
69) To kill foreground job cntl+c or cntl+z
$ sleep 500
Cntl+c
$ sleep 100&
70) ps or $ ps –f   : it displays current user account running process list (show status of active process)
71) $ps –a: it displays all user accounts running process list
72) Kill		     : it kill background process
Ex: kill PID
73) telnet    	     : to connect to remote server
74) ftp: file transfer protocol -----→transfer files from one server to another
    $ ftp ipaddress
Login: -------
Password: ------
Ftp>ls  (server)
Ftp>|ls(client)
Ftp>get filename (to download a file)
Ftp>mget file1 file2----- (to download multi files)
Ftp>put filename (to upload a file)
Ftp>mput file1 file2----- (to upload multi files)
75)Ftp: to transfer files from one server user account to another server user account
   $su root --→to switch to admin
76) Wall  		 : it is used for to sent broadcast message to all users who are currently working on server
$wall
Happy new-year
Cntl+d
77)mail 	:it is used for to send the mail, if user is not logged in then also we can send mail
i) $ mail techno1
Cntl+d every user contains mailbox
at a time we can send msg to multiple users
2) $mail techno1 techno2 techno 3
Sub: from techno
Cntl+d
iii) $ mail techno<stud
stud send content as a mail to techno3
mail is the cmd to read mails in the mailbox
$mail
1>first mail
2>second mail reading
&2 it quickly opens second mail
&q--→quit from mail box
&w to save mail contents to a file
&p→print mail contents
&r--→replays
&d-→delete mails
78)$mail –f:to read mails send to secondary mailbox
79) emacs	:full screen editor
80) echo	: echo the text string to on monitor
81) file 	: classify the file type
82) expr	: evaluates the arguments, used to do arithmetic,etc in the shell
83) find 	 : find files, matching a type or pattern
84) Hostname 	: display or set the name of the current machine
85)ln			: link the source to target
86)lpq	,lpstat		:show the status of the print jobs
87)lpr,lp  		:print to defind printer
88) lprm, cancel	: remove a print job from the print quee
89) man		:display manual of given cmd
90)od			:octal dump a binary file,in octal,ASCII,hex,decimal or char
91)passwd		:to set or change password
92) pr			: filter the file and print it on the terminal
93) rcp hostname	: remotely copy files from this machine to another machine
94) rlogine hostname: login remotely to another machine
95) rsh hostname	: remote shell to run on another machine
96) script file		: saves everything that appears on the screen to file until exit is executed
97) source file		: read cmds from the file and execute them in the current shell
98) string file			: used to search binary files for ASCII strings
99) Sty				: set or display terminal control options
100) uudecode file			: decode a uuencoded file, recreating the original file
101) uuencode new name		: encode the binary file to 7-bit ASCII,usefull when sending via email, to be Decode as new name at destination
102) vi			: visual ,full screen editor
103) jobs		: display background and suspended processes
104) kill %1		: remove suspended process #1
105) top 		: display the current, most computer-intensive commands
106) osview		: display the operating system statistics
107) setenv		: list environmental variables


UNIX


What is meant by passwd file?
This file maintains each and every user information with 7 fields. The 7 fields are Username: passwd: uid: gid: fullname: home: shell.
What is Shell?
Shell is a command line interpreter. Shell acts as an interface between user and the kernel.
What is Kernel?
Kernel is core part of  UNIX o/s. It is a group of hundreds of system calls.
What are different flavors of Unix o/s?
Any operating system designed based on unix kernel called as flavour of unix. The following are some flavours of unix
Linux ---- Red Hat
Sun solaris --- Sun Microsystem
IBM-AIX ----- IBM
Hp-ux ----- HP
Sco-unix ----- santa crus operations
IRIX------ Silicon Graphics.

What are the different security features in Unix?

 	1. Password protection.
	2. File permissions.
	3. Encryption.

What’s the command to find out today’s date? 
 date


What’s the command to find out users on the system? 
 who


How do you find out the current directory you’re in?
pwd


What is the command to see the location of command?
Where is  <command name>
How do you find out your own username?  
Whoami    (or) log name


How to close the current user account?
Exit

How to create empty file?
Touch <filename>
How do you remove a file? 
 Rm <filename>
How to join multifile files vertically?
Cat   file1 file2 file3 ……	
The file for which we do not have write permission can be deleted using the command?
rm -f  <filename>
How do you remove a directory and its subdirectories?
 rm –rf <directoryname>
How to rename a file?
Mv <filename>
How to copy multiple files and directories into some other directory?
cp -r source_directory destination_directory
How to see hodden files?
Ls –a
How to see files and subdirectories files recursively?
Ls –R
How to see files in long list format page wise?
Ls –l | more
How to identify whether a file is normal file or directory? 
$ls -l filename/directoryname
if the first digit is - then it is file,
if it is d then it is directory file

What is the difference between "ls -r" and "ls -R"?

 ls -r lists the files in reverse alphabetical order... whereas ls -R lists the files and directories recursively

The difference between a soft link and a hard link?
A symbolic (soft) linked file and the targeted file can be located on the same or different file system while for a hard link they must be located on the same file system.


what are the different commands used to create files?
1.touch - to create empty files (e.g) - touch <filename>
2.vi <filename>
3. cat>filename

List some wild card characters?
? -→ Iit matches any single character
* -→ It matches zero or more characters
[] -→ It matches any single character in given list
. -→ It matches any single character except enter key character
what is the output of the follwing command : ls [a-mno-r]* 

list all the files in the current directory starting alphabet
is between a to m  or n or between o to r
How do you count words, lines and characters in a file? 
 Wc <filename>
which command is used to identify the type of the file?
file
"grep" means 
Globally search a regular expression and print it

How do you search for a string inside a given file? 
 grep string filename
How do you search for a string inside a  current directory? 
 grep string *

How do you search for a string in a directory with the subdirectories recursed?
 grep -r string *
Difference between grep, egrep and fgrep

grep : does not accept more then one expression

egrep : accepts more than one pattern for search. Also accepts patterns from a file.

fgrep : accepts multiple patterns both from command line and file but does not accept regular expressions only strings. It is faster than the other two and should be used when using fixed strings.

What are line patterns?
^ -→ start of the line
$ -→ End of the line

How to search empty lines in a given file?
Grep “^$” <filename>

How to count no of blank lines in a file?
Grep –c “^$” <filename>
How to remove Empty lines form a given file?
Grep –v “^$”  filename > temfilename
Mv  tempfilename  filename
What is pattern to search 4 digit word in a file?
Grep “\<[0-9] [0-9] [0-9] [0-9]\>” filename
What is pattern to search the line having only three characters?
Grep “^…$” filename
What is pattern to display lines ending with “$” character in a given file?
Grep “\$$” filename

How to display 2 and 4 th fileds from a given file if the delimetr is “:”?
Cut –d”:” –f  2,4 filename
How to display unique lines from a given file?
Sort –u filename
How to eliminate completely duplicate lines from a given file?
Uniq –u filename
How to remove all duplicate lines from a file?
Uniq –u filename > tempfilename
Mv  tempfilename  filename
How to delete “hello” word from a given file?
Sed “s/hello//” filename
awk Command
awk is a powful Unix command. It allows the user to manipulate files that are structured as columns of data and

Once you understand the basics of awk you will find that it is surprisingly useful. You can use it to automate things in ways you have never thought about. It can be used for data processing and for automating the application of Unix commands. It also has many spreadsheet-type functionalities. 
There are two ways to run awk. A simple awk command can be run from the command line. More complex tasks should be written as awk programs ("scripts") to a file. Examples of each are provided below. 
Example: % awk 'pattern {action}' input-file > output-file
meaning: take each line of the input file; if the line contains the pattern apply the action to the line and write the resulting line to the output-file.
If the pattern is omitted, the action is applied to all lines:

How to compare two files are same or not?
Cmp
How to display the first 10 lines from a file?
Head  -10  filename
Write a one line command to convert all the capital letters of a file "test" into lower case?
	cat filename | tr "[A-Z]"  "[a-z]"

The pipeline to list the five largest files in the current directory is

 ls -l | tr -s ' ' | sort -t ' ' -fnr +4 -5 | head –5

The pipeline to find out the number of times the character ? occurs in the file is 
 tr -dc '?' < file | wc -c   ( Delete all the characters except ? and then make a word count.)

How to count total no. of users working in the system?
Who | wc –l

How to display the lines from 5 to 10 from a given file?
Head -10 filename | tail +5

what will be output of following command?
echo “Tecnosoft” | wc –c
9

What is the default umask?
022
What is the default permission for File & Directory ?
The Default privileges for file : 644 
The default privileges for directory :  755
What UNIX command will control the default file permissions when files are created?
Umask

Explain the read, write, and execute permissions on a UNIX directory.

Read allows you to see and list the directory contents.

Write allows you to create, edit and delete files and subdirectories in the directory.

Execute gives you the previous read/write permissions plus allows you to change into the directory and execute programs or shells from the directory.


What is chmod, chown and chgrp?
Chmod : It is used for to change permissions on files
Chown : It is used for to change ownership of a file
Chgrp : It is used for to change group of the file
If the owner doesn’t have write permission on a file, but his/her group has, can he/she edit it?
 No. He/she can't,because the owner's permission overrides the group's.
To see list of files and directories ,what permission required?
Read permission

What are PIDs? 
They are process IDs given to processes. A PID can vary from 0 to 65535.


How do you list currently running process? 
 ps


How do you stop a background process? 
 kill pid
How do you find out about all running processes? 
 ps -ag
How do you stop all the processes, except the shell window? 
 kill 0
How do you fire a process in the background?
 ./process-name &
What does the command "kill -9 $! " do?
kills the last background process

if there is a process u want to run even after exiting the shell what is the 
command used?
Nohup

 which command will get executed even after you log out?
 Nohup

which signal cannot be trapped?
kill –9

How to redirect standard error to a file? Answer
2> filename
What does the top command display?
top command displays the current ammount of memory occupied 
by the currently executing processes and the details. In addition to memory usage top command displays cpu usage and process details

What is the command to send message to all users who are logged in?
Wall

What is the command to send mail to other user?
Mail username
How to open secondary mail box?
Mail -f
What do you do if you don't want to be interrupted by other users' messages?
Ans. mesg n

Shell Scripting Interview questions

Difference between the output of echo ** and echo * *
echo ** lists all the filenames in the current directory..
echo * * lists all the filenames in the current directory twice.

The other way of running shell script apart from using sh command and chmod?

ans:- using ! we can run a shell script


19. How do you refer to the arguments passed to a shell script? - $1, $2 and so on. $0 is your script name.
20. What’s the conditional statement in shell scripting? - if {condition} then … fi
21. How do you do number comparison in shell scripts? - -eq, -ne, -lt, -le, -gt, -ge
22. How do you test for file properties in shell scripts? - -s filename tells you if the file is not empty, -f filename tells you whether the argument is a file, and not a directory, -d filename tests if the argument is a directory, and not a file, -w filename tests for writeability, -r filename tests for readability, -x filename tests for executability
23. How do you do Boolean logic operators in shell scripting? - ! tests for logical not, -a tests for logical and, and -o tests for logical or.
24. How do you find out the number of arguments passed to the shell script? - $#
25. What’s a way to do multilevel if-else’s in shell scripting? - if {condition} then {statement} elif {condition} {statement} fi
26. How do you write a for loop in shell? - for {variable name} in {list} do {statement} done
27. How do you write a while loop in shell? - while {condition} do {statement} done
28. How does a case statement look in shell scripts? - case {variable} in {possible-value-1}) {statement};; {possible-value-2}) {statement};; esac
29. How do you read keyboard input in shell scripts? - read {variable-name}
30. How do you define a function in a shell script? - function-name() { #some code here return }
31. How does getopts command work? - The parameters to your script can be passed as -n 15 -x 20. Inside the script, you can iterate through the getopts array as while getopts n:x option, and the variable $option contains the value of the entered option.

Batch file:
Batch files allow MS-DOS and Microsoft Windows users to create a lists of commands to run in sequence once the batch file has been executed. For example, a batch file could be used to run frequently run commands, deleting a series of files, moving files, etc. A simple batch file does not require any special programming skills and can be done by users who have a basic understanding of MS-DOS commands. 


ORACLE9i FAQ’s


1.	WHAT IS DATA OR INFORMATION?
Ans: The Matter that we feed into the Computer is called Data or Information.

2.	WHAT IS DATABASE?
Ans: The Collection of Interrelated Data is called Data Base.

3.	WHAT IS A DATABASE MANAGEMENT SYSTEM (DBMS) PACKAGE?
Ans: The Collection of Interrelated Data and some Programs to access 
the Data is Called Data Base Management System (DBMS).

4.	WHEN CAN WE SAY A DBMS PACKAGE AS RDBMS?
Ans: For a system to Qualify as RELATIONAL DATABASE MANAGEMENT system, 
it must use its RELATIONAL facilities to MANAGE the DATABASE.

5.	WHAT IS ORDBMS?
Ans: Object (oriented) Relational Data Base Management System is one 
that can store data, the relationship of the data, and the behavior of the data 
(i.e., the way it interacts with other data).

6.	NAME SOME CODD'S RULES.
Ans: Dr. E.F. Codd presented 12 rules that a database must obey if it 
is to be considered truly relational. Out those,  some are as follows
a)	The rules stem from a single rule- the ‘zero rule’: For a system to Qualify as RELATIONAL DATABASE MANAGEMENT system, it must use its RELATIONAL facilities 
to MANAGE the DATABASE.
b)	Information Rule: Tabular Representation of Information.
c)	Guaranteed Access Rule: Uniqueness of tuples for guaranteed accessibility.
d)	Missing Information Rule: Systematic representation of missing information as NULL   Values.
e)	Comprehensive Data Sub-Language Rule: QL to support Data definition, 
View definition, Data manipulation, Integrity, Authorization and Security.

7.	WHAT ARE HIERARCHICAL, NETWORK, AND RELATIONAL DATABASE MODELS?
Ans: a) Hierarchical Model: The Hierarchical Model was introduced in 
the Information Management System (IMS) developed by IBM in 1968. In this data is organized as a tree structure. Each tree is made of nodes and branches. 
The nodes of the tree represent the record types and it is a collection 
of data attributes entity at that point. The topmost node in the structure is called the root. Nodes succeeding lower levels are called children.

b) Network Model: The Network Model, also called as the CODSYL database 
structure, is an improvement over the Hierarchical mode, in this model concept of parent and child is expanded to have multiple parent-child relationships, i.e. any child can be subordinate to many different parents (or nodes). Data is represented by 
collection of records, and relationships among data are represented by 
links. A link is an association between precisely two records. Many-to-many relationships can exists between the parent and child.

c) Relational Model: The Relational Database Model eliminates the need 
for explicit parent-child relationships. In RDBMS, data is organized in two-dimensional tables consisting of relational, i.e. no pointers are maintained between tables.

8.	WHAT IS DATA MODELING?
Ans: Data Modeling describes relationship between the data objects. The 
relationships between the collections of data in a system may be graphically represented using data modeling.



9.	DEFINE ENTITY, ATTRIBUTE AND RELATIONSHIP.
Ans: Entity: An Entity is a thing, which can be easily identified. An entity is any object, place, person, concept or activity about which an enterprise records data.
Attribute: An attribute is the property of a given entity.
Relationship: Relationship is an association among entities.

10.	WHAT IS ER-MODELING?
Ans: The E-R modeling technique is the Top Down Approach. Entity 
relationship is technique for analysis and logical modeling of a system’s data requirements. It is the most widely used and has gained acceptance as the ideal database design. It uses three basic units: entities, their attributes and the relationship that exists between
 the entities. It uses a graphical notation for representing these.

11.	WHAT IS NORMALIZATION?
Ans: Normalization is a step-by-step decomposition of complex records 
into simple records.

12.	WHAT ARE VARIOUS NORMAL FORMS OF DATA?
Ans: The First Normal Form	1NF,
The Second Normal Form	2NF,
The Third Normal Form	3NF,
The Boyce and Codd Normal Form	BC NF.

13.	WHAT IS DENORMALIZATION?
Ans: The intentional introduction of redundancy to a table to improve 
performance is called DENORMALIZATION.

14.	WHAT ARE 1-TIER, 2-TIER, 3-TIER OR N-TIER DATABASE ARCHITECTURES?
Ans: 1-Tier Database Architecture is based on single system, which acts 
as both server and client.
2-Tier Architecture is based on one server and client. 
3-Tier Architecture is based on one server and client out that on 
client act as a remote system.
N-Tier Architecture is based on N no. Of servers and N no. Of clients.

15.	WHAT ARE A TABLE, COLUMN, AND RECORD?
Ans: Table:  A Table is a database object that holds your data. It is 
made up of many columns. Each of these columns has a data type associated with it.
Column: A column, referred to as an attribute, is similar to a field in 
the file system.
Record: A row, usually referred to as tuple, is similar to record in 
the file system.

16.	WHAT IS DIFFERENCE BETWEEN A PROCEDURAL LANGUAGE AND A 
NON-PROCEDURAL LANGUAGE?
Ans:
Procedural Language	NON-Procedural Language
A program in this implements a step-by-step algorithm to solve the 
problem. It contains what to do but not how to do .

17.WHAT TYPE OF LANGUAGE  "SQL" IS?
Ans: SQL is a Non-procedural, 4th generation Language,/ which concerts 
what to do rather than how to do any process. 

18.	CLASSIFICATION OF SQL COMMANDS?
Ans:
DDL (Data Definition Language)	DQL [Data Querying Lnaguage ]
DML (Data Manipulating Language)	DCL (Data Control Language)	
TCL(Data Transaction Language) 



Create  Alter Drop Truncate Rename, Select , Insert  Update Delete Merge , Grant Revoke , Rollback Commit savepoint
 
19.	WHAT IS DIFFERENCE BETWEEN DDL AND DML COMMANDS?
Ans: For DDL commands autocommit is ON implicitly whereas For DML 
commands autocommit is to be turned ON explicitly.

20.	WHAT IS DIFFERENCE BETWEEN A TRANSACTION AND A QUERY?
Ans: A Transaction is unit of some commands where as Query is a single 
line request for the information from the  database.

21.	WHAT IS DIFFERENCE BETWEEN TRUNCATE AND DELETE COMMANDS?
Ans: Truncate Command will delete all the records where as Delete 
Command will delete specified or all the records depending only on the condition given.

22.	WHAT IS DIFFERENCE BETWEEN UPDATE AND ALTER COMMANDS?
Ans: Alter command is used to modify the database objects where as the 
Update command is used to modify the values of a data base objects.

23.	WHAT ARE COMMANDS OF DCL CATEGORY?
Ans: Grant and Revoke are the two commands belong to the DCL Category.
 
24.	WHICH IS AN EFFICIENT COMMAND - TRUNCATE OR DELETE? WHY?
Ans: Delete is the efficient command because using this command we can 
delete only those records that are not really required.

25.	WHAT ARE RULES FOR NAMING A TABLE OR COLUMN?
Ans: 1) Names must be from 1 to 30 bytes long.
2) Names cannot contain quotation marks.
3) Names are not case sensitive.
4) A name must begin with an alphabetic character from your database 
character set and the characters $ and #.
 But these characters are discouraged.
5) A name cannot be ORACLE reserved word.
6) A name must be unique across its namespace. Objects in the name 
space must have different names.
7) A name can be enclosed in double quotes.

26.	HOW MANY COLUMNS CAN A TABLE HAVE?
Ans: A Table can have 1000 columns.

27.	WHAT ARE DIFFERENT DATATYPES SUPPORTED BY SQL?
Ans: Char (size), Nchar (size), Varchar2 (size), Nvarchar2 (size) data 
types for character values,
Number (precision, scale), Number, Number (n), Float, Float (binary precision) data types for numerical values, Date data type for date values,
Long, Raw (size), Long Raw, Clob, Blob, Nclob, Bfile for large objects.

28.	WHAT IS DIFFERENCE BETWEEN LONG AND LOB DATATYPES?
Ans:
LOB	LONG
1) The maximum size is 4GB. 
2) LOBs (except NCLOB) can be attributes of an object type. 
3) LOBs support random access to data.
4) Multiple LOB columns per table or LOB attributes in an object type.	
1) The maximum size is 2GB.  2) LONGs cannot.    3) LONGs support only 
sequential access. 
4) Only one LONG column was allowed in a table





29.	WHAT IS DIFFERENCE BETWEEN CHAR AND VARCHAR2 DATATYPES?
Ans: Varchar2 is similar to Char but can store variable no. Of 
characters and while querying the table varchar2  trims the extra spaces from the column and fetches the rows that exactly match the criteria.

30.  HOW MUCH MEMORY IS ALLOCATED FOR DATE DATATYPE? WHAT IS DEFAULT 
DATE  FORMAT IN ORACLE?

Ans: For Date data type oracle allocates 7 bytes Memory. 
  Default Date Format is: DD-MON-YY.

31.	WHAT IS RANGE FOR EACH DATATYPE OF SQL?
Ans:
Datatype	Range
Char   Varchar2  Number    Float     LONG, RAW, LONGRAW  Large Objects 
(LOB’s) 2000 bytes  4000 bytes  
Precision 1 to 38 Scale -84 to 127  Precision 38 decimals Or 122 binary 
precision   2 GB  4GB

32.	HOW TO RENAME A COLUMN?
Ans: We can’t rename a Column of a table directly. So we follow the 
following steps.
To Rename a Column:
a)	Alter the table specifying new column name to be given and data type.
b)	Then copy the values in the column to be renamed into new column.
c)	drop the old column.

33.	HOW TO DECREASE SIZE OR CHANGE DATATYPE OF A COLUMN?
Ans: To Decrease the size of a Data type of a column
i.	Truncate the table first.
ii.	Alter the table column whose size is to be decreased using the same 
name and data type but new size.

34.	WHAT IS A CONSTRAINT? WHAT ARE ITS VARIOUS LEVELS?
Ans: Constraint: Constraints are representators of the column to 
enforce data entity and consistency.There r two levels
1)Column-level constraints 2)Table-level constraints.
 
35.	LIST OUT ALL THE CONSTRAINTS SUPPORTED BY SQL.
Ans: Not Null, Unique, Check, Primary Key and Foreign Key or Referential Integrity.

36.	WHAT IS DIFFERENCE BETWEEN UNIQUE+NOT NULL AND PRIMARY KEY?
Ans: Unique and Not Null is a combination of two Constraints that can be present any number of times in a table and can’t be a referential key to any column of an another table where as Primary Key is single Constraint that can be only once for table and can be a referential key to a column of another table becoming a referential integrity.

37.	WHAT IS A COMPOSITE PRIMARY KEY?
Ans: A Primary key created on combination of columns is called Composite Primary Key.

38.	WHAT IS A CANDIDATE COLUMN? HOW MANY CANDIDATE COLUMNS CAN BE 
POSSIBLE PER COMPOSITE PRIMARY KEY?
Ans: It is a part of composite primary key.  Maximum 32 candidate key can be there in composite primary key.
 
39.	HOW TO DEFINE A NULL VALUE?
Ans: A NULL value is something which is unavailable, it is neither zero 
nor a space and any mathematical calculation with NULL is always NULL.





40. WHAT IS NULL?  A CONSTRAINT OR DEFAULT VALUE?
Ans: It is a default value.

41. WHAT IS DEFAULT VALUE FOR EVERY COLUMN OF A TABLE?
Ans: NULL.

42. WHAT IS CREATED IMPLICITLY FOR EVERY UNIQUE AND PRIMARY KEY 
COLUMNS?
Ans: Index.

43. WHAT ARE LIMITATIONS OF CHECK CONSTRAINT?
Ans: In this we can't specify Pseudo Columns like sysdate etc.

44. WHAT IS DIFFERENCE BETWEEN REFERENCES AND FOREIGN KEY CONSTRAINT?
Ans: References is used as column level key word where as foreign key 
is used as table level constraint.

45. WHAT IS "ON DELETE CASCADE"?
Ans: when this key word is included in the definition of a child table 
then	 whenever the records from the parent table is deleted automatically the respective values in the child table will be deleted.

46. WHAT IS PARENT-CHILD OR MASTER-DETAIL RELATIONSHIP?
Ans: A table which references a column of another table(using References)is called  as a child table(detail table) and a table  which is being referred  is called Parent (Master) Table .

47. HOW TO DROP A PARENT TABLE WHEN IT’S CHILD TABLE EXISTS?
Ans: Using "on delete cascade".

48. IS ORACLE CASE SENSITIVE?
Ans: NO

49. HOW ORACLE IDENTIFIES EACH RECORD OF TABLE UNIQUELY?
Ans: By Creating indexes and reference IDs.

50. WHAT IS A PSEUDO-COLUMN? NAME SOME PSEUDO-COLUMNS OF ORACLE?
Ans: Columns that are not created explicitly by the user and can be 
used explicitly in queries  are called Pseudo-Columns.
Ex:currval,nextval,sysdate,new,old,sqlcode,sqlerrm,rownum,rowid,level

51. WHAT FOR "ORDER BY" CLAUSE FOR A QUERY?
Ans: To arrange the query result in a specified 
Order (ascending,descending) by default it takes ascending order.

52. WHAT IS "GROUP BY" QUERIES?
Ans: To group the query results based on condition.

53. NAME SOME AGGREGATE FUNCTIONS OF SQL?
Ans: AVG, MAX, SUM, MIN,COUNT.

54. WHAT IS DIFFERENCE BETWEEN COUNT (), COUNT (*) FUNCTIONS?
Ans: Count () will count the specified column whereas count (*) will 
count total no. of rows in a table.

55. WHAT FOR ROLLUP AND CUBE OPERATORS ARE?
Ans: To get subtotals and grand total of values of a column.

56. WHAT IS A SUB-QUERY?
Ans: A query within a query  is called a sub query where the result of 
inner query will be used by the  outer query.



57. WHAT ARE SQL OPERATORS?
Ans: Value (), Ref () is SQL operator. ( Used with Objects )

 58. EXPLAIN "ANY","SOME","ALL","EXISTS" OPERATORS?
  Ans: Any: The Any (or it’s synonym SOME) operator computes the lowest 
value from the set and compares a value to each returned by a sub query.

All: ALL compares a value to every value returned by SQL.
Exists: This operator produces a BOOLWAN results. If a sub query 
produces any result then it evaluates it to TRUE else it evaluates it to FALSE.

59. WHAT IS A CORRELATED SUB QUERY, HOW IT IS DIFFERENT FROM A NORMAL 
SUB QUERY?
Ans: A correlated subquery is a nested subquery, which is executed once 
for each ‘Candidate row’ by the main query, which on execution uses a value from a column in the outer query. In normal sub query the result of inner query is dynamically substituted in the condition of the outer query where as in a correlated subquery, the column 
value used in inner query refers to the column value present in the 
outer query forming a correlated subquery.

 60. WHAT IS A JOIN - TYPES OF JOINS?
Ans: A join is used to combine two or more tables logically to get 
query results. 

    There are four types of Joins namely 
     EQUI Join
     NON-EQUI Join
     SELF Join 
     OUTER Join.

  61. WHAT ARE MINIMUM REQUIREMENTS FOR AN EQUI-JOIN?
Ans: There shold be atleast one common column between the joining tables.

  62. WHAT IS DIFFERENCE BETWEEN LEFT, RIGHT OUTER JOIN?
Ans:If there r any values in one table that do not have corresponding values in the other,in an equi join that row will not be selected.Such rows can be forcefully selected by using outer join symbol(+) on either of the sides(left or right)  based on the requirement.  

  63. WHAT IS DIFFERENCE BETWEEN EQUI AND SELF JOINS?
Ans: SELF JOIN is made within the table whereas 
     EQUI JOIN is made between  different tables having common column.

  64. WHAT ARE "SET" OPERATORS?
Ans: UNION ALL,UNION, INTERSECT ,MINUS are SET OPERATORS.

  65. WHAT IS DIFFERENCE BETWEEN "UNION" AND "UNION ALL" 
OPERATORS?
Ans: UNION will return the values distinctly whereas UNION ALL will 
return even duplicate values. 

  66. NAME SOME NUMBER, CHARACTER, DATE, CONVERSION, OTHER 
FUNCTIONS.
Ans: Number Functions:
                Round (m, [n]),  Trunc (m, [n]),  Power (m, n),  Sqrt(n), 
                Abs (m), Ceil (m),  Floor (m), Mod (m, n) ,sign(n)                                 

      Character Functions: 
                Chr (x), Concat (string1, string2), Lower (string)
                      Upper (string), Substr (string, from_str, to_str), ASCII (string)
                      Length (string), Initcap (string).  

    

  Date Functions: 
                 Sysdate, Months between (d1, d2), To_char (d, format)
                 Last day (d), Next_day (d, day).add_months(d,n), Extract
      Conversion Functions:     To_char,  To_date, To_number

  67. WHAT IS DIFFERENCE BETWEEN MAX () AND GREATEST () FUNCTIONS?
Ans: MAX is an aggregate function which takes only one column name of a table as parameter whereas Greatest is a general function which can take any number of values and column names from dual and table respectively.

  68. WHAT FOR NVL () FUNCTION IS?
Ans: NVL Function helps in substituting a value in place of a NULL.

  69. WHAT FOR DECODE () FUNCTION IS?
Ans: It is substitutes value basis and it actually does an 
'if-then-else' test.

  70. WHAT IS DIFFERENCE BETWEEN TRANSLATE () AND REPLACE () FUNCTIONS?
Ans: Translate()   is a superset of functionality provided by Replace().

  71. WHAT IS DIFFERENCE BETWEEN SUBSTR () AND INSTR () FUNCTIONS?
Ans: Substr() will return the specified part of a string whereas 
   
  Instr() return the position of the specified part of the string.

  72. WHAT IS A JULIAN DAY NUMBER?
Ans: It will return count of the no. Of days between January 1, 4712 BC 
and the given date.

  73. HOW TO DISPLAY TIME FROM A DATE DATA?
Ans: By using time format as 'hh [hh24]: mi: ss' in to_char() function.

  74. HOW TO INSERT DATE AND TIME INTO A DATE COLUMN?
Ans: By using format 'dd-mon-yy hh [hh24]: mi: ss' in to_date() function.

  75. WHAT IS DIFFERENCE BETWEEN TO_DATE () AND TO_CHAR () CONVERSION 
FUNCTIONS?
Ans: To_date converts character date to date format whereas 
     To_char function converts date or numerical values to characters.

  76. WHAT IS A VIEW? HOW IT IS DIFFERENT FROM A TABLE?
Ans: View is database object, which exists logically but contains no 
physical data and manipulates the base table. 
View is saved as a select statement in the database and contains no 
physical data whereas Table exists physically.

  77. WHAT IS DIFFERENCE BETWEEN SIMPLE AND COMPLEX VIEWS?
Ans: Simple views can be modified whereas Complex views (created based 
on more than one table) cannot be modified.

  78. WHAT IS AN INLINE VIEW?
Ans: Inline view is basically a subquery with an alias that u can use 
like a view inside a SQL statement. It is not a schema object like SQL-object.

  79. HOW TO UPDATE A COMPLEX VIEW?
Ans: Using  'INSTEAD OF' TRIGGERS Complex views can be Updated.

  80. WHAT FOR "WITH CHECK OPTION" FOR A VIEW?
Ans: "WITH CHECK OPTION" clause specifies that inserts and updates r performed through the view r not allowed to create rows  which the view cannot select and therefore allows integrity constraints and data validation checks to be enforced on data being inserted or updated.

81. WHAT IS AN INDEX? ADVANTAGE OF AN INDEX
Ans: An Index is a database object used n Oracle to provide quick 
access to rows in a table. An Index increases the performance of the database.

  82. WHAT IS A SEQUENCE? PSEUDO-COLUMNS ASSOCIATED WITH SEQUENCE? 
Ans: Sequence is a Database Object used to generate unique integers  to use as primary keys. Nextval, Currval are the Pseudo Columns associated with the sequence.

**83. WHAT IS A CLUSTER? WHEN TO USE A CLUSTER? HOW TO DROP A CLUSTER 
WHEN CLUSTERED TABLE EXISTS?
Ans: Cluster and Indexes are transparent to the user. Clustering is a 
method of storing tables that are intimately related and are often joined together into the same area on the disk. 
When cluster table exists then to drop cluster we have to drop the table first then only cluster is to be dropped.

  84. WHAT IS A SNAPSHOT OR MATERIALIZED VIEW?
Ans: Materialized views can be used to replicate data. Earlier the data 
was replicated through CREATE SNAPSHOT command. Now CREATE MATERIALIZED VIEW can be used as synonym for CREATE SNAPSHOT. Query performance is improved using the materialized view as these views pre calculate expensive joins and aggregate operations on the table.

85. WHAT IS A SYNONYM?
Ans:  A Synonym is a database object that allows you to create alternate names for Oracle tables and views. It is an alias for a table, view, snapshot, sequence, procedure, function or 
package.

  86. WHAT IS DIFFERENCE BETWEEN PRIVATE AND PUBLIC SYNONYM?
Ans: Only the user or table owner can reference Private synonym whereas 
any user can reference the Public synonym.

  87. WHAT IS DIFFERENCE BETWEEN "SQL" AND "SQL*PLUS" COMMANDS?
Ans:  SQL commands are stored in the buffer whereas SQL*PLUS are not.

**88. NAME SOME SQL*PLUS COMMANDS?
Ans:	DESC [CRIBE], START, GET, SAVE, / are SQL*PLUS COMMANDS.

  89. WHAT ARE "SQL*PLUS REPORTING" COMMANDS?
Ans: SPOOL file-name, SPOOL OFF, TTITLE, BTITLE, BREAK ON, COMPUTE <any 
aggregate function> OF <column name> [break] ON <column name> etc are SQL*PLUS REPORTING COMMANDS. 

  90. WHAT ARE SYSTEM AND OBJECT PRIVILEGES?
Ans: Connect and Resource etc are System Privileges. 
Create <object>, Select, Insert, Alter etc are Object Privileges.
	
  91. WHAT FOR DCL COMMANDS ARE?
Ans: Commit, Rollback are DCL commands.

  92. WHAT FOR GRANT COMMAND WITH "WITH GRANT OPTION"?
Ans: “With Grant Option” with Grant Command gives privileges to the 
user to grant privileges to other user(s) 
among the privileges he/she has.

  93. HOW TO CHANGE PASSWORD OF A USER?
Ans: Using Password command or 
Using ALTER USER <user name> IDENTIFIED BY <new password> COMAND.

94. WHAT IS A SCHEMA AND SCHEMA OBJECTS?
Ans: A schema is a collection of logical structures of data, or schema 


objects. A schema is owned by the database user and has the same name as that of user. Each user owns a single schema. Schema objects include following 
type of objects Clusters, Database Links, Functions, Indexes, Packages, 
Procedures, Sequences, Synonyms, Tables, Database Triggers, Views.

  **95. HOW TO STARTUP AND SHUTDOWN ORACLE DATABASE?
Ans: Startup and Shutdown Oracle database can be done by only the 
administator. Startup is done by using STARTUP command and Shutdown is done by SHUTDOWN command 

  96. WHAT IS A SESSION?
Ans: The period between Login and Logoff on schema.

  97. WHAT IS A CLIENT PROCESS? WHAT IS A SERVER PROCESS?
Ans: ref: 172 Q & A.

  98. HOW TO MAKE EVERY DML OPERATION AS AUTO COMMIT?
Ans: By using SET AUTOCOMMIT ON command.

  99. HOW TO DISPLAY DATA PAGE WISE IN SQL?
Ans: By using SET PAUSE ON command.

100. HOW TO CHANGE LINE SIZE, PAGE SIZE AND SQL PROMPT?
Ans: By using SET LINESIZE <value>, SET PAGESIZE <value>, 
     SET SQLPROMPT <new prompt>.

101. HOW PL/SQL IS DIFFERENT FROM SQL?
Ans: SQL is non-procedural language whereas PL/SQL is procedural 
language that includes features and design of programming language.

102. WHAT IS ARCHITECTURE OF PL/SQL?
Ans:   Give picture & Explain

103. WHAT IS A PL/SQL BLOCK?
Ans:	DECLARE 
	   <declarations>
	BEGIN
	   <Exececutable Statements>
	EXCEPTION
	   <Exception Handler(s)>
	END;

104. WHAT ARE DIFFERENT TYPES OF PL/SQL BLOCKS?
Ans: DECLARE BLOCK: In this block all the declarations of the variable 
used in the program is made. If no variables are used this block will become optional.
          BEGIN BLOCK: In this block all the executable statements are 
          placed. This block is Mandatory.
          EXCEPTION BLOCK: In this block all the exceptions are handled. 
                     This block is also very optional.
          END: Every begin must be ended with this END; statement.
  Anonymous & Named Blocks

105. WHAT ARE COMPOSITE DATA TYPES?
Ans: Records, Tables are two Composite data types.

106. WHAT IS SCOPE OF A VARIABLE IN PL/SQL BLOCK?
Ans: The visuability and accessibility of a variable within the 
block(s) is called scope of a variable.

107. WHAT IS A NESTED BLOCK?
Ans: A block within a block is called Nested Block.


108. WHAT IS A PL/SQL ENGINE?
Ans:  The PL/SQL engine accepts any valid PL/SQL block as input, executes the procedural part of the statements and sends the SQL statements to the SQL statement executor in the Oracle server.

109. WHAT IS DEFAULT VALUE FOR A NUMERIC PL/SQL VARIABLE?
Ans: NULL

110. WHAT IS DIFFERENCE BETWEEN SIMPLE LOOP AND A FOR LOOP?
Ans: Simple requires declaration of variables used in it and exit 
condition but For Loop doesn’t require this.

111. WHAT IS A CURSOR? STEPS TO USE A CURSOR?
Ans: Cursor is Private SQL area in PL/SQL. 
     Declare the Cursor,
     Open the Cursor, 
     Fetch values from SQL into the local Variables, 
     Close the Cursor.

112. HOW MANY TYPES OF CURSORS ARE SUPPORTED BY ORACLE?
Ans:  There are two types of cursors namely Implicit Cursor, Explicit Cursor.

113. WHAT IS A CURSOR FOR LOOP?
Ans: Cursor For Loop is shortcut process for Explicit Cursors because 
the Cursor is Open, Rows are fetched once for each iteration and the cursor is closed automatically when all the rows have been processed.

114. WHAT ARE CURSOR ATTRIBUTES?
Ans: %Found
     %NotFound
     %IsOpen
     %RowCount are the cursor attributes.

115. WHAT IS USE OF CURSOR WITH "FOR UPDATE OF" CLAUSE? 
Ans: This Clause stop accessing of other users on the particular 
columns used by the cursor until the COMMIT is issued.

116. WHAT IS AN EXCEPTION? HOW IT IS DIFFERENT FROM ERROR?
Ans: Whenever an error occurs Exception raises. Error is a bug whereas the Exception is a warning or error condition.

117. NAME SOME BUILT-IN EXCEPTIONS.
Ans: Too_Many_Rows,  No_Data_Found,   Zero_Divide,    Not_Logged_On
     Storage_Error,    Value_Error etc.

118. HOW TO CREATE A USER-DEFINED EXCEPTION?
Ans: User-Defined Exception is created as follows:
      DECLARE
	<exception name> EXCEPTION;
	- - - - - - - - - ;
 	- - - - - - - - -;
	BEGIN
 	- - - - - - - - -;
 	- - - - - - - - -;
	RAISE <exception name>;
	EXCEPTION
	WHEN <exception name> THEN
 	- - - - - - - - -;
 	- - - - - - - - -;
	END;



119. WHAT IS "OTHERS" EXCEPTION?
Ans: It is used to along with one or more exception handlers. 
     This will handle all the errors not already handled in the block.

120. WHAT IS SCOPE OF EXCEPTION HANDLING IN NESTED BLOCKS?
Ans: Exception scope will be with in that block in which exception 
handler is written. 

121. WHAT IS A SUB-PROGRAM?
Ans: A SUBPROGRAM IS A PL/SQL BLOCK, WHICH WILL BE INVOKED BY TAKING 
PARAMATERS.

122. WHAT ARE DIFFERENT TYPES OF SUB-PROGRAMS?
Ans: THEY R TWO TYPES: 1) PROCEDURE 2) FUNCION. 

123. HOW A PROCEDURE IS DIFFERENT FROM A FUNCTION?
Ans: Function has return key word and returns a value whereas a 
Procedure doesn’t return any value.

124. WHAT ARE TYPES OF PARAMETERS THAT CAN BE PASSED TO FUNCTION OR 
PROCEDURE?
Ans: IN, IN OUT, OUT.

125. WHAT IS "IN OUT" PARAMETER?
Ans: A parameter, which gets value into the Procedure or Function and 
takes the value out of the Procedure or 
Function area, is called IN OUT parameter.

126. DOES ORACLE SUPPORTS PROCEDURE OVERLOADING?
Ans:  NO.

127. WHAT IS A PACKAGE AND PACKAGE BODY?
Ans: Package is declarative part of the functions and procedures stored 
in that package and package body is 
the definition part of the functions and procedures of that package.

128. WHAT IS ADVANTAGE OF PACKAGE OVER PROCEDURE OR FUNCTION?
Ans: Packages provides Functions or Procedures Overloading facility and 
security to those Functions or 
Procedures.

129. IS IT POSSIBLE TO HAVE A PROCEDURE AND A FUNCTION WITH THE SAME 
NAME?
Ans: NO if it is out side a Package, YES if it is within a Package. 

130. DOES ORACLE SUPPORTS RECURSIVE FUNCTION CALLS?
Ans: YES.

131. WHAT IS A TRIGGER? HOW IT IS DIFFERENT FROM A PROCEDURE?
Ans: Trigger:  A Trigger is a stored PL/SQL program unit associated 
with a specific database table. 
     Procedure: A Procedure is to be explicitly called by the user 
whereas Triggers are automatically called implicitly 
    by Oracle itself whenever event Occurs.

132. WHAT IS DIFFERENCE BETWEEN A TRIGGER AND A CONSTRAINT?
Ans: Constraints are always TRUE whereas Triggers are NOT always TRUE 
and Constraints has some limitations whereas Trigger has no limitations.

133. WHAT ARE DIFFERENT EVENTS FOR A TRIGGER AND THEIR SCOPES?
Ans: Insert, Update or Delete.




134. WHAT IS DIFFERENCE BETWEEN TABLE LEVEL AND ROW LEVEL TRIGGERS?
Ans: Table level Triggers execute once for each table based transaction 
whereas Row level Triggers will execute once FOR EACH ROW.

** 135. WHAT ARE AUTONOMOUS TRIGGERS?
Ans: Supports to provide Commit statement in Triggers. Triggers a declared as independent
         Transactions.

136. WHAT IS AN "INSTEAD OF" TRIGGER?
Ans: These Triggers are used with the Complex Views only to make 
possible of Insert, Update and Delete on those Views.

** 137. HOW MANY TRIGGERS CAN BE CONFIGURED ON A TABLE AND VIEW?
Ans: 18 Triggers

138. WHAT IS "TABLE MUTATING" ERROR? HOW TO SOLVE IT?
Ans: ORA-04091:	Table name is mutating, trigger/function may not see it
Cause : A trigger or a user-defined PL/SQL function that is referenced 
in the statement attempted to query or modify a table that was in the middle of being modified by the statement that fired the trigger. 
Action : Rewrite the trigger or function so it does not read the table. 

139. WHEN TO USE ":NEW" AND ":OLD" SPECIFIERS?
Ans:  The prefix :old is used to refer to values already present in the 
table. The prefix :new is a correlation name that refers to the new value that  is inserted / updated.

** 141. HOW TO CREATE A USER-DEFINED VARIABLE IN PL/SQL?
Ans:  Define variable in declaration section

142. HOW TO CREATE AN ARRAY VARIABLE IN PL/SQL?
Ans: Using CREATE [OR REPLACE] TYPE <type name> 
AS VARRAY (size) OF ELEMENT_TYPE (NOT NULL) Command;  

**143. HOW TO MAKE A USER-DEFINED DATA TYPE GLOBAL IN PL/SQL? 
Ans: Declare the variable in a Package

144. HOW TO CREATE AN OBJECT IN ORACLE?
Ans: Using CREATE [OR REPLACE] TYPE <type name> AS OBJECT (ATTRIBUTE 
NAME DATA TYPE,..) Command   

145. WHAT IS A TRANSIENT AND PERSISTENT OBJECT?
Ans: The Object created in a table is called Persistent Object.
     Object created on execution of PL/SQL block is called Transient Object.

**146. WHAT IS A COLUMN OBJECT AND TABLE OBJECT?
Ans: A Column Object is only a Column of a table. 
   
147. HOW TO GRANT PERMISSION ON AN OBJECT TO OTHER USER?
Ans: GRANT <permission> ON <object name> TO <user name>.

148. WHAT IS A COLLECTION OF ORACLE?
Ans: Varray, Nested Table is a collection of Oracle.

149. WHAT IS DIFFERENCE BETWEEN VARRAY AND NESTED TABLE?
Ans: Varray has a fixed size.
     Nested tables can carry any number of values.




150. HOW TO MODIFY CONTENTS OF A VARRAY IN ORACLE?
Ans: To modify a stored VARRAY it has to selected into a
     PL/SQL variable and then inserted back into the table.

151. WHAT IS USE OF "THE" OPERATOR FOR NESTED TABLE?
Ans: THE operator allows nested tables to be manipulated using DML when 
it is stored in a Table.

152. WHICH PACKAGE IS USED FOR FILE INPUT/OUTPUT IN ORACLE?
Ans: UTL_FILE Package is used for File input/output in Oracle.

153. NAME SOME METHODS AND PROCEDURES OF FILE I/O PACKAGE?
Ans: FOPEN, FCLOSE,  FFLUSH, IS_OPEN, GET_LINE, PUT_LINE, PUTF, NEW_LINE
 
**154. WHAT IS SQLJ? HOW IT IS DIFFERENT FROM JDBC CONNECTIVITY?
Ans: SQLJ is basically a Java program containing embedded static SQL 
statements that are compatible with Java design philosophy.

155. WHAT IS AN ITERATOR? Name some TYPES OF ITERATORS?
Ans: SQLJ Iterators are basically record groups generated during 
transaction, which requires manipulation of more than one records from one or more tables. There are two types Iterators namely Named Iterator and Positional Iterator. 

** 156. WHAT ARE DIFFERENT STEPS TO WRITE A DYNAMIC SQL PROGRAM?
Ans:  Eg: char c_sqlstring[]={“DELETE FROM sailors WHERE rating>5”};
EXEC SQL PREPARE readytogo FROM :c_sqlstring;
EXEC SQL EXECUTE readytogo;

157. WHAT IS TABLE PARTITIONING AND INDEX PARTITIONING?
Ans: Oracle8 allows tables and Indexes to be partitioned or broken up into smaller parts based on range of key values. Partitioning is a “divide and conquer” strategy that improves administration and performance in data warehouse and OLTP systems.

159. WHAT IS PHYSICAL MEMORY STRUCTURE OF ORACLE?
Ans: The basic oracle memory structure associated with Oracle includes:
Software Code Areas The System Global Area (SGA) ,The Database Buffer Cache
The shared Pool, The Program Global Areas (PGA), Stack Areas ,Data Areas, Sort Areas

160. WHAT IS LOGICAL MEMORY STRUCTURE OF ORACLE?
Ans: Database, Tablespace , DB Object, Segment, Extents

161. WHAT IS SGA?
Ans: A System Global Area is a group of shared memory allocated by 
Oracle that contains data and control information for one Oracle database instance. IF the multiple users are concurrently connected to the same instance, the data in the instance’s SGA is “shared” among the users. 
Consequently, the SGA is often referred to as either the “system Global Area” or the “Shared 
Global Area”.

162. WHAT IS PGA?
Ans: The Program Global Area is a memory buffer that contains data and 
control information for a server process. A PGA is created by Oracle when a server process is started. The information in a PGA depends on the configuration of Oracle.

163. WHAT IS AN ORACLE INSTANCE?
Ans: Every time a database is started, an SGA is allocated and Oracle 
background processes are started. The combination of these processes and memory buffers is called an Oracle instance.

164. WHAT ARE DIFFERENT ORACLE PROCESSES?
Ans:  A process is a “thread of control” or a mechanism in an operating 
system that can be execute a series of steps. Some operating systems use terms jobs or 

task. A process normally has its own private memory area in which it runs. An Oracle database system has general types of process: User Processes and Oracle Processes.

**165. WHAT IS DIFFERENCE BETWEEN PMON AND SMON?
Ans: SMON (System Monitor) performs instance recovery at instance of 
startup. In a multiple instance system (one that uses the parallel server), SMON of one instance can also perform instance recovery other instance that have failed whereas The PMON (Process Monitor) performs process recovery when a user process fails. 

**166. WHAT IS DIFFERENCE BETWEEN DATABASE AND TABLESPACE? 
Ans:  Database is a physical Component
          Tablespace is a Logical component

167. WHAT IS JOB OF DATABASE WRITER (DBWR) PROCESS?
Ans: The Data Base Writer writes modified blocks from the database 
buffer cache to the data files.

168. WHAT IS JOB OF LOG WRITER (LGWR) PROC*SS?
Ans: The Log Writer writes redo log files to disk. Redo log data is 
generated in the redo log buffer of the SGA. As transactions commit and log buffer fills, LGWR writes redo entries into an online redo log file. 

169. WHAT IS RECOVERER?
Ans: The Recover (RECO) is used to resolve distributed transactions that are pending due to network or system failure in a distributed database. At timed intervals, the local RECO attempts to concept to remote database and automatically complete the commit or rollback of the local portion of any pending distributed transactions. 

170. WHAT IS ARCHIVER?
Ans:  The Archiver (ARCH) copies the online redo log files to archival storage when they are full. ,ARCH is active only when a database’s redo log is used ARCHILOG mode.

** 171. WHAT IS A STORED QUERY?
Ans: VIEW

172. WHAT IS USER PROCESS AND SERVER PROCESS?
Ans: A User process is created and maintained to execute the software 
code of an application program (such as PRO * Program) or an ORACLE tool (such as SQL * DBA). The User process also manages the communication 
with server processes. User processes communication with the server 
Processes through the program interface.

 Other processes call ORACLE processes. In a dedicated server 
configuration, a server Process handles requests for a single user process. A multithread 
server configuration allows many user processes to share a small number of server processes, minimizing the utilization of available system resources.

**173. WHAT IS A SELF REFERENTIAL INTEGRITY?
Ans: Table related to itself .Foreign key of the table links to primary  key of the same table.

174. WHAT IS A "RAISE" STATEMENT?
Ans: It is used to Raise Exceptions.

175. WHAT IS ROWID? HOW IT IS DIFFERENT FROM ROWNUM?
Ans: Rowid is the address of the row at where it is stored in the 
database. Rownum is count of records whereas Rowid is identification of the each row.


*** All The Best  -  SRIDHAR ***
9i features:

9i Joins:
Supports ANSI/ISO standard Sql 1999 syntax
Made easy for Appln s/w tools to understand Sql Queries
1. Natural Join		5. Left outer join
2. Join with Using	6. Right outer join
3. Join with ON		*7. Full outer join
4. Inner Join		8. Cross join

1. > select empno,ename,sal,job,deptno,dname,loc
       from emp natural join dept;

2. > select empno,ename,sal,job,deptno,dname,loc
       from emp join dept using(deptno);

3. > select e.empno, e.ename, e.sal, e.job, e.deptno,d.dname, d.loc from emp e Join dept d 
       on(e.deptno = d.deptno) ;

4. > select e.empno, e.ename, e.sal, e.job, e.deptno, d.dname, d.loc from emp e Inner Join dept d 
       on(e.deptno = d.deptno) ;

5. > select e.empno, e.ename, e.sal, e.job, e.deptno, d.dname, d.loc from emp e left outer join dept d 
      on(e.deptno = d.deptno) ;

6. > select e.empno, e.ename, e.sal, e.job, e.deptno,d.dname, d.loc from emp e right outer join dept d 
      on(e.deptno = d.deptno) ;

* 7. > select e.empno, e.ename, e.sal, e.job, e.deptno,d.dname, d.loc from emp e full outer join dept d 
          on(e.deptno = d.deptno) ;
** left outer join  union  right outer join  =  full outer join

8. > select empno,ename,sal,job,deptno,dname,loc
       from emp cross join dept;
----------------------------------------------------------------------------
New Date Functions:

* Systimestamp :  Gives date and time including fractional seconds in SERVER time zone
* current_timestamp:  Gives date and time including fractional seconds in CLIENT time zone
* sysdate:  Gives only date in server time zone
* current_date:  Gives only date in client time zone
* Extract : Used to retrieve a particular value from the given                 date   ( day / month / year ).
* to_timestamp(d) : Converts given date into date & time                                   information with am / pm .
* dbtimezone : Gives server time zone value
* Timestamp : Data type
Automatically stores date and time  information with am / pm .

>select systimestamp , current_timestamp from dual;
>select sysdate,current_date from dual;
>select dbtimezone from dual;
>select to_timestamp(sysdate) from dual;
   20-jan-09 6:48:23 pm
>select extract(day from sysdate) ,
 extract(month from sysdate),
 extract(year from sysdate) from dual;

 create table temp (c1 timestamp);
> insert into temp values(sysdate);
> select * from temp;
 20-jan-09 6:52:23 pm
----------------------------------------------------------------------------
New General Functions:
* Coalesce(expr1,expr2,expr3,.......) --- Picks the first not null expression result .
*nullif ( expr1,expr2 ) --- If expr1 and expr2 results are same it returns NULL value otherwise it return expr1 result.
* Nvl2(expr1,expr2,expr3) --- If expr1 is null it manipulates expr3 ,if expr1 is not null it manipulates expr2.

>select coalesce(100 + null, 128 - null + 1000, 12 * null,
                       225, 2345,9889) from dual; -- 225

>select ename, job, coalesce (comm * 2, sal * 1.5) bonus
 from emp;

>select nullif(100,50* 2), nullif(300,30 * 100),
   nullif (600,300 + 300)  from dual; -- null 300 null

>select roll, name, nullif(fee,2500) from student
  where course = 'Oracle9i';

>select ename, job, nvl2(comm,sal + comm,sal) net from emp; 
 ---------------------------------------------------------------------------
Mutiple Inserts:
Supports to insert into more than 1 table at a time.
But input must be retrieved from existing table.

Ex: Make 3 empty tables same as Dept table.
Create table D1 as select * from dept 
where rownum is null;
Create table D2 as select * from dept
 where rownum is null;
Create table D3 as select * from dept 
where rownum is null;

insert into D1 select * from dept;
insert into D2 select * from dept;
insert into D3 select * from dept;

insert all
into D1 values(deptno,dname,loc)
into D2 values(deptno,dname,loc)
into D3 values(deptno,dname,loc)
select * from dept;

Conditional Insert:
insert all
when (deptno <= 40) then
into D1 values(deptno,dname,loc)
when (deptno <= 90) then
into D2 values(deptno,dname,loc)
else
into D3(dname,loc) values(dname,loc)
select * from dept;

insert all
when course = 'Oracle9i' then                  
into stu_oracle values(roll,name,fee)
when course = 'd6i' then
into stu_d6i values(roll,name,fee)
when course = 'unix' then
into stu_unix values(roll,name,fee)
select * from student;

Student       stu_oracle
---------       ------------
Roll             Roll
name           name
course         fee
fee             
----------------------------------------------------------------------------
Merge :
Used to compare the 2 table contents and makes them equal. 
It supports only Update and Insert operations .

>merge                                        Clauses:
into Temp T                                  into -- Target
using emp E                                  Using -- Source
on ( T.empno = E.empno )             On -- Join condition
when matched then
update set t.sal = e.sal,
                t.comm = e.comm,
                t.deptno = e.deptno,
                t.job =  e.job,
                t.mgr  =  e.mgr
when not matched then
insert values(e.empno,e.ename,e.sal,e.comm,......);

Before :
Emp - 1 Crore rows
Temp - Copy of emp - 1 Crore rows
After :
Emp --- 5000 inserts  & 1000 Updates performed
---------------------------------------------------------------------------- 
Rename Constraint & Column :
Alter table emp rename constraint sys_c002325 to pk_emp;
Alter table emp rename column ename to emp_name;
----------------------------------------------------------------------------
9i Supports :
Advanced Features of JAVA
Improved internal Architecture related to JAVA
Supports XML. 



```
