---
title: Recordset2.MovePrevious, méthode (DAO)
TOCTitle: MovePrevious Method
ms:assetid: 8c433810-4b19-e7c1-3cee-a0bc50b23e8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197336(v=office.15)
ms:contentKeyID: 48546235
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9753d3bbb586e2c1bd44755deb529758d8eab060
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307244"
---
# <a name="recordset2moveprevious-method-dao"></a>Recordset2.MovePrevious, méthode (DAO)


**S’applique à** : Access 2013, Office 2013

Atteint l’enregistrement d’un objet **Recordset** précédent spécifié et en fait l’enregistrement actif.

## <a name="syntax"></a>Syntaxe

*.* MovePrevious

*expression* Variable qui représente un **objet Recordset2.**

## <a name="remarks"></a>Remarques

La méthode **Move** permet de passer d’un enregistrement à un autre sans appliquer de condition.

Si vous modifiez l’enregistrement actif, utilisez la méthode **Update** pour enregistrer les modifications avant de passer à un autre enregistrement. Si vous passez à un autre enregistrement sans procéder à la mise à jour, vos modifications seront perdues sans avertissement.

Lorsque vous ouvrez un objet **Recordset**, le premier enregistrement est actif et la propriété **BOF** a la valeur **False**. Si l’objet **Recordset** ne contient pas d’enregistrements, la propriété **BOF** a la valeur **True** et aucun enregistrement n’est actif.

Si vous utilisez **MovePrevious** alors que le premier enregistrement est actif, la propriété **BOF** a la valeur **True**, et aucun enregistrement n'est actif. Si vous utilisez à nouveau **MovePrevious**, une erreur se produit et **BOF** conserve la valeur **True**.

Si recordset fait référence à un objet **Recordset** de type table (espaces de travail Microsoft Access uniquement), le déplacement suit l’index actuel. Vous pouvez définir l'index actuel par le biais de la propriété **Index**. Si vous ne définissez pas l’index actuel, l’ordre des enregistrements renvoyés est indéfini.

Vous ne pouvez pas appliquer les méthodes **MoveFirst**, **MoveLast** et **MovePrevious** à un objet **Recordset** de type avant uniquement.

Pour faire avancer ou reculer l’enregistrement actif d’un certain nombre d’enregistrements dans un objet **Recordset**, utilisez la méthode **Move**.

