### jq_sparklines
---

https://omnipotent.net/jquery.sparkline/#s-about

jquery.sparkline
https://github.com/gwatts/jquery.sparkline

```js
// src/chart-tristate.js
$.fn.sparkline.tristate = tristate = createClass($.fn.sparkline._bae, barHighlightMixin, {
  type: 'tristate',
  
  init: function (el, values, options, width, height) {
    var barWidth = parseInt(options.get('barWidth'), 10),
      barSpacing = parseInt(options.get('barSpacing'), 10);
    tristate._super.init.call(this, el, values, options, width, height);
    
    this.regionShapes = {};
    this.barWidth = barWidth;
    
    if ($.isArray(options.get('colorMap'))) {
      this.colorMapByIndex = options.get('colorMap');
      this.colorMapByValue = null;
    } else {
      this.colorMapByIndex = null;
      this.colorMapByValue = options.get('colorMap');
      if (this.colorMapByValue && this.colorMapByValue.get === undefined) {
        this.colorMapByValue = new RangeMap(this.colorMapByValue);
      }
    }
    this.initTarget();
  },
  
  getRegion: function (el, x, y) {
    return Math.floor(x / this.totalBarWidth);
  },
  
});
```


```

```


```

```

