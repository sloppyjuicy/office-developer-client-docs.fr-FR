---
title: Contenu des messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 5e8debcd5a60357f05dfb7b6bde1faf972e50a26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784879"
---
# <a name="message-content"></a>Contenu des messages

  
  
**S’applique à**: Outlook 
  
Il existe deux codages possibles pour le contenu du message : un à l’aide de MIME, l’autre à l’aide d’uuencode. MIME est le codage par défaut. En outre, MAPI définit une propriété par destinataire, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), qui détermine les informations TNEF doivent être incluses dans un message sortant ou non. Ainsi, il existe un total de quatre façons de codage du contenu des messages :
  
- MIME avec TNEF
    
- MIME sans TNEF
    
- UUEncode avec TNEF
    
- UUEncode sans TNEF
    
Comment choisir MIME ou uuencode pour les messages sortants n’est pas spécifié.
  
Les propriétés suivantes sont exclues TNEF : **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**. Toutes les autres propriétés de message transmissible sont incluses dans le flux TNEF.
  
Les suggestions suivantes sont destinées à fournir une liste des paramètres de l’implémentation peut décider comment prendre en charge :
  
- S’il faut encoder à l’aide de MIME ou uuencode pour les messages sortants : boolean.
    
- À utiliser pour les messages sortants jeu de caractères : chaîne (copié directement dans le paramètre charset) ou énumération (traduit en interne pour la chaîne de jeu de caractères).
    

