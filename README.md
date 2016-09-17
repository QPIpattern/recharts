# An R Interface to Baidu Echarts2

[Echarts2](http://http://echarts.baidu.com/echarts2) is an open source d3-js library developed by Baidu Inc. for interactive charts. Compared to other popular d3-js libraries, Echarts is more Chinese-friendly. The latest stable release of Echarts2 is 2.2.7. The most up-to-date version is Echarts 3.2.3. 

This package is to facilitate `R` users to make use of Echarts2 library (Echarts3 is not supported yet). A hello world example is as below:

```r
echartr(iris, Sepal.Length, Sepal.Width, Species) %>% setTheme('macarons')
```
![hello_world](inst/figure-html/hello_world.png)

> The initial `recharts` package was developed by Yang Zhou and Taiyun Wei. The current branch was forked from [Yihui Xie](https://github.com/yihui/recharts). 

# Installation

```r
if (!require(devtools)) library(devtools)
devtools::install_github('madlogos/recharts')
```

As the package is under development, you may come across errors when requiring the package directly from Github. You can alternatively download the codes from Github and compile the codes using RStudio.

# Documentation

- `R` help system
- [Official help](https://madlogos.github.io/recharts)

# Development

The package was developed using RStudio under Ubuntu 16. 

## Design

The Echarts object is an S3 list, comprising of the following elements:

(1) **Timeline contained**
```
- timeline
- options
    - series
        - list 1
        - ...
    - widgets (title, legend, toolbox, dataRange, dataZoom, roamController)
    - ...
```
(2) **No timeline contained**
```
- series
    - list 1
    - ...
- widgets (title, legend, toolbox, dataRange, dataZoom, roamController)
- ...
```

The basic design is to configure an S3 object widget by widget and concatenate them by pipe operator (%>%). It is inspired by `ggplot2`.

The core function is `echartr`, which accepts basic settings of data source, variables, chart types and then constructs the framework of the S3 object (`options` part of the Echarts DOM object).

Then `echartr` parses the data source and calls series processing functions (`series_scatter`, `series_bar`, `series_line`, ...) to build the `series` part of the `options` object.

Then you can add more objects (`addMarkLine`, `addMarkPoint`, `addHeatmap`, `addNameMap`, ...) to the echarts object.

Then you can configure other widgets in the echarts object created by `echartr` to create/modify the widgets. E.g, `setTitle`, `setLegend`, `setToolbox`, `setDataZoom`, `setDataRange`, `setTimeline`, `setRoam`, axes such as `setAxis`, `setPolar` and aesthetics such as `setGrid`, `setSymbols`, `setTooltip`, `setTheme`.

You can further tune the series configuration using series tuning functions (under development) with full APIs from Echarts.

Finally, you can use `addMarkLine` or `addMarkPoint` to modify the `series` object step further. 

## Status

### Achievements

Current version is 0.0.5. 

- Major part of core function `echartr`
- Major part of widget functions `setTitle`, `setLegend`, `setDataRange`, `setDataZoom`, `setToolbox`, `setTimeline`, `setRoam`
- Additional element functions `addMarkLine`, `addMarkPoint`, `addNameMap`, `addHeatmap`, `addGeoCoord`
- Major part of Axis/grid functions `setAxis`, `setPolar`, `setGrid`
- Major part of aesthetic function `relocWidget`, `setTheme`, `setSymbols`, `setTooltip`
- Series processing fuenctions `series_scatter`, `series_bar`, `series_line`, `series_k`, `series_pie`, `series_funnel`, `series_radar`, `series_map`, `series_force`, `series_chord`, `series_gauge`, `series_wordCloud`, `series_tree`, `series_treemap`, `series_venn`, `series_riverEvent`, `series_heatmap`

### Supported chart types

1. Mono-coordinate System
    1. Cartesian Coordinate System
        1. Scatter
            1. [scatter|bubble](http://madlogos.github.io/recharts/Basic_Plots_01_Scatterplot.html)
        1. Bar
            1. [bar|hbar](http://madlogos.github.io/recharts/Basic_Plots_02_Bar.html#horizontal-bar-chart)
            1. [vbar|column](http://madlogos.github.io/recharts/Basic_Plots_02_Bar.html#vertical-bar-column-chart)
            1. [histogram|hist](http://madlogos.github.io/recharts/Basic_Plots_02_Bar.html#histogram)
        1. Line
            1. [line](http://madlogos.github.io/recharts/Basic_Plots_03_Line.html#line-chart)
            1. [curve](http://madlogos.github.io/recharts/Basic_Plots_03_Line.html#curve-smooth-line-chart)
            1. [area](http://madlogos.github.io/recharts/Basic_Plots_03_Line.html#area-chart)
            1. [wave](http://madlogos.github.io/recharts/Basic_Plots_03_Line.html#wave-smooth-area-chart)
        1. K
            1. [k|candlestick](http://madlogos.github.io/recharts/Basic_Plots_04_K.html)
        1. eventRiver
            1. [eventRiver](http://madlogos.github.io/recharts/Basic_Plots_05_eventRiver.html)
    1. Others
        1. [Force](http://madlogos.github.io/recharts/Basic_Plots_11_Force.html)
        1. [Chord](http://madlogos.github.io/recharts/Basic_Plots_12_Chord.html)
        1. [Word Cloud](http://madlogos.github.io/recharts/Basic_Plots_13_WordCloud.html)
        1. [Venn Chart](http://madlogos.github.io/recharts/Basic_Plots_14_Venn.html)
        1. [Heatmap](http://madlogos.github.io/recharts/Basic_Plots_15_Heatmap.html)
1. Multi-coordinate System
    1. Polar Coordinate System
        1. Pie
            1. [pie](http://madlogos.github.io/recharts/Basic_Plots_21_Pie.html#pie-chart)
            1. [ring](http://madlogos.github.io/recharts/Basic_Plots_21_Pie.html#ring-chart)
            1. [Rose](http://madlogos.github.io/recharts/Basic_Plots_21_Pie.html#nightingale-rose-chart)
        1. Funnel
            1. [Funnel](http://madlogos.github.io/recharts/Basic_Plots_22_Funnel.html#funnel-chart)
            1. [Pyramid](http://madlogos.github.io/recharts/Basic_Plots_22_Funnel.html#pyramid-chart)
        1. [Radar Chart](http://madlogos.github.io/recharts/Basic_Plots_23_Radar.html)
        1. [Gauge Chart](http://madlogos.github.io/recharts/Basic_Plots_24_Gauge.html)
    1. Others
        1. [Map](http://madlogos.github.io/recharts/Basic_Plots_31_Map.html)
        1. [Tree Chart](http://madlogos.github.io/recharts/Basic_Plots_32_Tree.html)
        1. [Treemap](http://madlogos.github.io/recharts/Basic_Plots_33_Treemap.html)

## To-do

- Tool functions to configure series precisely
- Bug fix
- Optimize algorithms

# License

Under the terms of [MIT](http://www.opensource.org/licenses/mit-license.php) + file license.
