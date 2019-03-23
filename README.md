FiSH for weechat
================

This is a python plugin for weechat.  It implements blowfish encryption and
DH1080 key exchange and should be compatible with FiSH from
http://fish.secure.la/

This version uses a separate blowfish library to allow usage of keys with a length of up to 72 bytes.

v0.10
----
Can use [weechat secured data][weechat-secure] to store keys. To encrypt keys:
```
/secure set fish *********
/set fish.secure.key "${sec.data.fish}"
```

Or you can set a randomly generated key with:
```
/blowkey genkey
```

To return to storing in plain text:
```
/set fish.secure.key ""
```

Install
------
Run `make` then if you store your weechat scripts in the standard location `~/.weechat/python`, just run `make install`.

Otherwise copy the resulting `fish.py` and `weechat.so` to your weechat installations `python` directory.

[weechat-secure]: http://dev.weechat.org/post/2013/08/04/Secured-data
