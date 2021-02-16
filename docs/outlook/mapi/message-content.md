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
ms.openlocfilehash: c4d2439c06da292c9cc72c1506a1ae4d10c6704f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435459"
---
# <a name="message-content"></a>Contenu du message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe deux codages possibles pour le contenu du message : l’un utilisant MIME, l’autre utilisant uuencode. MIME est le codage préféré. En outre, MAPI définit une propriété par destinataire, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), qui détermine si les informations TNEF doivent être incluses ou non dans un message sortant. Il existe donc un total de quatre façons d’encodage du contenu des messages :
  
- MIME avec TNEF
    
- MIME sans TNEF
    
- uuencode avec TNEF
    
- uuencode sans TNEF
    
La manière de choisir MIME ou uuencode pour les messages sortants n’est pas spécifiée.
  
Les propriétés suivantes sont exclues du TNEF **: \* PR_SENDER_**, **PR_ATTACH_DATA_ \***, **PR_BODY**. Toutes les autres propriétés de message transmises sont incluses dans le flux TNEF.
  
Les suggestions suivantes sont destinées à fournir une liste de paramètres que l’implémentation peut prendre en charge :
  
- S’il faut coder à l’aide de MIME ou uuencode pour les messages sortants : booléen.
    
- Jeu de caractères à utiliser pour les messages sortants : chaîne (copiée directement dans le paramètre charset) ou enumeration (traduite en chaîne de caractères en interne).
    

