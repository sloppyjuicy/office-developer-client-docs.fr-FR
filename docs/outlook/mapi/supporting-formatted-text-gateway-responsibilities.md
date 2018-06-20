---
title: Prise en charge des responsabilités de passerelle de texte mis en forme
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 6d2c85aa76a372ba79e55dbf5b22024288214df6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787286"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a>Prenant en charge le format texte : Responsabilités de passerelle

  
  
**S’applique à**: Outlook 
  
 **Pour gérer le Format RTF pour les messages sortants, passerelles**
  
1. Récupérer uniquement les propriétés d’un message **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) à partir de la banque de messages. Le principal avantage de la récupération uniquement la propriété **PR_RTF_COMPRESSED** est que le texte du message n’a pas besoin d’être envoyés entre les ordinateurs si la passerelle et la banque de messages existent sur des ordinateurs différents. 
    
2. Générer le texte du message à partir du texte mis en forme en appelant la fonction de bibliothèque RTF **HrTextFromCompressedRTFStream** ou, si le message est stocké localement, **RTFSync**. L’indicateur RTF_SYNC_RTF_CHANGED doit être défini dans l’appel à **RTFSync**. Pour plus d’informations, voir [RTFSync](rtfsync.md).
    
3. Apporter des modifications irréversibles au texte du message, telles que la suppression des caractères non pris en charge. 
    
4. Assurez-vous que **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) et toutes les propriétés auxiliaire RTF sont configurés ou absent.
    
5. Si des modifications ont été apportées, appelez **RTFSync** avec la RTF_SYNC_RTF_CHANGED et RTF_SYNC_BODY_CHANGED flags définie. **RTFSync** recalcule les propriétés d’auxiliaire RTF à partir du texte modifié. 
    
6. Apporter des modifications réversible au texte du message, telles que l’insertion des espaces réservés de la pièce jointe et effectue les conversions de page de code non destructifs.
    
7. Envoyer le message.
    
 **Pour gérer le Format RTF pour les messages entrants, passerelles**
  
1. Annuler les modifications de texte de message qui ont été apportées directement avant que le message a été envoyé. 
    
2. Appeler **RTFSync** si le message contient les propriétés de **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) et **PR_RTF_COMPRESSED** . 
    
3. Mettre à jour le message dans la banque de messages avec la propriété **PR_RTF_COMPRESSED** si le message contient mettre à jour avec la propriété **PR_BODY** uniquement si **PR_RTF_COMPRESSED** est absente. 
    
4. Ignorer les **PR_BODY** si le message contient cette propriété et la **PR_RTF_COMPRESSED**.
    
Passerelles appellent **RTFSync** pour éviter de transmettre le texte du message et le texte mis en forme si la banque de messages est sur un autre ordinateur. Si la passerelle est locale, il peut définir les propriétés et autoriser la banque de messages effectuer la synchronisation. 
  

