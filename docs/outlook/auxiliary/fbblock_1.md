---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Définit un bloc de données de libre/occupé. Il s’agit d’un élément d’un calendrier représenté par un rendez-vous ou une demande de réunion.
ms.openlocfilehash: 37dced409b4d9e194b4f20a3040588f6aecdc88b
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369727"
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
  
> Heure de début du bloc, exprimée en heure relative. Pour plus d’informations, voir [Utiliser l’heure relative pour accéder aux données de libre/occupé](how-to-use-relative-time-to-access-free-busy-data.md).

_m_tmEnd_
  
> Heure de fin du bloc, exprimée en temps relatif.

_m_fbStatus_
  
> L’état de la période de libre-service pour ce bloc, indiquant si l’utilisateur est en dehors du bureau, occupé, provisoire ou libre, pendant la période entre _m_tmStart_ et _m_tmEnd_.

## <a name="see-also"></a>Voir aussi

- [FBStatus](fbstatus.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)
- [Utiliser l’heure relative pour accéder aux données de disponibilité](how-to-use-relative-time-to-access-free-busy-data.md)
