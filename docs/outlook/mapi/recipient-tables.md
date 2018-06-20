---
title: Tables de destinataires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e77317-54c4-4fca-9ab4-835998ce07ce
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: cc7635c474b99898d59589f33fcf06cf24697378
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786968"
---
# <a name="recipient-tables"></a><span data-ttu-id="b79f7-103">Tables de destinataires</span><span class="sxs-lookup"><span data-stu-id="b79f7-103">Recipient Tables</span></span>

  
  
<span data-ttu-id="b79f7-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b79f7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b79f7-105">La table de destinataires contient des informations sur tous les destinataires d’un message.</span><span class="sxs-lookup"><span data-stu-id="b79f7-105">The recipient table contains information about all the recipients for a message.</span></span> <span data-ttu-id="b79f7-106">Tables de destinataires implémentés par les fournisseurs de banque de message et les applications clientes pour les utilisent.</span><span class="sxs-lookup"><span data-stu-id="b79f7-106">Message store providers implement recipient tables and client applications use them.</span></span> <span data-ttu-id="b79f7-107">Accéder à une table de destinataires par un appel à la méthode [IMessage::GetRecipientTable](imessage-getrecipienttable.md) clients, ou si la banque de messages fournisseur prend en charge, à la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="b79f7-107">Clients access a recipient table by making a call to the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, or if the message store provider supports it, to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="b79f7-108">Clients accéder aux tables de destinataires avec **OpenProperty** en spécifiant **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) pour la balise de propriété et IID_IMAPITable pour l’identificateur d’interface.</span><span class="sxs-lookup"><span data-stu-id="b79f7-108">Clients access recipient tables with **OpenProperty** by specifying **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> <span data-ttu-id="b79f7-109">Modifications apportées à une table de destinataires est possible en appelant la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="b79f7-109">Changes to a recipient table can be made by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
<span data-ttu-id="b79f7-110">Tables de destinataires ont une colonne différente selon que le message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="b79f7-110">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="b79f7-111">Les propriétés suivantes constituent la colonne obligatoire définie dans les tables de destinataires :</span><span class="sxs-lookup"><span data-stu-id="b79f7-111">The following properties make up the required column set in recipient tables:</span></span>
  
- <span data-ttu-id="b79f7-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b79f7-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="b79f7-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b79f7-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="b79f7-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b79f7-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span></span>
    
<span data-ttu-id="b79f7-115">Les propriétés facultatives sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="b79f7-115">The optional properties are:</span></span>
  
- <span data-ttu-id="b79f7-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b79f7-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="b79f7-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b79f7-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="b79f7-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b79f7-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="b79f7-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b79f7-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
<span data-ttu-id="b79f7-120">Messages envoyés doivent inclure les propriétés supplémentaires dans leur ensemble de colonnes requises :</span><span class="sxs-lookup"><span data-stu-id="b79f7-120">Submitted messages should include these additional properties in their required column set:</span></span>
  
- <span data-ttu-id="b79f7-121">**TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b79f7-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="b79f7-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b79f7-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span></span>
    
<span data-ttu-id="b79f7-123">En fonction de l’implémentation d’un fournisseur, des colonnes supplémentaires, telles que **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) et [ENTRYID](entryid.md), peut-être dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="b79f7-123">Depending on a provider's implementation, additional columns, such as **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) and [ENTRYID](entryid.md), might be in the table.</span></span>
  
<span data-ttu-id="b79f7-124">Tout fournisseur de banque de message qui prend en charge la transmission des messages, comme indiqué par le bit STORE_SUBMIT_OK défini dans la propriété de **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) du fournisseur — doit offrir un ensemble particulier de prise en charge restrictions dans une implémentation de la table des destinataires.</span><span class="sxs-lookup"><span data-stu-id="b79f7-124">Any message store provider that supports message transmission — as indicated by the STORE_SUBMIT_OK bit being set in the provider's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property — should offer support for a particular set of restrictions in a recipient table implementation.</span></span> <span data-ttu-id="b79f7-125">Le **et**, **ou**, existent et restrictions de propriété sont les types de restrictions qui doivent être disponibles aux utilisateurs de la table de destinataires.</span><span class="sxs-lookup"><span data-stu-id="b79f7-125">The **AND**, **OR**, exist, and property restrictions are among the types of restrictions that should be available to recipient table users.</span></span> <span data-ttu-id="b79f7-126">Seuls les opérateurs égales et n’est pas égales doivent être pris en charge sur la restriction de propriété.</span><span class="sxs-lookup"><span data-stu-id="b79f7-126">Only the equal and not equal operators need to be supported on the property restriction.</span></span> <span data-ttu-id="b79f7-127">Ces restrictions doivent fonctionner avec les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="b79f7-127">These restrictions must work with the following properties:</span></span>
  
- <span data-ttu-id="b79f7-128">**TYPEADR_PR**</span><span class="sxs-lookup"><span data-stu-id="b79f7-128">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="b79f7-129">**ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b79f7-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="b79f7-130">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="b79f7-130">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="b79f7-131">**PR_RESPONSIBILITY**</span><span class="sxs-lookup"><span data-stu-id="b79f7-131">**PR_RESPONSIBILITY**</span></span>
    
- <span data-ttu-id="b79f7-132">**PR_SPOOLER_STATUS**</span><span class="sxs-lookup"><span data-stu-id="b79f7-132">**PR_SPOOLER_STATUS**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b79f7-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b79f7-133">See also</span></span>



[<span data-ttu-id="b79f7-134">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="b79f7-134">MAPI Tables</span></span>](mapi-tables.md)

