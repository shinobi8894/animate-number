# Animate Number

index.js

```
function animateValue(obj, start, end, duration) {
    let startTimestamp = null;
    const step = (timestamp) => {
      if (!startTimestamp) startTimestamp = timestamp;
      const progress = Math.min((timestamp - startTimestamp) / duration, 1);
      obj.innerHTML = Math.floor(progress * (end - start) + start);
      if (progress < 1) {
        window.requestAnimationFrame(step);
      }
    };
    window.requestAnimationFrame(step);
  }
  
  const obj = document.getElementById("value");
  animateValue(obj, 100, 0, 5000);
  
```

You can make animation with requestAnimationFrame

🎈🎈🎈🎈🎈🎈🎈

Contributed by Shinobi!!!
