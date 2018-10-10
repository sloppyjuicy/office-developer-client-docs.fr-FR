---
title: Indexes.Delete Method (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b30748c0a1388a1175512e3b8d3fd1970795b821
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469957"
---
# <a name="indexesdelete-method-dao"></a>Indexes.Delete Method (DAO)


**S’applique à**: Access 2013 | Office 2013

Supprime l'objet **Index** spécifié de la collection **Indexes**.

## <a name="syntax"></a>Syntaxe

*expression* . Supprimer (***nom***)

*expression* Variable qui représente un objet **Indexes** .

### <a name="parameters"></a>Paramètres

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
<th><p>Obligatoire/Facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Name</p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Chaîne</strong></p></td>
<td><p>Nom de l'index à supprimer</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

La méthode **Delete** est pris en charge uniquement lorsque l’objet **Index** est nouveau et n’a pas été ajouté à la base de données.

