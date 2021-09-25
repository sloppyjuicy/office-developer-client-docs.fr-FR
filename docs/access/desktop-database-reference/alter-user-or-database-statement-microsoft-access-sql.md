---
title: ALTER USER ou DATABASE, instruction (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9e2ef710d9a7036cc9f15e2c69d37e84393f978d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559072"
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
<td><p><em>newpassword</em></p></td>
<td><p>Nouveau mot de passe à associer au nom de l'<em>utilisateur</em> ou de la <em>base de données</em> spécifié.</p></td>
</tr>
<tr class="odd">
<td><p><em>oldpassword</em></p></td>
<td><p>Mot de passe existant à associer au nom de l'<em>utilisateur</em> ou du <em>groupe</em> spécifié.</p></td>
</tr>
</tbody>
</table>

