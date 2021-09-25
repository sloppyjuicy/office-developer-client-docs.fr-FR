---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Définit un bloc de données de libre/occupé. Il s’agit d’un élément d’un calendrier représenté par un rendez-vous ou une demande de réunion.
ms.openlocfilehash: 5cf556e4df99801a56857d55c43b008f4071f714
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557322"
---
# <a name="fbblock_1"></a>FBBlock_1

Définit un bloc de données de libre/occupé. Il s’agit d’un élément d’un calendrier représenté par un rendez-vous ou une demande de réunion.
  
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
  
> Heure de début du bloc, exprimée en heure relative. Pour plus d’informations, voir [Utiliser l’heure relative pour accéder aux données de libre/occupé.](how-to-use-relative-time-to-access-free-busy-data.md)
    
_m_tmEnd_
  
> Heure de fin du bloc, exprimée en temps relatif.
    
_m_fbStatus_
  
> L’état de la période de libre-service pour ce bloc, indiquant si l’utilisateur est en dehors du bureau, occupé, provisoire ou gratuit, pendant la période entre  _m_tmStart_ et  _m_tmEnd_.
    
## <a name="see-also"></a>Voir aussi

- [FBStatus](fbstatus.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)
- [Utiliser l’heure relative pour accéder aux données de disponibilité](how-to-use-relative-time-to-access-free-busy-data.md)

