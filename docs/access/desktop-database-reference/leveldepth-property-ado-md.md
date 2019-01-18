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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708563"
---
# <a name="leveldepth-property-ado-md"></a>LevelDepth, propriété (ADO MD)


**S’applique à**: Access 2013, Office 2013

Indique le nombre de niveaux entre la racine de la hiérarchie et un membre.

## <a name="return-values"></a>Valeurs de retour

Retourne un entier de type **Long** et est en lecture seule.

## <a name="remarks"></a>Notes

Utilisez la propriété **LevelDepth** pour déterminer la distance de l'objet [Member](member-object-ado-md.md) par rapport au niveau racine de la hiérarchie. La valeur de la propriété **LevelDepth** d'un membre de niveau racine est 0. Cela correspond à la propriété [Depth](depth-property-ado-md.md) d'un objet [Level](level-object-ado-md.md).

