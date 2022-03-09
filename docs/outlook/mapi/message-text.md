---
title: Texte du message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4d1837f1-494f-481b-9e09-ab8249f1488c
ms.openlocfilehash: 2902b76594dd1976dd782d2c3796b0d16684ddb0
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63377035"
---
# <a name="message-text"></a>Texte du message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour les messages sortants en mode MIME, le type de contenu dépend de la nature des pièces jointes et de l’apparence du texte du message. S’il existe des pièces jointes, le type de contenu est en plusieurs parties  _/_ mixtes ; le texte du message et chaque pièce jointe deviennent une partie distincte du contenu du message, chacune avec son propre type de contenu. S’il n’existe aucune pièce jointe, le type de contenu du message est texte  _/simple_ et il n’y a qu’une seule partie. 
  
Le texte du message n’est pas wrapped ligne sauf si une ligne dépasse 140 caractères. Si c’est le cas, l’intégralité du texte est enveloppée de 76 colonnes et le codage entre caractères  _imprimables_ est utilisé pour conserver les coupures de lignes. Le type de contenu dépend des caractères trouvés dans le texte du message, comme suit : 
  
- Si seuls des caractères 7 bits sont trouvés et qu’aucune ligne ne dépasse 140 caractères, le message est du texte ASCII. _Content-type: text/plain; charset=us-ascii_ (Content-Transfer-Encoding=7bit is assumed.) 
    
- Si des lignes longues ou des caractères de 8 bits sont trouvés, le message est du texte et le jeu de caractères est déterminé par les paramètres régionaux. Il doit être choisi parmi les jeux de caractères définis par la norme ISO 8859. _Content-type: text/plain; charset=iso-8859-1_ (ou un autre jeu de caractères valide) 
    
     _Content-Transfer-Encoding: quoted-printable_
    
Pour les messages MIME entrants, si le premier élément de contenu de message possède  _content-type: text/\*_ (autrement dit, n’importe quel type de texte) et que son jeu de caractères est reconnu, il est mappé à **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). Un premier élément de contenu de message qui ne satisfait pas à ce critère devient une pièce jointe. Les parties suivantes deviennent également des pièces jointes.
  
En mode uuencode, le texte du message dans les messages sortants est entouré de 78 colonnes, comme pour MS Mail 3.x. Le type de contenu est « text/plain ». Pour conserver les interruptions de paragraphe du message d’origine dans ces circonstances, respectez les conventions suivantes dans le texte wrapped. Il existe trois raisons possibles pour mettre fin à une ligne de texte, chacune avec sa propre séquence de caractères :
  
- Line-break. Le texte d’origine contenait une nouvelle ligne entrée par l’utilisateur (marque de paragraphe). Dans le transport, cela est mapcé sur une nouvelle ligne sans aucun vide précédent. Si l’utilisateur entre une nouvelle ligne précédée de vides, ces derniers doivent être retirés.
    
- Line-nobreak. Le texte d’origine contenait un mot trop long pour tenir sur une seule ligne du message. Dans le transport, cela est mapcé sur une nouvelle ligne précédée de deux espaces vides.
    
- Wrap- line-wrap. Le texte d’origine ne contenait aucune nouvelle ligne, le texte est trop long pour tenir sur une seule ligne du message, mais il peut être rompu entre deux mots. Dans le transport, cela est mapcé sur une nouvelle ligne précédée d’un seul vide.
    

