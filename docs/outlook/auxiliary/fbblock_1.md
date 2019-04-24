---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Définit un bloc de données de disponibilité. Il s'agit d'un élément d'un calendrier représenté par une demande de rendez-vous ou de réunion.
ms.openlocfilehash: 60d2ff50081a8950a397df6f2f6bbfd37d3bdb61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317667"
---
# <a name="fbblock1"></a>FBBlock_1

Définit un bloc de données de disponibilité. Il s'agit d'un élément d'un calendrier représenté par une demande de rendez-vous ou de réunion.
  
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
  
> Heure de début du bloc, exprimée en heure relative. Pour plus d'informations, consultez la rubrique [utilisation de l'heure relative pour accéder aux données de](how-to-use-relative-time-to-access-free-busy-data.md)disponibilité.
    
_m_tmEnd_
  
> Heure de fin du bloc, exprimée en heure relative.
    
_m_fbStatus_
  
> État de disponibilité de ce bloc, indiquant si l'utilisateur est absent (e) du bureau, occupé, provisoire ou libre, pendant la période comprise entre _m_tmStart_ et _m_tmEnd_.
    
## <a name="see-also"></a>Voir aussi

- [FBStatus](fbstatus.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)
- [Utiliser l’heure relative pour accéder aux données de disponibilité](how-to-use-relative-time-to-access-free-busy-data.md)

