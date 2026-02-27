# Grain_Checker_QGISPlugin
A lightweight QGIS plugin for MAUP sensitivity stress testing of bivariate point-density relationships

Grain-Checker is a prototype QGIS plugin designed to quickly test whether a spatial relationship is sensitive to aggregation grain (i.e., the Modifiable Areal Unit Problem, MAUP).

It currently supports a workflow:
1) input two point layers (an event layer + a covariate layer),
2) aggregate both to multiple grid sizes,
3) compute grid-cell densities,
4) compare the Pearson correlation between the two density surfaces across scales,
5)  output a simple sensitivity summary.
