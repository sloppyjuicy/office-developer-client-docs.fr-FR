---
title: Prise en charge de texte mis en forme dans les responsabilités du Client les Messages sortants
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: d5ce2e6b0f10ff6c2f6fd91ca9f73953f3ee7cd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787273"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a>Prise en charge au format texte dans les Messages sortants : responsabilités du Client

  
  
**S’applique à**: Outlook 
  
Applications clientes définir la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou la propriété **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) pour un message sortant. Les clients qui prennent en charge que le texte brut définir uniquement la propriété **PR_BODY** . Rich Text Format (RTF)-connaissance clients peuvent définir à la fois **PR_BODY** et propriétés **PR_RTF_COMPRESSED** , ou uniquement **PR_RTF_COMPRESSED**, selon le message Enregistrer fournisseur utilisé. Clients prenant en charge HTML définir la propriété **PR_HTML** . 
  
Il est important pour un client pour vérifier la propriété de **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de la banque de messages pour déterminer si la banque prend en charge au format RTF. Si la banque de messages n’est pas en charge au format RTF, un client prenant en charge les RTF définit les propriétés de la **PR_BODY** et **PR_RTF_COMPRESSED** pour chaque message sortant. 
  
Si la banque de messages est prenant en charge au format RTF, seule la propriété **PR_RTF_COMPRESSED** doit être définie. 
  
 **Pour définir les PR_RTF_COMPRESSED et vérifiez que la synchronisation processus se produit en tant que nécessaires, RTF prenant en charge des clients**
  
1. Appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_RTF_COMPRESSED** , définition des indicateurs n’et MAPI_CREATE. MAPI_CREATE garantit que toutes les nouvelles données remplacent les anciennes données et ne permet de rendre les remplacements. 
    
2. Appelez la fonction [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , en transmettant STORE_UNCOMPRESSED_RTF si la banque de messages définit le bit STORE_UNCOMPRESSED_RTF dans sa propriété **PR_STORE_SUPPORT_MASK** , pour obtenir une version non compressée de le **PR_RTF_COMPRESSED **flux renvoyé par **OpenProperty**.
    
3. Écrire les données de texte du message dans le flux non compressé renvoyé à partir de **WrapCompressedRTFStream**.
    
4. Valider et libérer les flux et non compressées.
    
À ce stade, si le fournisseur de banque de message prend en charge le format RTF, vous avez réalisé tout ce qui est requis. Vous pouvez dépendent du fournisseur de magasin de message pour gérer le processus de synchronisation et la création de la propriété **PR_BODY** , si nécessaire. Toutefois, si le fournisseur de banque de messages n’accepte pas le format RTF, vous devez appeler la fonction [RTFSync](rtfsync.md) pour synchroniser le texte avec mise en forme, l’indicateur RTF_SYNC_RTF_CHANGED. 
  

