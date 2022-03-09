---
title: Copie d’un service de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
ms.openlocfilehash: 79c335354f303ca4976129ba6e270e67ff0f5370
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63381816"
---
# <a name="copying-a-message-service"></a>Copie d’un service de message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour copier un service de message dans un profil**
  
- [Appelez IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).
    
Lorsqu’un service de message est copié, la nouvelle instance du service est configurée exactement de la même manière que l’original. Parfois **, CopyMsgService renvoie** l’erreur MAPI_E_ACCESS_DENIED. La cause la plus courante de ce retour d’erreur est un service de message qui ne se permet pas d’être dupliqué. 
  

