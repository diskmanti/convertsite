---
title: QuickMapServces Plugin
tags: [qgis, plugin]
---

![](/img/qms-example.png)

Një nga plugin më të mirë që mund të ketë QGIS është [**QuickMapServices**](https://plugins.qgis.org/plugins/quick_map_services/). Ky është një plugin i cili lejon përdorueset e QGIS të shtojnë _baselayer_ të ndryshëm në hartat e tyre. Në fakt ky plugin kryen të njëjtin funksion si një plugin tjetër, shumë i njohur i QGIS, [**OpenLayers**](https://plugins.qgis.org/plugins/openlayers_plugin/) plugin.

OpenLayers plugin, për shumë kohe, ka qenë i vetmi plugin që kryente një funksion të tillë. Dhe e bënte shumë mirë. Përveç thjesht shtimit të baselayer të ndryshëm në QGIS, ai lejonte edhe download të të dhënave nga OSM, në format XML, dhe përdormini e tyre në QGIS, pa përdorur asnjë software shtesë dhe direkt nga GUI i QGIS. Por OpenLayers plugin kishte disa mangësi kyçe:

1. Në mënyre që baselayer, sidomos kur doje të përdorje një nga layer e Google, të puthiteshe sa më mire me të dhënat e tua duhet të përdorje _EPSG:3857_. Në rast të kundërtat do të viheshin re gabime apo QGIS edhe mund të shkonte në _crash_.


2. OpenLayers plugin kishte një listë të limituar me servise nga mund të shtoje baselayer dhe ajo listë nuk ishte e ndryshueshme nga përdoruesi. Kjo vinte për shkak sepse mbrapa këtij plugin qëndronte _OpenLayers.js_ dhe lista me baselayer ishte built-in bashke me plugin.


QuickMapServices nuk i ka këto problematika. Çdo baselayer i shtuar me anë te këtij plugin mund të riprojektohet _on-the-fly_ në çdo sistem koordinativ pa asnjë problem. Dhe gjithashtu mund të shtohen servise të ndryshme, nga burime të shumëllojshme(Server lokal ose jo).
QuickMapServices mund të instalohet direkte nga plugin repository zyrtar i QGIS dhe ai vjen i konfiguruar me disa servise. Në mënyre që ju të shtoni serviset më interesante(si Google, Stamen apo CartoDB) mjafton të ndiqni këto [hapa](http://nextgis.com/blog/quickmapservices-with-contributed-services/). Nqs doni të shtoni serviset tuaja mund të ndiqni këtë [link](https://github.com/nextgis/quickmapservices/wiki/Adding-data-source).


Servise default | Servise interesante
------------ | -------------
![default](/img/qms.png) | ![me servise shtesë](/img/qms-contrib.png)


QuickMapServices, në çdo aspekt të funksionalitet të tij, është superior ndaj OpenLayers plugin. Ai bën gjithçka ku OpenLayers plugin ngel mbrapa dhe vazhdon të jetë mbrapa. E vetmja gjë që OpenLayers ka më shumë se QuickMapServies është mundësia për të download të dhëna në mënyrë direkte nga OSM. Por QuickMapServices ka për qëllim vetëm menaxhimin e baselayers dhe këtë e bën shumë mirë. :thumbsup: :smile:

>diskmanti