---
title: Texte mis en forme dans MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d0ff834-253b-4e8c-a5be-6e4745a2a66c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bfaa4fd5f561c8138461db6ce8b9033c2a75b96b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580627"
---
# <a name="formatted-text-in-mapi"></a><span data-ttu-id="5e79c-103">Texte mis en forme dans MAPI</span><span class="sxs-lookup"><span data-stu-id="5e79c-103">Formatted Text in MAPI</span></span>

  
  
<span data-ttu-id="5e79c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e79c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e79c-105">Le texte d’un message peut être stocké et transmises à l’aide de texte brut ou texte mis en forme.</span><span class="sxs-lookup"><span data-stu-id="5e79c-105">The text of a message can be stored and transmitted using plain text or formatted text.</span></span> <span data-ttu-id="5e79c-106">Texte mis en forme améliore le texte du message en modifiant son apparence avec, par exemple, une ou plusieurs polices, les tailles de police ou les couleurs de texte.</span><span class="sxs-lookup"><span data-stu-id="5e79c-106">Formatted text enhances the message text by altering its appearance with, for example, one or more fonts, font sizes, or text colors.</span></span> <span data-ttu-id="5e79c-107">Il est recommandé que tous les clients et la mesure du possible, tous les fournisseurs de banque de messages, prennent en charge le texte mis en forme.</span><span class="sxs-lookup"><span data-stu-id="5e79c-107">It is recommended that all clients and whenever possible, all message store providers, support formatted text.</span></span> <span data-ttu-id="5e79c-108">Prise en charge de texte mis en forme dans les messages enrichit en améliorer la lisibilité de message et en gestion des messages plus facile et plus efficace.</span><span class="sxs-lookup"><span data-stu-id="5e79c-108">Supporting formatted text in messages adds value by improving message readability and making message handling easier and more efficient.</span></span>
  
<span data-ttu-id="5e79c-109">Texte mis en forme peut être implémenté de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="5e79c-109">Formatted text can be implemented in a variety of ways.</span></span> <span data-ttu-id="5e79c-110">Le moyen le plus courant est avec le Format de texte enrichi (RTF).</span><span class="sxs-lookup"><span data-stu-id="5e79c-110">The most common way is with the Rich Text Format (RTF).</span></span> <span data-ttu-id="5e79c-111">MAPI définit trois propriétés transmissible pour conserver les informations de texte de message : **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) pour le texte brut, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) pour le HTML et **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) ) pour le texte RTF qui a été compressé.</span><span class="sxs-lookup"><span data-stu-id="5e79c-111">MAPI defines three transmittable properties for holding message text information: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) for plain text, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) for HTML, and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) for RTF text that has been compressed.</span></span> <span data-ttu-id="5e79c-112">La version mise en forme d’un texte de message pouvant être deux fois aussi grande que la version sans la mise en forme, le texte RTF est compressé avant d’être transféré avec le message et stocké dans la propriété **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="5e79c-112">Because the formatted version of a message text can be twice as large as the version without the formatting, the RTF text is compressed before it is transferred with the message and stored in the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="5e79c-113">Lorsqu’il est temps pour afficher le message sur l’écran, il est décompressé à l’aide d’une fonction utilitaire fournie par MAPI.</span><span class="sxs-lookup"><span data-stu-id="5e79c-113">When it is time to display the message on the screen, it is uncompressed using a utility function provided by MAPI.</span></span> 
  
<span data-ttu-id="5e79c-114">MAPI définit ces deux propriétés de texte du message et pour la conversion entre les mécanismes de sorte que les clients prenant en charge les RTF peuvent interagir avec les clients et les systèmes de messagerie ne prenant pas en charge texte mis en forme.</span><span class="sxs-lookup"><span data-stu-id="5e79c-114">MAPI defines these two message text properties and mechanisms for conversion between them so that RTF-aware clients can interoperate with clients and messaging systems that do not support formatted text.</span></span>
  
### 

[<span data-ttu-id="5e79c-115">Synchronisation du texte et de la mise en forme</span><span class="sxs-lookup"><span data-stu-id="5e79c-115">Synchronizing Text and Formatting</span></span>](synchronizing-text-and-formatting.md)
  
> <span data-ttu-id="5e79c-116">Décrit comment maintenir la synchronisation avec la mise en forme du texte de message RTF.</span><span class="sxs-lookup"><span data-stu-id="5e79c-116">Describes how to keep RTF message text synchronized with the formatting.</span></span>
    
[<span data-ttu-id="5e79c-117">Prise en charge du texte mis en forme dans les messages sortants : responsabilités du client</span><span class="sxs-lookup"><span data-stu-id="5e79c-117">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> <span data-ttu-id="5e79c-118">Décrit les responsabilités du client application pour prendre en charge le texte mis en forme dans les messages sortants.</span><span class="sxs-lookup"><span data-stu-id="5e79c-118">Describes client application responsibilities for supporting formatted text in outgoing messages.</span></span>
    
[<span data-ttu-id="5e79c-119">Prise en charge du texte mis en forme dans les messages entrants : responsabilités du client</span><span class="sxs-lookup"><span data-stu-id="5e79c-119">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> <span data-ttu-id="5e79c-120">Décrit les responsabilités du client application pour prendre en charge le texte mis en forme dans les messages entrants.</span><span class="sxs-lookup"><span data-stu-id="5e79c-120">Describes client application responsibilities for supporting formatted text in incoming messages.</span></span>
    
[<span data-ttu-id="5e79c-121">Prise en charge du texte mis en forme : responsabilités de la banque de messages</span><span class="sxs-lookup"><span data-stu-id="5e79c-121">Supporting Formatted Text: Message Store Responsibilities</span></span>](supporting-formatted-text-message-store-responsibilities.md)
  
> <span data-ttu-id="5e79c-122">Décrit les responsabilités du magasin de message pour prendre en charge le texte mis en forme.</span><span class="sxs-lookup"><span data-stu-id="5e79c-122">Describes message store responsibilities for supporting formatted text.</span></span>
    
[<span data-ttu-id="5e79c-123">Prise en charge du texte mis en forme : rendu des pièces jointes</span><span class="sxs-lookup"><span data-stu-id="5e79c-123">Supporting Formatted Text: Rendering Attachments</span></span>](supporting-formatted-text-rendering-attachments.md)
  
> <span data-ttu-id="5e79c-124">Décrit comment choisir où les pièces jointes sont rendus.</span><span class="sxs-lookup"><span data-stu-id="5e79c-124">Describes how to choose where attachments are rendered.</span></span>
    
[<span data-ttu-id="5e79c-125">Prise en charge du texte mis en forme : responsabilités de passerelle</span><span class="sxs-lookup"><span data-stu-id="5e79c-125">Supporting Formatted Text: Gateway Responsibilities</span></span>](supporting-formatted-text-gateway-responsibilities.md)
  
> <span data-ttu-id="5e79c-126">Décrit les responsabilités de passerelle pour les messages texte mis en forme entrants et sortants.</span><span class="sxs-lookup"><span data-stu-id="5e79c-126">Describes the gateway responsibilities for outgoing and incoming formatted text messages.</span></span>
    

