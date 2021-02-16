---
title: Prise en charge des responsabilités de la passerelle de texte mise en forme
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d5c3480018be399a85ee0bfda7ce1ff9b701cecc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419428"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a>Prise en charge du texte formaté : responsabilités de la passerelle

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour gérer le format texte enrichi pour les messages sortants, passerelles**
  
1. Récupérez uniquement la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) d’un message à partir de la boutique de messages. Le principal avantage de la récupération de la propriété PR_RTF_COMPRESSED est que le texte du message **n’a** pas besoin d’être envoyé entre les ordinateurs si la passerelle et la boutique de messages existent sur différents ordinateurs. 
    
2. Générez le texte du message à partir du texte mis en forme en appelant la fonction de bibliothèque RTF **HrTextFromCompressedRTFStream** ou, si le message est stocké localement, **RTFSync**. L’RTF_SYNC_RTF_CHANGED doit être définie dans l’appel à **RTFSync**. Pour plus d’informations, [voir RTFSync](rtfsync.md).
    
3. Apporter des modifications irréversibles au texte du message, telles que le fait de laisser des caractères non pris en place. 
    
4. Assurez-vous **que PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) et toutes les propriétés auxilliary RTF sont définies ou absentes.
    
5. Si des modifications ont été apportées, appelez **RTFSync** avec les indicateurs RTF_SYNC_RTF_CHANGED et RTF_SYNC_BODY_CHANGED définies. **RTFSync** recalcule les propriétés auxilliary RTF à partir du texte modifié. 
    
6. A effectuez des modifications inversables dans le texte du message, telles que l’insertion d’espaces réservé de pièce jointe et la conversion de page de code nondestructive.
    
7. Envoyez le message.
    
 **Pour gérer le format texte enrichi pour les messages entrants, passerelles**
  
1. Annuler toutes les modifications de texte de message effectuées directement avant l’envoi du message. 
    
2. Appelez **RTFSync** si le message contient les propriétés **PR_RTF_COMPRESSED** et **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). 
    
3. Mettez à jour le message dans la magasin de messages avec **la propriété PR_RTF_COMPRESSED** si le message le contient ; mise à jour avec **la propriété PR_BODY** uniquement si **PR_RTF_COMPRESSED** est absent. 
    
4. Ignorer **PR_BODY** si le message contient à la fois cette propriété et **PR_RTF_COMPRESSED**.
    
Les passerelles **appellent RTFSync** pour éviter de transmettre à la fois le texte du message et le texte formaté si la boutique de messages se trouve sur un autre ordinateur. Si la passerelle est locale, elle peut définir les deux propriétés et autoriser la boutique de messages à effectuer la synchronisation. 
  

