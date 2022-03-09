---
title: FollowUpStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c3d0f6c4-4597-784f-8d44-6e5d905895b4
ms.openlocfilehash: b7de7699d2f95968d55dabf35d6257076fe38e84
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63378694"
---
# <a name="followupstatus"></a>FollowUpStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
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
  
> Nombre d’états différents pris en charge pour le suivi.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagFlagStatus](pidtagflagstatus-canonical-property.md)

