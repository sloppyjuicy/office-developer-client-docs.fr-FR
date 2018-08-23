---
title: Réception de messages via le traitement de pièce jointe personnalisé TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: 67c202e5130bd35e1277c5260bc1702043eadd95
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588026"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a>Réception de messages via le traitement de pièce jointe personnalisé TNEF

 
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Pour recevoir un message TNEF avec traitement personnalisé des pièces jointes :
  
1. Importer toutes les propriétés transmissible — ceux qui prend en charge par le système de messagerie, à partir du message entrant dans un nouveau message MAPI. Cela inclut le texte du message, qui contient le flux de données TNEF.
    
2. Identifier et décoder la pièce jointe spéciale qui contient le flux TNEF.
    
3. Extraire toutes les pièces jointes à partir du message entrant dans les pièces jointes MAPI sur le nouveau message MAPI. Les noms de fichiers récupérée ou autres marques d’identification sur les pièces jointes, doivent être placés dans la propriété **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) des nouvelles pièces jointes ainsi que la méthode [ITnef::ExtractProps](itnef-extractprops.md) pouvez l’associer ultérieurement la pièce jointe correcte avec les balises de pièce jointe codés dans le texte du message. 
    
4. Créer une interface OLE **IStream** habiller le flux TNEF décodé et d’utiliser cet objet ainsi que le nouveau message MAPI dans un appel à la fonction [OpenTnefStreamEx](opentnefstreamex.md) . 
    
5. Appelez la méthode **ITnef::ExtractProps** pour récupérer les propriétés nontransmittable sur le message à partir du flux de données TNEF. 
    
6. Appelez la méthode [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) avec l’ensemble d’indicateurs MAPI_CREATE et ne. Cet appel supprime les balises de pièce jointe dans le texte du message et les convertit les informations de position des pièces jointes dans le message MAPI. 
    
7. Remettre le message via le spouleur MAPI.
    

