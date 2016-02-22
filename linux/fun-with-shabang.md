# Fun with Sha-bang

The `#!` actually calls the command interpretter.  This allows you to do some cute things.

Self removing script:
```
#!/bin/rm
# Running this just deletes itself

THIS_WONT_HAPPEN=9001
```

Self-listing documentation:
```
#!/bin/more
# Self reading documentation
# Need to make it executable as well
```

[source](http://www.tldp.org/LDP/abs/html/sha-bang.html#EX1)