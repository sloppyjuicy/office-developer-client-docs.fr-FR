---
title: Recherche de l’icône d’un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
ms.openlocfilehash: 369693f4b9692685c3eeed445ef0da06a7f7b73d
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63377553"
---
# <a name="finding-the-icon-for-a-message"></a>Recherche de l’icône d’un message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour rechercher l’icône associée à un message**
  
1. Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) du message pour récupérer sa propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).
    
2. Appelez [MAPIOpenFormMgr pour](mapiopenformmgr.md) récupérer un pointeur d’interface **IMAPIFormMgr** . Passez votre **pointeur IMAPISession** dans le _paramètre pSession_ . 
    
3. [Appelez IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) pour récupérer un pointeur d’interface **IMAPIFormInfo**. 
    
4. Utilisez le pointeur **IMAPIFormInfo** pour appeler [IMAPIProp::GetProps](imapiprop-getprops.md) et récupérer les propriétés **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) et/ou **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). 
    

