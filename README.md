# Fire Mono font with italics

[Avi-D-coder's fork](https://github.com/Avi-D-coder/fira-mono-italic) of [zwaldowski's fork](https://github.com/zwaldowski/Fira/tree/zwaldowski/mod-new/otf) of [Mozilla Fira Mono v3.111](https://github.com/zwaldowski/Fira/tree/6a54e14aeb67bef790bb636730e0e2feadbaf7e6) but with hinted TrueType fonts.

I've bumped the version number to 3.112

Non-linux users, please be aware that this repository is case-sensitive.

## Prerequisites

```bash
pip3 install fontmake
pip install ttfautohint-py
(optionally) [brew](https://brew.sh/) install [fd](https://github.com/sharkdp/fd)
```

## Building

```bash
# build otf
fd --extension=ufo -x fontmake -u {} -o otf --output-dir distr/otf
# built ttf
fd --extension=ufo -x fontmake -u {} -o ttf -a --output-dir distr/ttf
```

## Issues

I could not figure out how to set isFixedPitch flag. I did it manually using ttx tool from [fontForge project](https://fontforge.org). Please see [this issue](https://github.com/googlefonts/fontmake/issues/688).
