

NewVM
=====

Just a handful of quick scripts for creating a virtual machine
using VirtualBox without a GUI.


Basic Usage:
------------

Create a machine::

    $ ./newvm mymachine

Optionally you can specify ISO image, e.g.::

    $ ./newvm mymachine ~/iso/Windows_XP.iso

Then set newly created machine running on your server::

    $ VBoxHeadless --startvm mymachine

Then locally hook up to it over RDP.  Defaults to port 3389.
This does require your copy of the server to have the VRDE extension
enabled.

Out-of-band access is usually only required for setup.
When you get to the point where you have working SSH (or
equivalent) you can launch the machine using::

    $ VBoxManage startvm mymachine --type headless

This command returns as soon as the machine is up and running.
If you no longer need the machine::

    $ ./deletevm mymachine

(The latter can throw up error messages, but does work.  Please
tell me if you have any good fixes for this.)


