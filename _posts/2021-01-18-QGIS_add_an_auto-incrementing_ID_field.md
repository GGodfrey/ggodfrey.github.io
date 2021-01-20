"---
title: 'QGIS add an auto-incrementing ID field'
layout: post
tags: []
category: 
Uncategoried
---

Sometimes it is useful to reference values in another table, in an expression. For example, when you want to use a value from a lookup table.

To achieve this use two functions together, 'attribute' and 'get feature'.

The syntax is as follows: attribute(get_feature('VALUE_LAYER_NAME', 'KEY_FIELD', KEY), 'VALUE_FIELD')

<img src=""https://i.stack.imgur.com/KrsjL.png"" />"
