---
title: Méthode TableDefs.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d511155f7a5fe1e6b83092e2065302bab99765b
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999007"
---
# <a name="tabledefsdelete-method-dao"></a>Méthode TableDefs.Delete (DAO)

**S’applique à**: Access 2013, Office 2013

Supprime l'objet **TableDef** spécifié de la collection **TableDefs**.

## <a name="syntax"></a>Syntaxe

*expression* . Supprimer (***nom***)

*expression* Variable qui représente un objet **TableDef** .

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
<td><p>Nom de l'objet TableDef à supprimer.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

La méthode Delete est pris en charge uniquement lorsque l’objet **TableDef** est nouveau et n’a pas été ajouté à la base de données, ou lorsque la propriété **Updatable** de l' **objet TableDef** est définie sur **True**.

