---
title: Prise en charge du texte formaté dans les responsabilités du client des messages sortants
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
ms.openlocfilehash: cc29c2f9ad7a2e249c1fb7f19b3cb803da7b3f9d
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63377693"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a>Prise en charge du texte formaté dans les messages sortants : responsabilités du client

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes définissent la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou la propriété **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) pour un message sortant. Les clients qui ne supportent que le texte simple définissent uniquement **PR_BODY** propriété. Les clients au format RTF (Rich Text Format) peuvent définir  des propriétés PR_BODY et **PR_RTF_COMPRESSED**, ou uniquement des **PR_RTF_COMPRESSED, selon** le fournisseur de magasin de messages utilisé. Les clients html définissent la **propriété PR_HTML** . 
  
Il est important pour un client de vérifier la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de sa boutique de messages pour déterminer si la boutique prend en charge rtf. Si la magasin de messages n’est pas sensible au rtf, un client rtf définit les  propriétés PR_BODY et **PR_RTF_COMPRESSED** pour chaque message sortant. 
  
Si la magasin de messages est sensible au rtf, seule la **propriété PR_RTF_COMPRESSED** doit être définie. 
  
 **Pour définir PR_RTF_COMPRESSED et vous assurer que le processus de synchronisation se produit si nécessaire, les clients rtF**
  
1. Appelez la [méthode IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_RTF_COMPRESSED** , en MAPI_CREATE et MAPI_MODIFY indicateurs. MAPI_CREATE s’assure que toutes les nouvelles données remplacent les anciennes données et MAPI_MODIFY vous permet d’effectuer ces remplacements. 
    
2. Appelez la fonction [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , en passant STORE_UNCOMPRESSED_RTF si la boutique de messages définit le bit STORE_UNCOMPRESSED_RTF dans sa propriété **PR_STORE_SUPPORT_MASK** , pour obtenir une version non compressée du flux **PR_RTF_COMPRESSED** renvoyée par **OpenProperty**.
    
3. Écrivez les données de texte du message dans le flux non compressé renvoyé par **WrapCompressedRTFStream**.
    
4. Valider et libérer les flux non compressés et non compressés.
    
À ce stade, si le fournisseur de magasin de messages prend en charge rtf, vous avez effectué tout ce qui est nécessaire. Vous pouvez dépendre du fournisseur de la boutique de messages pour gérer le processus de synchronisation et la création de la propriété **PR_BODY** , si nécessaire. Toutefois, si le fournisseur de magasin de messages ne prend pas en charge rtf, vous devez appeler la [fonction RTFSync](rtfsync.md) pour synchroniser le texte avec la mise en forme, en RTF_SYNC_RTF_CHANGED indicateur. 
  

