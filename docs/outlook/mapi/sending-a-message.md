---
title: Envoi d’un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 01fd66033da0f24948913f47a752d555eca655fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423621"
---
# <a name="sending-a-message"></a><span data-ttu-id="dc22d-103">Envoi d’un message</span><span class="sxs-lookup"><span data-stu-id="dc22d-103">Sending a Message</span></span>

  
  
<span data-ttu-id="dc22d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc22d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc22d-105">Lorsque vous êtes prêt à envoyer un message, appelez sa méthode [IMessage:: SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="dc22d-105">When you are ready to send a message, call its [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="dc22d-106">**SubmitMessage** place le message dans la file d'attente sortante et définit l'indicateur MSGFLAG_SUBMIT dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message.</span><span class="sxs-lookup"><span data-stu-id="dc22d-106">**SubmitMessage** places the message in the outgoing queue and sets the MSGFLAG_SUBMIT flag in the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="dc22d-107">Le fournisseur de banque de messages, s'il est étroitement couplé à un fournisseur de transport, transmet directement le message au transport qui le remet au système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="dc22d-107">The message store provider, if tightly coupled to a transport provider, gives the message directly to the transport which delivers it to the messaging system.</span></span> <span data-ttu-id="dc22d-108">Si elle n'est pas étroitement couplée, le fournisseur de banque de messages informe le spouleur MAPI que la file d'attente sortante a été modifiée et que le spouleur MAPI transfère le message à un fournisseur de transport approprié.</span><span class="sxs-lookup"><span data-stu-id="dc22d-108">If not tightly coupled, the message store provider informs the MAPI spooler that the outgoing queue has changed and the MAPI spooler transfers the message to an appropriate transport provider.</span></span>
  
<span data-ttu-id="dc22d-109">Si vous permettez aux utilisateurs d'annuler une opération d'envoi, appelez [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) pour implémenter cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="dc22d-109">If you allow users to cancel a send operation, call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) to implement this feature.</span></span> <span data-ttu-id="dc22d-110">**AbortSubmit** supprime le message de la file d'attente sortante.</span><span class="sxs-lookup"><span data-stu-id="dc22d-110">**AbortSubmit** removes the message from the outgoing queue.</span></span> <span data-ttu-id="dc22d-111">Les utilisateurs peuvent être autorisés à arrêter une émission jusqu'à ce que le message soit donné au système de messagerie sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="dc22d-111">Users can be allowed to stop a send from happening until the message is given to the underlying messaging system.</span></span> 
  
<span data-ttu-id="dc22d-112">Si **SubmitMessage** renvoie MAPI_E_CORRUPT_DATA, partez du principe que les données envoyées sont maintenant perdues.</span><span class="sxs-lookup"><span data-stu-id="dc22d-112">If **SubmitMessage** returns MAPI_E_CORRUPT_DATA, assume that the data being sent is now lost.</span></span> <span data-ttu-id="dc22d-113">Avant d'essayer d'envoyer une deuxième fois, ré-écrivez le message en appelant [IMAPIProp:: SetProps](imapiprop-setprops.md) et [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="dc22d-113">Before attempting to send a second time, re-write the message by calling [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="dc22d-114">Afficher une erreur à l'utilisateur si ces appels **IMAPIProp** échouent ou si **SubmitMessage** échoue une deuxième fois.</span><span class="sxs-lookup"><span data-stu-id="dc22d-114">Display an error to the user if these **IMAPIProp** calls fail or if **SubmitMessage** fails a second time.</span></span> 
  
<span data-ttu-id="dc22d-115">Après un appel réussi vers **SubmitMessage**, libérez de la mémoire allouée à la liste des destinataires, puis libérez le message et ses pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="dc22d-115">After a successful call to **SubmitMessage**, free any memory that was allocated for the recipient list and release the message and its attachments.</span></span> <span data-ttu-id="dc22d-116">Une fois qu'un message a été envoyé, MAPI n'autorise pas d'autres opérations sur les pointeurs pour ces objets.</span><span class="sxs-lookup"><span data-stu-id="dc22d-116">Once a message has been sent, MAPI does not permit any further operations on the pointers for these objects.</span></span> <span data-ttu-id="dc22d-117">La seule exception est l'appel de **IUnknown:: Release**.</span><span class="sxs-lookup"><span data-stu-id="dc22d-117">The one exception is calling **IUnknown::Release**.</span></span> <span data-ttu-id="dc22d-118">Aucun autre appel n'est autorisé car de nombreux fournisseurs de banques de messages invalident des identificateurs d'entrée pour les messages qui ont été envoyés.</span><span class="sxs-lookup"><span data-stu-id="dc22d-118">No other calls are allowed because many message store providers invalidate entry identifiers for messages that have been sent.</span></span>
  

