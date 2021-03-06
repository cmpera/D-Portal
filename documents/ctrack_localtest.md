
How to Install and Setup a test ctrack server
=============================================

First you need to install git and node this is a different problem 
depending on which operating system you are using and only needs to 
be done once so please check and follow the steps bellow carefully.

Github also has a help page for setting up git so you can have a 
little read of that first to give you an idea of what you are about 
to install.

https://help.github.com/articles/set-up-git


1. Installing git and node on Ubuntu
====================================

Open a command line and type the following one line at a time to 
create a directory in your home directory containing the project.

	cd ~
	sudo apt-get install git
	git clone https://github.com/IATI/D-Portal
	cd D-Portal/ctrack
	../bin/getapts

In the future you may return to this directory with just the 
following command.

	cd ~/D-Portal/ctrack


1. Installing git and node on Windows
=====================================

Download and install git and node for windows from the following 
locations, just go with the default settings when the installers asks 
you a complicated looking question and you will be fine.

http://git-scm.com/download/win

http://nodejs.org/download/

Now run "git bash" this can be found in your startmenu under git on 
windows 7 and below or searched for on windows 8 and above. When run 
it should open up a command line window, this is the window you need 
to type the commands on this page into.

Finally we need to grab the code with the following command

	git clone https://github.com/IATI/D-Portal

and then move into the ctrack directory, make sure you have moved 
into this directory before you try and perform any of the other 
steps on this page.

	cd D-Portal/ctrack


2. Prepare the required node modules.
=====================================

This only needs to be run once, it will download and install the 
node modules that ctrack depends upon.

	../install_deps
	
This will chug away for a little while downloading code.


3. Run the localhost server.
============================

This is only going to run ctrack module, the extra opton tells it to 
visit d-portal to fetch the data so you do not need to install or 
update the dstore data just to test ctrack.

	../serv -q http://d-portal.org/

If all goes well then ctrack should be available, from your machine 
in your browser at the following url

http://localhost:1337/


4. Refresh the localhost server.
================================

Press Control + C to stop this server and then just run the command 
again to start it up again. Since this also builds you should make 
changes to the source then stop the server (ctrl c) and run it again 
in order to see your updates. Pressing up arrow is an easy way to 
get the last typed in command without having to type it in again.


5. In the future
================

After rebooting your machine you will not need to perform all the 
above steps just the following,

Open a command line, see step 1 above for help on how to do this on 
your operating system. CD into the ctrack directory, again step 1 
above include help on how to do this.

Now you can repeat steps 3 and 4 to run the server again.

