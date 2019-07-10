---
layout: post
title: CRANsearcher - R package discovery made simple
author: Becca Krouse and Agustin Calatroni
---

It's a familiar story to many of us: we're working along and find that we need something very specific.  It could be a function or macro, or maybe an analysis technique.  It's also probably going to be quite difficult to create from scratch.  So we wonder, maybe this has been done before?  

As data scientists, exploratory analyses performed using emerging techniques are a regular part of the job.  We are pushing the limits of research and  constantly trying to discover and compare existing methods. We often find ourselves taking inventory of our analytical toolbox and trying to avoid reinventing the wheel.  Much of our data science work at Rho is performed using R, which offers a vast and rapidly growing ecosystem of [packages](https://cran.r-project.org/web/packages/available_packages_by_name.html).  Indeed, R packages extend from visualization to Bayesian inference, and from spatial analyses to pharmacokinetics. There is probably not an area of quantitative research that isn't represented by at least one R package.  R's great strength, however, can also be a weakness.  To answer the question of "has someone already created a tool for this" or "what is the best way to do X", we find ourselves navigating package websites, subscribing to blogs, and doing lots of googling. Unfortunately, this is also a diversion from our usual analysis workflow and is not always productive.   

In 2017, the 10,000th R package published to CRAN and this became a hot topic in the R community.  It turns out we were not the only people struggling to navigate through all of the options.  This provided the last bit of motivation we needed to create our own solution.  Thus, the idea of `CRANsearcher` was born to fulfill an unmet need.

We went about building `CRANsearcher` with the analysis workflow in mind.  The application, which allows for efficient navigation of tens of thousands of R packages, can be run directly from R.   With the click of a button in RStudio, `CRANsearcher` is launched; it loads the entire CRAN package database (in real time) into a table that is sortable and filterable by release date.  The user can perform multi-term search to discover packages through their names and descriptions.  Packages can be explored further through external links and installed with the click of a button.

<img src="https://raw.githubusercontent.com/RhoInc/CRANsearcher/master/inst/image/gif/CRANsearcher_addin.gif"/>

Although this tool immediately became an asset for internal R users, we were taken by surprise at how quickly it was embraced and even celebrated by the larger community.  We strongly believed this application could be useful to others, so we hosted its code on the Rho [GitHub site](https://github.com/RhoInc/CRANsearcher).  As a result, we've received great [feedback](https://twitter.com/juliasilge/status/866796243447463937), external [issues](https://github.com/RhoInc/CRANsearcher/issues?q=is%3Aissue+is%3Aclosed) for feature requests/bugs, and thoughtfully contributed [code](https://github.com/RhoInc/CRANsearcher/pulls?q=is%3Apr+is%3Aclosed+author%3Arpodcast). Sharing this code publicly has been a wonderful lesson in the power of community and collaboration, as well as innovation and transparency, all ideals we value in the Data Science group.  

As previously mentioned, at the time of `CRANsearcher`'s release, there were many related discussions happening in the R community.  In fact, we were fortunate to participate in a special session at UseR! 2017 conference called "Navigating the R Package Universe", which presented tools and strategies for finding and/or assessing packages.  Read Julia Silge's excellent follow-up blog post [here](https://juliasilge.com/blog/navigating-packages/). It has been incredibly rewarding to be a part of this community effort to develop supports around discovering new tools. 

In summary, we would like to share the two lessons we learned from this experience. First, innovation doesn't need to be something that is difficult to reach. Indeed, CRANsearcher is simply a web scraping tool with a simple interface. Its success came because there was a need and we took the time to code it so that we can work more effectively in the future.  Second, you are not alone. Get the structure ready and there are plenty of colleagues out there ready to pitch in so that the effort is collective.

`CRANsearcher` is available on [CRAN](https://cran.r-project.org/web/packages/CRANsearcher/index.html) and can be utilized as an Rstudio add-in or Shiny application.  