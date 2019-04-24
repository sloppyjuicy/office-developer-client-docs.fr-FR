---
title: Contenu du message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: c4d2439c06da292c9cc72c1506a1ae4d10c6704f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357000"
---
# <a name="message-content"></a>Contenu du message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe deux codages possibles pour le contenu du message: l'un avec MIME, l'autre avec UUEncode. MIME est le codage par défaut. De plus, MAPI définit une propriété par destinataire, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), qui régit si les informations TNEF doivent être incluses ou non dans un message sortant. Il y a quatre façons de coder le contenu des messages:
  
- MIME avec TNEF
    
- MIME sans TNEF
    
- UUEncode avec TNEF
    
- UUEncode sans TNEF
    
Le choix entre MIME ou uuencode pour les messages sortants n'est pas spécifié.
  
Les propriétés suivantes sont exclues de TNEF **:\*PR_SENDER_**, **PR_ATTACH_DATA_\***, **PR_BODY**. Toutes les autres propriétés de message transmissibles sont incluses dans le flux TNEF.
  
Les suggestions suivantes sont destinées à fournir une liste des paramètres que l'implémentation peut prendre en charge:
  
- Codage MIME ou uuencode pour les messages sortants: Boolean.
    
- Jeu de caractères à utiliser pour les messages sortants: chaîne (copié directement vers le paramètre charset) ou énumération (traduite en interne en chaîne charset).
    

