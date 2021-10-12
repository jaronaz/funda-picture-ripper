# Funda-Picture-Ripper
Quick and dirty way to download all pictures from specific real estate on Funda.nl

> **Warning:** this is extremely dirty, can break anytime with new Funda releases.

## Steps

### Browse to any Funda real estate object

### Open console

Open console and enter the following JS.

```javascript
var pics = document.getElementsByClassName("media-viewer-overview__section-image");
for (i = 0; i < pics.length; i++) {
 console.log(pics[i].src); 
}
```

### Save output 

Copy paste the output to links.txt, make sure every line only contains one URL and starts with https://

### Download images

```bash
$ wget -i links.txt
```

Enjoy your images
