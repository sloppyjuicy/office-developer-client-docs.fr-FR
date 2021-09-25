---
title: FBStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: f2d6a11e-847d-6bbe-cd77-e78ee961cb12
description: Une éumération pour l’état de libre/occupé des blocs de libre/occupé.
ms.openlocfilehash: 61ac90849e2a0d40b48281cb6f145fc5d997d545
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592801"
---
# <a name="fbstatus"></a>FBStatus

Une éumération pour l’état de libre/occupé des blocs de libre/occupé.
  
## <a name="quick-info"></a>Informations rapides

```cpp
enum  
    { 
      fbFree      = 0, 
      fbTentative = fbFree + 1, 
      fbBusy      = fbTentative + 1, 
      fbOutOfOffice = fbBusy + 1 
    }

```

## <a name="remarks"></a>Remarques

L’état de libre/occupé d’un bloc de temps détermine la façon dont il s’affiche dans un calendrier : **Libre,** **Occupé,** **Provisoire** ou **Hors** Office . 
  
## <a name="see-also"></a>Voir aussi

- [FBBlock_1](fbblock_1.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)

