---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Définit la plage de temps pour une énumération de blocs de données de disponibilité pour un utilisateur.
ms.openlocfilehash: 4647453acb0e530521aa808f7f017e3e311644bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317478"
---
# <a name="ifreebusydatasetfbrange"></a>IFreeBusyData::SetFBRange

Définit la plage de temps pour une énumération de blocs de données de disponibilité pour un utilisateur.
  
## <a name="quick-info"></a>Informations rapides

Voir [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a>Paramètres

_rtmStart_
  
> dans Une valeur de temps relative pour le début des informations de disponibilité. Cette valeur correspond au nombre de minutes écoulées depuis le 1er janvier 1601.
    
_rtmEnd_
  
> dans Valeur d'heure relative pour la fin des informations de disponibilité. Cette valeur correspond au nombre de minutes écoulées depuis le 1er janvier 1601.
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Remarques

Cette méthode est utilisée pour indiquer la plage horaire des éléments de calendrier pour lesquels récupérer les détails. Les valeurs de *ftmStart* et *ftmEnd* sont mises en cache et renvoyées lors d'un appel ultérieur de [IFreeBusyData:: GetFBPublishRange](ifreebusydata-getfbpublishrange.md).
  
## <a name="see-also"></a>Voir aussi

- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [Utiliser l’heure relative pour accéder aux données de disponibilité](how-to-use-relative-time-to-access-free-busy-data.md)

