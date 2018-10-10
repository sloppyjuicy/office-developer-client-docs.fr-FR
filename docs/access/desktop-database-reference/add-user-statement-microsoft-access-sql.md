---
title: ADD USER, instruction (Microsoft Access SQL)
TOCTitle: ADD USER Statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba08ab3104fa08780e8affa310b52a65f67d8831
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470883"
---
# <a name="add-user-statement-microsoft-access-sql"></a>ADD USER, instruction (Microsoft Access SQL)

**S’applique à**: Access 2013 | Office 2013

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

Une fois qu’un *utilisateur* a été ajouté à un *groupe,* l' *utilisateur* dispose des autorisations qui ont été accordées au *groupe*.

