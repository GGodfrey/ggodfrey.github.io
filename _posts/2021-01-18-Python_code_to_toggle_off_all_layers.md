"---
title: 'Python code to toggle off all layers'
layout: post
tags: []
category: 
Uncategoried
---
A really neat solution shared on stack exchange to the following question. <a class=""question-hyperlink"" style=""font-weight:bold;font-style:inherit;"" href=""https://gis.stackexchange.com/questions/226347/how-to-turn-on-off-all-labels-of-all-layers-in-qgis"">How to turn on/off all labels of all layers in QGIS.</a>

Uses python to generate a temporary button on the toolbar.

from PyQt4.QtCore import QObject, SIGNAL
from PyQt4.QtGui import QAction, QIcon

action = QAction(QIcon(""""), ""Turn labels"" + ""\n"" + ""ON/OFF"", iface.mainWindow())
action.setCheckable(True)
iface.addToolBarIcon(action)

def label_control():
for layer in QgsMapLayerRegistry.instance().mapLayers().values():
if action.isChecked() == True:
layer.setCustomProperty(""labeling/enabled"", True)
else:
layer.setCustomProperty(""labeling/enabled"", False)
layer.triggerRepaint()

QObject.connect(action, SIGNAL(""triggered()""), label_control)

&nbsp;

https://gis.stackexchange.com/questions/226347/how-to-turn-on-off-all-labels-of-all-layers-in-qgis"
