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
ms.openlocfilehash: 2d74c9d5632e81e5b98cd1a4a02d5646cf3f6300
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592310"
---
# <a name="message-text"></a>Texte du message

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Pour les messages sortants en mode MIME, le type de contenu dépend s’offrent à quoi ressemble le texte du message et des pièces jointes. S’il existe des pièces jointes, le type de contenu est _mixte/multipartie ;_ le texte du message et chaque pièce jointe deviennent une partie du contenu du message, chacun avec son propre type de contenu distincte. S’il n’y a pas de pièces jointes, le type de contenu du message est _text/plain_ et qu’une seule partie. 
  
Le texte du message n'est pas ligne-encapsulé, sauf si une ligne dépasse 140 caractères. Cas, la totalité du texte est ramené à 76 colonnes et _quoted-printable_ est utilisé pour conserver les sauts de ligne. Le type de contenu varie selon les caractères sont trouvent dans le texte du message, comme suit : 
  
- Si seuls les caractères 7 bits sont détectés et aucune ligne ne dépasse 140 caractères, le message est texte ASCII. _Type de contenu : texte/ordinaire ; charset = us-ascii_ (Content-Transfer-Encoding = 7 bits est supposé.) 
    
- Si les lignes longues ou caractères 8 bits sont détectés, le message est du texte et le jeu de caractères est déterminé par les paramètres régionaux. Il doit être choisie dans les jeux de caractères définis par la norme ISO 8859 standard. _Type de contenu : texte/ordinaire ; charset = iso-8859-1_ (ou un autre jeu de caractères valide) 
    
     _Content-Transfer-Encoding: quoted-printable_
    
Pour les messages MIME entrants, si le premier message de contenu de composant a _Content-type : texte /\* _ (c'est-à-dire, tout type de texte) et son jeu de caractères est reconnue, elle est mappée à **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). Une première partie du contenu message ne pas ce critère devient une pièce jointe. Tous les composants suivants sont également les pièces jointes.
  
En mode uuencode, texte du message dans les messages sortants est encapsulé en ligne pour les 78 colonnes, MS Mail 3.x. Le type de contenu est « text/plain ». Pour conserver les sauts de paragraphe du message d’origine dans ces circonstances, observez les conventions suivantes dans le texte renvoyé à la ligne. Il existe trois raisons possibles pour mettre fin à une ligne de texte, chacun avec son propre séquence de caractères :
  
- Saut de ligne. Le texte d’origine contenu un saut de ligne entré par l’utilisateur (marque de paragraphe). Dans le transport, correspond à un saut de ligne sans espace ci-dessus. Si l’utilisateur entre un saut de ligne précédé de cellules vides, les espaces doivent être supprimés.
    
- Ligne-nobreak. Le texte d’origine contenu un mot trop long pour tenir sur une seule ligne du message. Dans le transport, correspond à un saut de ligne précédé de deux espaces.
    
- Renvoyer à la ligne. Le texte d’origine ne contenu aucun saut de ligne, le texte est trop long pour tenir sur une seule ligne du message, mais il peut être interrompu entre deux mots. Dans le transport, cela correspond à un saut de ligne précédée d’un espace simple.
    

