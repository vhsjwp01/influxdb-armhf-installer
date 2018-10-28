## influxdb-armhf-installer
A shell script to aid in installing the influxdb binary distribution for ARMhf architecture from https://portal.influxdata.com/downloads

Target distro: debian/raspbian

## How to use this script:
STABLE Build:
~~~~
curl -L https://github.com/vhsjwp01/influxdb-armhf-installer/raw/master/influx-arm-installer.sh -s | bash
~~~~

Nightly Build:
~~~~
curl -OL https://github.com/vhsjwp01/influxdb-armhf-installer/raw/master/influx-arm-installer.sh -s | bash
chmod +x ./influx-arm-installer.sh
./influx-arm-installer.sh nightly
~~~~

## NOTES:
- On some systems with systemctl, simply creating the symlink is enough to make systemd think the service is enabled.  However, on some systems this is insufficient
- If ``systemctl start influxdb`` spits an error, run the following command:
  - ``systemctl list-unit-files | egrep influxdb``
  - if it reports 'linked', then run:
    - ``systemctl enable influxdb``
    - ``systemctl start influxdb``

