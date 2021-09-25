---
title: FollowUpStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c3d0f6c4-4597-784f-8d44-6e5d905895b4
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ad601ff547bfb89b98f0733b9e070b923ad92e1c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556734"
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

