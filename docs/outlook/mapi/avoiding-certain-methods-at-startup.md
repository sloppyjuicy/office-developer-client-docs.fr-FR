---
title: Éviter certaines méthodes au démarrage
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: 'Dernière modification : 07 décembre 2015'
ms.openlocfilehash: 345633700d921f617f65e0b5fefeba05deba7c72
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605138"
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
  

