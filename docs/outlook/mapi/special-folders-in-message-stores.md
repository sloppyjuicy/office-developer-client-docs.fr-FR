---
title: Dossiers sp�ciaux dans des magasins de Message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9462070e-1472-4e12-ba4e-e4ac60022892
ms.openlocfilehash: 27968188c366c0f4eb2b0dbb4eaf2b35369edfbf
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63368747"
---
# <a name="special-folders-in-message-stores"></a>Dossiers sp�ciaux dans des magasins de Message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Special folders such as the Inbox, Outbox, and search-results folder may be created in advance and protected by the message store provider. If the folders do not exist, MAPI will attempt to create them in the message store by calling the [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function. For more information, see [Dossiers sp�ciaux MAPI](mapi-special-folders.md).
  
## <a name="see-also"></a>Voir aussi



[Implémentation de dossiers dans des banques de messages](implementing-folders-in-message-stores.md)

