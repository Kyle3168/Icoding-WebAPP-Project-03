# App Project 03

## 移动端常见的布局处理技术：

- 流体布局
- rem 和 vw 布局
- 响应式布局
- Flex & Grid （工具）

- html root font-size in mobile device is : 16px; same with PC.
- rem unit = width & height px / html root font-size px;

> 1rem = device-width / 对应份数； normally is 10;

## 2. JS 动态实现不同设备下 1 rem 的大小

```
    <script>
        // 假设把页面分成 10份
        function initpage(){
            // 获取当前页面的 html 元素

            var html=document.documentElement;

            // 获取页面的可视宽
            var clientWidth = html.clientWidth;
            console.log(clientWidth / 10 + "px")
            html.style.fontSize = clientWidth / 10 + "px";
            console.log(html.style.fontsize);
        }
        initpage();
        window.onresize = initpage;

    </script>
```

## use px to rem extension tool (alt + z) to convert px to rem unit;