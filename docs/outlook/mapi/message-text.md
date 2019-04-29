---
title: Texte du message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d1837f1-494f-481b-9e09-ab8249f1488c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: fcbdec5adcb47ffac431a832cbb851ee4ebe16d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418546"
---
# <a name="message-text"></a>Texte du message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour les messages sortants en mode MIME, le type de contenu varie selon qu'il y a des pièces jointes et le texte du message. S'il y a des pièces jointes, le type de contenu est _multipart/mixed;_ le texte du message et chaque pièce jointe deviennent une partie distincte du contenu du message, chacune avec son propre type de contenu. S'il n'y a pas de pièces jointes, le type de contenu du message est _text/plain_ et il n'y a qu'un seul composant. 
  
Le texte du message n'est pas renvoyé à la ligne, sauf si une ligne dépasse 140 caractères. Si c'est le cas, l'intégralité du texte est enveloppée sur 76 colonnes et le codage _quoted-printable_ est utilisé pour conserver les sauts de ligne. Le type de contenu dépend des caractères figurant dans le texte du message, comme suit: 
  
- Si seuls les caractères 7 bits sont trouvés et qu'aucune ligne ne dépasse 140 caractères, le message est du texte ASCII. _Content-type: text/plain; charset = US-ASCII_ (Content-Transfer-Encoding = 7bit est supposé.) 
    
- Si des lignes longues ou des caractères 8 bits sont trouvés, le message est du texte et le jeu de caractères est déterminé par les paramètres régionaux. Il doit être choisi parmi les jeux de caractères définis par la norme ISO 8859. _Content-type: text/plain; charset = ISO-8859-1_ (ou un autre charset valide) 
    
     _Content-Transfer-Encoding: quoted-printable_
    
Pour les messages MIME entrants, si le premier composant de contenu de message a _Content-type\* : Text/_ (tout type de texte) et son jeu de caractères sont reconnus, il est mappé à **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). Une première partie de contenu de message ne répondant pas à ce critère devient une pièce jointe. Tous les composants suivants deviennent également des pièces jointes.
  
En mode UUEncode, le texte du message dans les messages sortants est renvoyé à la ligne sur 78 colonnes, comme pour MS Mail 3. x. Content-type est «text/plain». Pour conserver les sauts de paragraphe du message d'origine dans ces circonstances, observez les conventions suivantes dans le texte renvoyé à la commande. Il existe trois raisons possibles pour terminer une ligne de texte, chacune avec sa propre séquence de caractères:
  
- Saut de ligne. Le texte d'origine contient un saut de ligne entré par l'utilisateur (marque de paragraphe). Dans le transport, il est mappé à un saut de ligne sans espaces avant. Si l'utilisateur entre une ligne de saut de ligne précédée par des espaces, les blancs doivent être supprimés.
    
- Ligne-NOBREAK. Le texte d'origine contient un mot trop long pour tenir sur une seule ligne du message. Dans le transport, cette correspondance est mappée à une nouvelle ligne, précédée de deux espaces vides.
    
- Retour à la ligne. Le texte d'origine ne contient pas de saut de ligne, le texte est trop long pour tenir sur une seule ligne du message, mais il peut être brisé entre deux mots. Dans le transport, il est mappé à une nouvelle ligne, précédée d'un seul espace.
    

