---
title: Méthode Relations.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7c7a42098bcc64a58f8a004c0f1d5a35fd4f34b7
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998923"
---
# <a name="relationsdelete-method-dao"></a>Méthode Relations.Delete (DAO)

**S’applique à**: Access 2013, Office 2013

Supprime l'objet **Relation** spécifié de la collection **Relations**.

## <a name="syntax"></a>Syntaxe

*expression* . Supprimer (***nom***)

*expression* Variable qui représente un objet **Relations** .

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
<td><p>Nom de la relation à supprimer.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

La méthode **Delete** n'est prise en charge que lorsque l'objet **Relation** est un nouvel objet qui n'a pas été ajouté.

