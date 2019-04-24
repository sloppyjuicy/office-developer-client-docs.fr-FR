---
title: ALTER USER ou DATABASE, instruction (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2514ca6403ce70acae9e344d610fbd7b9ba7d73b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297178"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a>ALTER USER ou DATABASE, instruction (Microsoft Access SQL)

**S’applique à** : Access 2013, Office 2013

Change le mot de passe d'un utilisateur ou d'une base de données existant.

## <a name="syntax"></a>Syntaxe

ALTER DATABASE PASSWORD *nouveaumotdepasse ancienmotdepasse*

ALTER USER *utilisateur* PASSWORD *nouveaumotdepasse ancienmotdepasse*

L'instruction ALTER USER ou DATABASE est composée des arguments suivants :

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
<td><p><em>newPassword</em></p></td>
<td><p>Nouveau mot de passe à associer au nom de l'<em>utilisateur</em> ou de la <em>base de données</em> spécifié.</p></td>
</tr>
<tr class="odd">
<td><p><em>oldPassword</em></p></td>
<td><p>Mot de passe existant à associer au nom de l'<em>utilisateur</em> ou du <em>groupe</em> spécifié.</p></td>
</tr>
</tbody>
</table>

