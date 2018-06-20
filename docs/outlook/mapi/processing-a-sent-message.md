---
title: Traitement d’un Message
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0cea1a1008ecbff698b757d6c67af5c279954656
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786923"
---
# <a name="processing-a-sent-message"></a><span data-ttu-id="d6d2e-103">Traitement d’un Message</span><span class="sxs-lookup"><span data-stu-id="d6d2e-103">Processing a Sent Message</span></span>

  
  
<span data-ttu-id="d6d2e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d6d2e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d6d2e-105">Les messages, sortants une fois qu’ils ont été envoyés, peuvent rester dans la boîte d’envoi dossier, déplacé vers un dossier désigné pour stocker les messages envoyés ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-105">Outgoing messages, after they have been sent, can be left in the Outbox folder, moved to a folder designated to hold sent messages, or deleted.</span></span> <span data-ttu-id="d6d2e-106">Le type de traitement dépend si vous avez défini le message banque de propriétés :</span><span class="sxs-lookup"><span data-stu-id="d6d2e-106">The type of processing depends on whether or not you have set the message store properties:</span></span>
  
- <span data-ttu-id="d6d2e-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d6d2e-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span> 
    
- <span data-ttu-id="d6d2e-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d6d2e-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span> 
    
 <span data-ttu-id="d6d2e-109">**PR_DELETE_AFTER_SUBMIT** est une propriété booléenne, la valeur TRUE si les messages doivent être supprimées une fois qu’ils sont envoyés et FALSE dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-109">**PR_DELETE_AFTER_SUBMIT** is a Boolean property, set to TRUE if messages should be deleted after they are sent, and FALSE otherwise.</span></span> <span data-ttu-id="d6d2e-110">**PR_SENTMAIL_ENTRYID** est l’identificateur d’entrée d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-110">**PR_SENTMAIL_ENTRYID** is the entry identifier of a folder.</span></span> <span data-ttu-id="d6d2e-111">Lorsque cette propriété est définie, vous devez déplacer les messages envoyés vers le dossier représenté par cet identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-111">When this property is set, you should move sent messages to the folder represented by this entry identifier.</span></span> <span data-ttu-id="d6d2e-112">En général, les messages enregistrés ont l’identité de la dernière banque d’informations ou de les envoyer au fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-112">The saved messages typically have the identity of the last message store or transport provider to send them.</span></span> 
  
<span data-ttu-id="d6d2e-113">Un ou l’autre des deux ou aucune de ces propriétés doit être ensemble, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-113">Either one or the other, or neither of these properties should be set, but not both.</span></span> <span data-ttu-id="d6d2e-114">Toutefois, si vous définissez **PR_SENTMAIL_ENTRYID**, il doit contenir un identificateur d’entrée valide.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-114">However, if you set **PR_SENTMAIL_ENTRYID**, it must contain a valid entry identifier.</span></span> 
  
<span data-ttu-id="d6d2e-115">Le tableau suivant décrit la façon dont ces propriétés affectent que faire avec des messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-115">The following table describes how these properties affect what you do with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d6d2e-116">Si aucune propriété n’est définie :</span><span class="sxs-lookup"><span data-stu-id="d6d2e-116">If neither property is set:</span></span>  <br/> |<span data-ttu-id="d6d2e-117">Laissez le message dans le dossier à partir de laquelle il a été envoyé (généralement la boîte d’envoi).</span><span class="sxs-lookup"><span data-stu-id="d6d2e-117">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="d6d2e-118">Si **PR_SENTMAIL_ENTRYID** est défini :</span><span class="sxs-lookup"><span data-stu-id="d6d2e-118">If **PR_SENTMAIL_ENTRYID** is set:</span></span>  <br/> |<span data-ttu-id="d6d2e-119">Déplacer le message vers le dossier indiqué.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-119">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="d6d2e-120">Si **PR_DELETE_AFTER_SUBMIT** est défini :</span><span class="sxs-lookup"><span data-stu-id="d6d2e-120">If **PR_DELETE_AFTER_SUBMIT** is set:</span></span>  <br/> |<span data-ttu-id="d6d2e-121">Supprimer le message.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-121">Delete the message.</span></span>  <br/> |
   

