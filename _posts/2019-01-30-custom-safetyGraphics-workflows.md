---
layout: post
title: Custom safetyGraphics Workflows
author: Jeremy Wildfire
---

The `safetyGraphics` R package now supports for custom workflows allowing users to preload their own charts and data sets in the safetyGraphics Shiny Application. The best way to learn more is the new [Custom Workflows vignette](https://cran.r-project.org/web/packages/safetyGraphics/vignettes/customWorkflows.html) - which has been briefly summarized below.

The new [v1.1 release](https://github.com/SafetyGraphics/safetyGraphics/releases/tag/v1.1.0) of [safetyGraphics](https://github.com/SafetyGraphics/safetyGraphics) is [available now on CRAN](https://cran.r-project.org/web/packages/safetyGraphics/index.html).
  
# Loading data

Loading data in to the app is easy! Just run `safetyGraphicsApp(loadData=TRUE)` to preload all data.frames from your current R session in a new instance of the safetyGraphics Shiny app.

# Loading Charts

Loading custom charts is just slightly more complex. There are 4 steps required to create a custom chart for use in `safetyGraphics`:

1. Create custom chart code
2. Add new settings to the app (if needed)
3. Add the chart to the app
4. Initialize the app

For example, to create a trivially simple custom chart, make a file called `customSettings.R` with the following code: 

```
# Step 1 - Write custom chart code 
helloWorld <- function(data,settings){
  plot(-1:1, -1:1)
  text(runif(20, -1,1),runif(20, -1,1),"Hello World")
}

# Step 2 - Initialize Custom Settings 
# Not Applicable!

# Step 3 - Initialize the custom chart 
addChart( 
  chart=”hello_world”,
  main=”helloWorld",
  label=”Hello World”, 
)
```

Then initialize the app (Step 4) by running: 

```
setwd('/path/to/the/file/above')
safetyGraphicsApp()
```

Once the app opens, click the charts tab to view the new custom "hello_world" chart. 

<img src="https://user-images.githubusercontent.com/3680095/71821298-c0080980-305f-11ea-979e-6574ac30f706.png" style='max-width:700px'>

Again, see the [Custom Workflows vignette](https://github.com/SafetyGraphics/safetyGraphics/wiki/Vignette:-Custom-Workflows) for details and more complex examples.
