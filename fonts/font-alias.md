# Font Aliasing

Create a file at '/etc/fonts/local.conf' to handle font aliasing using font-config


Example:

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
