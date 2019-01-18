---
title: Instruction CREATE USER ou GROUP (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b294af16498778eae94b38a7a31b93fd029585e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710922"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a>Instruction CREATE USER ou GROUP (Microsoft Access SQL)

**S’applique à**: Access 2013, Office 2013

Crée un ou plusieurs nouveaux utilisateurs ou groupes.

## <a name="syntax"></a>Syntaxe

### <a name="create-a-user"></a>Créer un utilisateur

CREATE USER *utilisateur* *le mot de passe identifiant personnel* \[, *utilisateur* *le mot de passe identifiant personnel*,...\]

### <a name="create-a-group"></a>Créer un groupe

CREATE GROUP *groupe* *identifiant personnel*\[, *groupe* *identifiant personnel*,...\]

L'instruction CREATE USER ou GROUP est composée des arguments suivants :

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
<tr class="odd">
<td><p><em>mot de passe </em></p></td>
<td><p>Mot de passe à associer au nom de l'<em>utilisateur</em> spécifié.</p></td>
</tr>
<tr class="even">
<td><p><em>identifiant personnel</em></p></td>
<td><p>Identifiant personnel.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

Un *utilisateur* et un *groupe* ne peut pas avoir le même nom.

Un *mot de passe* est requis pour chaque *utilisateur* ou le *groupe* qui est créé.

