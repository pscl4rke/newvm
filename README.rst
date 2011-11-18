

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
Then you can stop using ``VBoxHeadless`` and switch over to
something like ``VBoxManage startvm`` instead.

If you no longer need the machine::

    $ ./deletevm mymachine

(The latter can throw up error messages, but does work.  Please
tell me if you have any good fixes for this.)


