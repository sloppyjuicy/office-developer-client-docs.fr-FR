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
ms.openlocfilehash: 7f37d65e4beb328c2c92cf0c2ab28586af6bee45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408088"
---
# <a name="formatted-text-in-mapi"></a><span data-ttu-id="20b0a-103">Texte mis en forme dans MAPI</span><span class="sxs-lookup"><span data-stu-id="20b0a-103">Formatted Text in MAPI</span></span>

  
  
<span data-ttu-id="20b0a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20b0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20b0a-105">Le texte d’un message peut être stocké et transmis à l’aide de texte simple ou de texte formaté.</span><span class="sxs-lookup"><span data-stu-id="20b0a-105">The text of a message can be stored and transmitted using plain text or formatted text.</span></span> <span data-ttu-id="20b0a-106">Le texte formaté améliore le texte du message en modifiant son apparence avec, par exemple, une ou plusieurs polices, tailles de police ou couleurs de texte.</span><span class="sxs-lookup"><span data-stu-id="20b0a-106">Formatted text enhances the message text by altering its appearance with, for example, one or more fonts, font sizes, or text colors.</span></span> <span data-ttu-id="20b0a-107">Il est recommandé que tous les clients et, dans la mesure du possible, tous les fournisseurs de magasins de messages, la prise en charge du texte formaté.</span><span class="sxs-lookup"><span data-stu-id="20b0a-107">It is recommended that all clients and whenever possible, all message store providers, support formatted text.</span></span> <span data-ttu-id="20b0a-108">La prise en charge du texte formaté dans les messages apporte de la valeur ajoutée en améliorant la lisibilité des messages et en rendant la gestion des messages plus facile et plus efficace.</span><span class="sxs-lookup"><span data-stu-id="20b0a-108">Supporting formatted text in messages adds value by improving message readability and making message handling easier and more efficient.</span></span>
  
<span data-ttu-id="20b0a-109">Le texte mis en forme peut être implémenté de différentes manières.</span><span class="sxs-lookup"><span data-stu-id="20b0a-109">Formatted text can be implemented in a variety of ways.</span></span> <span data-ttu-id="20b0a-110">Le moyen le plus courant est le format RTF (Rich Text Format).</span><span class="sxs-lookup"><span data-stu-id="20b0a-110">The most common way is with the Rich Text Format (RTF).</span></span> <span data-ttu-id="20b0a-111">MAPI définit trois propriétés transmises pour la tenue des informations sur le texte du message : **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) pour le texte brut, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) pour html et **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) pour le texte RTF qui a été compressé.</span><span class="sxs-lookup"><span data-stu-id="20b0a-111">MAPI defines three transmittable properties for holding message text information: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) for plain text, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) for HTML, and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) for RTF text that has been compressed.</span></span> <span data-ttu-id="20b0a-112">Étant donné que la version mise en forme d’un texte de message peut être deux fois plus grande que la version sans mise en forme, le texte RTF est compressé avant d’être transféré avec le message et stocké dans la propriété **PR_RTF_COMPRESSED.**</span><span class="sxs-lookup"><span data-stu-id="20b0a-112">Because the formatted version of a message text can be twice as large as the version without the formatting, the RTF text is compressed before it is transferred with the message and stored in the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="20b0a-113">Lorsqu’il est temps d’afficher le message à l’écran, il est décompressé à l’aide d’une fonction utilitaire fournie par MAPI.</span><span class="sxs-lookup"><span data-stu-id="20b0a-113">When it is time to display the message on the screen, it is uncompressed using a utility function provided by MAPI.</span></span> 
  
<span data-ttu-id="20b0a-114">MAPI définit ces deux propriétés et mécanismes de conversion de texte de message entre eux afin que les clients sensibles au format RTF peuvent interopérer avec les clients et les systèmes de messagerie qui ne peuvent pas prendre en charge le texte mis en forme.</span><span class="sxs-lookup"><span data-stu-id="20b0a-114">MAPI defines these two message text properties and mechanisms for conversion between them so that RTF-aware clients can interoperate with clients and messaging systems that do not support formatted text.</span></span>
  
### 

[<span data-ttu-id="20b0a-115">Synchronisation du texte et de la mise en forme</span><span class="sxs-lookup"><span data-stu-id="20b0a-115">Synchronizing Text and Formatting</span></span>](synchronizing-text-and-formatting.md)
  
> <span data-ttu-id="20b0a-116">Décrit comment maintenir la synchronisation du texte du message RTF avec la mise en forme.</span><span class="sxs-lookup"><span data-stu-id="20b0a-116">Describes how to keep RTF message text synchronized with the formatting.</span></span>
    
[<span data-ttu-id="20b0a-117">Prise en charge du texte formaté dans les messages sortants : responsabilités du client</span><span class="sxs-lookup"><span data-stu-id="20b0a-117">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> <span data-ttu-id="20b0a-118">Décrit les responsabilités de l’application cliente pour la prise en charge du texte formaté dans les messages sortants.</span><span class="sxs-lookup"><span data-stu-id="20b0a-118">Describes client application responsibilities for supporting formatted text in outgoing messages.</span></span>
    
[<span data-ttu-id="20b0a-119">Prise en charge du texte formaté dans les messages entrants : responsabilités du client</span><span class="sxs-lookup"><span data-stu-id="20b0a-119">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> <span data-ttu-id="20b0a-120">Décrit les responsabilités de l’application cliente pour la prise en charge du texte formaté dans les messages entrants.</span><span class="sxs-lookup"><span data-stu-id="20b0a-120">Describes client application responsibilities for supporting formatted text in incoming messages.</span></span>
    
[<span data-ttu-id="20b0a-121">Prise en charge du texte formaté : responsabilités de la boutique de messages</span><span class="sxs-lookup"><span data-stu-id="20b0a-121">Supporting Formatted Text: Message Store Responsibilities</span></span>](supporting-formatted-text-message-store-responsibilities.md)
  
> <span data-ttu-id="20b0a-122">Décrit les responsabilités de la boutique de messages pour la prise en charge du texte formaté.</span><span class="sxs-lookup"><span data-stu-id="20b0a-122">Describes message store responsibilities for supporting formatted text.</span></span>
    
[<span data-ttu-id="20b0a-123">Prise en charge du texte formaté : rendu des pièces jointes</span><span class="sxs-lookup"><span data-stu-id="20b0a-123">Supporting Formatted Text: Rendering Attachments</span></span>](supporting-formatted-text-rendering-attachments.md)
  
> <span data-ttu-id="20b0a-124">Indique comment choisir l’endroit où les pièces jointes sont rendues.</span><span class="sxs-lookup"><span data-stu-id="20b0a-124">Describes how to choose where attachments are rendered.</span></span>
    
[<span data-ttu-id="20b0a-125">Prise en charge du texte formaté : responsabilités de la passerelle</span><span class="sxs-lookup"><span data-stu-id="20b0a-125">Supporting Formatted Text: Gateway Responsibilities</span></span>](supporting-formatted-text-gateway-responsibilities.md)
  
> <span data-ttu-id="20b0a-126">Décrit les responsabilités de la passerelle pour les messages texte formatés sortants et entrants.</span><span class="sxs-lookup"><span data-stu-id="20b0a-126">Describes the gateway responsibilities for outgoing and incoming formatted text messages.</span></span>
    

