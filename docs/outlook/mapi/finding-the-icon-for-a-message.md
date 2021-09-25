---
title: Recherche de l’icône d’un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2016332f5347aeda46d65b03e87cc69f9f359867
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614198"
---
# <a name="finding-the-icon-for-a-message"></a>Recherche de l’icône d’un message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour rechercher l’icône associée à un message**
  
1. Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) du message pour récupérer sa propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).
    
2. Appelez [MAPIOpenFormMgr pour](mapiopenformmgr.md) récupérer un pointeur d’interface **IMAPIFormMgr.** Passez votre **pointeur IMAPISession** dans le _paramètre pSession._ 
    
3. Appelez [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) pour récupérer un pointeur d’interface **IMAPIFormInfo.** 
    
4. Utilisez le pointeur **IMAPIFormInfo** pour appeler [IMAPIProp::GetProps](imapiprop-getprops.md) et récupérer les propriétés **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) et/ou **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). 
    

