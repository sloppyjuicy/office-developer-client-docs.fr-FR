---
title: Prise en charge de mise en forme le texte dans les responsabilités du Client les Messages entrants
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d8fdd9ea4dfbc40d7e800be5e2df666738d2cd23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577456"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a><span data-ttu-id="ebee3-103">Prise en charge du texte mis en forme dans les messages entrants : responsabilités du client</span><span class="sxs-lookup"><span data-stu-id="ebee3-103">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="ebee3-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebee3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebee3-105">Les messages sont transférés entre les systèmes de messagerie, le spouleur MAPI permet de garantir que la mise en forme de texte enrichi reste synchronisé avec le texte du message.</span><span class="sxs-lookup"><span data-stu-id="ebee3-105">As messages are transferred between messaging systems, the MAPI spooler makes sure that the rich text formatting remains synchronized with the message text.</span></span> <span data-ttu-id="ebee3-106">Le spouleur MAPI appelle la fonction [RTFSync](rtfsync.md) dans une version encapsulée du message qu’il passe au fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="ebee3-106">The MAPI spooler calls the [RTFSync](rtfsync.md) function from within a wrapped version of the message that it passes to the transport provider.</span></span> <span data-ttu-id="ebee3-107">Le fournisseur de transport enregistre les modifications apportées au message en appelant la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , puis l’achemine vers le nouveau destinataire.</span><span class="sxs-lookup"><span data-stu-id="ebee3-107">The transport provider saves the changes made to the message by calling the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and then routes it to the new recipient.</span></span> 
  
<span data-ttu-id="ebee3-108">Lors de l’application cliente prenant en charge les RTF du destinataire ouvre le message pour afficher le texte, il doit synchroniser le texte avec la mise en forme et ouvrez **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) , en fonction de la propriété qui est disponible.</span><span class="sxs-lookup"><span data-stu-id="ebee3-108">When the recipient's RTF-aware client application opens the message to display the text, it must synchronize the text with the formatting and open either **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), depending on which property is available.</span></span>
  
 <span data-ttu-id="ebee3-109">**Pour ouvrir un message, les clients prenant en charge au format RTF**</span><span class="sxs-lookup"><span data-stu-id="ebee3-109">**To open a message, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="ebee3-110">Appelez **RTFSync** pour synchroniser le texte du message avec la mise en forme si la banque de messages n’est pas en charge au format RTF.</span><span class="sxs-lookup"><span data-stu-id="ebee3-110">Call **RTFSync** to synchronize the message text with the formatting if the message store is not RTF-aware.</span></span> <span data-ttu-id="ebee3-111">L’indicateur RTF_SYNC_BODY_CHANGED doit être passé dans le paramètre _ulFlags_ si la propriété **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) est manquante ou la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="ebee3-111">The RTF_SYNC_BODY_CHANGED flag should be passed in the  _ulFlags_ parameter if the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or set to FALSE.</span></span> <span data-ttu-id="ebee3-112">Utilisation des banques de messages RTF prenant en charge les clients ne doivent pas d’appeler le **RTFSync** car la banque de messages prend en charge de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="ebee3-112">Clients working with RTF-aware message stores need not make the **RTFSync** call because the message store takes care of it.</span></span> 
    
2. <span data-ttu-id="ebee3-113">Appeler [IMAPIProp::SaveChanges](imapiprop-savechanges.md) si le texte du message a été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="ebee3-113">Call [IMAPIProp::SaveChanges](imapiprop-savechanges.md) if the message text has been updated.</span></span> 
    
3. <span data-ttu-id="ebee3-114">Appelez [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="ebee3-114">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="ebee3-115">Si **PR_RTF_COMPRESSED** n’est pas disponible, vous devez ouvrir la propriété **PR_BODY** à la place pour afficher le contenu du message.</span><span class="sxs-lookup"><span data-stu-id="ebee3-115">If **PR_RTF_COMPRESSED** is not available, you should open the **PR_BODY** property instead to display the message content.</span></span> 
    
4. <span data-ttu-id="ebee3-116">Appelez la fonction [WrapCompressedRTFStream](wrapcompressedrtfstream.md) pour créer une version non compressée des données au format RTF compressées, si elle est disponible.</span><span class="sxs-lookup"><span data-stu-id="ebee3-116">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function to create an uncompressed version of the compressed RTF data, if available.</span></span> 
    
5. <span data-ttu-id="ebee3-117">Afficher les données de texte brut ou des données au format RTF décompressées à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ebee3-117">Display the uncompressed RTF data or the plain text data to the user.</span></span>
    
 <span data-ttu-id="ebee3-118">**RTFSync** renvoie une valeur de type Boolean qui indique si le message a été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="ebee3-118">**RTFSync** returns a Boolean value that indicates whether or not the message has been updated.</span></span> <span data-ttu-id="ebee3-119">Si cette valeur renvoie la valeur TRUE, appelez **SaveChanges** à un moment donné pour conserver la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="ebee3-119">If this value returns TRUE, call **SaveChanges** at some point to make the update permanent.</span></span> <span data-ttu-id="ebee3-120">L’appel n’a pas immédiatement après que renvoie **RTFSync** .</span><span class="sxs-lookup"><span data-stu-id="ebee3-120">The call does not have to be made immediately after **RTFSync** returns.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ebee3-121">Car c’est le cas de nombreux composants gèrent le texte mis en forme avant sa réception, il est possible de corruption.</span><span class="sxs-lookup"><span data-stu-id="ebee3-121">Because so many components handle the formatted text before you receive it, there is the possibility of corruption.</span></span> <span data-ttu-id="ebee3-122">Cela peut provenir le fournisseur de banque de messages, une application tierce, une passerelle ou une erreur de transmission.</span><span class="sxs-lookup"><span data-stu-id="ebee3-122">This corruption could come from the message store provider, a third party application, a gateway, or a transmission error.</span></span> 
  

