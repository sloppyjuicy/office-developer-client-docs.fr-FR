---
title: LevelDepth, propriété (ADO MD)
TOCTitle: LevelDepth property (ADO MD)
ms:assetid: ba680f1e-2731-ad6b-4cee-cd3d8d114788
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249894(v=office.15)
ms:contentKeyID: 48547366
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 664a21f8b642c8db27580993089268e5d7b6f4ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290005"
---
# <a name="leveldepth-property-ado-md"></a>LevelDepth, propriété (ADO MD)


**S’applique à** : Access 2013, Office 2013

Indique le nombre de niveaux entre la racine de la hiérarchie et un membre.

## <a name="return-values"></a>Valeurs de retour

Retourne un entier de type **Long** et est en lecture seule.

## <a name="remarks"></a>Remarques

Utilisez la propriété **LevelDepth** pour déterminer la distance de l’objet [Member](member-object-ado-md.md) par rapport au niveau racine de la hiérarchie. La valeur de la propriété **LevelDepth** d’un membre de niveau racine est 0. Cela correspond à la propriété [Depth](depth-property-ado-md.md) d’un objet [Level](level-object-ado-md.md).

