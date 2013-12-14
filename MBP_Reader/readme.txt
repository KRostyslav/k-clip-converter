MBP_Reader
----------

  This package reads a .MBP file,
which is the file that stores user added information to
any of the file formats that "mobipocket reader" can read.
(see www.mobipocket.com for a reader program).

  So, a .MBP file associated to a (for example) .PRC book file,
would contain annotations, corrections, drawings and marks
made by the user on the book content.

  Can you extract this notes to any other format?
Actually, not.
Except if you use this Perl script:


== PREVIOUS NOTE ==
  In order for this script to extract notes, you'll also need the 
GD perl module, and libgd library installed on your system.
  In case you do not have them properly installed, this script 
won't create GIF images from your mbp drawings.


== USAGE ==

-- WINDOWS --
1.  You have a windows executable in a different zip here:
  	http://www.angelfire.com/ego2/idleloop/mbp_reader.html
    Anyway, in case you wanna run these perl scripts in Windows,
  you need to install a Perl interpreter for Windows,
  for example ActivePerl:    	http://www.activestate.com/store/activeperl/download/
  (You don't have to give your data if you don't want to,
  just click "continue"...)
    When you have finished installing it, continue to next step.

-- WINDOWS & LINUX/UNIX --
2.  Decompress all files in the same FOLDER.
3.  Put a copy of your MBP FILE in that very same FOLDER.
3.  Open up a command-line console:
    In windows, a MS-DOS console.
4.  Situate the prompt in the FOLDER (cd... 'til reach FOLDER).
5.  Type:
  	perl MBP_reader.pl MBP_FILE_NAME.mbp
    to extract notes from a specific mbp file, or:
  	perl MBP_reader.pl
    in order to extract notes from ALL mbp files in this FOLDER.
6.  All your notes will be in text file(s) named:
	MBP_FILE_NAME.mbp_notes.txt
    If drawings exist in the mbp file, and the system has both the GD perl module and libgd libraries, they'll be exported to GIF images, named after the mbp file, plus a number and ".gif" extension.


== CONTACT ==
  Problems? suggestions? :
	idleloop@yahoo.com
  Looking for new versions? :
	http://www.angelfire.com/ego2/idleloop/


== HISTORY ==

  Can you extract this notes to any other format?
In mobipocket forums (www.mobipocket.com/forum/) developers
say that next versions of mobireader will have this 
functionality. I've been waiting for years.

  Unfortunately, I had a problem with a two-hundred-note MBP file,
which was corrupted (?) as I was reading a file... and I
simply couldn't lost all that info:
I "had" to make this Perl program to try to patch my file.
(In case you guess, yeah, I could patch it: it just had some 
bytes where it shouldn't ;)


== VERSION ==

  Version: 0.5.c, 11/2013

== VERSION HISTORY ==
Usually, each version upgrade upgrades also the mbp file format definition.

    * 0.5.c (11/2013)
      Patch: there can be two consecutive index entries pointing to the same note.
    * 0.5.b.1 (10/2013)
      only perl code retouched to eliminate obsolete "switch" statemet. Windows version untouched.
    * 0.5.b (06/2013)
      Adjusting value of SHOW_MARK_TYPE in mbp.parameters.txt will not print mark type descriptions.
    * 0.5.a (10/2012)
      Adjusting value of BKMK_PAGE_FACTOR in mbp.parameters.txt will print page locations.
    * 0.4.a (05/2012)
      Seems Kindle Fire stores notes in a different way. First approach.
    * 0.3.a (03/2012)
      International characters managed correctly (finally).
    * 0.2.f (12/2010)
      Corrected the mark detection algorithm. Again.
    * 0.2.e (12/2009)
      Corrected the mark detection algorithm to make it flexible enough to cope with not so well known bits.
    * 0.2.d (06/2009)
      Corrected a byte alignment detail that could have caused previous versions to provide no results.
    * 0.2.c (07/2008)
      Ups, previous 0.2.b wasn't as flexible as I thought... fixed. Also, PUBLISHER mark recognized.
    * 0.2.b (06/27/2008)
      adds support for these tags: GENRE, ABSTRACT, and COVER. Flexible handling of unknown tags... hope this won't mess things up. Also, this way, broken MBP files won't be so easily patched... but, hey, anyway, probably I'm the only one in the world who patched a broken MBP file ;)))   (if you've also done it, let me know!).
    * 0.2.a (04/30/2008)
      Now it can export user drawings to GIF images!.
    * 0.1.d (04/23/2008)
      adds support for these tags: AUTHOR, TITLE, and CATEGORY. More flexible tagging for Notes.
    * 0.1.c (04/2008)
      adds BOOKMARKs parsing.
    * 0.1.b (04/2008)
      initial release. 


== LICENSE ==

  Distributed under GPL 3
  (license text included in zip distribution file).

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.


== LINKS ==

	www.angelfire.com/ego2/idleloop
	www.angelfire.com/ego2/idleloop/mbp_reader.html

	www.mobipocket.com
	www.mobipocket.com/forum/

	en.wikipedia.org/wiki/Perl
	perldoc.perl.org
	www.activestate.com/store/activeperl/download/
