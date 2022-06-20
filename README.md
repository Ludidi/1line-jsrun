# 1line-jsrun
一行js代码，可通过标签栏直接执行

## Swagger 一键复制
基于Swagger doc，一键复制URL
```js
javascript: eval('const buttons=document.querySelectorAll(\".opblock-summary-control\");buttons.forEach((item,index)=>{const urlButton=document.createElement(\"span\");urlButton.className=\"opblock-summary-method \";urlButton.id=\"copypath\";urlButton.style=\"margin-right: 10px\";urlButton.innerText=\"复制URL\";urlButton.dataset.path=`${item.children[1].dataset.path}`;const path=`${item.children[1].dataset.path}`;const parent=item.parentElement;parent.appendChild(urlButton);urlButton.addEventListener(\"click\",function(e){const input=document.createElement(\"input\");document.body.appendChild(input);input.setAttribute(\"value\",`${e.target.dataset.path}`);input.select();if(document.execCommand(\"copy\")){document.execCommand(\"copy\");const divEle=document.createElement(\"div\");divEle.style=\"position: fixed;width: 200px;height: 30px;line-height: 30px;text-align: center;top: 20px;left: 0;right: 0;bottom: 0;margin:100px auto;background: #61affe;\";document.body.appendChild(divEle);divEle.innerText=\"复制成功\";setTimeout(()=>{document.body.removeChild(divEle)},1000)}document.body.removeChild(input)},false)});')
```

## SpacingJS 测量工具
基于[SpacingJS](https://github.com/stevenlei/spacingjs)测量网页间距，元素大小
```js
javascript: fetch('https://unpkg.com/spacingjs').then(res => res.text()).then(text => {eval(text); alert('spacingjs success')})
```
