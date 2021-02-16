---
title: Réception de messages à l’aide du traitement personnalisé des pièces jointes TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: 046b537d41b318fa857ef77f1906edcf2c3aa2bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429319"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a>Réception de messages à l’aide du traitement personnalisé des pièces jointes TNEF

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour recevoir un message TNEF avec traitement personnalisé des pièces jointes :
  
1. Importez toutes les propriétés transmises (celles que le système de messagerie prend en charge) du message entrant dans un nouveau message MAPI. Cela inclut le texte du message, qui contient le flux de données TNEF.
    
2. Identifiez et décodez la pièce jointe spéciale qui contient le flux TNEF.
    
3. Extrayez toutes les pièces jointes du message entrant dans les pièces jointes MAPI sur le nouveau message MAPI. Les noms de fichiers récupérés, ou d’autres marqueurs d’identification sur les pièces jointes, doivent être placés dans la propriété **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) des nouvelles pièces jointes afin que la méthode [ITnef::ExtractProps](itnef-extractprops.md) puisse ultérieurement associer la pièce jointe correcte aux balises de pièce jointe codées dans le texte du message. 
    
4. Créez une interface **OLE IStream** pour encapsuler le flux TNEF décodé et utilisez cet objet avec le nouveau message MAPI dans un appel à la fonction [OpenTnefStreamEx.](opentnefstreamex.md) 
    
5. Appelez la **méthode ITnef::ExtractProps** pour récupérer les propriétés nontransmitables du message à partir du flux de données TNEF. 
    
6. Appelez [la méthode ITnef::OpenTaggedBody](itnef-opentaggedbody.md) avec les indicateurs MAPI_CREATE et MAPI_MODIFY définies. Cet appel supprime les balises de pièce jointe du texte du message et les convertit en informations de position de pièce jointe dans le message MAPI. 
    
7. Remettre le message via lepooler MAPI.
    

