---
title: En savoir plus sur la persistance du recordset
TOCTitle: More about Recordset persistence
ms:assetid: f3248de7-6eef-1dd0-ff96-557b411789e7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250232(v=office.15)
ms:contentKeyID: 48548666
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 194dcf3826409c91f8d046b39b9009b43aee5477
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288847"
---
# <a name="more-about-recordset-persistence"></a>En savoir plus sur la persistance du recordset

**S’applique à** : Access 2013, Office 2013

L'objet Recordset ADO prend en charge le stockage du contenu d'un objet **Recordset** dans un fichier à l'aide de la méthode [Save](save-method-ado.md). Le fichier stocké de façon persistante peut se trouver sur un lecteur local, un serveur réseau ou en tant qu'URL sur un site Web. Par la suite, le fichier peut être restauré soit avec la méthode **Open** de l'objet [Recordset](open-method-ado-recordset.md), soit avec la méthode [Execute](connection-object-ado.md) de l'objet [Connection](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection).

En outre, la méthode [GetString](getstring-method-ado.md) convertit un objet **Recordset** dans un format où les lignes et les colonnes sont délimitées par des caractères que vous spécifiez.

Pour rendre un objet **Recordset** persistant, commencez par le convertir dans un format qui lui permet d'être stocké dans un fichier. Les objets **Recordset** peuvent être stockés au format ADTG (Advanced Data TableGram) propriétaire ou au format XML (Extensible Markup Language) ouvert. Des exemples utilisant ADTG sont présentés ci-dessous. Pour plus d'informations sur la persistance XML, consultez [Persistance des enregistrements au format XML](persisting-records-in-xml-format.md).

Save any pending changes in the persisted file. Doing this allows you to issue a query that returns a **Recordset** object, edits the **Recordset**, saves it and the pending changes, later restores the **Recordset**, and then updates the data source with the saved pending changes.

Pour plus d'informations sur le stockage persistant des objets **Stream**, consultez [Flux et persistance](streams-and-persistence.md) au chapitre 10.

Pour obtenir un exemple de persistance d’un objet **Recordset** , consultez  [Scénario de persistance des objets Recordset XML](xml-recordset-persistence-scenario.md).

## <a name="example"></a>Exemple

**Enregistrement d'un objet Recordset :**

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Save "c:\yourFile.adtg", adPersistADTG 
```

**Ouverture d'un fichier persistant avec Recordset.Open :**

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg", "Provider='MSPersist'",,,adCmdFile
```

Si vous le souhaitez et si l'objet **Recordset** ne présente pas de connexion active, vous pouvez accepter toutes les valeurs par défaut et simplement coder ce qui suit :

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg" 
```

**Ouverture d'un fichier persistant avec Connection.Execute :**

```vb 
 
Dim conn as New ADODB.Connection 
Dim rs as ADODB.Recordset 
conn.Open "Provider='MSPersist'" 
Set rs = conn.execute("c:\yourFile.adtg") 
```

**Ouverture d'un fichier persistant avec RDS.DataControl :**

Dans ce cas, la propriété **Server** n'est pas définie.

```vb 
 
Dim dc as New RDS.DataControl 
dc.Connection = "Provider='MSPersist'" 
dc.SQL = "c:\yourFile.adtg" 
dc.Refresh
```

