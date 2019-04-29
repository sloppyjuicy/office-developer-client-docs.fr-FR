---
title: Prise en charge du texte mis en forme dans les messages sortants responsabilités du client
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 01d5ae3fd06d570e15336fad9538f01e586cd0f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431602"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a>Prise en charge du texte mis en forme dans les messages sortants: responsabilités du client

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes définissent la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou la propriété **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) pour un message sortant. Les clients qui prennent en charge uniquement le texte brut ne définissent que la propriété **PR_BODY** . Les clients gérant le format RTF (Rich Text Format) peuvent définir les propriétés **PR_BODY** et **PR_RTF_COMPRESSED** , ou seulement **PR_RTF_COMPRESSED**, selon le fournisseur de banque de messages utilisé. Les clients compatibles HTML définissent la propriété **PR_HTML** . 
  
Il est important pour un client de vérifier la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de sa banque de messages pour déterminer si le magasin prend en charge le format RTF. Si la Banque de messages n'est pas compatible avec le format RTF, un client compatible avec le format RTF définit les propriétés **PR_BODY** et **PR_RTF_COMPRESSED** pour chaque message sortant. 
  
Si la base de messages est compatible avec le format RTF, seule la propriété **PR_RTF_COMPRESSED** doit être définie. 
  
 **Pour définir PR_RTF_COMPRESSED et vous assurer que le processus de synchronisation a lieu si nécessaire, les clients compatibles avec le format RTF**
  
1. Appelez la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_RTF_COMPRESSED** , en définissant les indicateurs MAPI_CREATE et MAPI_MODIFY. MAPI_CREATE garantit que toutes les nouvelles données remplacent les anciennes données et MAPI_MODIFY vous permet d'effectuer ces remplacements. 
    
2. Appelez la fonction [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , en passant STORE_UNCOMPRESSED_RTF si la Banque de messages définit le bit STORE_UNCOMPRESSED_RTF dans sa propriété **PR_STORE_SUPPORT_MASK** , pour obtenir une version non compressée du **PR_RTF_COMPRESSED **flux renvoyé à partir de **OpenProperty**.
    
3. Écrire les données de texte du message dans le flux non compressé renvoyé depuis **WrapCompressedRTFStream**.
    
4. Valider et libérer les flux non compressés et compressés.
    
À ce stade, si le fournisseur de banque de messages prend en charge le format RTF, vous avez réalisé tout ce qui est nécessaire. Vous pouvez dépendre du fournisseur de banque de messages pour gérer le processus de synchronisation et de la création de la propriété **PR_BODY** , si nécessaire. Toutefois, si le fournisseur de banque de messages ne prend pas en charge le format RTF, vous devez appeler la fonction [RTFSync](rtfsync.md) pour synchroniser le texte avec la mise en forme, en définissant l'indicateur RTF_SYNC_RTF_CHANGED. 
  

