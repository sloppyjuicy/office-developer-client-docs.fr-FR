---
title: Tables des destinataires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e77317-54c4-4fca-9ab4-835998ce07ce
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8950623308e85de1d239deb322f65ee867a33ca0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437286"
---
# <a name="recipient-tables"></a><span data-ttu-id="9d07b-103">Tables des destinataires</span><span class="sxs-lookup"><span data-stu-id="9d07b-103">Recipient Tables</span></span>

  
  
<span data-ttu-id="9d07b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d07b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d07b-105">La table des destinataires contient des informations sur tous les destinataires d’un message.</span><span class="sxs-lookup"><span data-stu-id="9d07b-105">The recipient table contains information about all the recipients for a message.</span></span> <span data-ttu-id="9d07b-106">Les fournisseurs de magasins de messages implémentent les tables des destinataires et les applications clientes les utilisent.</span><span class="sxs-lookup"><span data-stu-id="9d07b-106">Message store providers implement recipient tables and client applications use them.</span></span> <span data-ttu-id="9d07b-107">Les clients accèdent à une table des destinataires en appelant la méthode [IMessage::GetRecipientTable,](imessage-getrecipienttable.md) ou si le fournisseur de magasin de messages la prend en charge, à la méthode [IMAPIProp::OpenProperty.](imapiprop-openproperty.md)</span><span class="sxs-lookup"><span data-stu-id="9d07b-107">Clients access a recipient table by making a call to the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, or if the message store provider supports it, to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="9d07b-108">Clients access recipient tables with **OpenProperty** by specifying **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span><span class="sxs-lookup"><span data-stu-id="9d07b-108">Clients access recipient tables with **OpenProperty** by specifying **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> <span data-ttu-id="9d07b-109">Les modifications apportées à une table des destinataires peuvent être apportées en appelant la méthode [IMessage::ModifyRecipients.](imessage-modifyrecipients.md)</span><span class="sxs-lookup"><span data-stu-id="9d07b-109">Changes to a recipient table can be made by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
<span data-ttu-id="9d07b-110">Les tables des destinataires ont un ensemble de colonnes différent selon que le message a été envoyé ou non.</span><span class="sxs-lookup"><span data-stu-id="9d07b-110">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="9d07b-111">Les propriétés suivantes définissent la colonne requise dans les tables des destinataires :</span><span class="sxs-lookup"><span data-stu-id="9d07b-111">The following properties make up the required column set in recipient tables:</span></span>
  
- <span data-ttu-id="9d07b-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9d07b-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="9d07b-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9d07b-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="9d07b-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9d07b-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span></span>
    
<span data-ttu-id="9d07b-115">Les propriétés facultatives sont :</span><span class="sxs-lookup"><span data-stu-id="9d07b-115">The optional properties are:</span></span>
  
- <span data-ttu-id="9d07b-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9d07b-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="9d07b-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9d07b-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="9d07b-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9d07b-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="9d07b-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9d07b-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
<span data-ttu-id="9d07b-120">Les messages envoyés doivent inclure ces propriétés supplémentaires dans l’ensemble de colonnes requis :</span><span class="sxs-lookup"><span data-stu-id="9d07b-120">Submitted messages should include these additional properties in their required column set:</span></span>
  
- <span data-ttu-id="9d07b-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9d07b-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="9d07b-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9d07b-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span></span>
    
<span data-ttu-id="9d07b-123">Selon l’implémentation d’un fournisseur, des colonnes supplémentaires, telles que **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) et [ENTRYID](entryid.md), peuvent être dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="9d07b-123">Depending on a provider's implementation, additional columns, such as **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) and [ENTRYID](entryid.md), might be in the table.</span></span>
  
<span data-ttu-id="9d07b-124">Tout fournisseur de magasins de messages qui prend en charge la transmission de messages, comme indiqué par le bit STORE_SUBMIT_OK en cours de paralocalisation dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)du fournisseur, doit prendre en charge un ensemble particulier de restrictions dans l’implémentation d’une table des destinataires.</span><span class="sxs-lookup"><span data-stu-id="9d07b-124">Any message store provider that supports message transmission — as indicated by the STORE_SUBMIT_OK bit being set in the provider's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property — should offer support for a particular set of restrictions in a recipient table implementation.</span></span> <span data-ttu-id="9d07b-125">Les restrictions **and**, **OR**, existent et les restrictions de propriété font partie des types de restrictions qui doivent être disponibles pour les utilisateurs de la table des destinataires.</span><span class="sxs-lookup"><span data-stu-id="9d07b-125">The **AND**, **OR**, exist, and property restrictions are among the types of restrictions that should be available to recipient table users.</span></span> <span data-ttu-id="9d07b-126">Seuls les opérateurs égal et non égal doivent être pris en charge dans la restriction de propriété.</span><span class="sxs-lookup"><span data-stu-id="9d07b-126">Only the equal and not equal operators need to be supported on the property restriction.</span></span> <span data-ttu-id="9d07b-127">Ces restrictions doivent fonctionner avec les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d07b-127">These restrictions must work with the following properties:</span></span>
  
- <span data-ttu-id="9d07b-128">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="9d07b-128">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="9d07b-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9d07b-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="9d07b-130">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="9d07b-130">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="9d07b-131">**PR_RESPONSIBILITY**</span><span class="sxs-lookup"><span data-stu-id="9d07b-131">**PR_RESPONSIBILITY**</span></span>
    
- <span data-ttu-id="9d07b-132">**PR_SPOOLER_STATUS**</span><span class="sxs-lookup"><span data-stu-id="9d07b-132">**PR_SPOOLER_STATUS**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d07b-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d07b-133">See also</span></span>



[<span data-ttu-id="9d07b-134">MAPI Tables</span><span class="sxs-lookup"><span data-stu-id="9d07b-134">MAPI Tables</span></span>](mapi-tables.md)

