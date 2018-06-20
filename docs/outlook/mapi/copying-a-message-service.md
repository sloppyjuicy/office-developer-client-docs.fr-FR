---
title: Copie d’un Service de Message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 7d1296ba74bbafcd26a8878dfb1eb2f359ab3e03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783054"
---
# <a name="copying-a-message-service"></a>Copie d’un Service de Message

  
  
**S’applique à**: Outlook 
  
 **Pour copier un service de message à un profil**
  
- Appelez [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).
    
Lorsqu’un service de message est copié, la nouvelle instance du service est configurée de la même façon que l’original. Parfois **CopyMsgService** renvoie l’erreur MAPI_E_ACCESS_DENIED. La cause la plus courante de retour de cette erreur est un service de message qui n’autorise pas lui-même à dupliquer. 
  

