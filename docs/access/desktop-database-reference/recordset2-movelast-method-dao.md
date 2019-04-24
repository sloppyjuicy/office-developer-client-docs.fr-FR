---
title: Recordset2. MoveLast, méthode (DAO)
TOCTitle: MoveLast Method
ms:assetid: 32717786-c59c-ec22-666b-fc78e4265c5a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192306(v=office.15)
ms:contentKeyID: 48544079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 829c4dd759bce86388cc65aa5b63276eec438ea0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307258"
---
# <a name="recordset2movelast-method-dao"></a>Recordset2. MoveLast, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Atteint le dernier enregistrement d'un objet **Recordset** spécifié et en fait l'enregistrement actif.

## <a name="syntax"></a>Syntaxe

*expression* . MoveLast (***options***)

*expression* Variable qui représente un objet **Recordset2** .

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
<td><p><strong>Entier long</strong></p></td>
<td><p>Associez ce paramètre à la constante <strong>dbRunAsync</strong> pour obtenir une exécution asynchrone de l'appel de <strong>MoveLast</strong></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

La méthode **Move** permet de passer d’un enregistrement à un autre sans appliquer de condition.

Si vous modifiez l'enregistrement actif, utilisez la méthode **Update** pour enregistrer les modifications avant de passer à un autre enregistrement. Si vous passez à un autre enregistrement sans procéder à la mise à jour, vos modifications seront perdues sans avertissement.

Lorsque vous ouvrez un objet **Recordset**, le premier enregistrement est actif et la propriété **BOF** a la valeur **False**. Si l'objet **Recordset** ne contient pas d'enregistrements, la propriété **BOF** a la valeur **True** et aucun enregistrement n'est actif.

Si le premier ou le dernier enregistrement est déjà actif lorsque vous utilisez la méthode **MoveFirst** ou **MoveLast**, l'enregistrement actif ne change pas.

Si l'objet Recordset fait référence à un **objet Recordset** de type table (espaces de travail Microsoft Access uniquement), le déplacement suit l'index actif. Vous pouvez définir l'index actuel par le biais de la propriété **Index**. Si vous ne définissez pas l'index actuel, l'ordre des enregistrements renvoyés est indéfini.

> [!NOTE]
> [!REMARQUE] Vous pouvez utiliser la méthode **MoveLast** pour remplir entièrement un objet **Recordset** de type feuille de réponse dynamique ou instantané en vue de fournir le nombre actuel d'enregistrements présents dans l'objet **Recordset**. Toutefois, si vous utilisez **MoveLast** de cette manière, vous risquez de ralentir l'exécution de votre application. Il n'est conseillé d'utiliser la méthode **MoveLast** qu'en cas de nécessité absolue pour obtenir un décompte précis des enregistrements présents dans un objet **Recordset** récemment ouvert. 
>
> Si vous utilisez la constante **dbRunAsync** avec **MoveLast**, l'appel de la méthode est asynchrone. Vous pouvez utiliser la propriété **StillExecuting** pour déterminer à quel moment l'enregistrement **Recordset** est rempli entièrement, de même que vous pouvez utiliser la méthode **Cancel** pour terminer l'exécution de l'appel asynchrone de la méthode **MoveLast**.

Vous ne pouvez pas appliquer les méthodes **MoveFirst**, **MoveLast** et **MovePrevious** à un objet **Recordset** de type avant uniquement.

Pour faire avancer ou reculer l’enregistrement actif d’un certain nombre d’enregistrements dans un objet **Recordset**, utilisez la méthode **Move**.

