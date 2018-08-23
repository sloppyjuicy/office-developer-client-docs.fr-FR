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
# <a name="tracking-conversations"></a><span data-ttu-id="613c0-103">Suivi des Conversations</span><span class="sxs-lookup"><span data-stu-id="613c0-103">Tracking Conversations</span></span>

  
  
<span data-ttu-id="613c0-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="613c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="613c0-p101">Conversation suivi collecte des r�ponses � un message. Les clients doivent d�finir deux propri�t�s qui vous aident dans les conversations de suivi :</span><span class="sxs-lookup"><span data-stu-id="613c0-p101">Conversation tracking is collecting responses to a message. Clients should set two properties that aid in tracking conversations:</span></span>
  
- <span data-ttu-id="613c0-107">**PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="613c0-107">**PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))</span></span>
    
    <span data-ttu-id="613c0-108">**PR_CONVERSATION_TOPIC** est l'objet du message, l'objet sans les cha�nes de pr�fixe normalis�.</span><span class="sxs-lookup"><span data-stu-id="613c0-108">**PR_CONVERSATION_TOPIC** is the normalized subject of the message, the subject without the prefix strings.</span></span> <span data-ttu-id="613c0-109">Définir cette propriété à la valeur de la propriété **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) du message.</span><span class="sxs-lookup"><span data-stu-id="613c0-109">Set this property to the value of the message's **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span> 
    
- <span data-ttu-id="613c0-110">**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="613c0-110">**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))</span></span>
    
    <span data-ttu-id="613c0-p103">**PR_CONVERSATION_INDEX** indicates the position of the message within a particular conversation. It is a client's reponsibility to set **PR_CONVERSATION_INDEX** for each outgoing message, whether it is a new message, a forwarded message, or a reply. Clients can set this property manually or call [ScCreateConversationIndex](sccreateconversationindex.md), a utility function provided by MAPI.</span><span class="sxs-lookup"><span data-stu-id="613c0-p103">**PR_CONVERSATION_INDEX** indicates the position of the message within a particular conversation. It is a client's reponsibility to set **PR_CONVERSATION_INDEX** for each outgoing message, whether it is a new message, a forwarded message, or a reply. Clients can set this property manually or call [ScCreateConversationIndex](sccreateconversationindex.md), a utility function provided by MAPI.</span></span> 
    
 <span data-ttu-id="613c0-p104">**ScCreateConversationIndex** g�n�re la valeur d'un index de conversation pour tous les messages sortants. **ScCreateConversationIndex** impl�mente l'index sous la forme d'un bloc d'en-t�te est 22 octets de longueur, suivi de z�ro ou plusieurs enfants bloque chaque 5 octets de longueur.</span><span class="sxs-lookup"><span data-stu-id="613c0-p104">**ScCreateConversationIndex** generates the value of a conversation index for any outgoing message. **ScCreateConversationIndex** implements the index as a header block that is 22 bytes in length, followed by zero or more child blocks each 5 bytes in length.</span></span> 
  
<span data-ttu-id="613c0-116">Le bloc d'en-t�te est compos� de 22 octets, divis�es en trois parties :</span><span class="sxs-lookup"><span data-stu-id="613c0-116">The header block is composed of 22 bytes, divided into three parts:</span></span>
  
- <span data-ttu-id="613c0-p105">Un octet r�serv�. Sa valeur est 1.</span><span class="sxs-lookup"><span data-stu-id="613c0-p105">One reserved byte. Its value is 1.</span></span>
    
- <span data-ttu-id="613c0-119">Cinq octets pour l'heure syst�me actuelle converties au format de la structure [FILETIME](filetime.md) .</span><span class="sxs-lookup"><span data-stu-id="613c0-119">Five bytes for the current system time converted to the [FILETIME](filetime.md) structure format.</span></span> 
    
- <span data-ttu-id="613c0-120">16 octets contenant un identificateur global unique ou le [GUID](guid.md).</span><span class="sxs-lookup"><span data-stu-id="613c0-120">Sixteen bytes holding a [GUID](guid.md), or globally unique identifier.</span></span>
    
<span data-ttu-id="613c0-121">Chaque bloc enfant est compos� de 5 octets, r�partis comme suit :</span><span class="sxs-lookup"><span data-stu-id="613c0-121">Each child block is composed of 5 bytes, divided as follows:</span></span>
  
- <span data-ttu-id="613c0-p106">Un bit contenant un code qui repr�sente la diff�rence entre l'heure actuelle et l'heure stock�e dans le bloc de l'en-t�te. Ce bit est �gal � 0 si la diff�rence est inf�rieure �.02 deuxi�me et sup�rieur � deux ans et 1 si la diff�rence est inf�rieure � 1 seconde et sup�rieure � 56 ans.</span><span class="sxs-lookup"><span data-stu-id="613c0-p106">One bit containing a code representing the difference between the current time and the time stored in the header block. This bit will be 0 if the difference is less than .02 second and greater than two years and 1 if the difference is less than one second and greater than 56 years.</span></span>
    
- <span data-ttu-id="613c0-p107">Bits de trente un contenant la diff�rence entre l'heure actuelle et l'heure dans le bloc en-t�te exprim�e en unit�s de **FILETIME**. Cette partie du bloc enfant est g�n�r�e � l'aide d'une des deux strat�gies, selon la valeur du premier bit. Si ce bit est �gale � z�ro, **ScCreateConversationIndex** ignore les bits 15 et 18 bits de poids faibles. Si ce bit est 1, la fonction ignore les bits 10 et 23 bits de poids faibles.</span><span class="sxs-lookup"><span data-stu-id="613c0-p107">Thirty one bits containing the difference between the current time and the time in the header block expressed in **FILETIME** units.This part of the child block is produced using one of two strategies, depending on the value of the first bit. If this bit is zero, **ScCreateConversationIndex** discards the high 15 bits and the low 18 bits. If this bit is one, the function discards the high 10 bits and the low 23 bits.</span></span> 
    
- <span data-ttu-id="613c0-127">Quatre bits contenant un nombre al�atoire g�n�r� par l'appel de la fonction Win32 [GetTickCount](http://msdn.microsoft.com/en-us/library/ms724408%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="613c0-127">Four bits containing a random number generated by calling the Win32 function [GetTickCount](http://msdn.microsoft.com/en-us/library/ms724408%28VS.85%29.aspx).</span></span>
    
- <span data-ttu-id="613c0-128">Quatre bits contenant un d�compte de s�quence qui est extrait de la partie du nombre al�atoire.</span><span class="sxs-lookup"><span data-stu-id="613c0-128">Four bits containing a sequence count that is taken from part of the random number.</span></span>
    
<span data-ttu-id="613c0-129">Si vous choisissez de d�finir les index de conversations de messages manuellement, tenez compte des suggestions suivantes :</span><span class="sxs-lookup"><span data-stu-id="613c0-129">If you choose to set the conversation indexes of messages manually, consider the following suggestions:</span></span>
  
1. <span data-ttu-id="613c0-130">Conserver les diff�rences dans les fuseaux horaires des personnes interrog�es transparent. utiliser les heures UTC plut�t que l'heure locale.</span><span class="sxs-lookup"><span data-stu-id="613c0-130">Keep differences in the respondents' time zones transparent; use UTC times rather than local time.</span></span>
    
2. <span data-ttu-id="613c0-131">Retrait de chaque groupe de conversation du m�me montant.</span><span class="sxs-lookup"><span data-stu-id="613c0-131">Indent each conversation group by the same amount.</span></span>
    
3. <span data-ttu-id="613c0-132">Trier les r�ponses � la m�me date du message.</span><span class="sxs-lookup"><span data-stu-id="613c0-132">Sort responses to the same message date.</span></span>
    
4. <span data-ttu-id="613c0-133">Threads distincts d�marr� � des moments diff�rents qui partagent la m�me rubrique en r�alit�.</span><span class="sxs-lookup"><span data-stu-id="613c0-133">Separate threads started at different times that happen to share the same topic.</span></span> 
    
5. <span data-ttu-id="613c0-134">Pour impl�menter un tri par cat�gorie afin que les messages sont regroup�s par sujet, trier par **PR_CONVERSATION_TOPIC** en premier, puis par **PR_CONVERSATION_INDEX**.</span><span class="sxs-lookup"><span data-stu-id="613c0-134">To implement a categorized sort so that messages are grouped by topic, sort by **PR_CONVERSATION_TOPIC** first and then by **PR_CONVERSATION_INDEX**.</span></span> <span data-ttu-id="613c0-135">Pour présenter les résultats de l’ordre de tri, définir la propriété **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) à 0 pour les messages avec un index de conversation est 22 octets.</span><span class="sxs-lookup"><span data-stu-id="613c0-135">To present the results of the sort, set the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property to 0 for messages with a conversation index that is 22 bytes in length.</span></span> <span data-ttu-id="613c0-136">Ensuite, pour chaque incr�ment de 5 octets dans la longueur, incr�mente la valeur de la propri�t� **PR_DEPTH** d'une unit�.</span><span class="sxs-lookup"><span data-stu-id="613c0-136">Then, for every 5-byte increment in the length, increment the value of the **PR_DEPTH** property by one.</span></span> 
    
<span data-ttu-id="613c0-137">Le groupe PR_ORIGINAL de propri�t�s peut �galement servir de conversation de suivi.</span><span class="sxs-lookup"><span data-stu-id="613c0-137">The PR_ORIGINAL group of properties can also be used for conversation tracking.</span></span> <span data-ttu-id="613c0-138">D�finir ces propri�t�s pour lier r�pondre ou les messages transf�r�s au message d'origine.</span><span class="sxs-lookup"><span data-stu-id="613c0-138">Set these properties to link reply or forwarded messages to the original message.</span></span> <span data-ttu-id="613c0-139">Toutes les propri�t�s PR_ORIGINAL sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="613c0-139">All of the PR_ORIGINAL properties are optional.</span></span> <span data-ttu-id="613c0-140">Si vous ne définissez pas explicitement, par exemple, **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)), le fournisseur de magasin de message peut utiliser la valeur par défaut ou la valeur de la **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) propriété.</span><span class="sxs-lookup"><span data-stu-id="613c0-140">If you do not explicitly set, for example, **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)), the message store provider can use the default value, or the value of the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="613c0-141">De même, si vous ne définissez pas **PR_ORIGINAL_AUTHOR_NAME** ou **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)), ces propriétés par défaut pour les valeurs des **PR_ **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) CLIENT_SUBMIT_TIME** propriétés ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)), respectivement.</span><span class="sxs-lookup"><span data-stu-id="613c0-141">Likewise, if you do not set **PR_ORIGINAL_AUTHOR_NAME** or **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)), these properties can default to the values of the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) and **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) properties, respectively.</span></span> 
  

