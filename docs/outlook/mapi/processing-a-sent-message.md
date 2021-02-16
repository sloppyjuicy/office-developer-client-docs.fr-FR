---
title: Traitement d’un message envoyé
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 880731bf204778cde21da6cd9024a3ca86c6f6a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434675"
---
# <a name="processing-a-sent-message"></a><span data-ttu-id="1b934-103">Traitement d’un message envoyé</span><span class="sxs-lookup"><span data-stu-id="1b934-103">Processing a Sent Message</span></span>

  
  
<span data-ttu-id="1b934-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b934-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b934-105">Les messages sortants, une fois envoyés, peuvent être laissés dans le dossier Boîte d’envoi, déplacés vers un dossier désigné pour contenir les messages envoyés ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="1b934-105">Outgoing messages, after they have been sent, can be left in the Outbox folder, moved to a folder designated to hold sent messages, or deleted.</span></span> <span data-ttu-id="1b934-106">Le type de traitement varie selon que vous avez ou non définie les propriétés de la boutique de messages :</span><span class="sxs-lookup"><span data-stu-id="1b934-106">The type of processing depends on whether or not you have set the message store properties:</span></span>
  
- <span data-ttu-id="1b934-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1b934-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span> 
    
- <span data-ttu-id="1b934-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1b934-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span> 
    
 <span data-ttu-id="1b934-109">**PR_DELETE_AFTER_SUBMIT** est une propriété Boolean, définie sur TRUE si les messages doivent être supprimés après leur envoi, et FALSE dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1b934-109">**PR_DELETE_AFTER_SUBMIT** is a Boolean property, set to TRUE if messages should be deleted after they are sent, and FALSE otherwise.</span></span> <span data-ttu-id="1b934-110">**PR_SENTMAIL_ENTRYID** est l’identificateur d’entrée d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="1b934-110">**PR_SENTMAIL_ENTRYID** is the entry identifier of a folder.</span></span> <span data-ttu-id="1b934-111">Lorsque cette propriété est définie, vous devez déplacer les messages envoyés vers le dossier représenté par cet identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1b934-111">When this property is set, you should move sent messages to the folder represented by this entry identifier.</span></span> <span data-ttu-id="1b934-112">Les messages enregistrés ont généralement l’identité de la dernière boutique de messages ou du dernier fournisseur de transport pour les envoyer.</span><span class="sxs-lookup"><span data-stu-id="1b934-112">The saved messages typically have the identity of the last message store or transport provider to send them.</span></span> 
  
<span data-ttu-id="1b934-113">L’une ou l’autre, ou aucune de ces propriétés ne doit être définie, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="1b934-113">Either one or the other, or neither of these properties should be set, but not both.</span></span> <span data-ttu-id="1b934-114">Toutefois, si vous définissez **PR_SENTMAIL_ENTRYID,** il doit contenir un identificateur d’entrée valide.</span><span class="sxs-lookup"><span data-stu-id="1b934-114">However, if you set **PR_SENTMAIL_ENTRYID**, it must contain a valid entry identifier.</span></span> 
  
<span data-ttu-id="1b934-115">Le tableau suivant décrit comment ces propriétés affectent ce que vous faites avec les messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="1b934-115">The following table describes how these properties affect what you do with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1b934-116">Si aucune des propriétés n’est définie :</span><span class="sxs-lookup"><span data-stu-id="1b934-116">If neither property is set:</span></span>  <br/> |<span data-ttu-id="1b934-117">Laissez le message dans le dossier à partir duquel il a été envoyé (généralement la boîte d’envoi).</span><span class="sxs-lookup"><span data-stu-id="1b934-117">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="1b934-118">Si **PR_SENTMAIL_ENTRYID** est définie :</span><span class="sxs-lookup"><span data-stu-id="1b934-118">If **PR_SENTMAIL_ENTRYID** is set:</span></span>  <br/> |<span data-ttu-id="1b934-119">Déplacez le message vers le dossier indiqué.</span><span class="sxs-lookup"><span data-stu-id="1b934-119">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="1b934-120">Si **PR_DELETE_AFTER_SUBMIT** est définie :</span><span class="sxs-lookup"><span data-stu-id="1b934-120">If **PR_DELETE_AFTER_SUBMIT** is set:</span></span>  <br/> |<span data-ttu-id="1b934-121">Supprimez le message.</span><span class="sxs-lookup"><span data-stu-id="1b934-121">Delete the message.</span></span>  <br/> |
   

