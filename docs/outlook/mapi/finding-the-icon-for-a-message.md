---
title: Recherche de l’icône d’un Message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: b73545585d3279bc290524c7ccb26c14c2977fe4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783295"
---
# <a name="finding-the-icon-for-a-message"></a>Recherche de l’icône d’un Message

  
  
**S’applique à**: Outlook 
  
 **Pour rechercher l’icône associée à un message**
  
1. Appeler la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) du message pour récupérer la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).
    
2. Appelez [MAPIOpenFormMgr](mapiopenformmgr.md) pour récupérer un pointeur d’interface **IMAPIFormMgr** . Passez le pointeur **IMAPISession** dans le paramètre _pSession_ . 
    
3. Appelez [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) pour récupérer un pointeur d’interface **IMAPIFormInfo** . 
    
4. Utiliser le pointeur **IMAPIFormInfo** pour appeler [IMAPIProp::GetProps](imapiprop-getprops.md) et de récupérer les propriétés **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) et/ou de **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)). 
    

