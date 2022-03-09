---
title: Création d’un texte de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
ms.openlocfilehash: 3913a0e85c93a5bc2e45dcef118c49f09c712328
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63402644"
---
# <a name="creating-message-text"></a>Création d’un texte de message

**S’applique à** : Outlook 2013 | Outlook 2016
  
Bien que certains messages soient composés d’une liste de destinataires et d’une ligne d’objet, le contenu de la plupart des messages, en particulier IPM. Note messages, includes text. Le texte du message peut être simple ou formaté et stocké dans trois propriétés : **PRBODY\_** ([PidTagBody](pidtagbody-canonical-property.md)), **PRHTML\_** ([PidTagHtml](pidtaghtml-canonical-property.md)) et **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).

Si votre client est en texte simple, définissez **PRBODY\_**. Si vous prisez en charge le texte mis en forme au format RTF (Rich  Text Format), définissez PR_RTF_COMPRESSED uniquement ou les deux **PR_RTF_COMPRESSED** et **PRBODY\_**, en fonction du fournisseur de magasin de messages que vous utilisez. Lorsqu’un client rtF utilise un magasin de messages rtF, il définit **PR_RTF_COMPRESSED** uniquement. Lorsqu’un client rtF utilise un magasin de messages non RTF, il définit les deux propriétés. Si votre client prend en charge le code HTML, définissez **PR_HTML** propriété.
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a>Déterminer si votre magasin de messages prend en charge le format texte enrichi
  
1. Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de la boutique de messages pour récupérer la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).

2. Recherchez le STORE_RTF_OK bit. Si STORE_RTF_OK est définie, le fournisseur de magasins de messages prend en charge le texte RTF. S’il n’est pas définie, le fournisseur de magasin de messages prend en charge le texte simple uniquement.

## <a name="determine-whether-your-message-store-supports-html"></a>Déterminer si votre magasin de messages prend en charge le code HTML
  
1. Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de la boutique de messages pour récupérer **PR_STORE_SUPPORT_MASK** propriété.

2. Recherchez le STORE_HTML_OK bit. Si STORE_HTML_OK est définie, le fournisseur de magasin de messages prend en charge le texte HTML.

## <a name="set-pr_rtf_compressed"></a>Définir pr\_ RTF_COMPRESSED
  
1. Appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du message pour ouvrir la propriété **PR_RTF_COMPRESSED** , en spécifiant IID_IStream comme identificateur d’interface et en MAPI_CREATE indicateur.

2. Appelez [la fonction WrapCompressedRTFStream](wrapcompressedrtfstream.md), en passant l’indicateur STORE_UNCOMPRESSED_RTF si le bit STORE_UNCOMPRESSED_RTF est définie dans la propriété PR_STORE_SUPPORT_MASK **de message.**

3. Libérer le flux d’origine en appelant **sa méthode IUnknown::Release** .

4. Appelez **IStream::Write** ou **IStream::CopyTo** pour écrire le texte du message dans le flux renvoyé par **WrapCompressedRTFStream**.

5. Appelez **les méthodes Commit** et **Release** sur le flux renvoyé par la **méthode OpenProperty** .

À ce stade, si le fournisseur de magasin de messages prend en charge rtf, vous avez effectué tout ce qui est nécessaire. Vous pouvez dépendre du fournisseur de magasin de messages pour gérer la synchronisation du contenu et de la mise en forme des messages et créer la **propriété PRBODY\_** si nécessaire. Les magasins de messages rtF [appellent RTFSync](rtfsync.md) pour gérer la synchronisation. Si l’indicateur RTF\_ SYNC_BODY_CHANGED est définie sur TRUE, le fournisseur recompile la **propriété PR_BODY** .
  
Si votre fournisseur de magasins de messages ne prend pas en charge rtf, vous devez également ajouter du contenu de message non RTF en **PR_BODY propriété.**
  
## <a name="set-pr_html"></a>Définir PR_HTML
  
1. Appelez [la méthode IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_HTML** avec l’interface **IStream** .

2. **Appelez IStream::Write** pour écrire les données de texte du message dans le flux renvoyé par **OpenProperty**.

3. **Appelez IStream::Commit** et **IUnknown::Release** sur le flux pour valider les modifications et libérer sa mémoire.

## <a name="set-pr_body"></a>Définir PR_BODY
  
1. Appelez [la méthode IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_BODY** avec l’interface **IStream** .

2. **Appelez IStream::Write** pour écrire les données de texte du message dans le flux renvoyé par **OpenProperty**.

3. Appelez la [fonction RTFSync](rtfsync.md) pour synchroniser le texte avec la mise en forme. Comme il s’agit d’un nouveau message, définissez les indicateurs RTF_SYNC_RTF_CHANGED et RTF_SYNC_BODY_CHANGED pour indiquer que la version RTF et la version en texte simple du texte du message ont changé. **RTFSync** définira plusieurs propriétés connexes dont le fournisseur de magasins de messages a besoin, telles que **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), et les écrirea dans le message.

4. **Appelez IStream::Commit** et **IUnknown::Release** sur le flux pour valider les modifications et libérer sa mémoire.
