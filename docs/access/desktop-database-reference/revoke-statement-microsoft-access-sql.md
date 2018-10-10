---
title: REVOKE, instruction (Microsoft Access SQL)
TOCTitle: REVOKE Statement (Microsoft Access SQL)
ms:assetid: 69399fd6-c4e8-f2e2-e5f4-48ae779323f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195272(v=office.15)
ms:contentKeyID: 48545409
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277479
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bf8bbe65b8fe359e9e410d652deb41a1192efa92
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469734"
---
# <a name="revoke-statement-microsoft-access-sql"></a>REVOKE, instruction (Microsoft Access SQL)


**S’applique à**: Access 2013 | Office 2013

Révoque des privilèges spécifiques à un utilisateur ou à un groupe existant.

## <a name="syntax"></a>Syntaxe

REVOKE {*privilège*\[, *privilège*, … \]} ON {TABLE *table* | OBJET, *objet*|

{Container *conteneur*} FROM {*nomautorisation*\[, *nomautorisation*, … \]}

L'instruction REVOKE est composée des arguments suivants :

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
<td><p><em>privilège</em></p></td>
<td><p>L’ou les privilèges à révoquer. Les privilèges sont spécifiés à l’aide de mots clés suivants : sélectionnez, supprimer, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA et UPDATEOWNER.</p></td>
</tr>
<tr class="even">
<td><p><em>table</em></p></td>
<td><p>Tout nom de table valide.</p></td>
</tr>
<tr class="odd">
<td><p><em>object</em></p></td>
<td><p>Tout objet autre qu'une table. Il peut s'agir d'une requête stockée (vue ou procédure), par exemple.</p></td>
</tr>
<tr class="even">
<td><p><em>conteneur</em></p></td>
<td><p>Nom d'un conteneur valide.</p></td>
</tr>
<tr class="odd">
<td><p><em>nomautorisation</em></p></td>
<td><p>Nom d'utilisateur ou de groupe.</p></td>
</tr>
</tbody>
</table>

