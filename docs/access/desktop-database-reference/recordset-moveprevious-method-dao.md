---
title: Recordset.MovePrevious Method (DAO)
TOCTitle: MovePrevious Method
ms:assetid: 82a3bc3e-5221-9a1a-1350-47bc6759edeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196699(v=office.15)
ms:contentKeyID: 48545984
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052872
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bfd6682ea278d499a50c0632186b204610e80ea6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880326"
---
# <a name="recordsetmoveprevious-method-dao"></a>Recordset.MovePrevious Method (DAO)


**S’applique à**: Access 2013, Office 2013

Atteint l'enregistrement précédent d'un objet **Recordset** spécifié et en fait l'enregistrement actif.

## <a name="syntax"></a>Syntaxe

*expression* . MovePrevious

*expression* Variable qui représente un objet **Recordset** .

## <a name="remarks"></a>Remarques

Utilisez les méthodes **Move** pour vous déplacer entre les enregistrements sans appliquer de condition.

Si vous modifiez l'enregistrement actif, veillez à utiliser la méthode **Update** pour enregistrer les modifications avant de passer à un autre enregistrement. Si vous accédez à un autre enregistrement alors que vous effectuez une mise à jour, les modifications seront perdues sans notification.

Lorsque vous ouvrez un objet **Recordset**, le premier enregistrement est actif et la propriété **BOF** prend la valeur **False**. Si l'objet **Recordset** ne contient pas d'enregistrement, la propriété **BOF** prend la valeur **True**, et il n'y a pas d'enregistrement actif.

Si vous utilisez **MovePrevious** alors que le premier enregistrement est actif, la propriété **BOF** a la valeur **True**, et aucun enregistrement n'est actif. Si vous utilisez à nouveau **MovePrevious**, une erreur se produit et **BOF** conserve la valeur **True**.

Si le jeu d’enregistrements fait référence à un **objet Recordset** de type table (espaces de travail Microsoft Access uniquement), le déplacement suit l’index actuel. Vous pouvez définir l'index actif à l'aide de la propriété **Index**. Si vous ne définissez pas l'index actif, l'ordre des enregistrements renvoyés est indéfini.

Vous ne pouvez pas utiliser les méthodes **MoveFirst**, **MoveLast**et **MovePrevious** sur un objet **Recordset** de type avant uniquement.

Pour déplacer la position de l'enregistrement actif dans un objet **Recordset** d'un objet d'un nombre d'enregistrements spécifique vers l'avant ou l'arrière, utilisez la méthode **Move**.

