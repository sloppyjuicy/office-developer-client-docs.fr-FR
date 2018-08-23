---
title: Suivi des Conversations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0500dee8-a39d-45ce-87b1-c515e92e083d
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: ae8b5a474675c0afd771f4e8dfd060d0b379c8f4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572220"
---
# <a name="tracking-conversations"></a>Suivi des Conversations

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Conversation suivi collecte des r�ponses � un message. Les clients doivent d�finir deux propri�t�s qui vous aident dans les conversations de suivi :
  
- **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))
    
    **PR_CONVERSATION_TOPIC** est l'objet du message, l'objet sans les cha�nes de pr�fixe normalis�. Définir cette propriété à la valeur de la propriété **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) du message. 
    
- **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))
    
    **PR_CONVERSATION_INDEX** indicates the position of the message within a particular conversation. It is a client's reponsibility to set **PR_CONVERSATION_INDEX** for each outgoing message, whether it is a new message, a forwarded message, or a reply. Clients can set this property manually or call [ScCreateConversationIndex](sccreateconversationindex.md), a utility function provided by MAPI. 
    
 **ScCreateConversationIndex** g�n�re la valeur d'un index de conversation pour tous les messages sortants. **ScCreateConversationIndex** impl�mente l'index sous la forme d'un bloc d'en-t�te est 22 octets de longueur, suivi de z�ro ou plusieurs enfants bloque chaque 5 octets de longueur. 
  
Le bloc d'en-t�te est compos� de 22 octets, divis�es en trois parties :
  
- Un octet r�serv�. Sa valeur est 1.
    
- Cinq octets pour l'heure syst�me actuelle converties au format de la structure [FILETIME](filetime.md) . 
    
- 16 octets contenant un identificateur global unique ou le [GUID](guid.md).
    
Chaque bloc enfant est compos� de 5 octets, r�partis comme suit :
  
- Un bit contenant un code qui repr�sente la diff�rence entre l'heure actuelle et l'heure stock�e dans le bloc de l'en-t�te. Ce bit est �gal � 0 si la diff�rence est inf�rieure �.02 deuxi�me et sup�rieur � deux ans et 1 si la diff�rence est inf�rieure � 1 seconde et sup�rieure � 56 ans.
    
- Bits de trente un contenant la diff�rence entre l'heure actuelle et l'heure dans le bloc en-t�te exprim�e en unit�s de **FILETIME**. Cette partie du bloc enfant est g�n�r�e � l'aide d'une des deux strat�gies, selon la valeur du premier bit. Si ce bit est �gale � z�ro, **ScCreateConversationIndex** ignore les bits 15 et 18 bits de poids faibles. Si ce bit est 1, la fonction ignore les bits 10 et 23 bits de poids faibles. 
    
- Quatre bits contenant un nombre al�atoire g�n�r� par l'appel de la fonction Win32 [GetTickCount](http://msdn.microsoft.com/en-us/library/ms724408%28VS.85%29.aspx).
    
- Quatre bits contenant un d�compte de s�quence qui est extrait de la partie du nombre al�atoire.
    
Si vous choisissez de d�finir les index de conversations de messages manuellement, tenez compte des suggestions suivantes :
  
1. Conserver les diff�rences dans les fuseaux horaires des personnes interrog�es transparent. utiliser les heures UTC plut�t que l'heure locale.
    
2. Retrait de chaque groupe de conversation du m�me montant.
    
3. Trier les r�ponses � la m�me date du message.
    
4. Threads distincts d�marr� � des moments diff�rents qui partagent la m�me rubrique en r�alit�. 
    
5. Pour impl�menter un tri par cat�gorie afin que les messages sont regroup�s par sujet, trier par **PR_CONVERSATION_TOPIC** en premier, puis par **PR_CONVERSATION_INDEX**. Pour présenter les résultats de l’ordre de tri, définir la propriété **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) à 0 pour les messages avec un index de conversation est 22 octets. Ensuite, pour chaque incr�ment de 5 octets dans la longueur, incr�mente la valeur de la propri�t� **PR_DEPTH** d'une unit�. 
    
Le groupe PR_ORIGINAL de propri�t�s peut �galement servir de conversation de suivi. D�finir ces propri�t�s pour lier r�pondre ou les messages transf�r�s au message d'origine. Toutes les propri�t�s PR_ORIGINAL sont facultatives. Si vous ne définissez pas explicitement, par exemple, **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)), le fournisseur de magasin de message peut utiliser la valeur par défaut ou la valeur de la **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) propriété. De même, si vous ne définissez pas **PR_ORIGINAL_AUTHOR_NAME** ou **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)), ces propriétés par défaut pour les valeurs des **PR_ **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) CLIENT_SUBMIT_TIME** propriétés ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)), respectivement. 
  

