---
title: Copie d’un service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8388d14446a230b032e49ad0d614c85e79b8ece8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573718"
---
# <a name="copying-a-message-service"></a>Copie d’un service de messagerie

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
 **Pour copier un service de message à un profil**
  
- Appelez [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).
    
Lorsqu’un service de message est copié, la nouvelle instance du service est configurée de la même façon que l’original. Parfois **CopyMsgService** renvoie l’erreur MAPI_E_ACCESS_DENIED. La cause la plus courante de retour de cette erreur est un service de message qui n’autorise pas lui-même à dupliquer. 
  

