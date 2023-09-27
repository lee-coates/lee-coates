---
layout: post
title:  "Postgresql 16 Released!"
date:   2023-09-26 10:17:48 -0700
categories: databases postgresql
---

Postgresql 16 was released on September 14, 2023.

The first official version of Postgresql (version 6) was released on March 1, 1998. Here are the other major version release years:

![Postgresql Versioning over time](/assets/img/postgresql_versions_over_time.jpg "Postgresql Versioning over time")

[Postgresql Versioning](https://www.postgresql.org/support/versioning/)

As the graph shows, major versions have been released yearly since 2017. No wonder there are no so many amazing features!

Thanks Postgresql Team!

***r commands to produce graph***

    install.packages("ggplot2")
    install.packages("hrbrthemes")
    library(ggplot2)
    library(hrbrthemes)

    x <- c(2000, 2005, 2010, 2017, 2018, 2019, 2020, 2021, 2022, 2023)
    y <- c(7, 8, 9, 10, 11, 12, 13, 14, 15, 16)
    data <- data.frame(x, y)

    png(file = "postgresql_versions_over_time.jpg")

    plotted_data <- ggplot(data, aes(x=x, y=y)) + geom_line(color="#6Cb9c9", size=2, alpha=.9, linetype=1) + theme_ipsum() + ggtitle("Postgresql Releases over Time")

    dev.off()