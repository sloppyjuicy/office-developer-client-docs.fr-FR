---
title: Création de texte du message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 38be3bc2df8931ca45da12e43436377545e8a977
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783134"
---
# <a name="creating-message-text"></a>Création de texte du message

**S’applique à**: Outlook 
  
Bien que certains messages sont composés de rien de plus qu’une liste de destinataires et une ligne d’objet, le contenu de la plupart des messages, spécifiquement IPM. Remarque Les messages, contient du texte. Message texte peut être brut ou mise en forme et est stockée dans trois propriétés : **PR\_corps** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) et **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Si votre client est basé sur le texte brut, définissez **PR\_BODY**. Si vous prenez en charge texte mis en forme dans le Format de texte enrichi (RTF), définir **PR_RTF_COMPRESSED** ou les deux **PR_RTF_COMPRESSED** et **PR\_corps**, selon le fournisseur de banque de messages que vous utilisez. Lorsqu’un client prenant en charge les RTF utilise une banque de messages RTF prenant en charge, il définit **PR_RTF_COMPRESSED** uniquement. Lorsqu’un client prenant en charge les RTF utilise une banque de messages non compatible RICH, il définit les deux propriétés. Si votre client prend en charge HTML, définissez la propriété **PR_HTML** . 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a>Déterminer si la banque de messages prend en charge le Format RTF
  
1. Appeler la méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) de la banque de messages pour récupérer la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).
    
2. Recherchez le bit STORE_RTF_OK. Si STORE_RTF_OK est défini, le fournisseur de banque de message prend en charge le texte RTF. Si elle n’est pas définie, le fournisseur de banque de message prend en charge uniquement en texte brut.
    
## <a name="determine-whether-your-message-store-supports-html"></a>Déterminer si la banque de messages prend en charge HTML
  
1. Appeler la méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) de la banque de messages pour récupérer la propriété **PR_STORE_SUPPORT_MASK** . 
    
2. Recherchez le bit STORE_HTML_OK. Si STORE_HTML_OK est défini, le fournisseur de banque de message prend en charge le texte HTML. 
    
## <a name="set-prrtfcompressed"></a>Définir PR\_RTF_COMPRESSED
  
1. Appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du message pour ouvrir la propriété **PR_RTF_COMPRESSED** , spécifiant IID_IStream comme l’identificateur d’interface et la définition de l’indicateur MAPI_CREATE. 
    
2. Appelez la fonction [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , en passant l’indicateur STORE_UNCOMPRESSED_RTF si le bit STORE_UNCOMPRESSED_RTF est défini dans la propriété **PR_STORE_SUPPORT_MASK** du message. 
    
3. Publier le flux d’origine en appelant son ** IUnknown::Release ** méthode. 
    
4. Appeler ** IStream::Write ** ou **IStream::CopyTo** pour écrire le texte du message dans le flux renvoyé par **WrapCompressedRTFStream**.
    
5. Appeler les méthodes de **validation** et de **version** sur le flux retourné par la méthode **OpenProperty** . 
    
À ce stade, si le fournisseur de banque de message prend en charge le format RTF, vous avez réalisé tout ce qui est requis. Vous pouvez compter sur le fournisseur de banque de messages pour gérer la synchronisation du contenu du message et la mise en forme et créer la **PR\_corps** propriété si nécessaire. Banques de messages RTF prenant en charge appellent [RTFSync](rtfsync.md) pour gérer la synchronisation. Si le format RTF\_SYNC_BODY_CHANGED est défini sur TRUE, le fournisseur sera régénérer la propriété **PR_BODY** . 
  
Si votre fournisseur de magasin de message ne gère pas le format RTF, vous devez également ajouter le contenu des messages non RTF en définissant la propriété **PR_BODY** . 
  
## <a name="set-prhtml"></a>Set PR_HTML
  
1. Appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_HTML** avec l’interface **IStream** . 
    
2. Appelez **IStream::Write** pour écrire les données de texte du message dans le flux renvoyé par **OpenProperty**. 
    
3. Appelez **IStream::Commit** et **IUnknown::Release** sur le flux pour valider les modifications et libérer la mémoire. 
    
## <a name="set-prbody"></a>Définir PR_BODY
  
1. Appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_BODY** avec l’interface **IStream** . 
    
2. Appelez **IStream::Write** pour écrire les données de texte du message dans le flux renvoyé par **OpenProperty**. 
    
3. Appelez la fonction [RTFSync](rtfsync.md) pour synchroniser le texte avec la mise en forme. Car il s’agit d’un nouveau message, définir des indicateurs de la RTF_SYNC_RTF_CHANGED et RTF_SYNC_BODY_CHANGED pour indiquer que le texte brut et RTF version du texte du message a été modifié. **RTFSync** sera définir plusieurs propriétés liées par le fournisseur de banque de messages, tel que **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) et les enregistrer dans le message.
    
4. Appelez **IStream::Commit** et **IUnknown::Release** sur le flux pour valider les modifications et libérer la mémoire. 
    

