---
title: Éviter certaines méthodes au démarrage
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: 'Dernière modification : 07 décembre 2015'
ms.openlocfilehash: 5d26583ad7ad3b4a200daf321a8994e302b75a79
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580634"
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
  

