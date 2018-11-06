---
title: Méthode Indexes.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0c725919b6509b5c802502fc8280823c407516f6
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998825"
---
# <a name="indexesdelete-method-dao"></a>Méthode Indexes.Delete (DAO)

**S’applique à**: Access 2013, Office 2013

Supprime l'objet **Index** spécifié de la collection **Indexes**.

## <a name="syntax"></a>Syntaxe

*expression* . Supprimer (***nom***)

*expression* Variable qui représente un objet **Indexes** .

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Requis/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Chaîne</strong></p></td>
<td><p>Nom de l'index à supprimer</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

La méthode **Delete** est pris en charge uniquement lorsque l’objet **Index** est nouveau et n’a pas été ajouté à la base de données.

