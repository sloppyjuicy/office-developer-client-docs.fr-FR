---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Définit la plage de temps pour une éumération des blocs de données de la période de libre/occupé d’un utilisateur.
ms.openlocfilehash: 4647453acb0e530521aa808f7f017e3e311644bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421661"
---
# <a name="ifreebusydatasetfbrange"></a>IFreeBusyData::SetFBRange

Définit la plage de temps pour une éumération des blocs de données de la période de libre/occupé d’un utilisateur.
  
## <a name="quick-info"></a>Informations rapides

Voir [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a>Parameters

_rtmStart_
  
> [in] Valeur d’heure relative pour le début des informations de libre/occupé. Cette valeur est le nombre de minutes depuis le 1er janvier 1601.
    
_rtmEnd_
  
> [in] Valeur d’heure relative pour la fin des informations de libre/occupé. Cette valeur est le nombre de minutes depuis le 1er janvier 1601.
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Remarques

Cette méthode permet d’indiquer l’plage de temps des éléments de calendrier pour lesquels récupérer des détails. Les valeurs  *de ftmStart*  et  *ftmEnd*  sont mises en cache et renvoyées dans un appel ultérieur de [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).
  
## <a name="see-also"></a>Voir aussi

- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [Utiliser l’heure relative pour accéder aux données de disponibilité](how-to-use-relative-time-to-access-free-busy-data.md)

