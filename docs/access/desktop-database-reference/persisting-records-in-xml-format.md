---
title: Persistance des enregistrements au format XML
TOCTitle: Persisting records in XML format
ms:assetid: 8071e244-60c7-759c-094c-152add5d72e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249545(v=office.15)
ms:contentKeyID: 48545924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 10a5651c74580950810211c4f71e19fc80a16a95
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287565"
---
# <a name="persisting-records-in-xml-format"></a>Persistance des enregistrements au format XML

**S’applique à** : Access 2013, Office 2013

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

ADO always persists the entire **Recordset** object. If you wish to only persist a subset of rows of the **Recordset** object, use the **Filter** method to narrow down the rows or change your selection clause. Toutefois, vous devez ouvrir un objet **Recordset** avec un curseur côté client (**CursorLocation**  =  **adUseClient**) pour utiliser la méthode **Filter** pour enregistrer un sous-ensemble de lignes. For example, to retrieve titles that start with the letter "b," you can apply a filter to an open **Recordset** object:

```vb 
 
rs.Filter "title_id like 'B*'" 
rs.Save "btitles.sav", adPersistXML 
```

ADO utilise toujours le jeu de lignes du moteur du curseur client pour générer un objet **Recordset** avec défilement et signet en plus des données à défilement vers l'avant uniquement générées par le Fournisseur de persistance.

Cette section contient les rubriques suivantes :

- [XML Persistence Format](xml-persistence-format.md)

- [Namespaces](namespaces.md)

- [Schema Section](schema-section.md)

- [Data Section](data-section.md)

- [Hierarchical Recordsets in XML](hierarchical-recordsets-in-xml.md)

- [Recordset Dynamic Properties in XML](recordset-dynamic-properties-in-xml.md)

- [XSLT Transformations](xslt-transformations.md)

- [Saving to the XML DOM Object](saving-to-the-xml-dom-object.md)

- [XML Security Considerations](xml-security-considerations.md)

- [XML Recordset Persistence Scenario Topics](xml-recordset-persistence-scenario.md)
