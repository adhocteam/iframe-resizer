## Vue

Create the following Vue directive

```
import Vue from 'vue'
import {iframeResize} from 'iframe-resizer';

Vue.directive('resize', {
  bind: function(el, { value = {} }) {
    el.addEventListener('load', () => iFrameResize(value, el))
  }
})
```
and then include it on you page as follows.

```html
<iframe
  v-resize="{ log: true }"
  width="100%"
  src="myiframe.html"
  frameborder="0"
></iframe>
```

- Thanks to [Aldebaran Desombergh](https://github.com/davidjbradshaw/iframe-resizer/issues/513#issuecomment-538333854) for this example