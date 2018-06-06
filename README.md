## influxdb-armhf-installer
A shell script to aid in installing the influxdb binary distribution for ARMhf architecture from https://portal.influxdata.com/downloads

Target distro: debian/raspbian

## How to use this script:
~~~~
curl -H 'Accept: application/vnd.github.v3.raw' https://api.github.com/repos/vhsjwp01/influxdb-armhf-installer/contents/influxdb-arm-installer.sh -s | bash
~~~~

## NOTES:
- On some systems with systemctl, simply creating the symlink is enough to make systemd think the service is enabled.  However, on some systems this is insufficient
- If ``systemctl start influxdb`` spits an error, run the following command:
  - ``systemctl list-unit-files | egrep influxdb``
  - if it reports 'linked', then run:
    - ``systemctl enable influxdb``
    - ``systemctl start influxdb``

