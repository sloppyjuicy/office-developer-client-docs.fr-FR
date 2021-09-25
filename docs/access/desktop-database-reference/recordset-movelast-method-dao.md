---
title: Recordset.MoveLast, méthode (DAO)
TOCTitle: MoveLast method
ms:assetid: fc0f7a33-1f55-9f5b-b00d-1b81f49b1c3e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837192(v=office.15)
ms:contentKeyID: 48548881
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ac09a5a63da8748346fa94b4fc661653698c7521
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606211"
---
# <a name="recordsetmovelast-method-dao"></a>Recordset.MoveLast, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Atteint le dernier enregistrement d’un objet **Recordset** spécifié et en fait l’enregistrement actif.

## <a name="syntax"></a>Syntaxe

*.* MoveLast(***Options***)

*expression* Variable qui représente un objet **Recordset**.

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
<td><p><em>Options</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Associez ce paramètre à la constante <strong>dbRunAsync</strong> pour obtenir une exécution asynchrone de l'appel de <strong>MoveLast</strong></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

La méthode **Move** permet de passer d’un enregistrement à un autre sans appliquer de condition.

Si vous modifiez l’enregistrement actif, utilisez la méthode **Update** pour enregistrer les modifications avant de passer à un autre enregistrement. Si vous passez à un autre enregistrement sans procéder à la mise à jour, vos modifications seront perdues sans avertissement.

Lorsque vous ouvrez un objet **Recordset**, le premier enregistrement est actif et la propriété **BOF** a la valeur **False**. Si l’objet **Recordset** ne contient pas d’enregistrements, la propriété **BOF** a la valeur **True** et aucun enregistrement n’est actif.

Si le premier ou le dernier enregistrement est déjà actif lorsque vous utilisez la méthode **MoveFirst** ou **MoveLast**, l’enregistrement actif ne change pas.

Si recordset fait référence à un objet **Recordset** de type table (espaces de travail Microsoft Access uniquement), le déplacement suit l’index actuel. Vous pouvez définir l'index actuel par le biais de la propriété **Index**. Si vous ne définissez pas l’index actuel, l’ordre des enregistrements renvoyés est indéfini.

> [!NOTE]
> [!REMARQUE] Vous pouvez utiliser la méthode **MoveLast** pour remplir entièrement un objet **Recordset** de type feuille de réponse dynamique ou instantané en vue de fournir le nombre actuel d'enregistrements présents dans l'objet **Recordset**. Toutefois, si vous utilisez **MoveLast** de cette manière, vous risquez de ralentir l'exécution de votre application. Il n'est conseillé d'utiliser la méthode **MoveLast** qu'en cas de nécessité absolue pour obtenir un décompte précis des enregistrements présents dans un objet **Recordset** récemment ouvert. 
> 
> Si vous utilisez la constante **dbRunAsync** avec **MoveLast**, l'appel de la méthode est asynchrone. Vous pouvez utiliser la propriété **StillExecuting** pour déterminer à quel moment l'enregistrement **Recordset** est rempli entièrement, de même que vous pouvez utiliser la méthode **Cancel** pour terminer l'exécution de l'appel asynchrone de la méthode **MoveLast**.

Vous ne pouvez pas appliquer les méthodes **MoveFirst**, **MoveLast** et **MovePrevious** à un objet **Recordset** de type avant uniquement.

Pour faire avancer ou reculer l’enregistrement actif d’un certain nombre d’enregistrements dans un objet **Recordset**, utilisez la méthode **Move**.

