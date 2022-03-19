---
title: CREATE USER ou GROUP, instruction (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e10ffb62b7d045591d468a99be4538b27ad9b9cb
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63633595"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a>CREATE USER ou GROUP, instruction (Microsoft Access SQL)

**S’applique à** : Access 2013, Office 2013

Crée un ou plusieurs nouveaux utilisateurs ou groupes.

## <a name="syntax"></a>Syntaxe

### <a name="create-a-user"></a>Créer un utilisateur

CREATE USER *password* *pid* \[, *user* *password pid*, ...\]

### <a name="create-a-group"></a>Créer un groupe

CREATE GROUP *group* *pid*\[, *group* *pid*, ...\]

L'instruction CREATE USER ou GROUP est composée des arguments suivants :

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Quitter</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>utilisateur</em></p></td>
<td><p>Nom de l'utilisateur à ajouter au fichier d'informations du groupe de travail.</p></td>
</tr>
<tr class="even">
<td><p><em>groupe</em></p></td>
<td><p>Nom du groupe à ajouter au fichier d'informations du groupe de travail.</p></td>
</tr>
<tr class="odd">
<td><p><em>mot de passe</em></p></td>
<td><p>Mot de passe à associer au nom de l'<em>utilisateur</em> spécifié.</p></td>
</tr>
<tr class="even">
<td><p><em>pid</em></p></td>
<td><p>Identifiant personnel.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Un *utilisateur* et un *groupe* ne peuvent pas avoir le même nom.

Un *mot de passe* est requis pour chaque *utilisateur* ou *groupe* qui est créé.

