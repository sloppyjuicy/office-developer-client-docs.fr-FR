---
title: Prise en charge des responsabilités de la passerelle de texte mise en forme
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d5c3480018be399a85ee0bfda7ce1ff9b701cecc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419428"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a><span data-ttu-id="fbcbe-103">Prise en charge du texte formaté : responsabilités de la passerelle</span><span class="sxs-lookup"><span data-stu-id="fbcbe-103">Supporting Formatted Text: Gateway Responsibilities</span></span>

  
  
<span data-ttu-id="fbcbe-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fbcbe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="fbcbe-105">**Pour gérer le format texte enrichi pour les messages sortants, passerelles**</span><span class="sxs-lookup"><span data-stu-id="fbcbe-105">**To handle Rich Text Format for outgoing messages, gateways**</span></span>
  
1. <span data-ttu-id="fbcbe-106">Récupérez uniquement la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) d’un message à partir de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="fbcbe-106">Retrieve only a message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property from the message store.</span></span> <span data-ttu-id="fbcbe-107">Le principal avantage de la récupération de la propriété PR_RTF_COMPRESSED est que le texte du message **n’a** pas besoin d’être envoyé entre les ordinateurs si la passerelle et la boutique de messages existent sur différents ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="fbcbe-107">The main advantage in retrieving only the **PR_RTF_COMPRESSED** property is that the message text does not need to be sent between machines if the gateway and the message store exist on different machines.</span></span> 
    
2. <span data-ttu-id="fbcbe-108">Générez le texte du message à partir du texte mis en forme en appelant la fonction de bibliothèque RTF **HrTextFromCompressedRTFStream** ou, si le message est stocké localement, **RTFSync**.</span><span class="sxs-lookup"><span data-stu-id="fbcbe-108">Generate the message text from the formatted text either by calling the RTF library function **HrTextFromCompressedRTFStream** or, if the message is stored locally, **RTFSync**.</span></span> <span data-ttu-id="fbcbe-109">L’RTF_SYNC_RTF_CHANGED doit être définie dans l’appel à **RTFSync**.</span><span class="sxs-lookup"><span data-stu-id="fbcbe-109">The RTF_SYNC_RTF_CHANGED flag should be set in the call to **RTFSync**.</span></span> <span data-ttu-id="fbcbe-110">Pour plus d’informations, [voir RTFSync](rtfsync.md).</span><span class="sxs-lookup"><span data-stu-id="fbcbe-110">For more information, see [RTFSync](rtfsync.md).</span></span>
    
3. <span data-ttu-id="fbcbe-111">Apporter des modifications irréversibles au texte du message, telles que le fait de laisser des caractères non pris en place.</span><span class="sxs-lookup"><span data-stu-id="fbcbe-111">Make any irreversible modifications to the message text, such as dropping unsupported characters.</span></span> 
    
4. <span data-ttu-id="fbcbe-112">Assurez-vous **que PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) et toutes les propriétés auxilliary RTF sont définies ou absentes.</span><span class="sxs-lookup"><span data-stu-id="fbcbe-112">Ensure that both **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) and all of the RTF auxilliary properties are either set or absent.</span></span>
    
5. <span data-ttu-id="fbcbe-113">Si des modifications ont été apportées, appelez **RTFSync** avec les indicateurs RTF_SYNC_RTF_CHANGED et RTF_SYNC_BODY_CHANGED définies.</span><span class="sxs-lookup"><span data-stu-id="fbcbe-113">If any modifications were made, call **RTFSync** with both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags set.</span></span> <span data-ttu-id="fbcbe-114">**RTFSync** recalcule les propriétés auxilliary RTF à partir du texte modifié.</span><span class="sxs-lookup"><span data-stu-id="fbcbe-114">**RTFSync** will recalculate the RTF auxilliary properties from the modified text.</span></span> 
    
6. <span data-ttu-id="fbcbe-115">A effectuez des modifications inversables dans le texte du message, telles que l’insertion d’espaces réservé de pièce jointe et la conversion de page de code nondestructive.</span><span class="sxs-lookup"><span data-stu-id="fbcbe-115">Make any reversable modifications to the message text, such as inserting attachment placeholders and performing nondestructive code page conversions.</span></span>
    
7. <span data-ttu-id="fbcbe-116">Envoyez le message.</span><span class="sxs-lookup"><span data-stu-id="fbcbe-116">Send the message.</span></span>
    
 <span data-ttu-id="fbcbe-117">**Pour gérer le format texte enrichi pour les messages entrants, passerelles**</span><span class="sxs-lookup"><span data-stu-id="fbcbe-117">**To handle Rich Text Format for incoming messages, gateways**</span></span>
  
1. <span data-ttu-id="fbcbe-118">Annuler toutes les modifications de texte de message effectuées directement avant l’envoi du message.</span><span class="sxs-lookup"><span data-stu-id="fbcbe-118">Reverse any message text modifications that were made directly before the message was sent.</span></span> 
    
2. <span data-ttu-id="fbcbe-119">Appelez **RTFSync** si le message contient les propriétés **PR_RTF_COMPRESSED** et **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fbcbe-119">Call **RTFSync** if the message contains both the **PR_RTF_COMPRESSED** and **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) properties.</span></span> 
    
3. <span data-ttu-id="fbcbe-120">Mettez à jour le message dans la magasin de messages avec **la propriété PR_RTF_COMPRESSED** si le message le contient ; mise à jour avec **la propriété PR_BODY** uniquement si **PR_RTF_COMPRESSED** est absent.</span><span class="sxs-lookup"><span data-stu-id="fbcbe-120">Update the message in the message store with the **PR_RTF_COMPRESSED** property if the message contains it; update with the **PR_BODY** property only if **PR_RTF_COMPRESSED** is absent.</span></span> 
    
4. <span data-ttu-id="fbcbe-121">Ignorer **PR_BODY** si le message contient à la fois cette propriété et **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="fbcbe-121">Discard **PR_BODY** if the message contains both this property and **PR_RTF_COMPRESSED**.</span></span>
    
<span data-ttu-id="fbcbe-122">Les passerelles **appellent RTFSync** pour éviter de transmettre à la fois le texte du message et le texte formaté si la boutique de messages se trouve sur un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fbcbe-122">Gateways call **RTFSync** to avoid transmitting both the message text and formatted text if the message store is on a different machine.</span></span> <span data-ttu-id="fbcbe-123">Si la passerelle est locale, elle peut définir les deux propriétés et autoriser la boutique de messages à effectuer la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="fbcbe-123">If the gateway is local, it can set both properties and allow the message store to perform the synchronization.</span></span> 
  

