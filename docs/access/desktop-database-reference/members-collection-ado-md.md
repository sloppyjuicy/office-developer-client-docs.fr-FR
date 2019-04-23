---
title: Members, collection (ADO MD)
TOCTitle: Members collection (ADO MD)
ms:assetid: 1389c554-e4f1-107d-22c6-7fe851d53d23
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248910(v=office.15)
ms:contentKeyID: 48543371
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: adc8ed771bcba6a4b6532b33b27980f8aab695c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289240"
---
# <a name="members-collection-ado-md"></a>Members, collection (ADO MD)


**S’applique à** : Access 2013, Office 2013

Contient les objets [Member](member-object-ado-md.md) d’un niveau ou d’une position le long d’un axe.

## <a name="remarks"></a>Remarques

Une collection **Members** permet de contenir les types de membres suivants :

  - Les membres constituant un niveau dans un cube. Ils figurent dans la collection **Members** d'un objet [Level](level-object-ado-md.md). Par exemple, dans le cadre de l'exemple de la rubrique [Présentation des schémas et données multidimensionnels](overview-of-multidimensional-schemas-and-data.md), les quatre membres du niveau Pays sont Canada, USA, UK et Germany.

  - Les membres qui sont les enfants d'un membre spécifique au sein d'une hiérarchie. Ces membres sont renvoyés par la propriété [Children](children-property-ado-md.md) de l'objet **Member** parent. Par exemple, toujours dans le cadre du même exemple, les deux enfants du membre Canada sont Canada-East et Canada-West.

  - Les membres définissant une position spécifique le long d'un axe d'un [ensemble de cellules](cellset-object-ado-md.md). En se basant sur l'ensemble de cellules de l'exemple de la rubrique [Utilisation de données multidimensionnelles](working-with-multidimensional-data.md), les deux membres de la première position de l' axe des x sont Valentine et Seattle. Ces membres font partie de la collection **Members** d'un objet [Position](position-object-ado-md.md).

**Members** est une collection ADO standard. Avec les propriétés et méthodes d'une collection, vous pouvez :

  - Obtenir le nombre d'objets d'une collection à l'aide de la propriété [Count](count-property-ado.md).

  - Renvoyer un objet de la collection à l'aide de la propriété [Item](item-property-ado.md) par défaut.

  - Mettre à jour les objets de la collection à partir du fournisseur à l'aide de la méthode [Refresh](refresh-method-ado.md).

