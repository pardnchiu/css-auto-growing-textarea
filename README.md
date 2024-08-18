# 自動增長的輸入框 / Auto-Resizing Textarea

> 這個專案展示了一個自動增長的 `textarea` 元件，該元件會根據內容自動調整高度，確保所有文字可見，無需滾動。<br>
> This project showcases an auto-resizing `textarea` element that dynamically adjusts its height based on the content, ensuring that all text is visible without the need for scrolling.<br>
> 預覽: [jsfiddle](https://jsfiddle.net/pardnchiu/zjq293mt/4/)

## 功能 / Features

- **動態調整高度 / Dynamic Resizing**<br>
  <span>當更多文字被輸入時，`textarea` 的高度會自動增加，提供無縫的使用者體驗。</span><br>
  The height of the `textarea` automatically increases as more text is entered, providing a seamless user experience.
- **視覺反饋 / Visual Feedback**<br>
  <span>輸入的文字會顯示在 `pre` 元素中，增強可讀性。</span><br>
  Text entered into the textarea is displayed in a `pre` element, enhancing readability.

## 創建者 / Creator

<img src="https://pardn.io/image/head-s.jpg" align="left" width="96" height="96" style="float: left; margin-right: 0.5rem; width: 96px; height: 96px;" />

<h4 style="padding-top: 0">邱敬幃 Pardn Chiu</h4>

[![](https://pardn.io/image/mail.svg)](mailto:mail@pardn.ltd) [![](https://skillicons.dev/icons?i=linkedin)](https://linkedin.com/in/pardnchiu) 

## 代碼 / Code
- HTML
  ```html
  <label>
    <textarea oninput="this.nextElementSibling.innerHTML=this.value.replace(/\n/g, '<br>')"></textarea>
    <pre></pre>
  </label>
  ```
- SCSS
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
      width: 100%;
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
  
***

*All translations powered by ChatGPT*

***

©️ 2024 [邱敬幃 Pardn Chiu](https://www.linkedin.com/in/pardnchiu)
