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
ms.openlocfilehash: 753834ba4df6d0239a484af380e4fe0aa45666b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332962"
---
# <a name="creating-a-message-subject"></a><span data-ttu-id="da451-103">Création d’un objet de message</span><span class="sxs-lookup"><span data-stu-id="da451-103">Creating a Message Subject</span></span>

  
  
<span data-ttu-id="da451-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da451-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da451-105">L’objet d’un message, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), est une propriété facultative, utilisée pour résumer l’intention d’un message.</span><span class="sxs-lookup"><span data-stu-id="da451-105">The subject of a message, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), is an optional property, used to summarize the intent of a message.</span></span> <span data-ttu-id="da451-106">Si vous choisissez de la définir, faites-en une chaîne de caractères de 128 octets ou moins.</span><span class="sxs-lookup"><span data-stu-id="da451-106">If you choose to set it, make it a character string 128 bytes or less.</span></span> <span data-ttu-id="da451-107">La limite de 128 byte n’est pas une limite imposée par MAPI ; Il s’agit d’une limite imposée par certains fournisseurs de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="da451-107">The 128 byte limit is not a limit imposed by MAPI; it is a limit imposed by some message store providers.</span></span> <span data-ttu-id="da451-108">Pour garantir l’interopérabilité avec les fournisseurs qui l’imposent, limitez les sujets à 128 octets.</span><span class="sxs-lookup"><span data-stu-id="da451-108">To ensure interoperability with providers that do impose it, limit subjects to 128 bytes.</span></span> 
  
<span data-ttu-id="da451-109">Sachez que certains fournisseurs de magasins de messages n’autorisent **pas PR_SUBJECT’écriture** dans un flux avec [l’interface IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da451-109">Be aware that some message store providers do not allow **PR_SUBJECT** to be written to a stream with the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="da451-110">Ne définissez **pas PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) ; cette propriété est définie uniquement sur les réponses et les messages transmis.</span><span class="sxs-lookup"><span data-stu-id="da451-110">Do not set **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); this property is set only on replies and forwarded messages.</span></span> 
  

