---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Obtient une plage de temps prédéfinie pour une éumération des blocs de données de libre/occupé d’un utilisateur.
ms.openlocfilehash: 26951ea6a885f8d0e5e6a2fb5bcf9a63069c7f44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430076"
---
# <a name="ifreebusydatagetfbpublishrange"></a>IFreeBusyData::GetFBPublishRange

Obtient une plage de temps prédéfinie pour une éumération des blocs de données de libre/occupé d’un utilisateur.
  
## <a name="quick-info"></a>Informations rapides

Voir [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a>Parameters

_prtmStart_
  
> [out] Valeur d’heure relative pour le début des informations de libre/occupé. Cette valeur est le nombre de minutes depuis le 1er janvier 1601.
    
_prtmEnd_
  
> [out] Valeur d’heure relative pour la fin des informations de libre/occupé. Cette valeur est le nombre de minutes depuis le 1er janvier 1601.
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Remarques

Un fournisseur de libre/occupé appelle [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) ou [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) pour définir la plage de temps d’une éumération. Si [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) ou [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) n’a pas été appelé, les valeurs par défaut pour **prtmStart** et **prtmEnd** doivent être définies respectivement entre le 1er avril 1601 00:00:00Z et le 31 août 4500 11:59:59Z. En outre, vous ne devez pas définir l’heure de début pour qu’elle soit supérieure à l’heure de fin. 
  
**IFreeBusyData::GetFBPublishRange** must return the cached values for the time range set by the most recent call for **IFreeBusyData::EnumBlocks** or **IFreeBusyData::SetFBRange**. 
  
## <a name="see-also"></a>Voir aussi

- [Utiliser l’heure relative pour accéder aux données de disponibilité](how-to-use-relative-time-to-access-free-busy-data.md)
- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)

