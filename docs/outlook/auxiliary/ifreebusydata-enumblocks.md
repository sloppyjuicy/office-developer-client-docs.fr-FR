---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Obtient une interface qui énumère les blocs de données de disponibilité d'un utilisateur dans une plage de temps spécifiée.
ms.openlocfilehash: 51a77b2f47166628db07259ef841e0d6173ee370
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317555"
---
# <a name="ifreebusydataenumblocks"></a>IFreeBusyData::EnumBlocks

Obtient une interface qui énumère les blocs de données de disponibilité d'un utilisateur dans une plage de temps spécifiée.
  
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
  
> remarquer Interface permettant d'énumérer les blocs de disponibilité.
    
_ftmStart_
  
> dans Heure de début de l'énumération. Elle est exprimée dans [fileTime](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).
    
_ftmEnd_
  
> dans Heure de fin de l'énumération. Elle est exprimée dans **fileTime**. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Remarques

Cette méthode est utilisée pour indiquer la plage horaire des éléments de calendrier pour lesquels récupérer les détails. Les valeurs de *ftmStart* et *ftmEnd* sont mises en cache et renvoyées lors d'un appel ultérieur de [IFreeBusyData:: GetFBPublishRange](ifreebusydata-getfbpublishrange.md).
  
Un fournisseur de disponibilité peut également utiliser l'interface [IEnumFBBlock](ienumfbblock.md) renvoyée pour accéder à l'énumération. 
  
## <a name="see-also"></a>Voir aussi

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)
- [Utiliser l’heure relative pour accéder aux données de disponibilité](how-to-use-relative-time-to-access-free-busy-data.md)

