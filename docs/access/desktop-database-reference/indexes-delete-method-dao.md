---
title: Indexes.Delete, méthode (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3f3b271ccf0c7eb8eee1c95a19469bbe7a6cbf81
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63629929"
---
# <a name="indexesdelete-method-dao"></a>Indexes.Delete, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Supprime l'objet **Index** spécifié de la collection **Indexes**.

## <a name="syntax"></a>Syntaxe

*.* Delete(***Name***)

*expression* Variable qui représente un objet **Indexes** .

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Obligatoire/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Nom de l'index à supprimer</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

La méthode **Delete** n'est prise en charge que lorsque l'objet **Index** est nouveau et qu'il n'a pas été ajouté à la base de données.

