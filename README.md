# cesium-viewshed
基于Cesium的可视域分析

----------------------------------------------------------------------------------------------------------------------------------------
### 基于cesium的三维量测插件
### cesium-measure

### 说明
##### /cesium-viewshed/src/doc

### 使用

#####  在项目中引入Cesium.js

#####  然后引入 cesium-viewshed.js 即可

<a href="http://zhangticcc.gitee.io/webgis/"><img alt="" height="100%" src="https://img-blog.csdnimg.cn/20201029105641945.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MDkwMjUyNw==,size_16,color_FFFFFF,t_70" width="90%" ></a>&nbsp;

``` 
    // 初始化
    let viewer = new Cesium.Viewer("viewerContainer")

    // 分析参数
    var viewModel = { verticalAngle: 90, horizontalAngle: 120, distance: 10 };

    // 添加可视域
    var viewshed = new Cesium.ViewShed3D(viewer, {
        horizontalAngle: Number(viewModel.horizontalAngle),
        verticalAngle: Number(viewModel.verticalAngle),
        distance: Number(viewModel.distance),
        calback: function () {
          viewModel.distance = viewshed.distance
        }
    });

    // 清除可视域
    viewshed.destroy();

```


