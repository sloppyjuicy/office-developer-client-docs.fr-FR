---
title: Fourniture de rapports lus et non lus pour les fournisseurs de banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8e2552cbeaf528de634c39a5ebd175a2615782b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594438"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a><span data-ttu-id="06acb-103">Fourniture de rapports lus et non lus pour les fournisseurs de banques de messages</span><span class="sxs-lookup"><span data-stu-id="06acb-103">Providing Read and Nonread Reports for Message Store Providers</span></span>

  
  
<span data-ttu-id="06acb-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06acb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06acb-105">Si un fournisseur de magasin de message peut recevoir des messages, il est requis pour prendre en charge la lecture des rapports et nonread de messages reçus par le fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="06acb-105">If a message store provider can receive messages, it is required to support read reports and nonread reports of messages received by the message store provider.</span></span> <span data-ttu-id="06acb-106">Si un message reçu contient la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) et la valeur de cette propriété a la valeur TRUE, la banque de messages doit envoyer un message de notification à l’expéditeur lorsque l’utilisateur ouvre le message, indiquant que le message a été lu.</span><span class="sxs-lookup"><span data-stu-id="06acb-106">If a received message contains the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property and that property's value is TRUE, the message store should send a notification message to the sender when the user opens the message, indicating that the message has been read.</span></span> <span data-ttu-id="06acb-107">De même, si l’utilisateur supprime le message avant de l’ouvrir, la banque de messages doit émettre une réponse à l’expéditeur indiquant que le message n’a pas été lu.</span><span class="sxs-lookup"><span data-stu-id="06acb-107">Similarly, if the user deletes the message before opening it, the message store should issue a reply to the sender indicating that the message was not read.</span></span>
  
<span data-ttu-id="06acb-108">Émission de ces rapports est une question de la création d’un [IMessage : IMAPIProp](imessageimapiprop.md) objet, remplissez les propriétés pertinentes sur le message et l’envoi au spouleur MAPI comme si le message avait à l’origine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="06acb-108">Issuing these reports is a matter of creating an [IMessage : IMAPIProp](imessageimapiprop.md) object, filling out the relevant properties on the message, and submitting it to the MAPI spooler as if the message had originated with the user.</span></span> <span data-ttu-id="06acb-109">La méthode [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) peut être utilisée pour cela.</span><span class="sxs-lookup"><span data-stu-id="06acb-109">The [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) method can be used for this.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="06acb-110">Une attention particulière doit être prise lors d’une banque de messages effectue des copies d’un message non lu avec en attente de rapports de lecture ou nonread.</span><span class="sxs-lookup"><span data-stu-id="06acb-110">Special care must be taken when a message store makes copies of an unread message with pending read or nonread reports.</span></span> <span data-ttu-id="06acb-111">Ces rapports ne doivent pas être générées lorsque les utilisateurs lire toutes les copies d’un message pour lequel les rapports ont été demandées.</span><span class="sxs-lookup"><span data-stu-id="06acb-111">Such reports should not be generated when users read any copies of a message for which reports have been requested.</span></span> <span data-ttu-id="06acb-112">Lorsque vous effectuez une copie de ce message, le fournisseur de banque de messages doit inclure les indicateurs CLEAR_RN_PENDING et CLEAR_NRN_PENDING dans ses appels [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) et [IMessage::SetReadFlag](imessage-setreadflag.md).</span><span class="sxs-lookup"><span data-stu-id="06acb-112">When making a copy of such a message, the message store provider should include the CLEAR_RN_PENDING and CLEAR_NRN_PENDING flags in its calls to [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) and [IMessage::SetReadFlag](imessage-setreadflag.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="06acb-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06acb-113">See also</span></span>



[<span data-ttu-id="06acb-114">Fonctionnalit�s de la banque de messages</span><span class="sxs-lookup"><span data-stu-id="06acb-114">Message Store Features</span></span>](message-store-features.md)

