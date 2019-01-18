---
title: Création de la chaîne de connexion
TOCTitle: Creating the connection string
ms:assetid: 0d34b1c6-bf2e-1299-9778-573ccd2da1c7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248853(v=office.15)
ms:contentKeyID: 48543214
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f43207edec0c0acb58c66318e5dc7668a28ea595
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719917"
---
# <a name="creating-the-connection-string"></a>Création de la chaîne de connexion

**S’applique à**: Access 2013, Office 2013

ADO prend directement en charge cinq arguments dans une chaîne de connexion. D'autres arguments sont transférés au fournisseur mentionné dans l'argument *Fournisseur* sans aucun traitement de la part d'ADO.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Provider</em></p></td>
<td><p>Spécifie le nom d'un fournisseur à utiliser pour la connexion.</p></td>
</tr>
<tr class="even">
<td><p><em>Nom de fichier</em></p></td>
<td><p>Spécifie le nom d'un fichier spécifique au fournisseur (par exemple, un objet de source de données persistant) contenant des informations de connexion prédéfinies.</p></td>
</tr>
<tr class="odd">
<td><p><em>URL</em></p></td>
<td><p>Spécifie la chaîne de connexion sous la forme d'une URL absolue identifiant une ressource, comme un fichier ou un répertoire.</p></td>
</tr>
<tr class="even">
<td><p><em>Fournisseur distant</em></p></td>
<td><p>Spécifie le nom d'un fournisseur à utiliser lors de l'ouverture d'une connexion côté client (RDS uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><em>Serveur distant</em></p></td>
<td><p>Spécifie le nom du chemin d'accès du serveur à utiliser lors de l'ouverture d'une connexion côté client (RDS uniquement).</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> Dans les exemples suivants et dans le guide du programmeur ADO, l’id utilisateur « MyId » avec un mot de passe de « 123aBc » est utilisé pour authentifier auprès du serveur. Remplacez ces valeurs par des informations d'identification valides pour votre serveur. Remplacez également le nom de votre serveur par « MySqlServer ».

Dans le chapitre 1, l'application HelloData a utilisé la chaîne de connexion suivante :

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
```

Le seul paramètre ADO fourni dans cette chaîne de connexion était « Provider=SQLOLEDB », qui indiquait le fournisseur Microsoft OLE DB pour SQL Server. Reportez-vous à la documentation de chaque fournisseur pour déterminer les autres paramètres valides pouvant être transférés dans la chaîne de connexion. Selon le fournisseur OLE DB pour la documentation SQL Server, vous pouvez remplacer « Serveur » pour le paramètre *Source de données* et « Database » pour le paramètre *Initial Catalog* . Ainsi, la chaîne de connexion suivante devrait produire les mêmes résultats que la première :

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Server='MySqlServer';" & _ 
 "Database='Northwind';Integrated Security='SSPI';" 
```

Pour ouvrir la connexion, transmettez simplement la chaîne de connexion comme premier argument dans la méthode **Connection** objet **Open**:

```vb 
 
objConn.Open m_sConnStr 
```

Il est également possible de fournir la plupart de ces informations en définissant les propriétés de l'objet **Connection** avant d'ouvrir la connexion. Par exemple, vous pourriez obtenir le même résultat que la chaîne de connexion précédente en utilisant le code suivant :

```vb 
 
With objConn 
 .Provider = "SQLOLEDB" 
 .DefaultDatabase = "Northwind" 
 .Properties("Data Source") = "MySqlServer" 
 .Properties("Integrated Security") = "SSPI" 
 .Open 
End With 
```

