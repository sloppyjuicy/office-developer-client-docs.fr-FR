---
title: FollowUpStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c3d0f6c4-4597-784f-8d44-6e5d905895b4
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 2280ae9271ca73af33f395bf9e41a9ee8fa62f96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327523"
---
# <a name="followupstatus"></a>FollowUpStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie les différents statuts de suivi d'un message.
  
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
  
> Aucun suivi n'a été spécifié.
    
 _flwupComplete_
  
> Le message est terminé.
    
 _flwupMarked_
  
> Le message est marqué pour le suivi.
    
 _flwupMAX_
  
> Nombre d'États différents pris en charge pour le suivi.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagFlagStatus](pidtagflagstatus-canonical-property.md)

