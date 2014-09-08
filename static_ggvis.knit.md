---
title: "static_ggvis"
---


```r
library(ggvis)
library(dplyr)

cocaine %>% 
  mutate(price_wt = price/weight) %>% 
  group_by(state) %>% 
  summarise(m_price = mean(price_wt)) %>% 
  arrange(desc(m_price)) %>%
  mutate(rank = 1:45) %>%
  ggvis(x = ~m_price, y = ~state) %>%
  layer_points()
```

<!--html_preserve--><div id="plot_id752473013-container" class="ggvis-output-container">
<div id="plot_id752473013" class="ggvis-output"></div>
<div class="plot-gear-icon">
<nav class="ggvis-control">
<a class="ggvis-dropdown-toggle" title="Controls" onclick="return false;"></a>
<ul class="ggvis-dropdown">
<li>
Renderer: 
<a id="plot_id752473013_renderer_svg" class="ggvis-renderer-button" onclick="return false;" data-plot-id="plot_id752473013" data-renderer="svg">SVG</a>
 | 
<a id="plot_id752473013_renderer_canvas" class="ggvis-renderer-button" onclick="return false;" data-plot-id="plot_id752473013" data-renderer="canvas">Canvas</a>
</li>
<li>
<a id="plot_id752473013_download" class="ggvis-download" data-plot-id="plot_id752473013">Download</a>
</li>
</ul>
</nav>
</div>
</div>
<script type="text/javascript">
var plot_id752473013_spec = {
	"data" : [
		{
			"name" : "cocaine %&gt;% mutate(price_wt = price/weight) %&gt;% group_by(state) %&gt;%     summarise(m_price = mean(price_wt)) %&gt;% arrange(desc(m_price)) %&gt;%     mutate(rank = 1:45)0",
			"format" : {
				"type" : "csv",
				"parse" : {
					"m_price" : "number"
				}
			},
			"values" : "\"m_price\",\"state\"\n142.876232563733,\"ME\"\n107.774846325304,\"WV\"\n100,\"SD\"\n85.4977366515086,\"FL\"\n83.4330470657137,\"IA\"\n78.6363636363636,\"UT\"\n77.6049591360325,\"MA\"\n72.4049659686296,\"VA\"\n71.9725056362482,\"MN\"\n71.7034548959077,\"NH\"\n71.1996891996892,\"HI\"\n69.4698528925259,\"PA\"\n68.6646128382718,\"DC\"\n64.8799629096382,\"MO\"\n64.6432216105021,\"AL\"\n64.5794746978873,\"OH\"\n63.8858982619298,\"NY\"\n58.811537432466,\"IN\"\n56.4429440538123,\"MS\"\n55.5933990851584,\"NJ\"\n54.0187824817492,\"TX\"\n51.1620206813875,\"TN\"\n50.0677331282277,\"OK\"\n50,\"MT\"\n49.7678768562166,\"MD\"\n49.6724989915672,\"CT\"\n49.1462793068298,\"AK\"\n45.7769896571711,\"WI\"\n43.815152799064,\"MI\"\n43.1388611388611,\"DE\"\n41.1768318682678,\"KY\"\n40.8073360331425,\"RI\"\n39.4557150508207,\"NC\"\n38.9098317537178,\"GA\"\n38.4484175040942,\"IL\"\n38.3686082441865,\"WA\"\n36.9854923429307,\"LA\"\n35.0800018556095,\"SC\"\n30.8726708074534,\"KS\"\n30.3772899439212,\"CA\"\n29.6397941680961,\"AR\"\n28.9154981546103,\"NV\"\n28.6355619688953,\"AZ\"\n24.0740740740741,\"OR\"\n21.8390804597701,\"NM\""
		},
		{
			"name" : "scale/x",
			"format" : {
				"type" : "csv",
				"parse" : {
					"domain" : "number"
				}
			},
			"values" : "\"domain\"\n15.787222854572\n148.928090168931"
		},
		{
			"name" : "scale/y",
			"format" : {
				"type" : "csv",
				"parse" : null
			},
			"values" : "\"domain\"\n\"ME\"\n\"WV\"\n\"SD\"\n\"FL\"\n\"IA\"\n\"UT\"\n\"MA\"\n\"VA\"\n\"MN\"\n\"NH\"\n\"HI\"\n\"PA\"\n\"DC\"\n\"MO\"\n\"AL\"\n\"OH\"\n\"NY\"\n\"IN\"\n\"MS\"\n\"NJ\"\n\"TX\"\n\"TN\"\n\"OK\"\n\"MT\"\n\"MD\"\n\"CT\"\n\"AK\"\n\"WI\"\n\"MI\"\n\"DE\"\n\"KY\"\n\"RI\"\n\"NC\"\n\"GA\"\n\"IL\"\n\"WA\"\n\"LA\"\n\"SC\"\n\"KS\"\n\"CA\"\n\"AR\"\n\"NV\"\n\"AZ\"\n\"OR\"\n\"NM\""
		}
	],
	"scales" : [
		{
			"name" : "x",
			"domain" : {
				"data" : "scale/x",
				"field" : "data.domain"
			},
			"zero" : false,
			"nice" : false,
			"clamp" : false,
			"range" : "width"
		},
		{
			"name" : "y",
			"type" : "ordinal",
			"domain" : {
				"data" : "scale/y",
				"field" : "data.domain"
			},
			"points" : true,
			"sort" : false,
			"range" : "height",
			"padding" : 0.5
		}
	],
	"marks" : [
		{
			"type" : "symbol",
			"properties" : {
				"update" : {
					"fill" : {
						"value" : "#000000"
					},
					"size" : {
						"value" : 50
					},
					"x" : {
						"scale" : "x",
						"field" : "data.m_price"
					},
					"y" : {
						"scale" : "y",
						"field" : "data.state"
					}
				},
				"ggvis" : {
					"data" : {
						"value" : "cocaine %&gt;% mutate(price_wt = price/weight) %&gt;% group_by(state) %&gt;%     summarise(m_price = mean(price_wt)) %&gt;% arrange(desc(m_price)) %&gt;%     mutate(rank = 1:45)0"
					}
				}
			},
			"from" : {
				"data" : "cocaine %&gt;% mutate(price_wt = price/weight) %&gt;% group_by(state) %&gt;%     summarise(m_price = mean(price_wt)) %&gt;% arrange(desc(m_price)) %&gt;%     mutate(rank = 1:45)0"
			}
		}
	],
	"width" : 672,
	"height" : 480,
	"legends" : [],
	"axes" : [
		{
			"type" : "x",
			"scale" : "x",
			"orient" : "bottom",
			"layer" : "back",
			"grid" : true,
			"title" : "m_price"
		},
		{
			"type" : "y",
			"scale" : "y",
			"orient" : "left",
			"layer" : "back",
			"grid" : true,
			"title" : "state"
		}
	],
	"padding" : null,
	"ggvis_opts" : {
		"keep_aspect" : false,
		"resizable" : true,
		"padding" : {},
		"duration" : 250,
		"renderer" : "svg",
		"hover_duration" : 0,
		"width" : 672,
		"height" : 480
	},
	"handlers" : null
};
ggvis.getPlot("plot_id752473013").parseSpec(plot_id752473013_spec);
</script><!--/html_preserve-->

This is a static HTML document with a ggvis.

If you have no need for shiny-based interactivity, this approach can be useful. 

You can compile your site using a makefile (or jekyll, maybe). Check out the [makefile](https://github.com/rstudio/rmarkdown/blob/gh-pages/Makefile) that RStudio uses to build the RMarkdown site.

The benefits of using "non-shiny" html are:

* no need for a corresponding R session
* fast page-loads
* can be hosted at github pages

