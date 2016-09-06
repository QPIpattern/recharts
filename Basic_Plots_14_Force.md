# Basic Plots 14 - Force Chart



First, you should load `recharts`:

```r
library(recharts)
```

# Introduction

Force plot includes 2 basic types:

- Force chart with curve
- Force chart with line

<table id='intro'>
<tr><td>
<!--html_preserve--><div id="echarts-4407ff1642f7f4066ebb4e053ec09482637e623e" style="width:400px;height:300px;" class="echarts html-widget"></div>
<script type="application/json" data-for="echarts-4407ff1642f7f4066ebb4e053ec09482637e623e">{"x":{"series":[{"type":"force","name":"Connection","roam":"move","itemStyle":{"normal":{"label":{"show":true,"textStyle":{"color":"#333"}},"nodeStyle":{"brushType":"both","strokeColor":"rgba(255,215,0,0.4)"},"linkStyle":{"type":"curve"}},"emphasis":{"label":{"show":false},"nodeStyle":[],"lineStyle":[]}},"minRadius":8,"maxRadius":20,"nodes":[{"category":0,"name":"曾麟书","value":3},{"category":1,"name":"曾国藩","value":9},{"category":2,"name":"曾纪泽","value":3},{"category":2,"name":"曾纪鸿","value":3},{"category":3,"name":"曾广珊","value":3},{"category":0,"name":"俞文葆","value":3},{"category":1,"name":"俞明震","value":6},{"category":1,"name":"俞明颐","value":3},{"category":1,"name":"俞明诗","value":3},{"category":0,"name":"陈宝箴","value":6},{"category":1,"name":"陈三立","value":3},{"category":2,"name":"陈寅恪","value":9},{"category":2,"name":"陈衡恪","value":3},{"category":2,"name":"俞大维","value":3},{"category":2,"name":"俞大拔","value":3},{"category":2,"name":"俞大纲","value":3},{"category":2,"name":"俞大缜","value":3},{"category":1,"name":"曾国潢","value":3},{"category":2,"name":"曾纪梁","value":3},{"category":3,"name":"曾广祚","value":3},{"category":4,"name":"曾昭抡","value":6},{"category":2,"name":"俞大絪","value":3},{"category":2,"name":"傅斯年","value":6},{"category":2,"name":"俞大彩","value":3},{"category":0,"name":"蒋介石","value":9},{"category":1,"name":"蒋经国","value":9},{"category":3,"name":"俞扬和","value":3},{"category":2,"name":"蒋孝章","value":3},{"category":4,"name":"俞祖声","value":3},{"category":2,"name":"俞大纯","value":3},{"category":1,"name":"曾国荃","value":6},{"category":2,"name":"曾广江","value":3},{"category":3,"name":"曾昭和","value":3},{"category":4,"name":"曾宪植","value":6},{"category":4,"name":"叶剑英","value":6},{"category":3,"name":"赵太侔","value":6},{"category":3,"name":"俞珊","value":3},{"category":3,"name":"俞瑾","value":3},{"category":3,"name":"俞启考","value":3},{"category":3,"name":"俞启信","value":3},{"category":3,"name":"俞启威","value":3},{"category":3,"name":"俞启忠","value":3},{"category":4,"name":"俞强声","value":3},{"category":4,"name":"俞正声","value":6},{"category":3,"name":"毛泽东","value":9},{"category":3,"name":"江青","value":6},{"category":0,"name":"范寿钟","value":3},{"category":1,"name":"范文澜","value":6},{"category":1,"name":"范瑾","value":3}],"categories":[{"name":"Root"},{"name":"Node 1"},{"name":"Node 2"},{"name":"Node 3"},{"name":"Leaf"}],"links":[{"source":"曾麟书","target":"曾国藩","name":"父子","weight":1},{"source":"曾麟书","target":"曾国荃","name":"父子","weight":1},{"source":"曾麟书","target":"曾国潢","name":"父子","weight":1},{"source":"曾国藩","target":"曾纪泽","name":"父子","weight":1},{"source":"曾国藩","target":"曾纪鸿","name":"父子","weight":1},{"source":"曾国潢","target":"曾纪梁","name":"父子","weight":1},{"source":"曾纪梁","target":"曾广祚","name":"父子","weight":1},{"source":"曾广祚","target":"曾昭抡","name":"父子","weight":1},{"source":"曾国荃","target":"曾广江","name":"父子","weight":1},{"source":"曾广江","target":"曾昭和","name":"父子","weight":1},{"source":"曾昭和","target":"曾宪植","name":"父女","weight":1},{"source":"叶剑英","target":"曾宪植","name":"夫妻","weight":1},{"source":"曾纪鸿","target":"曾广珊","name":"父女","weight":1},{"source":"俞文葆","target":"俞明震","name":"父子","weight":1},{"source":"俞文葆","target":"俞明颐","name":"父子","weight":1},{"source":"俞文葆","target":"俞明诗","name":"父女","weight":1},{"source":"陈宝箴","target":"陈三立","name":"父子","weight":1},{"source":"陈三立","target":"俞明诗","name":"夫妻","weight":1},{"source":"陈三立","target":"陈寅恪","name":"父子","weight":1},{"source":"陈三立","target":"陈衡恪","name":"父子","weight":1},{"source":"俞明颐","target":"曾广珊","name":"夫妻","weight":1},{"source":"俞明颐","target":"俞大维","name":"父子","weight":1},{"source":"俞大维","target":"俞扬和","name":"父子","weight":1},{"source":"俞明颐","target":"俞大拔","name":"父子","weight":1},{"source":"俞明颐","target":"俞大纲","name":"父子","weight":1},{"source":"俞明颐","target":"俞大缜","name":"父子","weight":1},{"source":"俞明颐","target":"俞大絪","name":"父女","weight":1},{"source":"俞明颐","target":"俞大彩","name":"父女","weight":1},{"source":"俞明震","target":"俞大纯","name":"父子","weight":1},{"source":"赵太侔","target":"俞珊","name":"夫妻","weight":1},{"source":"俞大纯","target":"俞珊","name":"父女","weight":1},{"source":"俞大纯","target":"俞瑾","name":"父女","weight":1},{"source":"俞大纯","target":"俞启考","name":"父子","weight":1},{"source":"俞大纯","target":"俞启信","name":"父子","weight":1},{"source":"俞大纯","target":"俞启威","name":"父子","weight":1},{"source":"俞启威","target":"江青","name":"夫妻","weight":1},{"source":"毛泽东","target":"江青","name":"夫妻","weight":1},{"source":"俞大纯","target":"俞启忠","name":"父子","weight":1},{"source":"俞启威","target":"俞强声","name":"父子","weight":1},{"source":"俞启威","target":"俞正声","name":"父子","weight":1},{"source":"曾昭抡","target":"俞大絪","name":"夫妻","weight":1},{"source":"傅斯年","target":"俞大彩","name":"夫妻","weight":1},{"source":"蒋介石","target":"蒋经国","name":"父子","weight":1},{"source":"蒋经国","target":"蒋孝章","name":"父女","weight":1},{"source":"俞扬和","target":"蒋孝章","name":"夫妻","weight":1},{"source":"俞扬和","target":"俞祖声","name":"父子","weight":1},{"source":"范寿钟","target":"范文澜","name":"父子","weight":1},{"source":"范寿钟","target":"范瑾","name":"父女","weight":1},{"source":"俞启威","target":"范瑾","name":"夫妻","weight":1}],"ribbonType":false,"showScale":false,"showScaleText":false}],"legend":{"show":true,"data":["Root","Node 1","Node 2","Node 3","Leaf"],"x":"left","y":"top","orient":"horizontal"},"tooltip":{"show":true,"trigger":"item","axisPointer":{"type":"none","crossStyle":{"type":"dashed"},"lineStyle":"solid"},"textStyle":{"color":"#fff"},"formatter":"function (params) {\n    if (params.indicator2) {    // is edge\n    return params.indicator2 + \" \" +\n    params.name + \" \" + params.indicator + \" : \" +\n    params.value.weight;\n    } else {    // is node\n    return params.name\n    }\n    }","backgroundColor":"rgba(0,0,0,0.7)"},"toolbox":{"show":true,"feature":{"mark":{"show":true},"dataZoom":{"show":false},"dataView":{"show":false},"magicType":{"show":true,"type":["force","chord"]},"restore":{"show":true},"saveAsImage":{"show":true}},"x":"right","y":"top","orient":"horizontal"},"title":{"text":"Yu Family of Shaoxing","subtext":"","x":"center","y":"bottom","orient":"horizontal"},"color":["#CD853F","#00CD00","#00EE00","#7CFC00","#C0FF3E"]},"evals":["tooltip.formatter"],"jsHooks":[]}</script><!--/html_preserve-->
</td>
<td>
<!--html_preserve--><div id="echarts-94827d8fe12007010faf80d673954be45ce2b105" style="width:400px;height:300px;" class="echarts html-widget"></div>
<script type="application/json" data-for="echarts-94827d8fe12007010faf80d673954be45ce2b105">{"x":{"series":[{"type":"force","name":"Connection","roam":"move","itemStyle":{"normal":{"label":{"show":true,"textStyle":{"color":"#333"}},"nodeStyle":{"brushType":"both","strokeColor":"rgba(255,215,0,0.4)"},"linkStyle":{"type":"line"}},"emphasis":{"label":{"show":false},"nodeStyle":[],"lineStyle":[]}},"minRadius":8,"maxRadius":20,"nodes":[{"category":0,"name":"曾麟书","value":3},{"category":1,"name":"曾国藩","value":9},{"category":2,"name":"曾纪泽","value":3},{"category":2,"name":"曾纪鸿","value":3},{"category":3,"name":"曾广珊","value":3},{"category":0,"name":"俞文葆","value":3},{"category":1,"name":"俞明震","value":6},{"category":1,"name":"俞明颐","value":3},{"category":1,"name":"俞明诗","value":3},{"category":0,"name":"陈宝箴","value":6},{"category":1,"name":"陈三立","value":3},{"category":2,"name":"陈寅恪","value":9},{"category":2,"name":"陈衡恪","value":3},{"category":2,"name":"俞大维","value":3},{"category":2,"name":"俞大拔","value":3},{"category":2,"name":"俞大纲","value":3},{"category":2,"name":"俞大缜","value":3},{"category":1,"name":"曾国潢","value":3},{"category":2,"name":"曾纪梁","value":3},{"category":3,"name":"曾广祚","value":3},{"category":4,"name":"曾昭抡","value":6},{"category":2,"name":"俞大絪","value":3},{"category":2,"name":"傅斯年","value":6},{"category":2,"name":"俞大彩","value":3},{"category":0,"name":"蒋介石","value":9},{"category":1,"name":"蒋经国","value":9},{"category":3,"name":"俞扬和","value":3},{"category":2,"name":"蒋孝章","value":3},{"category":4,"name":"俞祖声","value":3},{"category":2,"name":"俞大纯","value":3},{"category":1,"name":"曾国荃","value":6},{"category":2,"name":"曾广江","value":3},{"category":3,"name":"曾昭和","value":3},{"category":4,"name":"曾宪植","value":6},{"category":4,"name":"叶剑英","value":6},{"category":3,"name":"赵太侔","value":6},{"category":3,"name":"俞珊","value":3},{"category":3,"name":"俞瑾","value":3},{"category":3,"name":"俞启考","value":3},{"category":3,"name":"俞启信","value":3},{"category":3,"name":"俞启威","value":3},{"category":3,"name":"俞启忠","value":3},{"category":4,"name":"俞强声","value":3},{"category":4,"name":"俞正声","value":6},{"category":3,"name":"毛泽东","value":9},{"category":3,"name":"江青","value":6},{"category":0,"name":"范寿钟","value":3},{"category":1,"name":"范文澜","value":6},{"category":1,"name":"范瑾","value":3}],"categories":[{"name":"Root"},{"name":"Node 1"},{"name":"Node 2"},{"name":"Node 3"},{"name":"Leaf"}],"links":[{"source":"曾麟书","target":"曾国藩","name":"父子","weight":1},{"source":"曾麟书","target":"曾国荃","name":"父子","weight":1},{"source":"曾麟书","target":"曾国潢","name":"父子","weight":1},{"source":"曾国藩","target":"曾纪泽","name":"父子","weight":1},{"source":"曾国藩","target":"曾纪鸿","name":"父子","weight":1},{"source":"曾国潢","target":"曾纪梁","name":"父子","weight":1},{"source":"曾纪梁","target":"曾广祚","name":"父子","weight":1},{"source":"曾广祚","target":"曾昭抡","name":"父子","weight":1},{"source":"曾国荃","target":"曾广江","name":"父子","weight":1},{"source":"曾广江","target":"曾昭和","name":"父子","weight":1},{"source":"曾昭和","target":"曾宪植","name":"父女","weight":1},{"source":"叶剑英","target":"曾宪植","name":"夫妻","weight":1},{"source":"曾纪鸿","target":"曾广珊","name":"父女","weight":1},{"source":"俞文葆","target":"俞明震","name":"父子","weight":1},{"source":"俞文葆","target":"俞明颐","name":"父子","weight":1},{"source":"俞文葆","target":"俞明诗","name":"父女","weight":1},{"source":"陈宝箴","target":"陈三立","name":"父子","weight":1},{"source":"陈三立","target":"俞明诗","name":"夫妻","weight":1},{"source":"陈三立","target":"陈寅恪","name":"父子","weight":1},{"source":"陈三立","target":"陈衡恪","name":"父子","weight":1},{"source":"俞明颐","target":"曾广珊","name":"夫妻","weight":1},{"source":"俞明颐","target":"俞大维","name":"父子","weight":1},{"source":"俞大维","target":"俞扬和","name":"父子","weight":1},{"source":"俞明颐","target":"俞大拔","name":"父子","weight":1},{"source":"俞明颐","target":"俞大纲","name":"父子","weight":1},{"source":"俞明颐","target":"俞大缜","name":"父子","weight":1},{"source":"俞明颐","target":"俞大絪","name":"父女","weight":1},{"source":"俞明颐","target":"俞大彩","name":"父女","weight":1},{"source":"俞明震","target":"俞大纯","name":"父子","weight":1},{"source":"赵太侔","target":"俞珊","name":"夫妻","weight":1},{"source":"俞大纯","target":"俞珊","name":"父女","weight":1},{"source":"俞大纯","target":"俞瑾","name":"父女","weight":1},{"source":"俞大纯","target":"俞启考","name":"父子","weight":1},{"source":"俞大纯","target":"俞启信","name":"父子","weight":1},{"source":"俞大纯","target":"俞启威","name":"父子","weight":1},{"source":"俞启威","target":"江青","name":"夫妻","weight":1},{"source":"毛泽东","target":"江青","name":"夫妻","weight":1},{"source":"俞大纯","target":"俞启忠","name":"父子","weight":1},{"source":"俞启威","target":"俞强声","name":"父子","weight":1},{"source":"俞启威","target":"俞正声","name":"父子","weight":1},{"source":"曾昭抡","target":"俞大絪","name":"夫妻","weight":1},{"source":"傅斯年","target":"俞大彩","name":"夫妻","weight":1},{"source":"蒋介石","target":"蒋经国","name":"父子","weight":1},{"source":"蒋经国","target":"蒋孝章","name":"父女","weight":1},{"source":"俞扬和","target":"蒋孝章","name":"夫妻","weight":1},{"source":"俞扬和","target":"俞祖声","name":"父子","weight":1},{"source":"范寿钟","target":"范文澜","name":"父子","weight":1},{"source":"范寿钟","target":"范瑾","name":"父女","weight":1},{"source":"俞启威","target":"范瑾","name":"夫妻","weight":1}],"ribbonType":false,"showScale":false,"showScaleText":false}],"legend":{"show":true,"data":["Root","Node 1","Node 2","Node 3","Leaf"],"x":"left","y":"top","orient":"horizontal"},"tooltip":{"show":true,"trigger":"item","axisPointer":{"type":"none","crossStyle":{"type":"dashed"},"lineStyle":"solid"},"textStyle":{"color":"#fff"},"formatter":"function (params) {\n    if (params.indicator2) {    // is edge\n    return params.indicator2 + \" \" +\n    params.name + \" \" + params.indicator + \" : \" +\n    params.value.weight;\n    } else {    // is node\n    return params.name\n    }\n    }","backgroundColor":"rgba(0,0,0,0.7)"},"toolbox":{"show":true,"feature":{"mark":{"show":true},"dataZoom":{"show":false},"dataView":{"show":false},"magicType":{"show":true,"type":["force","chord"]},"restore":{"show":true},"saveAsImage":{"show":true}},"x":"right","y":"top","orient":"horizontal"},"title":{"text":"Yu Family of Shaoxing","subtext":"","x":"center","y":"bottom","orient":"horizontal"},"color":["#CD853F","#00CD00","#00EE00","#7CFC00","#C0FF3E"]},"evals":["tooltip.formatter"],"jsHooks":[]}</script><!--/html_preserve-->
</td></tr>
</table>

The keys are:

- data structure:
  - matrix mode: A data.frame comprising of a column of name, and a numeric matrix. Assign the name column to x, the matrix to y.
  - node/link mode: node data.frame [x, NA, series, weight]; link data.frame [x, x1, relation, value]. Combine them using `rbind`. If you don't provide node data.frame, recharts will build it automatically. Assign the param list [x, x1, series/relation, weight/value] accordingly.
- force chart and chord chart are exchangeble by the toolbox buttons.

# Function Call

```r
echartr(data, x, <y>, <series>, <z>, <type>, <subtype>)
```

+--------+--------------------------------------------------------------------+
| Arg    |  Requirement                                                       |
+========+====================================================================+
|**data**| source data in the form of data.frame |
+--------+--------------------------------------------------------------------+
| **x**  | character independent variable. Other type will be coerced to factors. For node/link mode, you must provide two columns of `x`. For matrix mode, only the first column of `x` is accepted. |
+--------+--------------------------------------------------------------------+
| **y**  | numeric dependent variable. For node/link mode, only the first column of `y` is accepted. For matrix mode, all the columns of `y` are accepted. |
+--------+--------------------------------------------------------------------+
| series | series variable which will be coerced to factors. Each level of `series` is treated as a subsetting factor to produce separate pies. Only the first one is accepted if multiple variables are provided. |
+--------+--------------------------------------------------------------------+
|  z     | timeline variable which will be coerced to factors. Only the first one is accepted if multiple variables are provided. |
+--------+--------------------------------------------------------------------+
| type   | 'force'/'force_curve', 'force_line'. |
+--------+--------------------------------------------------------------------+
| subtype| - radar: c("arrow", "triangle") | 
|        |     + arrow: The end symbol of the connection lines is arrow. |
|        |     + triangle: The end symbol of the connection lines is triangle |
+--------+--------------------------------------------------------------------+

# Showcase

## Data Preparation


### Matrix Mode


```r
grpmtx <- matrix(c(11975, 5871, 8916, 2868, 1951, 10048, 2060, 6171, 8010, 16145,
                   8090, 8045, 1013, 990, 940, 6907), byrow=TRUE, nrow=4)
grpmtx <- as.data.frame(grpmtx)
names(grpmtx) <- paste0('Group', 1:4)
grpmtx$Name <- paste0('Group', 1:4)
knitr::kable(grpmtx, align=c('lllll'))
```



Group1   Group2   Group3   Group4   Name   
-------  -------  -------  -------  -------
11975    5871     8916     2868     Group1 
1951     10048    2060     6171     Group2 
8010     16145    8090     8045     Group3 
1013     990      940      6907     Group4 

The first 4 columns are exactly a matrix structure and the last column is a name vector. So this meets data structure requirements for matrix mode.

Matrix mode can be transformed to node/link mode as well. Matrix[i, j] represents 2 nodes (i & j) and 1 link (i -> j).

### Node/link Mode


```r
str(yuNetwork)
```

```
## List of 2
##  $ nodes:'data.frame':	49 obs. of  3 variables:
##   ..$ name  : chr [1:49] "曾麟书" "曾国藩" "曾纪泽" "曾纪鸿" ...
##   ..$ series: chr [1:49] "Root" "Node 1" "Node 2" "Node 2" ...
##   ..$ value : num [1:49] 3 9 3 3 3 3 6 3 3 6 ...
##  $ links:'data.frame':	49 obs. of  4 variables:
##   ..$ source  : chr [1:49] "曾麟书" "曾麟书" "曾麟书" "曾国藩" ...
##   ..$ target  : chr [1:49] "曾国藩" "曾国荃" "曾国潢" "曾纪泽" ...
##   ..$ relation: chr [1:49] "父子" "父子" "父子" "父子" ...
##   ..$ weight  : num [1:49] 1 1 1 1 1 1 1 1 1 1 ...
```

The yuNetwork dataset contains a nodes data.frame and a links data.frame. You can then combine them into one.

- nodes: 
    - `name`: the nodes name, 
    - `series`: the series that the nodes belongs to, 
    - `value`: the importance score of the nodes.
- links: 
    - `source` and `target`: defines the connections, 
    - `relation`: the name of the connections, 
    - `weight`: the importance sorce of the connections.


```r
nodes <- cbind(yuNetwork$nodes[,1], NA, yuNetwork$nodes[,2:3],
               stringsAsFactors=FALSE)
names(nodes) <- names(yuNetwork$links)
yu <- rbind(yuNetwork$links, nodes, stringsAsFactors=FALSE)
```


## Force Chart

### Force with Curve

Set `type` 'force'.


```r
echartr(yu, c(source, target), weight, relation, type='force') %>% 
    setTitle("Yu Family of Shaoxing") %>% setTheme(palette=c(
        'tan3','green3','green2','lawngreen','olivedrab1'))
```

<!--html_preserve--><div id="echarts-da22f16343fc1f41f69b6bcad9fbbbb155e66b76" style="width:672px;height:480px;" class="echarts html-widget"></div>
<script type="application/json" data-for="echarts-da22f16343fc1f41f69b6bcad9fbbbb155e66b76">{"x":{"series":[{"type":"force","name":"Connection","roam":"move","itemStyle":{"normal":{"label":{"show":true,"textStyle":{"color":"#333"}},"nodeStyle":{"brushType":"both","strokeColor":"rgba(255,215,0,0.4)"},"linkStyle":{"type":"curve"}},"emphasis":{"label":{"show":false},"nodeStyle":[],"lineStyle":[]}},"minRadius":8,"maxRadius":20,"nodes":[{"category":0,"name":"曾麟书","value":3},{"category":1,"name":"曾国藩","value":9},{"category":2,"name":"曾纪泽","value":3},{"category":2,"name":"曾纪鸿","value":3},{"category":3,"name":"曾广珊","value":3},{"category":0,"name":"俞文葆","value":3},{"category":1,"name":"俞明震","value":6},{"category":1,"name":"俞明颐","value":3},{"category":1,"name":"俞明诗","value":3},{"category":0,"name":"陈宝箴","value":6},{"category":1,"name":"陈三立","value":3},{"category":2,"name":"陈寅恪","value":9},{"category":2,"name":"陈衡恪","value":3},{"category":2,"name":"俞大维","value":3},{"category":2,"name":"俞大拔","value":3},{"category":2,"name":"俞大纲","value":3},{"category":2,"name":"俞大缜","value":3},{"category":1,"name":"曾国潢","value":3},{"category":2,"name":"曾纪梁","value":3},{"category":3,"name":"曾广祚","value":3},{"category":4,"name":"曾昭抡","value":6},{"category":2,"name":"俞大絪","value":3},{"category":2,"name":"傅斯年","value":6},{"category":2,"name":"俞大彩","value":3},{"category":0,"name":"蒋介石","value":9},{"category":1,"name":"蒋经国","value":9},{"category":3,"name":"俞扬和","value":3},{"category":2,"name":"蒋孝章","value":3},{"category":4,"name":"俞祖声","value":3},{"category":2,"name":"俞大纯","value":3},{"category":1,"name":"曾国荃","value":6},{"category":2,"name":"曾广江","value":3},{"category":3,"name":"曾昭和","value":3},{"category":4,"name":"曾宪植","value":6},{"category":4,"name":"叶剑英","value":6},{"category":3,"name":"赵太侔","value":6},{"category":3,"name":"俞珊","value":3},{"category":3,"name":"俞瑾","value":3},{"category":3,"name":"俞启考","value":3},{"category":3,"name":"俞启信","value":3},{"category":3,"name":"俞启威","value":3},{"category":3,"name":"俞启忠","value":3},{"category":4,"name":"俞强声","value":3},{"category":4,"name":"俞正声","value":6},{"category":3,"name":"毛泽东","value":9},{"category":3,"name":"江青","value":6},{"category":0,"name":"范寿钟","value":3},{"category":1,"name":"范文澜","value":6},{"category":1,"name":"范瑾","value":3}],"categories":[{"name":"Root"},{"name":"Node 1"},{"name":"Node 2"},{"name":"Node 3"},{"name":"Leaf"}],"links":[{"source":"曾麟书","target":"曾国藩","name":"父子","weight":1},{"source":"曾麟书","target":"曾国荃","name":"父子","weight":1},{"source":"曾麟书","target":"曾国潢","name":"父子","weight":1},{"source":"曾国藩","target":"曾纪泽","name":"父子","weight":1},{"source":"曾国藩","target":"曾纪鸿","name":"父子","weight":1},{"source":"曾国潢","target":"曾纪梁","name":"父子","weight":1},{"source":"曾纪梁","target":"曾广祚","name":"父子","weight":1},{"source":"曾广祚","target":"曾昭抡","name":"父子","weight":1},{"source":"曾国荃","target":"曾广江","name":"父子","weight":1},{"source":"曾广江","target":"曾昭和","name":"父子","weight":1},{"source":"曾昭和","target":"曾宪植","name":"父女","weight":1},{"source":"叶剑英","target":"曾宪植","name":"夫妻","weight":1},{"source":"曾纪鸿","target":"曾广珊","name":"父女","weight":1},{"source":"俞文葆","target":"俞明震","name":"父子","weight":1},{"source":"俞文葆","target":"俞明颐","name":"父子","weight":1},{"source":"俞文葆","target":"俞明诗","name":"父女","weight":1},{"source":"陈宝箴","target":"陈三立","name":"父子","weight":1},{"source":"陈三立","target":"俞明诗","name":"夫妻","weight":1},{"source":"陈三立","target":"陈寅恪","name":"父子","weight":1},{"source":"陈三立","target":"陈衡恪","name":"父子","weight":1},{"source":"俞明颐","target":"曾广珊","name":"夫妻","weight":1},{"source":"俞明颐","target":"俞大维","name":"父子","weight":1},{"source":"俞大维","target":"俞扬和","name":"父子","weight":1},{"source":"俞明颐","target":"俞大拔","name":"父子","weight":1},{"source":"俞明颐","target":"俞大纲","name":"父子","weight":1},{"source":"俞明颐","target":"俞大缜","name":"父子","weight":1},{"source":"俞明颐","target":"俞大絪","name":"父女","weight":1},{"source":"俞明颐","target":"俞大彩","name":"父女","weight":1},{"source":"俞明震","target":"俞大纯","name":"父子","weight":1},{"source":"赵太侔","target":"俞珊","name":"夫妻","weight":1},{"source":"俞大纯","target":"俞珊","name":"父女","weight":1},{"source":"俞大纯","target":"俞瑾","name":"父女","weight":1},{"source":"俞大纯","target":"俞启考","name":"父子","weight":1},{"source":"俞大纯","target":"俞启信","name":"父子","weight":1},{"source":"俞大纯","target":"俞启威","name":"父子","weight":1},{"source":"俞启威","target":"江青","name":"夫妻","weight":1},{"source":"毛泽东","target":"江青","name":"夫妻","weight":1},{"source":"俞大纯","target":"俞启忠","name":"父子","weight":1},{"source":"俞启威","target":"俞强声","name":"父子","weight":1},{"source":"俞启威","target":"俞正声","name":"父子","weight":1},{"source":"曾昭抡","target":"俞大絪","name":"夫妻","weight":1},{"source":"傅斯年","target":"俞大彩","name":"夫妻","weight":1},{"source":"蒋介石","target":"蒋经国","name":"父子","weight":1},{"source":"蒋经国","target":"蒋孝章","name":"父女","weight":1},{"source":"俞扬和","target":"蒋孝章","name":"夫妻","weight":1},{"source":"俞扬和","target":"俞祖声","name":"父子","weight":1},{"source":"范寿钟","target":"范文澜","name":"父子","weight":1},{"source":"范寿钟","target":"范瑾","name":"父女","weight":1},{"source":"俞启威","target":"范瑾","name":"夫妻","weight":1}],"ribbonType":false,"showScale":false,"showScaleText":false}],"legend":{"show":true,"data":["Root","Node 1","Node 2","Node 3","Leaf"],"x":"left","y":"top","orient":"horizontal"},"tooltip":{"show":true,"trigger":"item","axisPointer":{"type":"none","crossStyle":{"type":"dashed"},"lineStyle":"solid"},"textStyle":{"color":"#fff"},"formatter":"function (params) {\n    if (params.indicator2) {    // is edge\n    return params.indicator2 + \" \" +\n    params.name + \" \" + params.indicator + \" : \" +\n    params.value.weight;\n    } else {    // is node\n    return params.name\n    }\n    }","backgroundColor":"rgba(0,0,0,0.7)"},"toolbox":{"show":true,"feature":{"mark":{"show":true},"dataZoom":{"show":false},"dataView":{"show":false},"magicType":{"show":true,"type":["force","chord"]},"restore":{"show":true},"saveAsImage":{"show":true}},"x":"right","y":"top","orient":"horizontal"},"title":{"text":"Yu Family of Shaoxing","subtext":"","x":"center","y":"bottom","orient":"horizontal"},"color":["#CD853F","#00CD00","#00EE00","#7CFC00","#C0FF3E"]},"evals":["tooltip.formatter"],"jsHooks":[]}</script><!--/html_preserve-->

### Force with Line

#### Matrix Mode


```r
echartr(grpmtx, Name, c(Group1, Group2, Group3, Group4), type='force_line') %>% 
  setTitle('Test Data', 'Force with ribbon')
```

<!--html_preserve--><div id="echarts-8643c1d086f57b9b6d1a0e8fd588f50bd9469f1a" style="width:672px;height:480px;" class="echarts html-widget"></div>
<script type="application/json" data-for="echarts-8643c1d086f57b9b6d1a0e8fd588f50bd9469f1a">{"x":{"series":[{"type":"force","name":"Connection","roam":"move","itemStyle":{"normal":{"label":{"show":true,"textStyle":{"color":"#333"}},"nodeStyle":{"brushType":"both","strokeColor":"rgba(255,215,0,0.4)"},"linkStyle":{"type":"line"}},"emphasis":{"label":{"show":false},"nodeStyle":[],"lineStyle":[]}},"minRadius":8,"maxRadius":20,"matrix":[[11975,5871,8916,2868],[1951,10048,2060,6171],[8010,16145,8090,8045],[1013,990,940,6907]],"data":[{"name":"Group1"},{"name":"Group2"},{"name":"Group3"},{"name":"Group4"}],"ribbonType":true,"showScale":false,"showScaleText":false}],"tooltip":{"show":true,"trigger":"item","axisPointer":{"type":"none","crossStyle":{"type":"dashed"},"lineStyle":"solid"},"textStyle":{"color":"#fff"},"formatter":"function (params) {\n    if (params.indicator2) {    // is edge\n    return params.indicator2 + \" \" +\n    params.name + \" \" + params.indicator + \" : \" +\n    params.value.weight;\n    } else {    // is node\n    return params.name\n    }\n    }","backgroundColor":"rgba(0,0,0,0.7)"},"toolbox":{"show":true,"feature":{"mark":{"show":true},"dataZoom":{"show":false},"dataView":{"show":false},"magicType":{"show":true,"type":["force","chord"]},"restore":{"show":true},"saveAsImage":{"show":true}},"x":"right","y":"top","orient":"horizontal"},"legend":{"show":true,"data":["Group1","Group2","Group3","Group4"],"x":"left","y":"top","orient":"horizontal"},"title":{"text":"Test Data","subtext":"Force with ribbon","x":"center","y":"bottom","orient":"horizontal"}},"evals":["tooltip.formatter"],"jsHooks":[]}</script><!--/html_preserve-->

#### Node/link Mode

Set `type` 'force_line'.


```r
echartr(yu, c(source, target), weight, relation, type='force_line') %>% 
    setTitle("Yu Family of Shaoxing") %>% setTheme(palette=c(
        'tan3','green3','green2','lawngreen','olivedrab1'))
```

<!--html_preserve--><div id="echarts-5ca5a69ca75ad096cf8a5447d8c7c6be766cc6c1" style="width:672px;height:480px;" class="echarts html-widget"></div>
<script type="application/json" data-for="echarts-5ca5a69ca75ad096cf8a5447d8c7c6be766cc6c1">{"x":{"series":[{"type":"force","name":"Connection","roam":"move","itemStyle":{"normal":{"label":{"show":true,"textStyle":{"color":"#333"}},"nodeStyle":{"brushType":"both","strokeColor":"rgba(255,215,0,0.4)"},"linkStyle":{"type":"line"}},"emphasis":{"label":{"show":false},"nodeStyle":[],"lineStyle":[]}},"minRadius":8,"maxRadius":20,"nodes":[{"category":0,"name":"曾麟书","value":3},{"category":1,"name":"曾国藩","value":9},{"category":2,"name":"曾纪泽","value":3},{"category":2,"name":"曾纪鸿","value":3},{"category":3,"name":"曾广珊","value":3},{"category":0,"name":"俞文葆","value":3},{"category":1,"name":"俞明震","value":6},{"category":1,"name":"俞明颐","value":3},{"category":1,"name":"俞明诗","value":3},{"category":0,"name":"陈宝箴","value":6},{"category":1,"name":"陈三立","value":3},{"category":2,"name":"陈寅恪","value":9},{"category":2,"name":"陈衡恪","value":3},{"category":2,"name":"俞大维","value":3},{"category":2,"name":"俞大拔","value":3},{"category":2,"name":"俞大纲","value":3},{"category":2,"name":"俞大缜","value":3},{"category":1,"name":"曾国潢","value":3},{"category":2,"name":"曾纪梁","value":3},{"category":3,"name":"曾广祚","value":3},{"category":4,"name":"曾昭抡","value":6},{"category":2,"name":"俞大絪","value":3},{"category":2,"name":"傅斯年","value":6},{"category":2,"name":"俞大彩","value":3},{"category":0,"name":"蒋介石","value":9},{"category":1,"name":"蒋经国","value":9},{"category":3,"name":"俞扬和","value":3},{"category":2,"name":"蒋孝章","value":3},{"category":4,"name":"俞祖声","value":3},{"category":2,"name":"俞大纯","value":3},{"category":1,"name":"曾国荃","value":6},{"category":2,"name":"曾广江","value":3},{"category":3,"name":"曾昭和","value":3},{"category":4,"name":"曾宪植","value":6},{"category":4,"name":"叶剑英","value":6},{"category":3,"name":"赵太侔","value":6},{"category":3,"name":"俞珊","value":3},{"category":3,"name":"俞瑾","value":3},{"category":3,"name":"俞启考","value":3},{"category":3,"name":"俞启信","value":3},{"category":3,"name":"俞启威","value":3},{"category":3,"name":"俞启忠","value":3},{"category":4,"name":"俞强声","value":3},{"category":4,"name":"俞正声","value":6},{"category":3,"name":"毛泽东","value":9},{"category":3,"name":"江青","value":6},{"category":0,"name":"范寿钟","value":3},{"category":1,"name":"范文澜","value":6},{"category":1,"name":"范瑾","value":3}],"categories":[{"name":"Root"},{"name":"Node 1"},{"name":"Node 2"},{"name":"Node 3"},{"name":"Leaf"}],"links":[{"source":"曾麟书","target":"曾国藩","name":"父子","weight":1},{"source":"曾麟书","target":"曾国荃","name":"父子","weight":1},{"source":"曾麟书","target":"曾国潢","name":"父子","weight":1},{"source":"曾国藩","target":"曾纪泽","name":"父子","weight":1},{"source":"曾国藩","target":"曾纪鸿","name":"父子","weight":1},{"source":"曾国潢","target":"曾纪梁","name":"父子","weight":1},{"source":"曾纪梁","target":"曾广祚","name":"父子","weight":1},{"source":"曾广祚","target":"曾昭抡","name":"父子","weight":1},{"source":"曾国荃","target":"曾广江","name":"父子","weight":1},{"source":"曾广江","target":"曾昭和","name":"父子","weight":1},{"source":"曾昭和","target":"曾宪植","name":"父女","weight":1},{"source":"叶剑英","target":"曾宪植","name":"夫妻","weight":1},{"source":"曾纪鸿","target":"曾广珊","name":"父女","weight":1},{"source":"俞文葆","target":"俞明震","name":"父子","weight":1},{"source":"俞文葆","target":"俞明颐","name":"父子","weight":1},{"source":"俞文葆","target":"俞明诗","name":"父女","weight":1},{"source":"陈宝箴","target":"陈三立","name":"父子","weight":1},{"source":"陈三立","target":"俞明诗","name":"夫妻","weight":1},{"source":"陈三立","target":"陈寅恪","name":"父子","weight":1},{"source":"陈三立","target":"陈衡恪","name":"父子","weight":1},{"source":"俞明颐","target":"曾广珊","name":"夫妻","weight":1},{"source":"俞明颐","target":"俞大维","name":"父子","weight":1},{"source":"俞大维","target":"俞扬和","name":"父子","weight":1},{"source":"俞明颐","target":"俞大拔","name":"父子","weight":1},{"source":"俞明颐","target":"俞大纲","name":"父子","weight":1},{"source":"俞明颐","target":"俞大缜","name":"父子","weight":1},{"source":"俞明颐","target":"俞大絪","name":"父女","weight":1},{"source":"俞明颐","target":"俞大彩","name":"父女","weight":1},{"source":"俞明震","target":"俞大纯","name":"父子","weight":1},{"source":"赵太侔","target":"俞珊","name":"夫妻","weight":1},{"source":"俞大纯","target":"俞珊","name":"父女","weight":1},{"source":"俞大纯","target":"俞瑾","name":"父女","weight":1},{"source":"俞大纯","target":"俞启考","name":"父子","weight":1},{"source":"俞大纯","target":"俞启信","name":"父子","weight":1},{"source":"俞大纯","target":"俞启威","name":"父子","weight":1},{"source":"俞启威","target":"江青","name":"夫妻","weight":1},{"source":"毛泽东","target":"江青","name":"夫妻","weight":1},{"source":"俞大纯","target":"俞启忠","name":"父子","weight":1},{"source":"俞启威","target":"俞强声","name":"父子","weight":1},{"source":"俞启威","target":"俞正声","name":"父子","weight":1},{"source":"曾昭抡","target":"俞大絪","name":"夫妻","weight":1},{"source":"傅斯年","target":"俞大彩","name":"夫妻","weight":1},{"source":"蒋介石","target":"蒋经国","name":"父子","weight":1},{"source":"蒋经国","target":"蒋孝章","name":"父女","weight":1},{"source":"俞扬和","target":"蒋孝章","name":"夫妻","weight":1},{"source":"俞扬和","target":"俞祖声","name":"父子","weight":1},{"source":"范寿钟","target":"范文澜","name":"父子","weight":1},{"source":"范寿钟","target":"范瑾","name":"父女","weight":1},{"source":"俞启威","target":"范瑾","name":"夫妻","weight":1}],"ribbonType":false,"showScale":false,"showScaleText":false}],"legend":{"show":true,"data":["Root","Node 1","Node 2","Node 3","Leaf"],"x":"left","y":"top","orient":"horizontal"},"tooltip":{"show":true,"trigger":"item","axisPointer":{"type":"none","crossStyle":{"type":"dashed"},"lineStyle":"solid"},"textStyle":{"color":"#fff"},"formatter":"function (params) {\n    if (params.indicator2) {    // is edge\n    return params.indicator2 + \" \" +\n    params.name + \" \" + params.indicator + \" : \" +\n    params.value.weight;\n    } else {    // is node\n    return params.name\n    }\n    }","backgroundColor":"rgba(0,0,0,0.7)"},"toolbox":{"show":true,"feature":{"mark":{"show":true},"dataZoom":{"show":false},"dataView":{"show":false},"magicType":{"show":true,"type":["force","chord"]},"restore":{"show":true},"saveAsImage":{"show":true}},"x":"right","y":"top","orient":"horizontal"},"title":{"text":"Yu Family of Shaoxing","subtext":"","x":"center","y":"bottom","orient":"horizontal"},"color":["#CD853F","#00CD00","#00EE00","#7CFC00","#C0FF3E"]},"evals":["tooltip.formatter"],"jsHooks":[]}</script><!--/html_preserve-->


### Force with Timeline

Let's use `year` columns as timeline.


```r
echartr(deutsch, c(club, player), weight, role, z=year,
        type='force', sub='arrow') %>% 
  setTitle('Club Orientation of Deutsch Soccer Team')
```

<!--html_preserve--><div id="echarts-6bfb90d462fba30d61d9ed03eff7f9fa8163cc78" style="width:672px;height:480px;" class="echarts html-widget"></div>
<script type="application/json" data-for="echarts-6bfb90d462fba30d61d9ed03eff7f9fa8163cc78">{"x":{"timeline":{"type":"number","data":[2014,2016],"x":80,"x2":80,"y2":50},"options":[{"series":[{"type":"force","name":"Connection","roam":"move","itemStyle":{"normal":{"label":{"show":true,"textStyle":{"color":"#333"}},"nodeStyle":{"brushType":"both","strokeColor":"rgba(255,215,0,0.4)"},"linkStyle":{"type":"curve"}},"emphasis":{"label":{"show":false},"nodeStyle":[],"lineStyle":[]}},"minRadius":8,"maxRadius":20,"nodes":[{"name":"Monchengladbach"},{"name":"Bayern"},{"name":"Dortmund"},{"name":"Kruse"},{"name":"Kramer"},{"name":"Neuer"},{"name":"Boateng"},{"name":"Lahm"},{"name":"Kroos"},{"name":"Muller"},{"name":"Gotze"},{"name":"Badstuber"},{"name":"Hummels"},{"name":"Weidenfeller"},{"name":"Reus"},{"name":"Gundogan"}],"links":[{"source":"Monchengladbach","target":"Kruse","name":"Fw","weight":1},{"source":"Monchengladbach","target":"Kramer","name":"Mf","weight":1},{"source":"Bayern","target":"Neuer","name":"Gk","weight":1},{"source":"Bayern","target":"Boateng","name":"Df","weight":1},{"source":"Bayern","target":"Lahm","name":"Df","weight":1},{"source":"Bayern","target":"Kroos","name":"Mf","weight":1},{"source":"Bayern","target":"Muller","name":"Mf","weight":1},{"source":"Bayern","target":"Gotze","name":"Fw","weight":1},{"source":"Bayern","target":"Badstuber","name":"Df","weight":1},{"source":"Dortmund","target":"Hummels","name":"Df","weight":1},{"source":"Dortmund","target":"Weidenfeller","name":"Gk","weight":1},{"source":"Dortmund","target":"Reus","name":"Df","weight":1},{"source":"Dortmund","target":"Gundogan","name":"Md","weight":1}],"linkSymbol":"arrow","ribbonType":false,"showScale":false,"showScaleText":false}],"legend":{"show":true,"data":[],"x":"left","y":"top","orient":"horizontal"},"tooltip":{"show":true,"trigger":"item","axisPointer":{"type":"none","crossStyle":{"type":"dashed"},"lineStyle":"solid"},"textStyle":{"color":"#fff"},"formatter":"function (params) {\n    if (params.indicator2) {    // is edge\n    return params.indicator2 + \" \" +\n    params.name + \" \" + params.indicator + \" : \" +\n    params.value.weight;\n    } else {    // is node\n    return params.name\n    }\n    }","backgroundColor":"rgba(0,0,0,0.7)"},"toolbox":{"show":true,"feature":{"mark":{"show":true},"dataZoom":{"show":false},"dataView":{"show":false},"magicType":{"show":true,"type":["force","chord"]},"restore":{"show":true},"saveAsImage":{"show":true}},"x":"right","y":"top","orient":"horizontal"},"title":{"text":"Club Orientation of Deutsch Soccer Team ( = 2014)","subtext":"","x":"center","y":"bottom","orient":"horizontal"}},{"series":[{"type":"force","name":"Connection","roam":"move","itemStyle":{"normal":{"label":{"show":true,"textStyle":{"color":"#333"}},"nodeStyle":{"brushType":"both","strokeColor":"rgba(255,215,0,0.4)"},"linkStyle":{"type":"curve"}},"emphasis":{"label":{"show":false},"nodeStyle":[],"lineStyle":[]}},"minRadius":8,"maxRadius":20,"nodes":[{"name":"Bayern"},{"name":"Leverkusen"},{"name":"Schalke"},{"name":"Arsenal"},{"name":"Madrid"},{"name":"Dortmund"},{"name":"Neuer"},{"name":"Leno"},{"name":"Hummels"},{"name":"Kimmich"},{"name":"Howedes"},{"name":"Mustafi"},{"name":"Ozil"},{"name":"Tah"},{"name":"Muller"},{"name":"Meyer"},{"name":"Kroos"},{"name":"Gotze"},{"name":"Volland"}],"links":[{"source":"Bayern","target":"Neuer","name":"Gk","weight":1},{"source":"Leverkusen","target":"Leno","name":"Gk","weight":1},{"source":"Bayern","target":"Hummels","name":"Df","weight":1},{"source":"Bayern","target":"Kimmich","name":"Df","weight":1},{"source":"Schalke","target":"Howedes","name":"Df","weight":1},{"source":"Arsenal","target":"Mustafi","name":"Df","weight":1},{"source":"Arsenal","target":"Ozil","name":"Mf","weight":1},{"source":"Leverkusen","target":"Tah","name":"Mf","weight":1},{"source":"Bayern","target":"Muller","name":"Mf","weight":1},{"source":"Schalke","target":"Meyer","name":"Mf","weight":1},{"source":"Madrid","target":"Kroos","name":"Mf","weight":1},{"source":"Dortmund","target":"Gotze","name":"Fw","weight":1},{"source":"Leverkusen","target":"Volland","name":"Fw","weight":1}],"linkSymbol":"arrow","ribbonType":false,"showScale":false,"showScaleText":false}],"title":{"text":"Club Orientation of Deutsch Soccer Team ( = 2016)","subtext":"","x":"center","y":"bottom","orient":"horizontal"}}]},"evals":["options.0.tooltip.formatter"],"jsHooks":[]}</script><!--/html_preserve-->

# Futher Setup

Then you can configure the widgets, add markLines and/or markPoints, fortify the chart.

You can refer to related functions to play around on your own.

