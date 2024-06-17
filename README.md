# flm02_patch
patched file(s) to get flukso v2 working again

sadly wget on the FLM02 does not support HTTPS so you can't download from github directly, 
if more people need this I can look at setting up a public http or ftp server for this file
(all my servers enforce https currently)

if you have the file on some http server, follow this procedure:

ssh into the FLM02
```
cd usr/sbin/
mv fluksod.lua fluksod.lua.bak
wget http://yourserver/fluksod.lua
chmod 0755 fluksod.lua
ls -l
```
(verify you have the fluksod.lua file and it has the same size and access rights as the .bak file)
```
reboot now
```
