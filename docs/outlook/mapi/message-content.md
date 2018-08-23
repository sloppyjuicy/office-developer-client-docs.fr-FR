---
title: Contenu du message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 85bd3f7db53f195295405fb0b02c25f084786a67
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586080"
---
# <a name="message-content"></a>Contenu du message

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
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
    

