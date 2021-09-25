---
title: Copie d’un service de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2f3f3d505d720fb00fabcad40761e573ecd47a45
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617068"
---
# <a name="copying-a-message-service"></a>Copie d’un service de message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour copier un service de message dans un profil**
  
- Appelez [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).
    
Lorsqu’un service de message est copié, la nouvelle instance du service est configurée exactement de la même manière que l’original. Parfois, **CopyMsgService renvoie** l’erreur MAPI_E_ACCESS_DENIED. La cause la plus courante de ce retour d’erreur est un service de message qui ne se permet pas d’être dupliqué. 
  

