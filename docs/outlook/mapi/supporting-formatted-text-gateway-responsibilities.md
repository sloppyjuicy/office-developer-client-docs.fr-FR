---
title: Prise en charge des responsabilités de passerelle de texte mis en forme
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 6d2c85aa76a372ba79e55dbf5b22024288214df6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787286"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a><span data-ttu-id="c53ca-103">Prenant en charge le format texte : Responsabilités de passerelle</span><span class="sxs-lookup"><span data-stu-id="c53ca-103">Supporting Formatted Text: Gateway Responsibilities</span></span>

  
  
<span data-ttu-id="c53ca-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c53ca-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="c53ca-105">**Pour gérer le Format RTF pour les messages sortants, passerelles**</span><span class="sxs-lookup"><span data-stu-id="c53ca-105">**To handle Rich Text Format for outgoing messages, gateways**</span></span>
  
1. <span data-ttu-id="c53ca-106">Récupérer uniquement les propriétés d’un message **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) à partir de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="c53ca-106">Retrieve only a message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property from the message store.</span></span> <span data-ttu-id="c53ca-107">Le principal avantage de la récupération uniquement la propriété **PR_RTF_COMPRESSED** est que le texte du message n’a pas besoin d’être envoyés entre les ordinateurs si la passerelle et la banque de messages existent sur des ordinateurs différents.</span><span class="sxs-lookup"><span data-stu-id="c53ca-107">The main advantage in retrieving only the **PR_RTF_COMPRESSED** property is that the message text does not need to be sent between machines if the gateway and the message store exist on different machines.</span></span> 
    
2. <span data-ttu-id="c53ca-108">Générer le texte du message à partir du texte mis en forme en appelant la fonction de bibliothèque RTF **HrTextFromCompressedRTFStream** ou, si le message est stocké localement, **RTFSync**.</span><span class="sxs-lookup"><span data-stu-id="c53ca-108">Generate the message text from the formatted text either by calling the RTF library function **HrTextFromCompressedRTFStream** or, if the message is stored locally, **RTFSync**.</span></span> <span data-ttu-id="c53ca-109">L’indicateur RTF_SYNC_RTF_CHANGED doit être défini dans l’appel à **RTFSync**.</span><span class="sxs-lookup"><span data-stu-id="c53ca-109">The RTF_SYNC_RTF_CHANGED flag should be set in the call to **RTFSync**.</span></span> <span data-ttu-id="c53ca-110">Pour plus d’informations, voir [RTFSync](rtfsync.md).</span><span class="sxs-lookup"><span data-stu-id="c53ca-110">For more information, see [RTFSync](rtfsync.md).</span></span>
    
3. <span data-ttu-id="c53ca-111">Apporter des modifications irréversibles au texte du message, telles que la suppression des caractères non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c53ca-111">Make any irreversible modifications to the message text, such as dropping unsupported characters.</span></span> 
    
4. <span data-ttu-id="c53ca-112">Assurez-vous que **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) et toutes les propriétés auxiliaire RTF sont configurés ou absent.</span><span class="sxs-lookup"><span data-stu-id="c53ca-112">Ensure that both **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) and all of the RTF auxilliary properties are either set or absent.</span></span>
    
5. <span data-ttu-id="c53ca-113">Si des modifications ont été apportées, appelez **RTFSync** avec la RTF_SYNC_RTF_CHANGED et RTF_SYNC_BODY_CHANGED flags définie.</span><span class="sxs-lookup"><span data-stu-id="c53ca-113">If any modifications were made, call **RTFSync** with both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags set.</span></span> <span data-ttu-id="c53ca-114">**RTFSync** recalcule les propriétés d’auxiliaire RTF à partir du texte modifié.</span><span class="sxs-lookup"><span data-stu-id="c53ca-114">**RTFSync** will recalculate the RTF auxilliary properties from the modified text.</span></span> 
    
6. <span data-ttu-id="c53ca-115">Apporter des modifications réversible au texte du message, telles que l’insertion des espaces réservés de la pièce jointe et effectue les conversions de page de code non destructifs.</span><span class="sxs-lookup"><span data-stu-id="c53ca-115">Make any reversable modifications to the message text, such as inserting attachment placeholders and performing nondestructive code page conversions.</span></span>
    
7. <span data-ttu-id="c53ca-116">Envoyer le message.</span><span class="sxs-lookup"><span data-stu-id="c53ca-116">Send the message.</span></span>
    
 <span data-ttu-id="c53ca-117">**Pour gérer le Format RTF pour les messages entrants, passerelles**</span><span class="sxs-lookup"><span data-stu-id="c53ca-117">**To handle Rich Text Format for incoming messages, gateways**</span></span>
  
1. <span data-ttu-id="c53ca-118">Annuler les modifications de texte de message qui ont été apportées directement avant que le message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="c53ca-118">Reverse any message text modifications that were made directly before the message was sent.</span></span> 
    
2. <span data-ttu-id="c53ca-119">Appeler **RTFSync** si le message contient les propriétés de **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) et **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="c53ca-119">Call **RTFSync** if the message contains both the **PR_RTF_COMPRESSED** and **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) properties.</span></span> 
    
3. <span data-ttu-id="c53ca-120">Mettre à jour le message dans la banque de messages avec la propriété **PR_RTF_COMPRESSED** si le message contient mettre à jour avec la propriété **PR_BODY** uniquement si **PR_RTF_COMPRESSED** est absente.</span><span class="sxs-lookup"><span data-stu-id="c53ca-120">Update the message in the message store with the **PR_RTF_COMPRESSED** property if the message contains it; update with the **PR_BODY** property only if **PR_RTF_COMPRESSED** is absent.</span></span> 
    
4. <span data-ttu-id="c53ca-121">Ignorer les **PR_BODY** si le message contient cette propriété et la **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="c53ca-121">Discard **PR_BODY** if the message contains both this property and **PR_RTF_COMPRESSED**.</span></span>
    
<span data-ttu-id="c53ca-122">Passerelles appellent **RTFSync** pour éviter de transmettre le texte du message et le texte mis en forme si la banque de messages est sur un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c53ca-122">Gateways call **RTFSync** to avoid transmitting both the message text and formatted text if the message store is on a different machine.</span></span> <span data-ttu-id="c53ca-123">Si la passerelle est locale, il peut définir les propriétés et autoriser la banque de messages effectuer la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="c53ca-123">If the gateway is local, it can set both properties and allow the message store to perform the synchronization.</span></span> 
  

