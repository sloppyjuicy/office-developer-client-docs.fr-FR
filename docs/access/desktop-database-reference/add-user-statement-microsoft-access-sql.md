---
title: ADD USER, instruction (Microsoft Access SQL)
TOCTitle: ADD USER statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9eed2a6f66a2e23294aa3354178a051fe4a699b7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590169"
---
# <a name="add-user-statement-microsoft-access-sql"></a>ADD USER, instruction (Microsoft Access SQL)

**S’applique à** : Access 2013, Office 2013

Ajoute un ou plusieurs *utilisateurs* existants à un *groupe* existant.

## <a name="syntax"></a>Syntaxe

AJOUTER un *utilisateur,* \[ un *utilisateur,*... \] Groupe  TO

L'instruction ADD USER comporte trois parties :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Élément</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>utilisateur</em></p></td>
<td><p>Nom de l'utilisateur à ajouter au fichier d'informations du groupe de travail.</p></td>
</tr>
<tr class="even">
<td><p><em>group</em></p></td>
<td><p>Nom du groupe à ajouter au fichier d'informations du groupe de travail.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Une fois *qu’un* utilisateur *a* été ajouté à un groupe, *il* dispose de toutes les autorisations qui ont été accordées au *groupe.*

