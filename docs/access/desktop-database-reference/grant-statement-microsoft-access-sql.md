---
title: GRANT, instruction (Microsoft Access SQL)
TOCTitle: GRANT statement (Microsoft Access SQL)
ms:assetid: 50ae97ae-d5be-57e5-d9da-f3fc42f01d83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193820(v=office.15)
ms:contentKeyID: 48544800
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277478
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4357099f8bcb9b2308b5cda3543949765b8c3420
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292131"
---
# <a name="grant-statement-microsoft-access-sql"></a>GRANT, instruction (Microsoft Access SQL)

**S’applique à** : Access 2013, Office 2013

Accorde des privilèges spécifiques à un utilisateur ou un groupe existant.

## <a name="syntax"></a>Syntaxe

GRANT {*privilège* \[ , *privilège*, ... \] } ON{Table *|* OBJECT, *objet*|

CONTAINER *container* } TO {*authorizationname* \[ , *authorizationname*, ... \] }

L'instruction GRANT est composée des arguments suivants :

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
<td><p><em>privilège</em></p></td>
<td><p>Privilège à accorder. Les privilèges sont spécifiés à l’aide des mots clés suivants : SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA et UPDATEOWNER.</p></td>
</tr>
<tr class="even">
<td><p><em>tablename</em></p></td>
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
<td><p><em>authorizationname</em></p></td>
<td><p>Nom d'utilisateur ou de groupe.</p></td>
</tr>
</tbody>
</table>

