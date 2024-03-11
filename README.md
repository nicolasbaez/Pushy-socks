# Pushy-socks
Scanning new worlds

![buh](https://github.com/nicolasbaez/Pushy-socks/blob/main/xp029.gif)
```javascript
k = 0;
l = 50;
h = 250;
d = 0.1;
e = 11;
setup = (_) => createCanvas((w = 500), w, WEBGL);
draw = (_) => {
  clear();
  rotateX(1);
  rotateY(0.3);
  stroke(128);
  for (i = 0; i < e; i += d)
    for (j = 0; j < e; j += d) point(i * l - h, j * l - h, noise(i, j) * l);
  stroke(0, h, random(h));
  for (i = 0; i < e; i += d) point(k * l - h, i * l - h, noise(k, i) * l);
  k += d / 2;
};

keyPressed = (_) => {
  if (key === "s") {
    saveGif("xp029.gif", 220, { delay: 0, units: "frames" });
  }
};
