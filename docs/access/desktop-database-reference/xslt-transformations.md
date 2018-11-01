---
title: Transformations XSLT
TOCTitle: XSLT Transformations
ms:assetid: 6a19310d-027f-e8d6-9859-0b545ae7e2f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249418(v=office.15)
ms:contentKeyID: 48545425
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8bbb7e935dece05d4616044b399601c393d5f07c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889433"
---
# <a name="xslt-transformations"></a>Transformations XSLT


**S’applique à**: Access 2013, Office 2013

## <a name="xslt-transformations"></a>Transformations XSLT

XSLT peut être appliqué au XML généré pour le transformer en un autre format. Il est utile de comprendre le format XML dans ADO, afin de permettre le développement de modèles XSLT, qui peuvent transformer le format XML en un format plus convivial.

Par exemple, vous savez que chaque ligne de l'objet **Recordset** est enregistrée en tant qu'élément z:row dans l'élément rs:data. De même, chaque champ de l'objet **Recordset** est enregistré en tant que paire attribut-valeur associée à cet élément.

Le script XSLT suivant peut être appliqué au XML illustré à la section précédente, afin de le transformer en table HTML affichable par le navigateur :

```xml 
 
<?xml version="1.0" encoding="ISO-8859-1"?> 
<html xmlns:xsl="https://www.w3.org/TR/WD-xsl"> 
<body STYLE="font-family:Arial, helvetica, sans-serif; font-size:12pt; background-color:white"> 
<table border="1" style="table-layout:fixed" width="600"> 
  <col width="200"></col> 
  <tr bgcolor="teal"> 
    <th><font color="white">CustomerId</font></th> 
    <th><font color="white">CompanyName</font></th> 
    <th><font color="white">ContactName</font></th> 
  </tr> 
<xsl:for-each select="xml/rs:data/z:row"> 
  <tr bgcolor="navy"> 
    <td><font color="white"><xsl:value-of select="@CustomerID"/></font></td> 
    <td><font color="white"><xsl:value-of select="@CompanyName"/></font></td> 
    <td><font color="white"><xsl:value-of select="@ContactName"/></font></td>  
  </tr> 
</xsl:for-each> 
</table> 

</body> 
</html> 
```

XSLT convertit la chaîne XML générée par la méthode ADO **Save** en une table HTML qui affiche tous les champs de l'objet **Recordset** ainsi que le titre de la table. Les titres et les lignes de la table se voient par ailleurs attribuer différentes polices et couleurs.

