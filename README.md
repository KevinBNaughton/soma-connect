# soma-connect

Creating a debian / ubuntu package for soma-connect 2.3.2 for use on my
raspberry pi 5

## Build and install from this repo source

```shell
dpkg-deb --build soma-connect
```

Then on my raspberry pi 5:

```shell
sudo dpkg -i soma-connect.deb


Selecting previously unselected package soma-connect.
(Reading database ... xx files and directories currently installed.)
Preparing to unpack soma-connect.deb ...
Unpacking soma-connect (2.3.2) ...
Setting up soma-connect (2.3.2) ...
hci0 new_settings: powered ssp br/edr le secure-conn
Changing power on succeeded
Processing triggers for rsyslog (8.2312.0-3ubuntu9.1) ...
```

And now for the moment of truth...

Ah! Not a 64-bit file. WIP.

## Get files from the source zip file

The files in this repo are from the original Soma downloaded zip file.

I split up the zip file provided by SOMA into `files/` by running:

```shell
split -b 50000000 -d 2.3.2.soma.connect.zip files/soma.part_
```

Recombine with:

```shell
cat files/soma.part_* > 2.3.2.soma.connect.zip
```

Check md5sum:

```shell
md5sum 2.3.2.soma.connect.zip
```

md5 hash provided by SOMA Connect installation page as of Feb 2nd 2026 (believe
me or don't ¯\(ツ)/¯):

- 2.3.2.soma.connect.zip 3da2f8abaff2fe6d73b9ae4e9de826cc
- 2.3.2.soma.connect.img f9444ecccc547680d469ed78088da836

## Acknowledgements

Thank you very much to the SOMA Simple Smart Home company and team!
