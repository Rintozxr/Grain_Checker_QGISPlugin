# Grain_Checker_QGISPlugin
A lightweight QGIS plugin for MAUP sensitivity stress testing of bivariate point-density relationships

Grain-Checker is a prototype QGIS plugin designed to quickly test whether a spatial relationship is sensitive to aggregation grain.In spatial analysis, conclusions can change when the aggregation unit changes.In practice, many workflows choose one grid size and proceed directly to modeling, without checking whether the observed relationship is stable across scales. Grain-Checker is meant to act as a quick methodological stress test before downstream modeling.

🔴Installation (prototype / local use)
Copy the plugin folder into your QGIS plugins directory (e.g. on Windows):
C:\Users\<username>\AppData\Roaming\QGIS\QGIS3\profiles\default\python\plugins\grain_checker
1)Restart QGIS.
2)Enable the plugin in Plugins → Manage and Install Plugins.
3)Run Grain Checker from the toolbar/menu.

🔵What it accepts:
1)Event point layer 
2)Covariate point layer
3)3 grid sizes

🔵For each scale:
1)Creates a grid
2)Counts event points per grid cell
3)Counts covariate points per grid cell
4)Converts counts to densities
5)Computes Pearson correlation between event density and covariate density

🔵Returns:
1)correlation at each scale
2)summary statistics

a simple grain-sensitivity label (fine/medium/coarse)

🔵Workflow:
1)Load two point layers in QGIS (event + covariate).
2)Open Grain-Checker.
3)Select the two layers and specify three grid sizes.
4)Run the plugin, and the plugin will do:
  a)creates three grid layers,
  b)counts points in each cell,
  c)computes density–density Pearson correlation for each scale,
  d)reports the grain sensitivity of the relationship.

🔵Notes on input data 
1) Both layers must be point layers.
2) If your covariate is a line layer, preprocess it into points.
3) Very fine grids may produce highly sparse event densities; this can make correlation unstable or less interpretable.

  
