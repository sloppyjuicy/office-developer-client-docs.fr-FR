---
title: FollowUpStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c3d0f6c4-4597-784f-8d44-6e5d905895b4
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e59c0ba7810741943883b9e86e84c6fe141f3050
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783330"
---
# <a name="followupstatus"></a>FollowUpStatus

  
  
**S’applique à**: Outlook 
  
Spécifie les différents statuts de suivi d’un message.
  
## <a name="quick-info"></a>Informations rapides

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a>Membres

 _flwupNone_
  
> Aucun suivi n’a été spécifié.
    
 _flwupComplete_
  
> Le message est terminé.
    
 _flwupMarked_
  
> Le message est marqué pour le suivi.
    
 _flwupMAX_
  
> Le nombre de différents statuts pris en charge pour le suivi.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagFlagStatus](pidtagflagstatus-canonical-property.md)

