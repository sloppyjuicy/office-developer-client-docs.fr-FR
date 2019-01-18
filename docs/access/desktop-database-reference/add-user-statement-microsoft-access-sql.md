---
title: Instruction ADD USER (Microsoft Access SQL)
TOCTitle: ADD USER statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ba60a646fd234748bcc39b9a5604a33675caee5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705392"
---
# <a name="add-user-statement-microsoft-access-sql"></a>Instruction ADD USER (Microsoft Access SQL)

**S’applique à**: Access 2013, Office 2013

Ajoute un ou plusieurs *utilisateurs* existants à un *groupe* existant.

## <a name="syntax"></a>Syntaxe

Ajouter un utilisateur *utilisateur*\[, *utilisateur*,... \] Au *groupe*

L'instruction ADD USER comporte trois parties :

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
<td><p><em>utilisateur</em></p></td>
<td><p>Nom de l'utilisateur à ajouter au fichier d'informations du groupe de travail.</p></td>
</tr>
<tr class="even">
<td><p><em>Groupe</em></p></td>
<td><p>Nom du groupe à ajouter au fichier d'informations du groupe de travail.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

Une fois un *utilisateur* a été ajouté à un *groupe*, l' *utilisateur* dispose des autorisations qui ont été accordées au *groupe*.

