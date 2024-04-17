
# Air pollution and health

### [📋 Add graphic to your story](https://airpollution.360visuals.org/airpollution-temperature?edshare) • [📊 Get the data](data) • [💻 Reproduce the analysis](#-reproduce-the-analysis)

Visualises the changing risks of heat, cold and ambient air pollution

## ♻️ Use + Remix rights

<figure>
<img
src="https://mirrors.creativecommons.org/presskit/buttons/80x15/png/by-nc.png"
alt="Creative Commons Attribution Non-Commercial 4.0" />
<figcaption aria-hidden="true"><a
href="https://creativecommons.org/licenses/by-nc/4.0">Creative Commons
Attribution Non-Commercial 4.0</a></figcaption>
</figure>

These charts, as well as the analyses that underpin them, are available
under a [Creative Commons Attribution Non-Commercial 4.0
licence](https://creativecommons.org/licenses/by-nc/4.0).

<!-- Do any of the data sources fall under a different licence? If so, describe the licence and which parts of the data fall under it here! if most of it does, change the above and replace LICENCE.md too -->

Data in these charts comes from:

<ul>  
<li>  
<a href="https://ghdx.healthdata.org/gbd-2019">Global Burden of Disease
(2019)</a>  
</li>  
</ul>

> \[!IMPORTANT\] GBD data is used under the [IHME Free-of-Charge
> Non-commercial User
> Agreement](https://www.healthdata.org/about/ihme-free-charge-non-commercial-user-agreement),
> which forbids commercial use of the data. Contact IHME for commercial
> uses.

**Please attribute 360info and the data sources when you use and remix
these visualisations.**

## 💻 Reproduce the analysis

### Quickstart: use the dev container

This project comes with a ready-to-use [dev
container](https://code.visualstudio.com/docs/remote/containers) that
includes everything you need to reproduce the analysis (or do a similar
one of your own!), including [R](https://r-project.org) and
[Quarto](https://quarto.org).

[![Open in GitHub
Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/360-info/report-airpollution-health?quickstart=1)

If you have Docker installed, you can build and run the container
locally:

- Download or clone the project
- Open it in [Visual Studio Code](https://code.visualstudio.com)
- Run the **Remote-Containers: Reopen in Container** command

Once the container has launched (it might take a few minutes to set up
the first time), you can run the analysis scripts with:

``` sh
quarto render
```

Or look for the `.qmd` files to modify the analysis.

### Manual setup

To setup a development environment manually,

You’ll need to:

- [Download and install Quarto](https://quarto.org/docs/get-started)
- [Download the install R](https://www.r-project.org)
- Satisfy the R package dependencies. In R:
  - Install the [`renv`](https://rstudio.github.io/renv) package with
    `install.packages("renv")`,
  - Then run `renv::restore()` to install the R package dependencies.
  - (For problems satisfying R package dependencies, refer to [Quarto’s
    documentation on virtual
    environments](https://quarto.org/docs/projects/virtual-environments.html).)

Now, render the `.qmd` files to the `/out` directory with:

``` sh
quarto render
```

## ❓ Help

If you find any problems with our analysis or charts, please feel free
to [create an
issue](https://github.com/360-info/report-airpollution-health/issues/new)!
