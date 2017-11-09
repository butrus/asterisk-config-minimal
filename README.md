# asterisk-config-minimal
Basic configuration for the Asterisk PBX with only a few necesary config files (see description)

# Beware! This is a Work-in-Progress !

Here I try to maintain a basic configuration for the Asterisk PBX (www.asterisk.com) -
currently for the version 11.

The problem is that the configuration as distributed along with Asterisk has virtually all
of the modules loaded ("autoload => yes") which means that many features not used are active.
Not only is this unnecessary and takes up resources such as memory or CPU power, but it can
also lead to security problems.

E.g. there is (was?) an example configuration in extensions.ael and extensions.lua along
with extenstions.conf. If pbx_ael and pbx_lua were loaded but the administrator was only
aware of extensions.conf beeing used the security could have been compromised.

I try therefore to come up with a configuration that presents a sensible default. E.g. only
the SIP protocol is considered every other protocol (or hardware access) must be configured
by the user.

For more information, please study modules.conf and other configuration files.

