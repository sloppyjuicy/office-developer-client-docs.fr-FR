---
title: Méthode Recordset.MoveLast (DAO)
TOCTitle: MoveLast method
ms:assetid: fc0f7a33-1f55-9f5b-b00d-1b81f49b1c3e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837192(v=office.15)
ms:contentKeyID: 48548881
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 79799742499e163a43d51a2d8553adcadf27b36d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715269"
---
# <a name="recordsetmovelast-method-dao"></a>Méthode Recordset.MoveLast (DAO)

**S’applique à**: Access 2013, Office 2013

Atteint le dernier enregistrement d'un objet **Recordset** spécifié et en fait l'enregistrement actif.

## <a name="syntax"></a>Syntaxe

*expression* . MoveLast (***Options***)

*expression* Variable qui représente un objet **Recordset** .

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
<th><p>Requis/facultatif</p></th>
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

Utilisez les méthodes **Move** pour vous déplacer entre les enregistrements sans appliquer de condition.

Si vous modifiez l'enregistrement actif, veillez à utiliser la méthode **Update** pour enregistrer les modifications avant de passer à un autre enregistrement. Si vous accédez à un autre enregistrement alors que vous effectuez une mise à jour, les modifications seront perdues sans notification.

Lorsque vous ouvrez un objet **Recordset**, le premier enregistrement est actif et la propriété **BOF** a la valeur **False**. Si l'objet **Recordset** ne contient pas d'enregistrements, la propriété **BOF** a la valeur **True** et aucun enregistrement n'est actif.

Si le premier ou le dernier enregistrement est déjà actif lorsque vous utilisez la méthode **MoveFirst** ou **MoveLast**, l'enregistrement actif ne change pas.

Si le jeu d’enregistrements fait référence à un **objet Recordset** de type table (espaces de travail Microsoft Access uniquement), le déplacement suit l’index actuel. Vous pouvez définir l'index actif à l'aide de la propriété **Index**. Si vous ne définissez pas l'index actuel, l'ordre des enregistrements renvoyés est indéfini.

> [!NOTE]
> [!REMARQUE] Vous pouvez utiliser la méthode **MoveLast** pour remplir entièrement un objet **Recordset** de type feuille de réponse dynamique ou instantané en vue de fournir le nombre actuel d'enregistrements présents dans l'objet **Recordset**. Toutefois, si vous utilisez **MoveLast** de cette manière, vous risquez de ralentir l'exécution de votre application. Il n'est conseillé d'utiliser la méthode **MoveLast** qu'en cas de nécessité absolue d'obtenir un décompte précis des enregistrements présents dans un objet **Recordset** récemment ouvert. 
> 
> Si vous utilisez la constante **dbRunAsync** avec **MoveLast**, l'appel de la méthode est asynchrone. Vous pouvez utiliser la propriété **StillExecuting** pour déterminer à quel moment l'enregistrement **Recordset** est rempli entièrement, de même que vous pouvez utiliser la méthode **Cancel** pour terminer l'exécution de l'appel asynchrone de la méthode **MoveLast**.

Vous ne pouvez pas utiliser les méthodes **MoveFirst**, **MoveLast**et **MovePrevious** sur un objet **Recordset** de type avant uniquement.

Pour déplacer la position de l'enregistrement actif dans un objet **Recordset** d'un objet d'un nombre d'enregistrements spécifique vers l'avant ou l'arrière, utilisez la méthode **Move**.

