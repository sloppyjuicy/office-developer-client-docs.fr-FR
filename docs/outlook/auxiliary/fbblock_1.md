---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Définit un bloc de données et de disponibilité. Il s’agit d’un élément dans un calendrier représenté par une demande de réunion ou de rendez-vous.
ms.openlocfilehash: 93418e3777e9d9f0a016822ea5897b8fccc37ac3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782551"
---
# <a name="fbblock1"></a>FBBlock_1

Définit un bloc de données et de disponibilité. Il s’agit d’un élément dans un calendrier représenté par une demande de réunion ou de rendez-vous.
  
## <a name="quick-info"></a>Informations rapides

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a>Membres

_m_tmStart_
  
> L’heure de début pour le bloc, exprimée en heure relative. Pour plus d’informations, voir [heure relative utilisés pour accéder aux données et de disponibilité](how-to-use-relative-time-to-access-free-busy-data.md).
    
_m_tmEnd_
  
> L’heure de fin pour le bloc, exprimée en heure relative.
    
_m_fbStatus_
  
> L’état de disponibilité pour ce bloc, qui indique si l’utilisateur est absent du bureau, occupé (e), provisoire ou gratuite, au cours de la période de temps entre _m_tmStart_ et _m_tmEnd_.
    
## <a name="see-also"></a>Voir aussi

- [FBStatus](fbstatus.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)
- [Utiliser l’heure relative pour accéder aux données et de disponibilité](how-to-use-relative-time-to-access-free-busy-data.md)

