# soma-connect

Creating a debian / ubuntu package for soma-connect 2.3.2 for use on my
raspberry pi 5

## Zip file

I split up the zip file provided by SOMA into `files/` by running:

```shell
zip 2.3.2.soma.connect.zip --out files/2.3.2.soma.connect.zip -s 50m
```

You can unzip with:

```shell
zip -FF 2.3.2.soma.connect.zip --out

```

md5 hash provided by SOMA Connect installation page as of Feb 2nd 2026 (believe
me or don't):

- 2.3.2.soma.connect.zip 3da2f8abaff2fe6d73b9ae4e9de826cc
- 2.3.2.soma.connect.img f9444ecccc547680d469ed78088da836
