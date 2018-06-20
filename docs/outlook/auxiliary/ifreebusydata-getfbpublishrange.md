---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Obtient une énumération des informations de disponibilité des blocs de données pour un utilisateur une plage de temps prédéfini.
ms.openlocfilehash: 2a322a43da38a0b902789f4c83baaabd769154c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782583"
---
# <a name="ifreebusydatagetfbpublishrange"></a>IFreeBusyData::GetFBPublishRange

Obtient une énumération des informations de disponibilité des blocs de données pour un utilisateur une plage de temps prédéfini.
  
## <a name="quick-info"></a>Informations rapides

Voir [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a>Paramètres

_prtmStart_
  
> [out] Une valeur d’heure relative du début de la disponibilité des informations. Cette valeur est le nombre de minutes depuis le 1er janvier 1601.
    
_prtmEnd_
  
> [out] Une valeur d’heure relative à la fin des informations de disponibilité. Cette valeur est le nombre de minutes depuis le 1er janvier 1601.
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Note

Un fournisseur et de disponibilité appelle [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) ou [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) pour définir la période pour une énumération. Si [l’IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) ou [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) n’a pas été appelée, les valeurs par défaut pour **prtmStart** et **prtmEnd** doivent être définies entre le 1er avril 1601 00:00:00Z et le 31 août 4500 11:59:59Z respectivement. En outre, vous ne devez pas définir l’heure de début est supérieure à l’heure de fin. 
  
**IFreeBusyData::GetFBPublishRange** doit renvoyer que les valeurs mises en cache pour la période définie par l’appel le plus récent pour **IFreeBusyData::EnumBlocks** ou **IFreeBusyData::SetFBRange**. 
  
## <a name="see-also"></a>Voir aussi

- [Utiliser l’heure relative pour accéder aux données et de disponibilité](how-to-use-relative-time-to-access-free-busy-data.md)
- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)

