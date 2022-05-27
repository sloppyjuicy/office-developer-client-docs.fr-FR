---
title: Réception de messages à l’aide du traitement des pièces jointes personnalisées TNEF
description: Décrit comment recevoir un message TNEF avec un traitement de pièces jointes personnalisé. Cette rubrique s’applique à Outlook 2013 et Outlook 2016.
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
ms.openlocfilehash: 2634f903b0718dabe9900ea0ae000192a34d2799
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752749"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a>Réception de messages à l’aide du traitement des pièces jointes personnalisées TNEF

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour recevoir un message TNEF avec un traitement des pièces jointes personnalisé :
  
1. Importez toutes les propriétés transmissibles , celles prises en charge par le système de messagerie, à partir du message entrant dans un nouveau message MAPI. Cela inclut le texte du message, qui contient le flux de données TNEF.
    
2. Identifiez et décodez la pièce jointe spéciale qui contient le flux TNEF.
    
3. Extrayez toutes les pièces jointes du message entrant dans les pièces jointes MAPI du nouveau message MAPI. Les noms de fichiers récupérés, ou d’autres marqueurs d’identification sur les pièces jointes, doivent être placés dans la propriété **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) des nouvelles pièces jointes afin que la méthode [ITnef::ExtractProps](itnef-extractprops.md) puisse associer ultérieurement la pièce jointe correcte aux balises de pièce jointe encodées dans le texte du message. 
    
4. Créez une interface OLE **IStream** pour encapsuler le flux TNEF décodé et utilisez cet objet avec le nouveau message MAPI dans un appel à la fonction [OpenTnefStreamEx](opentnefstreamex.md) . 
    
5. Appelez la méthode **ITnef::ExtractProps** pour récupérer les propriétés non transférables sur le message à partir du flux de données TNEF. 
    
6. Appelez la méthode [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) avec les indicateurs MAPI_CREATE et MAPI_MODIFY définis. Cet appel supprime les balises de pièce jointe du texte du message et les convertit en informations de position de pièce jointe dans le message MAPI. 
    
7. Remettre le message via le spouleur MAPI.
    

