---
title: SaveOptionsEnum (référence de base de données du bureau Access)
TOCTitle: SaveOptionsEnum
ms:assetid: 2a4e4c7a-6331-7270-0514-cc549c721ffd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249053(v=office.15)
ms:contentKeyID: 48543906
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 1dacfd11edd2cc8b4e939efc3c40d98437f0b41f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889419"
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
<th><p>Constant</p></th>
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

