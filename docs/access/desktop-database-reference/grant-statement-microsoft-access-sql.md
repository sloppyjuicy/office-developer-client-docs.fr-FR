---
title: GRANT, instruction (Microsoft Access SQL)
TOCTitle: GRANT Statement (Microsoft Access SQL)
ms:assetid: 50ae97ae-d5be-57e5-d9da-f3fc42f01d83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193820(v=office.15)
ms:contentKeyID: 48544800
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277478
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d4fffc9ac40586be899de0dd4054ba39dd3a6489
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469107"
---
# <a name="grant-statement-microsoft-access-sql"></a>GRANT, instruction (Microsoft Access SQL)


**S’applique à**: Access 2013 | Office 2013

Accorde des privilèges spécifiques à un utilisateur ou un groupe existant.

## <a name="syntax"></a>Syntaxe

GRANT {*privilège*\[, *privilège*, … \]} ON {TABLE *table* | OBJET, *objet*|

CONTENEUR *conteneur* } TO {*nomautorisation*\[, *nomautorisation*, … \]}

L'instruction GRANT est composée des arguments suivants :

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
<td><p>L’ou les privilèges à accorder. Les privilèges sont spécifiés à l’aide de mots clés suivants : sélectionnez, supprimer, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA et UPDATEOWNER.</p></td>
</tr>
<tr class="even">
<td><p><em>nomtable</em></p></td>
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

