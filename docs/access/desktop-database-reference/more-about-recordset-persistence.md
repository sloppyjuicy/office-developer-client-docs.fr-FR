---
title: Informations complémentaires sur la persistance des objets Recordset
TOCTitle: More About Recordset Persistence
ms:assetid: f3248de7-6eef-1dd0-ff96-557b411789e7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250232(v=office.15)
ms:contentKeyID: 48548666
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 05287befde90319ad2844effef8ef2d47e1241b7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471282"
---
# <a name="more-about-recordset-persistence"></a>Informations complémentaires sur la persistance des objets Recordset


**S’applique à**: Access 2013 | Office 2013

L'objet Recordset ADO prend en charge le stockage du contenu d'un objet **Recordset** dans un fichier à l'aide de la méthode [Save](save-method-ado.md). Le fichier stocké avec persistance peut-être exister sur un lecteur local, serveur réseau, ou en tant qu’URL sur un site Web. Par la suite, le fichier peut être restauré soit avec la méthode **Open** de l'objet [Recordset](open-method-ado-recordset.md), soit avec la méthode [Execute](connection-object-ado.md) de l'objet [Connection](https://msdn.microsoft.com/library/jj249832\(v=office.15\)).

En outre, la méthode [GetString](getstring-method-ado.md) convertit un objet **Recordset** dans un format où les lignes et les colonnes sont délimitées par des caractères que vous spécifiez.

Pour rendre un objet **Recordset** persistant, commencez par le convertir dans un format qui lui permet d'être stocké dans un fichier. Les objets **Recordset** peuvent être stockés au format ADTG (Advanced Data TableGram) propriétaire ou au format XML (Extensible Markup Language) ouvert. Des exemples utilisant ADTG sont présentés ci-dessous. Pour plus d'informations sur la persistance XML, consultez [Persistance des enregistrements au format XML](persisting-records-in-xml-format.md).

Enregistrez les modifications en attente dans le fichier persisté. Cela vous permet d’émettre une requête qui renvoie un objet **Recordset** , modifie le **jeu d’enregistrements**, enregistre ainsi que les modifications en attente, restaure l' **objet Recordset**et met à jour la source de données avec les modifications en attente.

Pour plus d'informations sur le stockage persistant des objets **Stream**, consultez [Flux et persistance](streams-and-persistence.md) au chapitre 10.

Pour obtenir un exemple de persistance d'un objet **Recordset**, consultez [Scénario de persistance des objets Recordset XML](xml-recordset-persistence-scenario.md).

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

