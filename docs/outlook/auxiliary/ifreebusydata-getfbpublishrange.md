---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Obtient une plage de temps prédéfinie pour une énumération de blocs de données de disponibilité pour un utilisateur.
ms.openlocfilehash: 26951ea6a885f8d0e5e6a2fb5bcf9a63069c7f44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317527"
---
# <a name="ifreebusydatagetfbpublishrange"></a>IFreeBusyData::GetFBPublishRange

Obtient une plage de temps prédéfinie pour une énumération de blocs de données de disponibilité pour un utilisateur.
  
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
  
> remarquer Une valeur de temps relative pour le début des informations de disponibilité. Cette valeur correspond au nombre de minutes écoulées depuis le 1er janvier 1601.
    
_prtmEnd_
  
> remarquer Valeur d'heure relative pour la fin des informations de disponibilité. Cette valeur correspond au nombre de minutes écoulées depuis le 1er janvier 1601.
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Remarques

Un fournisseur de disponibilité appelle [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md) ou [IFreeBusyData:: SetFBRange](ifreebusydata-setfbrange.md) pour définir la plage horaire pour une énumération. Si [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md) ou [IFreeBusyData:: SetFBRange](ifreebusydata-setfbrange.md) n'a pas été appelé, les valeurs par défaut pour **prtmStart** et **PrtmEnd** doivent être définies entre le 1er avril 1601 00:00:00Z et le 31 août 4500 11:59:59Z légumes. En outre, vous ne devez pas définir l'heure de début sur une valeur supérieure à l'heure de fin. 
  
**IFreeBusyData:: GetFBPublishRange** doit renvoyer les valeurs mises en cache pour la plage horaire définie par l'appel le plus récent pour **IFreeBusyData:: EnumBlocks** ou **IFreeBusyData:: SetFBRange**. 
  
## <a name="see-also"></a>Voir aussi

- [Utiliser l’heure relative pour accéder aux données de disponibilité](how-to-use-relative-time-to-access-free-busy-data.md)
- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)

