---
title: Enregistrements persistants au format XML
TOCTitle: Persisting Records in XML Format
ms:assetid: 8071e244-60c7-759c-094c-152add5d72e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249545(v=office.15)
ms:contentKeyID: 48545924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 77a8f14cf76e87060d73d0b3a6a6939c292c422e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868055"
---
# <a name="persisting-records-in-xml-format"></a>Persistance des enregistrements au format XML


**S’applique à**: Access 2013, Office 2013

À l'instar du format ADTG, la persistance des **jeux d'enregistrements** au format XML est mise en œuvre par le Microsoft OLE DB Persistence Provider. Ce fournisseur génère un jeu de lignes à défilement vers l'avant uniquement et en lecture seule à partir d'un fichier ou flux XML contenant les informations de schéma générées par ADO. De la même manière, il prend un **jeu d'enregistrements** ADO, génère un code XML et l'enregistre dans un fichier ou tout objet implémentant l'interface COM **IStream**. (En fait, un fichier est juste un autre exemple d'objet prenant en charge **IStream**.) Pour les versions 2.5 et ultérieures, ADO repose sur le parseur Microsoft XML (MSXML) pour charger le code XML dans le **jeu d'enregistrements**; par conséquent msxml.dll est indispensable. Pour la version 2.5, MSXML est fourni avec Internet Explorer 5. Pour la version 2.6, MSXML est fourni avec SQL Server 2000.

> [!NOTE]
> [!REMARQUE] Certaines restrictions s'appliquent lorsque vous enregistrez des **jeux d'enregistrements** (formes de données) au format XML. Vous ne pouvez pas sauvegarder au format XML si le **jeu d'enregistrements** hiérarchique renferme des mises à jour en suspens et vous ne pouvez pas non plus sauvegarder un **jeu d'enregistrements** hiérarchique paramétré. Pour en savoir plus, reportez-vous à la rubrique [Jeux d'enregistrements hiérarchiques dans XML](hierarchical-recordsets-in-xml.md).


Le moyen le plus simple de conserver des données au format XML et de les recharger dans ADO est d'utiliser respectivement les méthodes **Save** et **Open**. L'exemple de code ADO suivant illustre l'enregistrement de données de la table Titles dans un fichier appelé titles.sav.

```vb 
 
Dim rs as new Recordset 
Dim rs2 as new Recordset 
Dim c as new Connection 
Dim s as new Stream 
 
' Query the Titles table. 
c.Open "provider='sqloledb';data source='mydb';initial catalog='pubs';Integrated Security='SSPI'" 
rs.cursorlocation = adUseClient 
rs.Open "select * from titles", c, adOpenStatic 
 
' Save to the file in the XML format. Note that if you don't specify 
' adPersistXML, a binary format (ADTG) will be used by default. 
rs.Save "titles.sav", adPersistXML 
 
' Save the Recordset into the ADO Stream object. 
rs.save s, adPersistXML 
rs.Close 
c.Close 
 
set rs = nothing 
 
Reopen the file. 
rs.Open "titles.sav",,,,adCmdFile 
'Open the Stream back into a Recordset. 
rs2.open s 
```

ADO conserve toujours l’ensemble de l’objet **Recordset** . Si vous souhaitez conserver uniquement un sous-ensemble de lignes de l’objet **Recordset** , utilisez la méthode **Filter** pour cibler les lignes ou modifier la clause de sélection. Toutefois, vous devez ouvrir un objet **Recordset** avec un curseur côté client (**CursorLocation** = **adUseClient**) d’utiliser la méthode de **filtre** pour l’enregistrement d’un sous-ensemble de lignes. Par exemple, pour extraire des titres commençant par la lettre « b », vous pouvez appliquer un filtre à un objet **Recordset** ouvert :

```vb 
 
rs.Filter "title_id like 'B*'" 
rs.Save "btitles.sav", adPersistXML 
```

ADO utilise toujours le jeu de lignes du moteur du curseur client pour générer un objet **Recordset** avec défilement et signet en plus des données à défilement vers l'avant uniquement générées par le Fournisseur de persistance.

Cette section comprend les rubriques suivantes :

- [Format de persistance XML](xml-persistence-format.md)

- [Namespaces](namespaces.md)

- [Section Schéma](schema-section.md)

- [Section Données](data-section.md)

- [Recordsets hiérarchiques au format XML](hierarchical-recordsets-in-xml.md)

- [Propriétés dynamiques du jeu d’enregistrements au format XML](recordset-dynamic-properties-in-xml.md)

- [Transformations XSLT](xslt-transformations.md)

- [Enregistrement dans un objet XML DOM](saving-to-the-xml-dom-object.md)

- [Considérations relatives à la sécurité XML](xml-security-considerations.md)

- [XML Recordset Persistence Scenario Topics](xml-recordset-persistence-scenario.md)