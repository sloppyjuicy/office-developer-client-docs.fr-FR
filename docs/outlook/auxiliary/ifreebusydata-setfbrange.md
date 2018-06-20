---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Définit l’intervalle de temps pour une énumération des blocs de données de disponibilité d’un utilisateur.
ms.openlocfilehash: 84a25a2dd43f594caa075d90e4f183086452184a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782601"
---
# <a name="ifreebusydatasetfbrange"></a>IFreeBusyData::SetFBRange

Définit l’intervalle de temps pour une énumération des blocs de données de disponibilité d’un utilisateur.
  
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
  
> [in] Une valeur d’heure relative du début de la disponibilité des informations. Cette valeur est le nombre de minutes depuis le 1er janvier 1601.
    
_rtmEnd_
  
> [in] Une valeur d’heure relative à la fin des informations de disponibilité. Cette valeur est le nombre de minutes depuis le 1er janvier 1601.
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Note

Cette méthode est utilisée pour indiquer la plage de temps des éléments de calendrier pour lequel récupérer les détails. Les valeurs de *ftmStart* et *ftmEnd* sont mis en cache et retournés dans un autre appel de [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).
  
## <a name="see-also"></a>Voir aussi

- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [Utiliser l’heure relative pour accéder aux données et de disponibilité](how-to-use-relative-time-to-access-free-busy-data.md)

