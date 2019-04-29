---
title: Création d’un texte de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5b4a4107d6326a61f50a4023ebc2538f699224b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428003"
---
# <a name="creating-message-text"></a>Création d’un texte de message

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Bien que certains messages soient constitués de rien de plus qu'une liste de destinataires et d'une ligne d'objet, le contenu de la plupart des messages, en particulier IPM. Remarque les messages, y compris le texte. Le texte du message peut être brut ou mis en forme et stocké dans trois propriétés: **PR\_Body** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_html** ([PidTagHtml](pidtaghtml-canonical-property.md)) et **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Si votre client est en texte brut, définissez **PR\_Body**. Si vous prenez en charge le texte mis en forme au format RTF (Rich Text Format), définissez **PR_RTF_COMPRESSED** uniquement ou **PR_RTF_COMPRESSED** et **PR\_Body**, selon le fournisseur de banque de messages que vous utilisez. Lorsqu'un client compatible RTF utilise un magasin de messages compatible avec le format RTF, il définit **PR_RTF_COMPRESSED** uniquement. Lorsqu'un client compatible RTF utilise un magasin de messages non compatible RTF, il définit les deux propriétés. Si votre client prend en charge le format HTML, définissez la propriété **PR_HTML** . 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a>Déterminer si votre magasin de messages prend en charge le format RTF
  
1. Appelez la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de la Banque de messages pour extraire la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).
    
2. Vérifiez le bit STORE_RTF_OK. Si STORE_RTF_OK est défini, le fournisseur de banque de messages prend en charge le texte RTF. S'il n'est pas défini, le fournisseur de banque de messages prend en charge uniquement le texte brut.
    
## <a name="determine-whether-your-message-store-supports-html"></a>Déterminer si votre magasin de messages prend en charge le format HTML
  
1. Appelez la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de la Banque de messages pour extraire la propriété **PR_STORE_SUPPORT_MASK** . 
    
2. Vérifiez le bit STORE_HTML_OK. Si STORE_HTML_OK est défini, le fournisseur de banque de messages prend en charge le texte HTML. 
    
## <a name="set-prrtfcompressed"></a>Définir PR\_RTF_COMPRESSED
  
1. Appelez la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_RTF_COMPRESSED** , en spécifiant IID_IStream comme identificateur d'interface et en définissant l'indicateur MAPI_CREATE. 
    
2. Appelez la fonction [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , en transmettant l'indicateur STORE_UNCOMPRESSED_RTF si le bit STORE_UNCOMPRESSED_RTF est défini dans la propriété **PR_STORE_SUPPORT_MASK** de la Banque de messages. 
    
3. Libérez le flux d'origine en appelant sa méthode * * IUnknown:: Release * *. 
    
4. Appelez soit * * IStream:: Write * * ou **IStream:: CopyTo** pour écrire le texte du message dans le flux renvoyé à partir de **WrapCompressedRTFStream**.
    
5. Appelez les méthodes **Commit** et **Release** sur le flux renvoyé par la méthode **OpenProperty** . 
    
À ce stade, si le fournisseur de banque de messages prend en charge le format RTF, vous avez réalisé tout ce qui est nécessaire. Vous pouvez dépendre du fournisseur de banque de messages pour gérer la synchronisation du contenu et de la mise en forme du message et pour créer la propriété **PR\_Body** si nécessaire. Les banques de messages prenant en charge le format RTF appellent [RTFSync](rtfsync.md) pour gérer la synchronisation. Si l'indicateur\_SYNC_BODY_CHANGED RTF est défini sur true, le fournisseur recalcule la propriété **PR_BODY** . 
  
Si votre fournisseur de banque de messages ne prend pas en charge le format RTF, vous devez également ajouter du contenu de message non RTF en définissant la propriété **PR_BODY** . 
  
## <a name="set-prhtml"></a>Définir PR_HTML
  
1. Appelez la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_HTML** avec l'interface **IStream** . 
    
2. Appelez **IStream:: Write** pour écrire les données de texte du message dans le flux renvoyé à partir de **OpenProperty**. 
    
3. Appelez **IStream:: Commit** et **IUnknown:: Release** sur le flux pour valider les modifications et libérer sa mémoire. 
    
## <a name="set-prbody"></a>Définir PR_BODY
  
1. Appelez la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_BODY** avec l'interface **IStream** . 
    
2. Appelez **IStream:: Write** pour écrire les données de texte du message dans le flux renvoyé à partir de **OpenProperty**. 
    
3. Appelez la fonction [RTFSync](rtfsync.md) pour synchroniser le texte avec la mise en forme. Étant donné qu'il s'agit d'un nouveau message, définissez les indicateurs RTF_SYNC_RTF_CHANGED et RTF_SYNC_BODY_CHANGED pour indiquer que la version au format RTF et texte brut du texte du message a changé. **RTFSync** définit plusieurs propriétés connexes requises par le fournisseur de banque de messages, telles que **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), et les écrit dans le message.
    
4. Appelez **IStream:: Commit** et **IUnknown:: Release** sur le flux pour valider les modifications et libérer sa mémoire. 
    

