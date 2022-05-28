---
title: Éviter certaines méthodes au démarrage
description: Décrit comment améliorer les performances au démarrage dans Outlook en évitant certaines méthodes.
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
ms.openlocfilehash: d72015056fc2a1212058157098e8731fabcd7e30
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65771103"
---
# <a name="avoiding-certain-methods-at-startup"></a>Éviter certaines méthodes au démarrage

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour améliorer les performances au moment du démarrage, évitez d’effectuer les appels suivants :
  
- [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md)
    
- [IMAPISession::GetStatusTable](imapisession-getstatustable.md)
    
- [IMAPISession::Logoff](imapisession-logoff.md)
    
- [IMAPISession::QueryIdentity](imapisession-queryidentity.md)
    
- [IMAPIStatus::ValidateState](imapistatus-validatestate.md)
    
L’appel à **IMAPIStatus::ValidateState** a une incidence sur les performances uniquement lorsqu’il est effectué sur le spouleur MAPI ou le sous-système MAPI. Ces méthodes ralentissent le traitement du démarrage, car elles ne peuvent pas être effectuées tant que le spouleur MAPI n’a pas terminé ses tâches de démarrage. 
  
Vous devez également éviter d’effectuer une recherche dans la banque de messages lors du démarrage. Exécutez votre appel [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) une fois le traitement du démarrage terminé. 
  

