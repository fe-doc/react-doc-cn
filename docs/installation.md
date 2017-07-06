

React 可被灵活地运用在各种项目中。你可以用它创建新的应用程序，也可以逐渐地将其加入到现有的代码库中而无需重写。

<div class="toggler">
  <style>
    .toggler li {
       display: inline-block;
       position: relative;
       top: 1px;
       padding: 10px;
       margin: 0px 2px 0px 2px;
       border: 1px solid #05A5D1;
       border-bottom-color: transparent;
       border-radius: 3px 3px 0px 0px;
       color: #05A5D1;
       background-color: transparent;
       font-size: 0.99em;
       cursor: pointer;
    }
    .toggler li:first-child {
      margin-left: 0;
    }
    .toggler li:last-child {
      margin-right: 0;
    }
    .toggler ul {
      display: inline-block;
      list-style-type: none;
      margin: 0;
      border-bottom: 1px solid #05A5D1;
      cursor: default;
    }
    @media screen and (max-width: 960px) {
      .toggler li,
      .toggler li:first-child,
      .toggler li:last-child {
        display: block;
        border-bottom-color: #05A5D1;
        border-radius: 3px;
        margin: 2px 0px 2px 0px;
      }
      .toggler ul {
        border-bottom: 0;
      }
    }
    .display-target-fiddle .toggler .button-fiddle:focus,
    .display-target-newapp .toggler .button-newapp:focus,
    .display-target-existingapp .toggler .button-existingapp:focus {
      background-color: #046E8B;
      color: white;
    }
    .display-target-fiddle .toggler .button-fiddle,
    .display-target-newapp .toggler .button-newapp,
    .display-target-existingapp .toggler .button-existingapp {
      background-color: #05A5D1;
      color: white;
    }
    block {
      display: none;
    }
    .display-target-fiddle .fiddle,
    .display-target-newapp .newapp,
    .display-target-existingapp .existingapp {
      display: block;
    }
  </style>
  <script>
    document.querySelector('.toggler').parentElement.className += ' display-target-fiddle';
  </script>
  <span>下一步你想做什么？</span>
  <br />
  <br />
   <ul role="tablist" >
      <li id="fiddle" class="button-fiddle" aria-selected="false" role="tab" tabindex="0" aria-controls="fiddletab"
          onclick="display('target', 'fiddle')" onkeyup="keyToggle(event, 'fiddle', 'existingapp', 'newapp')">
        尝试 React
      </li>
      <li id="newapp" class="button-newapp" aria-selected="false" role="tab" tabindex="-1" aria-controls="newapptab"
          onclick="display('target', 'newapp')" onkeyup="keyToggle(event, 'newapp', 'fiddle', 'existingapp')">
        创建新应用
      </li>
      <li id="existingapp" class="button-existingapp" aria-selected="false" role="tab" tabindex="-1" aria-controls="existingapptab"
          onclick="display('target', 'existingapp')" onkeyup="keyToggle(event, 'existingapp', 'newapp', 'fiddle')">
        添加 React 到现有应用
      </li>
    </ul>
</div>

<block id="fiddletab" role="tabpanel" class="fiddle"  />

## 尝试 React

如果你只是想简单尝试下 React，可以使用 CodePen. 首先试试这个 [Hello World 示例代码](http://codepen.io/gaearon/pen/rrpgNB?editors=0010)。你不需要安装任何东西，还能简单修改下代码使其生效。

如果你喜欢使用自己的文本编辑器，你还可以 <a href="/react/downloads/single-file-example.html" download="hello.html">下载此 HTML 文件</a> 进行编辑, 然后在本地浏览器中打开。它会执行缓慢的运行时代码转换，所以不要在生产环境中使用。

如果你想在一个完整的项目中使用 React，一般有两种方式：创建 React 应用或添加 React 到现有应用。
