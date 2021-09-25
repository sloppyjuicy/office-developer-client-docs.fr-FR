---
title: Création d’un texte de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 20f9201c3aab95735bf2c11a2951dd3052e61b66
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551722"
---
# <a name="creating-message-text"></a>Création d’un texte de message

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Bien que certains messages soient composés d’une liste de destinataires et d’une ligne d’objet, le contenu de la plupart des messages, en particulier IPM. Note messages, includes text. Le texte du message peut être brut ou mis en forme et est stocké dans trois propriétés : **PR \_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR \_ HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) et **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Si votre client est en texte simple, définissez **PR \_ BODY**. Si vous prisez en charge le texte mis  en forme au format RTF (Rich Text Format), définissez PR_RTF_COMPRESSED uniquement ou les deux **PR_RTF_COMPRESSED** et **PR \_ BODY,** en fonction du fournisseur de magasin de messages que vous utilisez. Lorsqu’un client rtF utilise une magasine de messages rtF, il définit **PR_RTF_COMPRESSED** uniquement. Lorsqu’un client rtF utilise un magasin de messages non RTF, il définit les deux propriétés. Si votre client prend en charge le code HTML, définissez **PR_HTML** propriété. 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a>Déterminer si votre magasin de messages prend en charge le format texte enrichi
  
1. Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de la boutique de messages pour récupérer la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask).](pidtagstoresupportmask-canonical-property.md)
    
2. Recherchez le STORE_RTF_OK bit. Si STORE_RTF_OK est définie, le fournisseur de magasins de messages prend en charge le texte RTF. S’il n’est pas définie, le fournisseur de magasin de messages prend en charge le texte simple uniquement.
    
## <a name="determine-whether-your-message-store-supports-html"></a>Déterminer si votre magasin de messages prend en charge le code HTML
  
1. Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de la boutique de messages pour récupérer **PR_STORE_SUPPORT_MASK** propriété. 
    
2. Recherchez le STORE_HTML_OK bit. Si STORE_HTML_OK est définie, le fournisseur de magasins de messages prend en charge le texte HTML. 
    
## <a name="set-pr_rtf_compressed"></a>Définir \_ les RTF_COMPRESSED
  
1. Appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du message pour ouvrir la propriété **PR_RTF_COMPRESSED,** en spécifiant IID_IStream comme identificateur d’interface et en MAPI_CREATE indicateur. 
    
2. Appelez la [fonction WrapCompressedRTFStream,](wrapcompressedrtfstream.md) en passant l’indicateur STORE_UNCOMPRESSED_RTF si le bit STORE_UNCOMPRESSED_RTF est définie dans la propriété PR_STORE_SUPPORT_MASK de **message.** 
    
3. Release the original stream by calling its ** IUnknown::Release ** method. 
    
4. Appelez ** IStream::Write ** ou **IStream::CopyTo** pour écrire le texte du message dans le flux renvoyé par **WrapCompressedRTFStream**.
    
5. Appelez **les méthodes Commit** et **Release** sur le flux renvoyé par la **méthode OpenProperty.** 
    
À ce stade, si le fournisseur de magasin de messages prend en charge rtf, vous avez effectué tout ce qui est nécessaire. Vous pouvez dépendre du fournisseur de la boutique de messages pour gérer la synchronisation du contenu et de la mise en forme des messages et créer la propriété **\_ PR BODY** si nécessaire. Les magasins de messages rtfs [appellent RTFSync](rtfsync.md) pour gérer la synchronisation. Si l’indicateur SYNC_BODY_CHANGED RTF est définie sur TRUE, le fournisseur \_ recompile **la propriété PR_BODY.** 
  
Si votre fournisseur de magasins de messages ne prend pas en charge le rtf, vous devez également ajouter du contenu de message non RTF en PR_BODY **propriété.** 
  
## <a name="set-pr_html"></a>Définir PR_HTML
  
1. Appelez [la méthode IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_HTML** avec **l’interface IStream.** 
    
2. Appelez **IStream::Write** pour écrire les données de texte du message dans le flux renvoyé par **OpenProperty**. 
    
3. Appelez **IStream::Commit** et **IUnknown::Release** sur le flux pour valider les modifications et libérer sa mémoire. 
    
## <a name="set-pr_body"></a>Définir PR_BODY
  
1. Appelez [la méthode IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_BODY** avec **l’interface IStream.** 
    
2. Appelez **IStream::Write** pour écrire les données de texte du message dans le flux renvoyé par **OpenProperty**. 
    
3. Appelez la [fonction RTFSync](rtfsync.md) pour synchroniser le texte avec la mise en forme. Comme il s’agit d’un nouveau message, définissez les indicateurs RTF_SYNC_RTF_CHANGED et RTF_SYNC_BODY_CHANGED pour indiquer que la version RTF et la version en texte simple du texte du message ont changé. **RTFSync** définira plusieurs propriétés connexes dont le fournisseur de magasins de messages a besoin, telles que **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), et les écrire dans le message.
    
4. Appelez **IStream::Commit** et **IUnknown::Release** sur le flux pour valider les modifications et libérer sa mémoire. 
    

