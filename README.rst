SMaSH: The Systems Management Shell
===================================

SMaSH is a configurable and extensible shell that is designed to run on
a bastion host jump box to provide both direct controlled access to
systems within a network and to provide a limited set of commandlets that
can be run by helpdesk representatives. It can also be used as part of a
more complete monitoring and management platform.

This project is currently being developed with the following goals:

- Written in C.
- Built with a focus on security foremost. No direct access is given to
  the bastion host the shell is running on, and utmost care is taken in
  order to prevent common vulnerabilities.
- A built in array of built-in commands for managing the shell
  environment, setting server and command permissions, and other basic
  functions.
- No shell programming environment is provided for safety and security
  reasons, as well as for the sake of simplicity of design.
- Extensibility is provided by the choice of a built-in interpreter such
  as Perl, Python, or Ruby. New commands can be written for specific
  working environments and executed safely on hosts from the bastion host.
- Servers may be accessed either directly or via a "call-back" reverse SSH
  connection that prevents your jump box from needing a private SSH key
  and ensures the flow of trust never moves in the wrong direction.

Initial development will focus on basic shell functionality and management
as well as on solidifying the security model and command syntax. The first
embedded language will be Perl, followed by Python, then Ruby. This is a
part-time/free-time project, so don't expect things to move quickly.

Obtaining SMaSH
---------------

- Git::

    git clone https://github.com/deriamis/smash.git
    ./configure && make && make install

Documentation
-------------

The documentation for the stable version is available at:
http://smash.readthedocs.org/

The documentation for the latest development version is available at:
http://smash.readthedocs.org/en/latest/
