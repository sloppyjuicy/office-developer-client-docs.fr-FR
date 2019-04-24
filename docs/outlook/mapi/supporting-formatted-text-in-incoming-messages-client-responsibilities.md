---
title: Prise en charge du texte mis en forme dans les messages entrants responsabilités du client
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 7f3cf5b245bdcd2c2707f0e2028d52a15c7e0f6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327411"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a><span data-ttu-id="9cf62-103">Prise en charge du texte mis en forme dans les messages entrants: responsabilités du client</span><span class="sxs-lookup"><span data-stu-id="9cf62-103">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="9cf62-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9cf62-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9cf62-105">Lorsque les messages sont transférés entre les systèmes de messagerie, le spouleur MAPI garantit que la mise en forme de texte enrichi reste synchronisée avec le texte du message.</span><span class="sxs-lookup"><span data-stu-id="9cf62-105">As messages are transferred between messaging systems, the MAPI spooler makes sure that the rich text formatting remains synchronized with the message text.</span></span> <span data-ttu-id="9cf62-106">Le spouleur MAPI appelle la fonction [RTFSync](rtfsync.md) à partir d'une version encapsulée du message qu'il transmet au fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="9cf62-106">The MAPI spooler calls the [RTFSync](rtfsync.md) function from within a wrapped version of the message that it passes to the transport provider.</span></span> <span data-ttu-id="9cf62-107">Le fournisseur de transport enregistre les modifications apportées au message en appelant la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) , puis l'achemine vers le nouveau destinataire.</span><span class="sxs-lookup"><span data-stu-id="9cf62-107">The transport provider saves the changes made to the message by calling the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and then routes it to the new recipient.</span></span> 
  
<span data-ttu-id="9cf62-108">Lorsque l'application cliente compatible RTF du destinataire ouvre le message pour afficher le texte, elle doit synchroniser le texte avec la mise en forme et ouvrir **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) , en fonction de la disponibilité de la propriété.</span><span class="sxs-lookup"><span data-stu-id="9cf62-108">When the recipient's RTF-aware client application opens the message to display the text, it must synchronize the text with the formatting and open either **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), depending on which property is available.</span></span>
  
 <span data-ttu-id="9cf62-109">**Pour ouvrir un message, les clients compatibles RTF**</span><span class="sxs-lookup"><span data-stu-id="9cf62-109">**To open a message, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="9cf62-110">Appelez **RTFSync** pour synchroniser le texte du message avec la mise en forme si la Banque de messages n'est pas compatible avec le format RTF.</span><span class="sxs-lookup"><span data-stu-id="9cf62-110">Call **RTFSync** to synchronize the message text with the formatting if the message store is not RTF-aware.</span></span> <span data-ttu-id="9cf62-111">L'indicateur RTF_SYNC_BODY_CHANGED doit être passé dans le paramètre _ulFlags_ si la propriété **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) est MANQUante ou a la valeur false.</span><span class="sxs-lookup"><span data-stu-id="9cf62-111">The RTF_SYNC_BODY_CHANGED flag should be passed in the  _ulFlags_ parameter if the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or set to FALSE.</span></span> <span data-ttu-id="9cf62-112">Les clients qui travaillent avec des banques de messages compatibles RTF n'ont pas besoin d'effectuer l'appel **RTFSync** , car la Banque de messages s'en charge.</span><span class="sxs-lookup"><span data-stu-id="9cf62-112">Clients working with RTF-aware message stores need not make the **RTFSync** call because the message store takes care of it.</span></span> 
    
2. <span data-ttu-id="9cf62-113">Appelez [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) si le texte du message a été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="9cf62-113">Call [IMAPIProp::SaveChanges](imapiprop-savechanges.md) if the message text has been updated.</span></span> 
    
3. <span data-ttu-id="9cf62-114">Appelez [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="9cf62-114">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="9cf62-115">Si **PR_RTF_COMPRESSED** n'est pas disponible, vous devez ouvrir la propriété **PR_BODY** à la place pour afficher le contenu du message.</span><span class="sxs-lookup"><span data-stu-id="9cf62-115">If **PR_RTF_COMPRESSED** is not available, you should open the **PR_BODY** property instead to display the message content.</span></span> 
    
4. <span data-ttu-id="9cf62-116">Appelez la fonction [WrapCompressedRTFStream](wrapcompressedrtfstream.md) pour créer une version non compressée des données RTF compressées, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="9cf62-116">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function to create an uncompressed version of the compressed RTF data, if available.</span></span> 
    
5. <span data-ttu-id="9cf62-117">Afficher les données RTF non compressées ou les données en texte brut à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9cf62-117">Display the uncompressed RTF data or the plain text data to the user.</span></span>
    
 <span data-ttu-id="9cf62-118">**RTFSync** renvoie une valeur de type Boolean qui indique si le message a été mis à jour ou non.</span><span class="sxs-lookup"><span data-stu-id="9cf62-118">**RTFSync** returns a Boolean value that indicates whether or not the message has been updated.</span></span> <span data-ttu-id="9cf62-119">Si cette valeur retourne la valeur TRUE, appelez **SaveChanges** à un moment donné pour faire en sorte que la mise à jour soit définitive.</span><span class="sxs-lookup"><span data-stu-id="9cf62-119">If this value returns TRUE, call **SaveChanges** at some point to make the update permanent.</span></span> <span data-ttu-id="9cf62-120">L'appel ne doit pas être effectué immédiatement après le retour de **RTFSync** .</span><span class="sxs-lookup"><span data-stu-id="9cf62-120">The call does not have to be made immediately after **RTFSync** returns.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9cf62-121">Étant donné que de nombreux composants gèrent le texte mis en forme avant que vous ne le receviez, il existe un risque d'endommagement.</span><span class="sxs-lookup"><span data-stu-id="9cf62-121">Because so many components handle the formatted text before you receive it, there is the possibility of corruption.</span></span> <span data-ttu-id="9cf62-122">Cette altération peut provenir du fournisseur de banque de messages, d'une application tierce, d'une passerelle ou d'une erreur de transmission.</span><span class="sxs-lookup"><span data-stu-id="9cf62-122">This corruption could come from the message store provider, a third party application, a gateway, or a transmission error.</span></span> 
  

