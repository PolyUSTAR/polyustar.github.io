# Member portrait workflow

Only commit the final `*-card.webp` portrait. Do not keep the original JPG,
JPEG, or PNG file in this directory.

Requires [ImageMagick](https://imagemagick.org/). Put the source image here
temporarily, then run:

```sh
magick member.jpg -auto-orient -resize '900x1200' -strip -quality 90 member-card.webp
```

The image is resized proportionally without cropping. Rename the output with
the member's lowercase, hyphenated name, update the member front matter, and
delete the source image:

```toml
portrait = "/portraits/official/member-card.webp"
```
