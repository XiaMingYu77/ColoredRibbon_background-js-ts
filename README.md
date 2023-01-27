# 彩带背景

基于 canvas 绘制动态彩带背景

你可以在使用时自定义传入样式、模式参数

效果：

![image-20230127230417391](https://gcore.jsdelivr.net/gh/XiaMingYu77/My-Markdown-Picture/img/202301272304559.png)

演示地址：

http://www.coloredribbon.moming.asia/



## js

这里介绍 js 版本如何使用

1. 获取 coloredRibbon.js 文件，将其放入项目中

2. 引用该文件

   ```js
   import createRibbons from './coloredRibbon.js'
   ```

   **注意：本处路径取决于你放置的位置，请自行引入**

3. 使用上面引入的方法，传入 builder 对象

   ```html
   <script type="module">
       import createRibbons from './coloredRibbon.js'
   
       createRibbons({ //默认对象，对象属性按需使用，不选则使用默认
           horizontalSpeed: 150, //颜色传播速度，注意：由于振幅不变，速度变慢的话看起来色带会更加尖锐
           colorCycleSpeed: 5,   //颜色循环速度（颜色变化速度）
           ribbonCount: 4,       //一个轮回Tick彩带数
           colorAlpha: 0.65,     //彩带的颜色透明度
           strokeSize: 0,        //描边
           margin: "auto",
           padding: "0",
           border: "0",
           //采用absolute布局，并且生成的canvas会搭载在document.cody上
           position: {top: '0', bottom: '0', left: '0', right: '0'}, //位置
           width: "100%",
           height: "100%",
           z_index: "-1",
           color: "#E4EFF0", //背景颜色
           id: "bgCanvas",    //生成的canvas的id
       });
   </script>
   ```

   **builder 对象中的属性可以按需引入，上面是默认值**

   

##  ts

此处介绍 ts 版本如何使用

1. 获取 coloredRibbon.ts 文件，将其放入项目中

2. 引用该文件

   ```ts
   import createRibbons from './components/coloredRibbon'
   ```

   **注意：本处路径取决于你放置的位置，请自行引入**

3. 使用上面引入的方法，传入 builder 对象

   ```vue
   <script lang="ts" setup>
   import createRibbons from './components/coloredRibbon'
   
   createRibbons({
       horizontalSpeed: 150,
       colorCycleSpeed: 5,
       ribbonCount: 4,
       colorAlpha: 0.65,
       strokeSize: 0,
       margin: "auto",
       padding: "0",
       border: "0",
       position: { top: '0', bottom: '0', left: '0', right: '0' },
       width: "100%",
       height: "100%",
       z_index: "-1",
       color: "#E4EFF0",
       id: "bgCanvas"
   })
   </script>
   ```

