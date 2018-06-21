---
title: Prise en charge de mise en forme le texte dans les responsabilités du Client les Messages entrants
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 863c95856f3198c74bb9d72881154676386f6a9f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/21/2018
ms.locfileid: "19787292"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a><span data-ttu-id="6acdc-103">Prise en charge au format texte dans les Messages entrants : responsabilités du Client</span><span class="sxs-lookup"><span data-stu-id="6acdc-103">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="6acdc-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6acdc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6acdc-105">Les messages sont transférés entre les systèmes de messagerie, le spouleur MAPI permet de garantir que la mise en forme de texte enrichi reste synchronisé avec le texte du message.</span><span class="sxs-lookup"><span data-stu-id="6acdc-105">As messages are transferred between messaging systems, the MAPI spooler makes sure that the rich text formatting remains synchronized with the message text.</span></span> <span data-ttu-id="6acdc-106">Le spouleur MAPI appelle la fonction [RTFSync](rtfsync.md) dans une version encapsulée du message qu’il passe au fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="6acdc-106">The MAPI spooler calls the [RTFSync](rtfsync.md) function from within a wrapped version of the message that it passes to the transport provider.</span></span> <span data-ttu-id="6acdc-107">Le fournisseur de transport enregistre les modifications apportées au message en appelant la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , puis l’achemine vers le nouveau destinataire.</span><span class="sxs-lookup"><span data-stu-id="6acdc-107">The transport provider saves the changes made to the message by calling the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and then routes it to the new recipient.</span></span> 
  
<span data-ttu-id="6acdc-108">Lors de l’application cliente prenant en charge les RTF du destinataire ouvre le message pour afficher le texte, il doit synchroniser le texte avec la mise en forme et ouvrez **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) , en fonction de la propriété qui est disponible.</span><span class="sxs-lookup"><span data-stu-id="6acdc-108">When the recipient's RTF-aware client application opens the message to display the text, it must synchronize the text with the formatting and open either **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), depending on which property is available.</span></span>
  
 <span data-ttu-id="6acdc-109">**Pour ouvrir un message, les clients prenant en charge au format RTF**</span><span class="sxs-lookup"><span data-stu-id="6acdc-109">**To open a message, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="6acdc-110">Appelez **RTFSync** pour synchroniser le texte du message avec la mise en forme si la banque de messages n’est pas en charge au format RTF.</span><span class="sxs-lookup"><span data-stu-id="6acdc-110">Call **RTFSync** to synchronize the message text with the formatting if the message store is not RTF-aware.</span></span> <span data-ttu-id="6acdc-111">L’indicateur RTF_SYNC_BODY_CHANGED doit être passé dans le paramètre _ulFlags_ si la propriété **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) est manquante ou la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="6acdc-111">The RTF_SYNC_BODY_CHANGED flag should be passed in the  _ulFlags_ parameter if the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or set to FALSE.</span></span> <span data-ttu-id="6acdc-112">Utilisation des banques de messages RTF prenant en charge les clients ne doivent pas d’appeler le **RTFSync** car la banque de messages prend en charge de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="6acdc-112">Clients working with RTF-aware message stores need not make the **RTFSync** call because the message store takes care of it.</span></span> 
    
2. <span data-ttu-id="6acdc-113">Appeler [IMAPIProp::SaveChanges](imapiprop-savechanges.md) si le texte du message a été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="6acdc-113">Call [IMAPIProp::SaveChanges](imapiprop-savechanges.md) if the message text has been updated.</span></span> 
    
3. <span data-ttu-id="6acdc-114">Appelez [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="6acdc-114">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="6acdc-115">Si **PR_RTF_COMPRESSED** n’est pas disponible, vous devez ouvrir la propriété **PR_BODY** à la place pour afficher le contenu du message.</span><span class="sxs-lookup"><span data-stu-id="6acdc-115">If **PR_RTF_COMPRESSED** is not available, you should open the **PR_BODY** property instead to display the message content.</span></span> 
    
4. <span data-ttu-id="6acdc-116">Appelez la fonction [WrapCompressedRTFStream](wrapcompressedrtfstream.md) pour créer une version non compressée des données au format RTF compressées, si elle est disponible.</span><span class="sxs-lookup"><span data-stu-id="6acdc-116">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function to create an uncompressed version of the compressed RTF data, if available.</span></span> 
    
5. <span data-ttu-id="6acdc-117">Afficher les données de texte brut ou des données au format RTF décompressées à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6acdc-117">Display the uncompressed RTF data or the plain text data to the user.</span></span>
    
 <span data-ttu-id="6acdc-118">**RTFSync** renvoie une valeur de type Boolean qui indique si le message a été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="6acdc-118">**RTFSync** returns a Boolean value that indicates whether or not the message has been updated.</span></span> <span data-ttu-id="6acdc-119">Si cette valeur renvoie la valeur TRUE, appelez **SaveChanges** à un moment donné pour conserver la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="6acdc-119">If this value returns TRUE, call **SaveChanges** at some point to make the update permanent.</span></span> <span data-ttu-id="6acdc-120">L’appel n’a pas immédiatement après que renvoie **RTFSync** .</span><span class="sxs-lookup"><span data-stu-id="6acdc-120">The call does not have to be made immediately after **RTFSync** returns.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6acdc-121">Car c’est le cas de nombreux composants gèrent le texte mis en forme avant sa réception, il est possible de corruption.</span><span class="sxs-lookup"><span data-stu-id="6acdc-121">Because so many components handle the formatted text before you receive it, there is the possibility of corruption.</span></span> <span data-ttu-id="6acdc-122">Cela peut provenir le fournisseur de banque de messages, une application tierce, une passerelle ou une erreur de transmission.</span><span class="sxs-lookup"><span data-stu-id="6acdc-122">This corruption could come from the message store provider, a third party application, a gateway, or a transmission error.</span></span> 
  

