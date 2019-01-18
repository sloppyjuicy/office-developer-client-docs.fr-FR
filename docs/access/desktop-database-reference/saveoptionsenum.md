---
title: SaveOptionsEnum (référence de base de données du bureau Access)
TOCTitle: SaveOptionsEnum
ms:assetid: 2a4e4c7a-6331-7270-0514-cc549c721ffd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249053(v=office.15)
ms:contentKeyID: 48543906
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77a617dc54d8acd145648d926e10cf7c9a3cf252
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705994"
---
# <a name="saveoptionsenum"></a>SaveOptionsEnum

**S’applique à**: Access 2013, Office 2013

Spécifie si un fichier doit être créé ou remplacé en cas de sauvegarde d'un objet [Stream](stream-object-ado.md). Les valeurs peuvent être combinées avec un opérateur AND.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adSaveCreateNotExist</strong></p></td>
<td><p>1</p></td>
<td><p>Par défaut. Crée un nouveau fichier si le fichier spécifié par le paramètre <em>FileName</em> n'existe pas déjà.</p></td>
</tr>
<tr class="even">
<td><p><strong>valeur adSaveCreateOverWrite</strong></p></td>
<td><p>2</p></td>
<td><p>Remplace le fichier avec les données de l'objet <strong>Stream</strong> ouvert, si le fichier spécifié par le paramètre <em>Filename</em> existe déjà.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Équivalent ADO/WFC

Ces constantes ne possèdent pas d'équivalent ADO/WFC.

