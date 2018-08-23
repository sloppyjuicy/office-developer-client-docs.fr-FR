---
title: Recherche d’une icône pour un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 512c686a9e5afeadacd8edccedba2c257df48f71
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567810"
---
# <a name="finding-the-icon-for-a-message"></a>Recherche d’une icône pour un message

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
 **Pour rechercher l’icône associée à un message**
  
1. Appeler la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) du message pour récupérer la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).
    
2. Appelez [MAPIOpenFormMgr](mapiopenformmgr.md) pour récupérer un pointeur d’interface **IMAPIFormMgr** . Passez le pointeur **IMAPISession** dans le paramètre _pSession_ . 
    
3. Appelez [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) pour récupérer un pointeur d’interface **IMAPIFormInfo** . 
    
4. Utiliser le pointeur **IMAPIFormInfo** pour appeler [IMAPIProp::GetProps](imapiprop-getprops.md) et de récupérer les propriétés **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) et/ou de **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)). 
    

