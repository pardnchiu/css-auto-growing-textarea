```html
<label>
  <textarea oninput="this.nextElementSibling.innerHTML=this.value.replace(/\n/g, '<br>')"></textarea>
  <pre></pre>
</label>
```

```SCSS
label {
  position: relative;
  display: block;
  padding: 0.5rem;
  width: 256px;
  line-height: 1.5rem;
  min-height: 1.5rem;
  font-family: sans-serif;
  font-size: 1rem;
  letter-spacing: 0;
  color: red;
  border: 1px solid #0000001a;
  box-sizing: border-box;
  overflow: hidden;
  
  pre,
  textarea {
    margin: 0;
    line-height: inherit;
    min-height: inherit;
    font-size: inherit;
    letter-spacing: inherit;
    font-family: inherit;
    box-sizing: border-box;
  }
  
  pre {
    display: block;
    padding: 0;
    width: inherit;
    white-space: pre-line;
    overflow-wrap: break-word;
  }
  
  textarea {
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    padding: inherit;
    width: inherit;
    height: inherit;
    resize: none;
    color: transparent;
    background-color: transparent;
    border: none;
    overflow: hidden;
  }
}
```

預覽: [jsfiddle](https://jsfiddle.net/pardnchiu/zjq293mt/1/)
