---
title: TableDefs.Delete, méthode (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63f543fd86e309372e0432c3e45513cd9d3942ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313992"
---
# <a name="tabledefsdelete-method-dao"></a>TableDefs.Delete, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Supprime l'objet **TableDef** spécifié de la collection **TableDefs**.

## <a name="syntax"></a>Syntaxe

*.* Delete(***Name***)

*expression* Variable qui représente un **objet TableDefs.**

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
<td><p>Nom de l'objet TableDef à supprimer.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

La méthode Delete n'est prise en charge que lorsque l'objet **TableDef** est nouveau et n'a pas été ajouté à la base de données, ou lorsque la propriété **Updatable** de l'objet **TableDef** prend la valeur **True**.

