---
title: SQLServer
layout: post
tags: [SQLServer, databaze, shapefile]
---
![](/img/sqlserver.png)


Kur po punoja në një zyrë më rastisi që duhet të përdorja ++SQLServer++, nga Microsft, sepse i gjithë informacioni qe ata kishin ishte në SQLServer. Zakonisht unë përdor Postgresql me PostGIS extension(jua këshilloj dhe juve :smiley: ) për të ruajtur dhe menaxhuar të dhënat e mia hapësinore, por në këtë rast isha i detyruar të përdorja SQLServer.

Ajo që mua mu duk mangësi kryesore e SQLServer ishte mungesa e një mënyre për të hedhur të dhëna hapësinore në server. Kjo mu duk shume e çuditshme sepse SQLServer suportonte spatial data që nga versioni i vitit 2008 dhe kishte përdorues(edhe pse shume pak) që e përdornin.
Mbas disa kërkimesh arrita të gjej 2 mjete që arrinin të bënin çfarë unë kërkoja: [Shape2SQL](http://www.sharpgis.net/page/Shape2SQL), [SHP Importer](http://www.dknezevic.com/blog/2014/10/import-shapefiles-into-sql-server.html)

Të dy këto mjete nuk janë zyrtare nga Microsoft, por të krijuar nga __devs__ për të përmbushur nevojat e tyre, dhe për ketë arsye kane disa mangësi. Mangësia e parë është që duhet të dish character encoding që kane tabelat e tua ne shapefile. Kjo nuk është gjithmonë diçka që mund të dihet, apo të gjendet kollaj. Mangësia e dytë është fakti që këto mjete krijojnë një kolonë të re në data bazë ku ruajnë një ID të krijuar prej tyre, sepse nuk janë në gjendje të njohin ID që mund të ketë vetë shapefile.

Si përfundim, këto mjete edhe pse kane mangësitë e tyre gjejnë vend për përdorim sepse ofrojnë diçka që i mungon SQLServer dhe të lejojnë të arrish qëllimin tënd. Gjithashtu është e vetmja mënyre që unë gjeta si alternative ndaj OGR. :wink:


>diskmanti