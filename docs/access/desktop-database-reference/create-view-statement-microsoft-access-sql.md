---
title: CREATE VIEW, instruction (Microsoft Access SQL)
TOCTitle: CREATE VIEW statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 2f46b897ba4e37f454c656f39333f5c4e0389e94
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581587"
---
# <a name="create-view-statement-microsoft-access-sql"></a>CREATE VIEW, instruction (Microsoft Access SQL)

**S’applique à** : Access 2013, Office 2013

Crée un affichage.

> [!NOTE]
> Le moteur de base de données Microsoft Access ne prend pas en charge l’utilisation de CRÉER UN AFFICHAGE, ni d’aucune des instructions DDL, avec des bases de données d’un moteur de base de données autre que Microsoft Access.

## <a name="syntax"></a>Syntaxe

CREATE VIEW *view* \[(*field1*\[, *field2*\[, …\]\])\] AS *selectstatement*

L’instruction CRÉER UN AFFICHAGE est composée des éléments suivants :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Quitter</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>view</em></p></td>
<td><p>Nom de l’affichage à créer.</p></td>
</tr>
<tr class="even">
<td><p><em>champ1</em>, <em>champ2</em></p></td>
<td><p>Nom du ou des champs pour les champs correspondants spécifiés dans <em>instructionselect</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>instructionselect</em></p></td>
<td><p>Instruction SELECT SQL. Pour plus d’informations, voir <a href="select-statement-microsoft-access-sql.md">SELECT, instruction</a>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

L’instruction SELECT qui définit l’affichage ne peut pas être une instruction [SELECT INTO](select-into-statement-microsoft-access-sql.md).

L’instruction SELECT qui définit l’affichage ne peut pas contenir de paramètres.

Le nom de l’affichage ne peut pas être identique au nom d’une table existante.

Si la requête définie par l'instruction SELECT est modifiable, l'affichage l'est également. Sinon, l’affichage est en lecture seule.

Si deux des champs de la requête définis par l’instruction SELECT ont le même nom, la définition de l’affichage doit comporter une liste de champs spécifiant des noms uniques pour chacun des champs de la requête.

