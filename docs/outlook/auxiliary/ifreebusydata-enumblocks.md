---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Obtient une interface qui éumène les blocs de données de la période spécifiée pour un utilisateur.
ms.openlocfilehash: d33d4718707b44c481e5e54be47e4dad6b3b6bfa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572220"
---
# <a name="ifreebusydataenumblocks"></a>IFreeBusyData::EnumBlocks

Obtient une interface qui éumène les blocs de données de la période spécifiée pour un utilisateur.
  
## <a name="quick-info"></a>Informations rapides

Voir [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a>Paramètres

_ppenumfb_
  
> [out] Interface qui permet d’éumer les blocs de libre/occupé.
    
_ftmStart_
  
> [in] Heure de début de l’éumération. Il est exprimé en [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).
    
_ftmEnd_
  
> [in] Heure de fin de l’éumération. Il est exprimé en **FILETIME**. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Remarques

Cette méthode permet d’indiquer l’plage de temps des éléments de calendrier pour lesquels récupérer des détails. Les valeurs  *de ftmStart* et *ftmEnd* sont mises en cache et renvoyées dans un appel ultérieur de [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).
  
Un fournisseur de libre/occupé peut également utiliser par la suite l’interface [IEnumFBBlock](ienumfbblock.md) renvoyée pour accéder à l’éumération. 
  
## <a name="see-also"></a>Voir aussi

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)
- [Utiliser l’heure relative pour accéder aux données de disponibilité](how-to-use-relative-time-to-access-free-busy-data.md)

