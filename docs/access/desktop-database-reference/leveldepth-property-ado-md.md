---
title: LevelDepth, propriété (ADO MD)
TOCTitle: LevelDepth property (ADO MD)
ms:assetid: ba680f1e-2731-ad6b-4cee-cd3d8d114788
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249894(v=office.15)
ms:contentKeyID: 48547366
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8ea31e6197e1c646632a312ed417bbbd1be9f4d7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923503"
---
# <a name="leveldepth-property-ado-md"></a>LevelDepth, propriété (ADO MD)


**S’applique à**: Access 2013, Office 2013

Indique le nombre de niveaux entre la racine de la hiérarchie et un membre.

## <a name="return-values"></a>Valeurs de retour

Retourne un entier de type **Long** et est en lecture seule.

## <a name="remarks"></a>Notes

Utilisez la propriété **LevelDepth** pour déterminer la distance de l'objet [Member](member-object-ado-md.md) par rapport au niveau racine de la hiérarchie. La valeur de la propriété **LevelDepth** d'un membre de niveau racine est 0. Cela correspond à la propriété [Depth](depth-property-ado-md.md) d'un objet [Level](level-object-ado-md.md).

