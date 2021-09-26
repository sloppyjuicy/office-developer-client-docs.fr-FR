---
title: Enregistrement dans un objet DOM XML
TOCTitle: Saving to the XML DOM object
ms:assetid: 3c61fc30-9862-347b-c215-08597eccfead
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249160(v=office.15)
ms:contentKeyID: 48544318
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2d1cbc4e1c87e0c63ccbd397b74abd0ce1292cd4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611552"
---
# <a name="saving-to-the-xml-dom-object"></a>Enregistrement dans un objet DOM XML

**S’applique à** : Access 2013, Office 2013

## <a name="saving-to-the-xml-dom-object"></a>Enregistrement dans un objet XML DOM

Vous pouvez sauvegarder un **jeu d'enregistrements** au format XML dans une instance d'un objet MSXML DOM, comme illustré dans le code Visual Basic suivant :

```vb 
 
Dim xDOM As New MSXML.DOMDocument 
Dim rsXML As New ADODB.Recordset 
Dim sSQL As String, sConn As String 
     
sSQL = "SELECT customerid, companyname, contactname FROM customers" 
sConn="Provider=Microsoft.Jet.OLEDB.4.0;Data Source=D:\Program Files" & _ 
        "\Common Files\System\msadc\samples\NWind.mdb" 
rsXML.Open sSQL, sConn 
rsXML.Save xDOM, adPersistADO   'Save Recordset directly into a DOM tree. 
... 
```

