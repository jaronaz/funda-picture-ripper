# Funda-Picture-Ripper
Quick and dirty way to download all pictures from specific real estate on Funda.nl

> **Warning:** this is extremely dirty, can break anytime with new Funda releases.

## Steps

### Browse to any Funda real estate object

### Open console

Open console and enter the following JS.

```javascript
var pics = document.getElementsByClassName("media-viewer-item-content");
for (i = 0; i < pics.length; i++) {
    if(!!pics[i].srcset) {
      var url = pics[i].srcset.split(",")[5].split(" ")[1];
      console.log(url); 
  }
    if(!!pics[i].getAttribute("data-lazy-srcset")) {
      var url = pics[i].getAttribute("data-lazy-srcset").split(",")[5].split(" ")[1];
      console.log(url); 
  }
}
```

### Save output 

Copy paste the output to links.txt

### Download images

```bash
$ wget -i links.txt
```

Enjoy your images
