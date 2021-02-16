---
title: Prise en charge du texte formaté dans les responsabilités du client des messages entrants
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7f3cf5b245bdcd2c2707f0e2028d52a15c7e0f6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434500"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a><span data-ttu-id="7ec8c-103">Prise en charge du texte formaté dans les messages entrants : responsabilités du client</span><span class="sxs-lookup"><span data-stu-id="7ec8c-103">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="7ec8c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ec8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ec8c-105">Lorsque les messages sont transférés entre les systèmes de messagerie, lepooler MAPI s’assure que la mise en forme de texte enrichi reste synchronisée avec le texte du message.</span><span class="sxs-lookup"><span data-stu-id="7ec8c-105">As messages are transferred between messaging systems, the MAPI spooler makes sure that the rich text formatting remains synchronized with the message text.</span></span> <span data-ttu-id="7ec8c-106">Lepooler MAPI appelle la [fonction RTFSync](rtfsync.md) à partir d’une version wrapped du message qu’il transmet au fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="7ec8c-106">The MAPI spooler calls the [RTFSync](rtfsync.md) function from within a wrapped version of the message that it passes to the transport provider.</span></span> <span data-ttu-id="7ec8c-107">Le fournisseur de transport enregistre les modifications apportées au message en appelant la méthode [IMAPIProp::SaveChanges,](imapiprop-savechanges.md) puis l’a acheminé vers le nouveau destinataire.</span><span class="sxs-lookup"><span data-stu-id="7ec8c-107">The transport provider saves the changes made to the message by calling the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and then routes it to the new recipient.</span></span> 
  
<span data-ttu-id="7ec8c-108">Lorsque l’application cliente RTF du destinataire ouvre le message pour afficher le texte, elle doit synchroniser le texte avec la mise en forme et ouvrir **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), en fonction de la propriété disponible.</span><span class="sxs-lookup"><span data-stu-id="7ec8c-108">When the recipient's RTF-aware client application opens the message to display the text, it must synchronize the text with the formatting and open either **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), depending on which property is available.</span></span>
  
 <span data-ttu-id="7ec8c-109">**Pour ouvrir un message, clients rtF**</span><span class="sxs-lookup"><span data-stu-id="7ec8c-109">**To open a message, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="7ec8c-110">Appelez **RTFSync pour** synchroniser le texte du message avec la mise en forme si la boutique de messages n’est pas sensible au format RTF.</span><span class="sxs-lookup"><span data-stu-id="7ec8c-110">Call **RTFSync** to synchronize the message text with the formatting if the message store is not RTF-aware.</span></span> <span data-ttu-id="7ec8c-111">L’RTF_SYNC_BODY_CHANGED doit être transmis dans le paramètre  _ulFlags_ si la propriété **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) est manquante ou définie sur FALSE.</span><span class="sxs-lookup"><span data-stu-id="7ec8c-111">The RTF_SYNC_BODY_CHANGED flag should be passed in the  _ulFlags_ parameter if the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or set to FALSE.</span></span> <span data-ttu-id="7ec8c-112">Les clients qui travaillent avec des magasins de messages rtF n’ont pas besoin d’effectuer l’appel **RTFSync,** car la boutique de messages s’en charge.</span><span class="sxs-lookup"><span data-stu-id="7ec8c-112">Clients working with RTF-aware message stores need not make the **RTFSync** call because the message store takes care of it.</span></span> 
    
2. <span data-ttu-id="7ec8c-113">Appelez [IMAPIProp::SaveChanges](imapiprop-savechanges.md) si le texte du message a été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="7ec8c-113">Call [IMAPIProp::SaveChanges](imapiprop-savechanges.md) if the message text has been updated.</span></span> 
    
3. <span data-ttu-id="7ec8c-114">Appelez [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour ouvrir **PR_RTF_COMPRESSED** propriété.</span><span class="sxs-lookup"><span data-stu-id="7ec8c-114">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="7ec8c-115">Si **PR_RTF_COMPRESSED** n’est pas disponible, vous devez ouvrir la **propriété PR_BODY** à la place pour afficher le contenu du message.</span><span class="sxs-lookup"><span data-stu-id="7ec8c-115">If **PR_RTF_COMPRESSED** is not available, you should open the **PR_BODY** property instead to display the message content.</span></span> 
    
4. <span data-ttu-id="7ec8c-116">Appelez la [fonction WrapCompressedRTFStream](wrapcompressedrtfstream.md) pour créer une version non compressée des données RTF compressées, si disponible.</span><span class="sxs-lookup"><span data-stu-id="7ec8c-116">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function to create an uncompressed version of the compressed RTF data, if available.</span></span> 
    
5. <span data-ttu-id="7ec8c-117">Affichez les données RTF non compressées ou les données en texte simple à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7ec8c-117">Display the uncompressed RTF data or the plain text data to the user.</span></span>
    
 <span data-ttu-id="7ec8c-118">**RTFSync renvoie** une valeur boolé américaine qui indique si le message a été mis à jour ou non.</span><span class="sxs-lookup"><span data-stu-id="7ec8c-118">**RTFSync** returns a Boolean value that indicates whether or not the message has been updated.</span></span> <span data-ttu-id="7ec8c-119">Si cette valeur renvoie TRUE, appelez **SaveChanges** à un moment donné pour rendre la mise à jour permanente.</span><span class="sxs-lookup"><span data-stu-id="7ec8c-119">If this value returns TRUE, call **SaveChanges** at some point to make the update permanent.</span></span> <span data-ttu-id="7ec8c-120">L’appel n’a pas besoin d’être effectué immédiatement après le **retour de RTFSync.**</span><span class="sxs-lookup"><span data-stu-id="7ec8c-120">The call does not have to be made immediately after **RTFSync** returns.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7ec8c-121">Étant donné que de nombreux composants gèrent le texte formaté avant de le recevoir, il existe un risque d’altération.</span><span class="sxs-lookup"><span data-stu-id="7ec8c-121">Because so many components handle the formatted text before you receive it, there is the possibility of corruption.</span></span> <span data-ttu-id="7ec8c-122">Cette altération peut être le fait du fournisseur de la boutique de messages, d’une application tierce, d’une passerelle ou d’une erreur de transmission.</span><span class="sxs-lookup"><span data-stu-id="7ec8c-122">This corruption could come from the message store provider, a third party application, a gateway, or a transmission error.</span></span> 
  

