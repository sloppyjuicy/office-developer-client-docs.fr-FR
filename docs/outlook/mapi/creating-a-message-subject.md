---
title: Création d’un objet de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: cae255b90e8f2ccaaec4736c7ba1e9d6b7764f58
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593108"
---
# <a name="creating-a-message-subject"></a><span data-ttu-id="fd82f-103">Création d’un objet de message</span><span class="sxs-lookup"><span data-stu-id="fd82f-103">Creating a Message Subject</span></span>

  
  
<span data-ttu-id="fd82f-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd82f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd82f-105">L’objet d’un message, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), est une propriété facultative, utilisée pour résumer l’objectif d’un message.</span><span class="sxs-lookup"><span data-stu-id="fd82f-105">The subject of a message, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), is an optional property, used to summarize the intent of a message.</span></span> <span data-ttu-id="fd82f-106">Si vous choisissez de définir, rendre une chaîne de caractères 128 octets ou moins.</span><span class="sxs-lookup"><span data-stu-id="fd82f-106">If you choose to set it, make it a character string 128 bytes or less.</span></span> <span data-ttu-id="fd82f-107">La limite de 128 octets n’est pas une limite imposée par MAPI ; Il est une limite imposée par des fournisseurs de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="fd82f-107">The 128 byte limit is not a limit imposed by MAPI; it is a limit imposed by some message store providers.</span></span> <span data-ttu-id="fd82f-108">Pour garantir l’interopérabilité avec des fournisseurs qui imposent il, limiter les sujets à 128 octets.</span><span class="sxs-lookup"><span data-stu-id="fd82f-108">To ensure interoperability with providers that do impose it, limit subjects to 128 bytes.</span></span> 
  
<span data-ttu-id="fd82f-109">Sachez que certains fournisseurs de banque de messages ne permettent pas **PR_SUBJECT** est écrit dans un stream à l’interface [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="fd82f-109">Be aware that some message store providers do not allow **PR_SUBJECT** to be written to a stream with the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="fd82f-110">Ne définissez pas de **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) ; Cette propriété est définie uniquement sur les réponses et les messages transférée.</span><span class="sxs-lookup"><span data-stu-id="fd82f-110">Do not set **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); this property is set only on replies and forwarded messages.</span></span> 
  

