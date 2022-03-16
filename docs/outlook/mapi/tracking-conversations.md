---
title: Suivi des Conversations
manager: lindalu
ms.date: 03/11/2022
ms.audience: Developer
api_type:
- COM
ms.assetid: 0500dee8-a39d-45ce-87b1-c515e92e083d
ms.localizationpriority: high
ms.openlocfilehash: 8a7763caf228e160f3bcbe46dabb74ce30f7c2b5
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63508309"
---
# <a name="tracking-conversations"></a>Suivi de conversations

**S’applique à** : Outlook 2013 | Outlook 2016
  
Le suivi de conversations vise à collecter les réponses à un message. Les clients doivent définir deux propriétés qui aident dans le suivi des conversations :
  
- **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))

    **PR_CONVERSATION_TOPIC** est l’objet normalisé du message, l’objet sans les chaînes de préfixe. Définissez cette propriété sur la valeur de la **PR_NORMALIZED_SUBJECT** du message ([propriété PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).

- **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))

    **PR_CONVERSATION_INDEX** indique la position du message dans une conversation particulière. Il incombe au client de définir **PR_CONVERSATION_INDEX** pour chaque message sortant, qu'il s'agisse d'un nouveau message, d'un message transféré ou d'une réponse. Les clients peuvent définir cette propriété manuellement ou appeler [ScCreateConversationIndex](sccreateconversationindex.md), une fonction utilitaire fournie par MAPI.

 **ScCreateConversationIndex** g�n�re la valeur d'un index de conversation pour tous les messages sortants. **ScCreateConversationIndex** impl�mente l'index sous la forme d'un bloc d'en-t�te est 22 octets de longueur, suivi de z�ro ou plusieurs enfants bloque chaque 5 octets de longueur.
  
Le bloc d'en-t�te est compos� de 22 octets, divis�es en trois parties :
  
- Un octet r�serv�. Sa valeur est 1.
- Cinq octets pour l'heure syst�me actuelle converties au format de la structure [FILETIME](filetime.md) .
- 16 octets contenant un identificateur global unique ou le [GUID](guid.md).

Chaque bloc enfant est compos� de 5 octets, r�partis comme suit :
  
- Un bit contenant un code qui repr�sente la diff�rence entre l'heure actuelle et l'heure stock�e dans le bloc de l'en-t�te. Ce bit est �gal � 0 si la diff�rence est inf�rieure �.02 deuxi�me et sup�rieur � deux ans et 1 si la diff�rence est inf�rieure � 1 seconde et sup�rieure � 56 ans.

- Bits de trente un contenant la diff�rence entre l'heure actuelle et l'heure dans le bloc en-t�te exprim�e en unit�s de **FILETIME**. Cette partie du bloc enfant est g�n�r�e � l'aide d'une des deux strat�gies, selon la valeur du premier bit. Si ce bit est �gale � z�ro, **ScCreateConversationIndex** ignore les bits 15 et 18 bits de poids faibles. Si ce bit est 1, la fonction ignore les bits 10 et 23 bits de poids faibles.

- Quatre bits contenant un nombre al�atoire g�n�r� par l'appel de la fonction Win32 [GetTickCount](https://msdn.microsoft.com/library/ms724408%28VS.85%29.aspx).

- Quatre bits contenant un d�compte de s�quence qui est extrait de la partie du nombre al�atoire.

Si vous choisissez de d�finir les index de conversations de messages manuellement, tenez compte des suggestions suivantes :
  
1. Conserver les diff�rences dans les fuseaux horaires des personnes interrog�es transparent. utiliser les heures UTC plut�t que l'heure locale.

2. Retrait de chaque groupe de conversation du m�me montant.

3. Trier les r�ponses � la m�me date du message.

4. Threads distincts d�marr� � des moments diff�rents qui partagent la m�me rubrique en r�alit�.

5. Pour implémenter un tri classé afin que les messages soient regroupés par rubrique, triez d’abord par **PR_CONVERSATION_TOPIC**, puis par **PR_CONVERSATION_INDEX**. Pour présenter les résultats du tri, définissez la propriété **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) sur 0 pour les messages dont la longueur est de 22 octets dans l’index de conversation. Ensuite, pour chaque incrément de 5 octets dans la longueur, incrémentez la valeur de la propriété **PR_DEPTH** d’un.

Le PR_ORIGINAL groupe de propriétés peut également être utilisé pour le suivi des conversations. Définissez ces propriétés pour lier les messages de réponse ou transférés au message d’origine. Toutes les propriétés PR_ORIGINAL sont facultatives. Si vous ne définissez pas explicitement, par exemple, **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)), le fournisseur de magasin de messages peut utiliser la valeur par défaut ou la valeur de la propriété **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)). De même, si vous ne définissez pas **PR_ORIGINAL_AUTHOR_NAME** ou **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)), ces propriétés peuvent par défaut avoir les valeurs des propriétés **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) et **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)), respectivement.
  