# Font Aliasing

Create a file at `/etc/fonts/local.conf` to handle font aliasing using font-config.

Files in `/etc/conf.d` are symlinks to files in `/etc/conf.avail`. Each file handles aliases. Add your desired font as a symlink here or edit the existing files.

Example `/etc/fonts/local.conf`:
```
<?xml version='1.0'?>
<!DOCTYPE fontconfig SYSTEM 'fonts.dtd'>
<fontconfig>
	<alias>
		<family>sans-serif</family>
		<prefer><family>Sans Serif Font</family></prefer>
	</alias>
	<alias>
		<family>sans</family>
		<prefer><family>Sans Font</family></prefer>
	</alias>
	<alias binding="same">
		<family>monospace</family>
		<prefer><family>Monospace Font</family></prefer>
	</alias>
</fontconfig>
```
