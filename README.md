piconscripts
============

A collection of scripts related to @ocram's picons

* `piconlinks.py` is a Python 2.x script that takes 
  your particular VDR-style `channels.conf` and a
  directory with picons to create a shell script for
  Enigma2 style service reference symlinks.
  It tries a simple matching algorithm from channel
  name to picon name, and leaves everything else
  commented out for manual correction/addition.

  For usage instructions, see:

  ```python2 piconlinks.py -h```

  **Important note:** Your `channels.conf` should be created
  by the [w_scan](http://wirbel.htpc-forum.de/w_scan/index2.html)
  tool or the [vdr-wirbelscan plugin](http://wirbel.htpc-forum.de/wirbelscan/index2.html).
  Using a `channels.conf` created by the `scan` tool from the
  [dvb-apps](http://www.linuxtv.org/) will not work properly.

* `kabelbw.sh` creates the same symlinks as @ocram's
  [picons.sh](https://github.com/ocram/picons/blob/master/picons.sh),
  but only for the German DVB-C provider Kabel BW.

* `channelsdiff.py` basically does a comparison between your
  current `channels.conf` and a new one, ideally generated by
  [w_scan](http://wirbel.htpc-forum.de/w_scan/index2.html).
  The order of channels in the files is irrelevant, so if you - like me -
  cleaned up and reordered your `channels.conf`, you'll probably love this tool.
  The output has at most four sections:

		1. Channel PARAMETER changes - for channels that changed frequency etc. since last scan
		2. Channel NAME changes - for channels that were replaced by others
		3. Channels that are NO LONGER found
		4. NEW Channels

  For usage instructions, see:

  ```python2 channelsdiff.py -h```


