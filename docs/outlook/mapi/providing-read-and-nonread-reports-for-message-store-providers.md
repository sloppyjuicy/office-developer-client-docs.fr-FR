---
title: Fourniture de rapports en lecture et non lus pour les fournisseurs de magasins de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 96546d3d766af398ff7acb50f4fc3a479b5668b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432337"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a><span data-ttu-id="b096b-103">Fourniture de rapports en lecture et non lus pour les fournisseurs de magasins de messages</span><span class="sxs-lookup"><span data-stu-id="b096b-103">Providing Read and Nonread Reports for Message Store Providers</span></span>

  
  
<span data-ttu-id="b096b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b096b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b096b-105">Si un fournisseur de magasins de messages peut recevoir des messages, il est nécessaire de prendre en charge les rapports de lecture et les rapports non lus des messages reçus par le fournisseur de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="b096b-105">If a message store provider can receive messages, it is required to support read reports and nonread reports of messages received by the message store provider.</span></span> <span data-ttu-id="b096b-106">Si un message reçu contient la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) et que la valeur de cette propriété est TRUE, la boutique de messages doit envoyer un message de notification à l’expéditeur lorsque l’utilisateur ouvre le message, indiquant que le message a été lu.</span><span class="sxs-lookup"><span data-stu-id="b096b-106">If a received message contains the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property and that property's value is TRUE, the message store should send a notification message to the sender when the user opens the message, indicating that the message has been read.</span></span> <span data-ttu-id="b096b-107">De même, si l’utilisateur supprime le message avant de l’ouvrir, la boutique de messages doit envoyer une réponse à l’expéditeur indiquant que le message n’a pas été lu.</span><span class="sxs-lookup"><span data-stu-id="b096b-107">Similarly, if the user deletes the message before opening it, the message store should issue a reply to the sender indicating that the message was not read.</span></span>
  
<span data-ttu-id="b096b-108">L’émission de ces rapports consiste à créer un objet [IMessage : IMAPIProp,](imessageimapiprop.md) à remplir les propriétés pertinentes du message et à l’envoyer aupooler MAPI comme si le message provenait de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b096b-108">Issuing these reports is a matter of creating an [IMessage : IMAPIProp](imessageimapiprop.md) object, filling out the relevant properties on the message, and submitting it to the MAPI spooler as if the message had originated with the user.</span></span> <span data-ttu-id="b096b-109">La [méthode IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) peut être utilisée pour cela.</span><span class="sxs-lookup"><span data-stu-id="b096b-109">The [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) method can be used for this.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b096b-110">Une attention particulière doit être prise lorsqu’une magasin de messages effectue des copies d’un message non lu avec des rapports en attente de lecture ou non lus.</span><span class="sxs-lookup"><span data-stu-id="b096b-110">Special care must be taken when a message store makes copies of an unread message with pending read or nonread reports.</span></span> <span data-ttu-id="b096b-111">Ces rapports ne doivent pas être générés lorsque les utilisateurs lisent des copies d’un message pour lequel des rapports ont été demandés.</span><span class="sxs-lookup"><span data-stu-id="b096b-111">Such reports should not be generated when users read any copies of a message for which reports have been requested.</span></span> <span data-ttu-id="b096b-112">Lors de la copie d’un tel message, le fournisseur de magasin de messages doit inclure les indicateurs CLEAR_RN_PENDING et CLEAR_NRN_PENDING dans ses appels à [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) et [IMessage::SetReadFlag](imessage-setreadflag.md).</span><span class="sxs-lookup"><span data-stu-id="b096b-112">When making a copy of such a message, the message store provider should include the CLEAR_RN_PENDING and CLEAR_NRN_PENDING flags in its calls to [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) and [IMessage::SetReadFlag](imessage-setreadflag.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b096b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b096b-113">See also</span></span>



[<span data-ttu-id="b096b-114">Fonctionnalit�s de la banque de messages</span><span class="sxs-lookup"><span data-stu-id="b096b-114">Message Store Features</span></span>](message-store-features.md)

