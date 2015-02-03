# mangos-init-script

init script of MaNGOS/CMaNGOS for CentOS/RedHat

## Usage

Put `realmd` and `mangosd` into `/etc/init.d/`

Set permissions

	chmod a+x /etc/init.d/realmd
	chmod a+x /etc/init.d/mangosd
	
Start service

	service realmd start
	service mangosd start
	
Start with system

	chkconfig realmd on
	chkconfig mangosd on
	
Reattach
	
	screen -r realmd
	screen -r mangosd
	
Stop service

	service realmd stop
	service mangosd stop

## Customize

### realmd

	BASENAME=realmd
	EXEC=/opt/mangos/bin/$BASENAME
	USER=mangos
	
`BASENAME` the executable binary name

`EXEC` path to `BASENAME`

`USER` the user to run in

### mangosd

see above