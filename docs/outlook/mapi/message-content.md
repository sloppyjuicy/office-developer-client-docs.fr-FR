---
title: Contenu du message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b1523d230ae49e8ca779bab12e5ce6264f6300dc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592059"
---
# <a name="message-content"></a>Contenu du message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe deux codages possibles pour le contenu du message : l’un utilisant MIME, l’autre utilisant uuencode. MIME est le codage préféré. En outre, MAPI définit une propriété par destinataire, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), qui détermine si les informations TNEF doivent être incluses ou non dans un message sortant. Il existe donc un total de quatre façons d’encodage du contenu des messages :
  
- MIME avec TNEF
    
- MIME sans TNEF
    
- uuencode avec TNEF
    
- uuencode sans TNEF
    
La manière de choisir MIME ou uuencode pour les messages sortants n’est pas spécifiée.
  
Les propriétés suivantes sont exclues du TNEF : **PR_SENDER_ \* *_, _* PR_ATTACH_DATA_ \* *_, _* PR_BODY**. Toutes les autres propriétés de message transmises sont incluses dans le flux TNEF.
  
Les suggestions suivantes sont destinées à fournir une liste de paramètres que l’implémentation peut prendre en charge :
  
- S’il faut coder à l’aide de MIME ou uuencode pour les messages sortants : booléen.
    
- Jeu de caractères à utiliser pour les messages sortants : chaîne (copiée directement dans le paramètre charset) ou enumeration (traduite en chaîne de caractères en interne).
    

