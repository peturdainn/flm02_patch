# flm02_patch
patched file(s) to get flukso v2 working again

sadly wget on the FLM02 does not support HTTPS so you can't download from github directly,<br> 
I have copied the file on a server of mine (public.lunda.be), feel free to use your own.<br> 
The original file is also on there

the links are:<br> 
http://public.lunda.be/fluksod.lua<br> 
http://public.lunda.be/fluksod.lua.org<br> 

*MAKE SURE YOU DO THIS ON AN FLM02 and no other model!!!*

ssh into the FLM02:
```
ssh root@192.168.0.2
```
replace 192.168.0.2 with the IP address of your flukso<br> 
if SSH fails because of an unsupported cipher you may need to allow this explicitly in your SSH client<br> 
for example, in linux this probably means editing .ssh/config (from your home dir) and adding:<br> 

```
Host 192.168.0.2
	HostKeyAlgorithms +ssh-rsa,ssh-dss 
```

Then proceed with these commands:

```
cd /usr/sbin/
mv fluksod.lua fluksod.lua.bak
wget http://public.lunda.be/fluksod.lua
chmod 0755 fluksod.lua
ls -l
```
(verify you have the fluksod.lua file and it has the same size and access rights as the .bak file)
```
reboot now
```
