---
title: Microsoft Data Shaping Service pour OLE DB (fournisseur de services ADO)
TOCTitle: Microsoft Data Shaping Service for OLE DB (ADO Service Provider)
ms:assetid: 6e6e5f39-6f43-7c7b-5812-796096d1d31b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249436(v=office.15)
ms:contentKeyID: 48545511
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5065b966608f8d6a3ef1cb05be890b9a1f147dc8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288959"
---
# <a name="microsoft-data-shaping-service-for-ole-db-ado-service-provider"></a>Microsoft Data Shaping Service pour OLE DB (fournisseur de services ADO)


**S’applique à** : Access 2013, Office 2013

Microsoft Data Shaping Service pour le fournisseur de services OLE DB prend en charge la construction d'objets [Recordset](recordset-object-ado.md) hiérarchiques (mis en forme) provenant d'un fournisseur de données.

## <a name="provider-keyword"></a>Mot clé du fournisseur

Pour invoquer Microsoft Data Shaping Service pour OLE DB, spécifiez le mot clé et la valeur suivants dans la chaîne de connexion.

```vb 
 
"Provider=MSDataShape" 
```

## <a name="dynamic-properties"></a>Propriétés dynamiques

Lorsque ce fournisseur de services est appelé, les propriétés dynamiques suivantes sont ajoutées à la collection [Properties](connection-object-ado.md) de l'objet [Connection](properties-collection-ado.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom de la propriété dynamique</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Unique Reshape Names</strong></p></td>
<td><p>Indique si les objets <strong>Recordset</strong> dont les propriétés <strong>Reshape Name</strong> présentent des valeurs dupliquées sont autorisés. Si cette propriété dynamique a la valeur <strong>True</strong> et que l'utilisateur crée un nouveau <strong>Recordset</strong> en lui attribuant le même nom de modification de forme qu'un objet <strong>Recordset</strong> existant, le nom de la modification de forme du nouvel objet <strong>Recordset</strong> sera modifié de façon à être unique. Si cette propriété a la valeur <strong>False</strong> et que l'utilisateur crée un nouveau <strong>Recordset</strong> en lui attribuant le même nom de modification de forme qu'un objet <strong>Recordset</strong> existant, les deux objets <strong>Recordset</strong> auront le même nom de modification de forme. Dans ce cas, la mise en forme de ces deux objets <strong>Recordset</strong> ne pourra pas être modifiée tant que ces deux objets coexisteront. La valeur par défaut de la propriété est <strong>False</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Data Provider</strong></p></td>
<td><p>Indique le nom du fournisseur qui fournira les lignes à mettre en forme.

Cette valeur sera NONE si le fournisseur n'est pas destiné à être utilisé pour fournir des lignes.</p></td>
</tr>
</tbody>
</table>


Vous pouvez aussi définir des propriétés dynamiques en écriture en spécifiant leurs noms en tant que mots clé dans la chaîne de connexion. Par exemple dans Microsoft Visual Basic, définissez la propriété dynamique **Data Provider** sur « MSDASQL » en spécifiant :

```vb 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MSDataShape;Data Provider=MSDASQL" 
```

Vous pouvez également définir ou extraire une propriété dynamique en spécifiant son nom en tant qu'index de la propriété [Properties](properties-collection-ado.md). Par exemple, vous pouvez obtenir et imprimer la valeur actuelle de la propriété dynamique **Data Provider**, puis définir une nouvelle valeur de la façon suivante :

```vb 
 
Debug.Print cn.Properties("Data Provider") 
cn.Properties("Data Provider") = "MSDASQL" 
```

Pour plus d'informations sur la mise en forme des données, consultez la rubrique [Mise en forme des données](data-shaping.md).

