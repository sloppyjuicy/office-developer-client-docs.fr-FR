---
title: Relations.Delete, méthode (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 21f61f562a50dab3bf4256f6b56afa39c7715a89
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557868"
---
# <a name="relationsdelete-method-dao"></a>Relations.Delete, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Supprime l'objet **Relation** spécifié de la collection **Relations**.

## <a name="syntax"></a>Syntaxe

*.* Delete(***Name***)

*expression* Variable qui représente un objet **Relations.**

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
<td><p>Nom de la relation à supprimer.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

La méthode **Delete** n'est prise en charge que lorsque l'objet **Relation** est un nouvel objet qui n'a pas été ajouté.

