---
title: Éviter de certaines méthodes au démarrage
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: db327fdd239684140e4feeeb2a6045a2fcd5c410
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782987"
---
# <a name="avoiding-certain-methods-at-startup"></a>Éviter de certaines méthodes au démarrage

 
  
**S’applique à**: Outlook 
  
Pour améliorer les performances lors du démarrage, évitez les appels suivants :
  
- [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md)
    
- [IMAPISession::GetStatusTable](imapisession-getstatustable.md)
    
- [IMAPISession::Logoff](imapisession-logoff.md)
    
- [IMAPISession::QueryIdentity](imapisession-queryidentity.md)
    
- [IMAPIStatus::ValidateState](imapistatus-validatestate.md)
    
L’appel vers **IMAPIStatus::ValidateState** affecte les performances que s’il fait sur le spouleur MAPI ou le sous-système MAPI. Que ces méthodes ralentissent le traitement de démarrage est, car ils ne peuvent pas effectuer jusqu'à ce que le spouleur MAPI a terminé ses tâches de démarrage. 
  
Vous devez également éviter de recherche dans la banque de messages au démarrage. Appelez votre [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) de traitement de démarrage est terminée. 
  

