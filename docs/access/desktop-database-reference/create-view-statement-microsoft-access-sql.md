---
title: Instruction CREATE VIEW (Microsoft Access SQL)
TOCTitle: CREATE VIEW statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: f1d13cef4551975dc316b2fbedf2388028956fb3
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862904"
---
# <a name="create-view-statement-microsoft-access-sql"></a>Instruction CREATE VIEW (Microsoft Access SQL)

**S’applique à**: Access 2013 | Office 2013

Crée un nouvel affichage.

> [!NOTE]
> [!REMARQUE] Le moteur de base de données Microsoft Access ne prend pas en charge l'instruction CREATE VIEW, ni les instructions DDL, avec les bases de données autres que Microsoft Access.

## <a name="syntax"></a>Syntaxe

CREATE VIEW *affichage* \[(*champ1*\[, *champ2*\[,... \] \])\] AS *instructionselect*

L'instruction CREATE VIEW est composée des arguments suivants :

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
<td><p><em>view</em></p></td>
<td><p>Nom de l'affichage à créer.</p></td>
</tr>
<tr class="even">
<td><p><em>champ1</em>, <em>champ2</em></p></td>
<td><p>Nom des champs correspondants spécifiés dans <em>instuctionselect</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>instructionselect</em></p></td>
<td><p>Instruction SELECT SQL. Pour plus d’informations, voir <a href="select-statement-microsoft-access-sql.md">l’instruction SELECT</a>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

L'instruction SELECT qui définit l'affichage ne peut pas être une instruction [SELECT INTO](select-into-statement-microsoft-access-sql.md).

Cette instruction ne peut pas non plus contenir de paramètres.

Le nom de l'affichage ne peut pas être le même que le nom d'une table existante.

Si la requête définie par l’instruction SELECT est modifiable, l’affichage est également être mise à jour. Sinon, l'affichage est en lecture seule.

Si deux champs dans la requête définie par l'instruction SELECT ont le même nom, la définition de l'affichage doit inclure une liste de noms uniques pour les champs dans la requête.

