---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Obtient une interface qui énumère les informations de disponibilité des blocs de données pour un utilisateur au sein d’une plage de temps spécifié.
ms.openlocfilehash: 51a77b2f47166628db07259ef841e0d6173ee370
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394537"
---
# <a name="ifreebusydataenumblocks"></a>IFreeBusyData::EnumBlocks

Obtient une interface qui énumère les informations de disponibilité des blocs de données pour un utilisateur au sein d’une plage de temps spécifié.
  
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
  
> [out] Une interface pour énumérer les blocs de disponibilité.
    
_ftmStart_
  
> [in] Heure de début de l’énumération. Il est exprimé en [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).
    
_ftmEnd_
  
> [in] Heure de fin de l’énumération. Il est exprimé en **FILETIME**. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Note

Cette méthode est utilisée pour indiquer la plage de temps des éléments de calendrier pour lequel récupérer les détails. Les valeurs de *ftmStart* et *ftmEnd* sont mis en cache et retournés dans un autre appel de [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).
  
Un fournisseur et de disponibilité peut également ensuite utiliser l’interface [IEnumFBBlock](ienumfbblock.md) retournée pour accéder l’énumération. 
  
## <a name="see-also"></a>Voir aussi

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)
- [Utiliser l’heure relative pour accéder aux données de disponibilité](how-to-use-relative-time-to-access-free-busy-data.md)

