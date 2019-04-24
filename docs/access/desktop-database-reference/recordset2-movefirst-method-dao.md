---
title: Recordset2. MoveFirst, méthode (DAO)
TOCTitle: MoveFirst Method
ms:assetid: 74b186d0-8f6a-d136-a563-04f58d67b122
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195879(v=office.15)
ms:contentKeyID: 48545667
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a54658e1259a49a1c92facf988076e6b6e1dd961
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309659"
---
# <a name="recordset2movefirst-method-dao"></a>Recordset2. MoveFirst, méthode (DAO)


**S’applique à** : Access 2013, Office 2013

Atteint le premier enregistrement d’un objet **Recordset** spécifié et en fait l’enregistrement actif.

## <a name="syntax"></a>Syntaxe

*expression* . Méthodes

*expression* Variable qui représente un objet **Recordset2** .

## <a name="remarks"></a>Remarques

La méthode **Move** permet de passer d’un enregistrement à un autre sans appliquer de condition.

Si vous modifiez l'enregistrement actif, utilisez la méthode **Update** pour enregistrer les modifications avant de passer à un autre enregistrement. Si vous passez à un autre enregistrement sans procéder à la mise à jour, vos modifications seront perdues sans avertissement.

Lorsque vous ouvrez un objet **Recordset**, le premier enregistrement est actif et la propriété **BOF** a la valeur **False**. Si l'objet **Recordset** ne contient pas d'enregistrements, la propriété **BOF** a la valeur **True** et aucun enregistrement n'est actif.

Si le premier ou le dernier enregistrement est déjà actif lorsque vous utilisez la méthode **MoveFirst** ou **MoveLast**, l'enregistrement actif ne change pas.

Si l'objet Recordset fait référence à un **objet Recordset** de type table (espaces de travail Microsoft Access uniquement), le déplacement suit l'index actif. Vous pouvez définir l'index actuel par le biais de la propriété **Index**. Si vous ne définissez pas l’index actuel, l’ordre des enregistrements renvoyés est indéfini.

Vous ne pouvez pas appliquer les méthodes **MoveFirst**, **MoveLast** et **MovePrevious** à un objet **Recordset** de type avant uniquement.

Pour faire avancer ou reculer l’enregistrement actif d’un certain nombre d’enregistrements dans un objet **Recordset**, utilisez la méthode **Move**.

