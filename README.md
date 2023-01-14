# mesa-freeworld
freeworld build of mesa for Manjaro unstable branch

Forked from [https://gitlab.manjaro.org/packages/extra/mesa/-/blob/master/PKGBUILD][1]

## Build instructions

Ensure you have the **base-devel** package synced

```
sudo pacman -Syu base-devel git bison byacc flex --needed
```

Then clone

```
git clone https://github.com/mesa-freeworld/mesa-freeworld.git
```

## Check the PKGBUILD for correct versions.

Check with upstream and modify the version.

Bump pkgrel to a high number to ensure your current build is only replaced on regular version changes.

Build and install the package.

```
cd mesa-freeworld
makepkg --geninteg --syndeps --install
```

### on keyerror 
Import public key in case you are missing out (8D8E31AFC32428A6) and rerun makepkg command
```
gpg --recv-keys 8D8E31AFC32428A6
```

Buildtime will vary depending on your hardware.

Highend workstation

```
 $ makepkg -Cf
 ...
==> Finished making: mesa 22.3.2-4.5 (tor 05 jan 2023 13:57:19 CET)

real    1m27,862s
user    19m16,230s
sys     1m50,794s

```

Yepo Celeron J3455 8GB ram and ssd

```
 $ makepkg -Cf
 ...
==> Finished making: mesa 22.3.2-4.5 (Thu 05 Jan 2023 08:00:36 AM EST)

real    37m9.483s
user    128m18.964s
sys     8m28.153s
```

[1]: https://gitlab.manjaro.org/packages/extra/mesa/-/blob/master/PKGBUILD

