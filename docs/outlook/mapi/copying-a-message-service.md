---
title: Copie d'un service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a4db4ed1c3098226891edca054621fe145daaa1f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425392"
---
# <a name="copying-a-message-service"></a>Copie d'un service de messagerie

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour copier un service de messagerie vers un profil**
  
- Appelez [IMsgServiceAdmin:: CopyMsgService](imsgserviceadmin-copymsgservice.md).
    
Lors de la copie d'un service de messagerie, la nouvelle instance du service est configurée exactement de la même façon que l'original. Parfois **CopyMsgService** renvoie l'erreur MAPI_E_ACCESS_DENIED. La cause la plus fréquente de cette erreur renvoyée est un service de messagerie qui ne peut pas être dupliqué. 
  

