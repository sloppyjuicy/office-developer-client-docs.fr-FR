---
title: Recordset2.MoveLast Method (DAO)
TOCTitle: MoveLast Method
ms:assetid: 32717786-c59c-ec22-666b-fc78e4265c5a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192306(v=office.15)
ms:contentKeyID: 48544079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c66adcadcf07ab18db60ba39ae6bc66d58d5e5db
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472556"
---
# <a name="recordset2movelast-method-dao"></a>Recordset2.MoveLast Method (DAO)


**S’applique à**: Access 2013 | Office 2013

Atteint le dernier enregistrement d'un objet **Recordset** spécifié et en fait l'enregistrement actif.

## <a name="syntax"></a>Syntaxe

*expression* . MoveLast (***Options***)

*expression* Variable qui représente un objet **Recordset2** .

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
<td><p>Options</p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Entier long</strong></p></td>
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
> <P>[!REMARQUE] Vous pouvez utiliser la méthode <STRONG>MoveLast</STRONG> pour remplir entièrement un objet <STRONG>Recordset</STRONG> de type feuille de réponse dynamique ou instantané en vue de fournir le nombre actuel d'enregistrements présents dans l'objet <STRONG>Recordset</STRONG>. Toutefois, si vous utilisez <STRONG>MoveLast</STRONG> de cette manière, vous risquez de ralentir l'exécution de votre application. Il n'est conseillé d'utiliser la méthode <STRONG>MoveLast</STRONG> qu'en cas de nécessité absolue d'obtenir un décompte précis des enregistrements présents dans un objet <STRONG>Recordset</STRONG> récemment ouvert. Si vous utilisez la constante <STRONG>dbRunAsync</STRONG> avec <STRONG>MoveLast</STRONG>, l'appel de la méthode est asynchrone. Vous pouvez utiliser la propriété <STRONG>StillExecuting</STRONG> pour déterminer à quel moment l'enregistrement <STRONG>Recordset</STRONG> est rempli entièrement, de même que vous pouvez utiliser la méthode <STRONG>Cancel</STRONG> pour terminer l'exécution de l'appel asynchrone de la méthode <STRONG>MoveLast</STRONG>.</P>



Vous ne pouvez pas utiliser les méthodes **MoveFirst**, **MoveLast**et **MovePrevious** sur un objet **Recordset** de type avant uniquement.

Pour déplacer la position de l'enregistrement actif dans un objet **Recordset** d'un objet d'un nombre d'enregistrements spécifique vers l'avant ou l'arrière, utilisez la méthode **Move**.

