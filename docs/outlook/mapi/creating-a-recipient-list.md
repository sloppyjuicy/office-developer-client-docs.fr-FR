---
title: Création d'une liste de destinataires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e3aa1f2b2e1e7c6d8a9be3fff451002952930ffb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428213"
---
# <a name="creating-a-recipient-list"></a><span data-ttu-id="7dde4-103">Création d'une liste de destinataires</span><span class="sxs-lookup"><span data-stu-id="7dde4-103">Creating a Recipient List</span></span>

  
  
<span data-ttu-id="7dde4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7dde4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7dde4-105">Une liste de destinataires est une structure [ADRLIST](adrlist.md) qui contient un tableau de structures de valeurs de propriétés pour chaque destinataire de message: destination du message.</span><span class="sxs-lookup"><span data-stu-id="7dde4-105">A recipient list is an [ADRLIST](adrlist.md) structure that contains an array of property value structures for each message recipient — destination for the message.</span></span> <span data-ttu-id="7dde4-106">Un destinataire peut représenter un utilisateur humain, un ordinateur ou un dossier.</span><span class="sxs-lookup"><span data-stu-id="7dde4-106">A recipient can represent a human user, a machine, or a folder.</span></span> <span data-ttu-id="7dde4-107">Tous les messages à envoyer nécessitent au moins un destinataire qui a été redirigé par le processus de résolution de noms, ce qui permet de s'assurer que la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) est incluse dans le tableau de valeurs de la propriété du destinataire.</span><span class="sxs-lookup"><span data-stu-id="7dde4-107">All messages to be sent require at least one recipient that has been through the name resolution process — a process for ensuring that the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included in the recipient's property value array.</span></span> 
  
<span data-ttu-id="7dde4-108">Les propriétés d'un destinataire sont une combinaison de propriétés de carnet d'adresses et de propriétés de message.</span><span class="sxs-lookup"><span data-stu-id="7dde4-108">The properties of a recipient are a combination of address book properties and message properties.</span></span> <span data-ttu-id="7dde4-109">Les propriétés du destinataire peuvent s'appliquer soit à tous les messages pour un destinataire particulier, soit uniquement au message actif.</span><span class="sxs-lookup"><span data-stu-id="7dde4-109">Recipient properties can apply either to all messages for a particular recipient or only to the current message.</span></span> <span data-ttu-id="7dde4-110">Les fournisseurs de banque de messages et de transport peuvent définir les propriétés des destinataires.</span><span class="sxs-lookup"><span data-stu-id="7dde4-110">Both message store and transport providers can set recipient properties.</span></span> 
  
<span data-ttu-id="7dde4-111">Chaque destinataire doit disposer d'un ensemble principal de propriétés dans son tableau de valeurs de propriétés, au moment où le message est prêt à être envoyé.</span><span class="sxs-lookup"><span data-stu-id="7dde4-111">Each recipient must have a core set of properties in its property value array by the time the message is ready to be sent.</span></span> <span data-ttu-id="7dde4-112">Les propriétés de destinataire requises sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="7dde4-112">The required set of recipient properties include:</span></span>
  
- <span data-ttu-id="7dde4-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7dde4-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="7dde4-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7dde4-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="7dde4-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7dde4-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="7dde4-116">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="7dde4-116">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="7dde4-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7dde4-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="7dde4-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7dde4-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="7dde4-119">Ces propriétés sont utilisées pour accéder au destinataire, lui envoyer des messages et pour le comparer à d'autres.</span><span class="sxs-lookup"><span data-stu-id="7dde4-119">These properties are used to access the recipient, send messages to it, and to compare it to others.</span></span> <span data-ttu-id="7dde4-120">Toutes ces propriétés ne doivent pas être disponibles immédiatement.</span><span class="sxs-lookup"><span data-stu-id="7dde4-120">Not all of these properties need to be available right away.</span></span> <span data-ttu-id="7dde4-121">Vous pouvez ajouter un destinataire initialement sans connaître son identificateur d'entrée, en utilisant le processus de résolution de noms pour affecter cette propriété.</span><span class="sxs-lookup"><span data-stu-id="7dde4-121">You can add a recipient initially without knowing its entry identifier, relying on the name resolution process to assign this property.</span></span> <span data-ttu-id="7dde4-122">À un moment donné, avant d'envoyer un message, appelez [IAddrBook:: ResolveName](iaddrbook-resolvename.md) pour vous assurer que tous les destinataires de votre liste de destinataires sont résolus.</span><span class="sxs-lookup"><span data-stu-id="7dde4-122">At some point before you send a message, call [IAddrBook::ResolveName](iaddrbook-resolvename.md) to make sure that all of the recipients in your recipient list are resolved.</span></span> <span data-ttu-id="7dde4-123">Pour plus d'informations, consultez la rubrique relative à [la résolution d'un nom de destinataire](resolving-a-recipient-name.md).</span><span class="sxs-lookup"><span data-stu-id="7dde4-123">For more information, see [Resolving a Recipient Name](resolving-a-recipient-name.md).</span></span>
  
<span data-ttu-id="7dde4-124">Les listes de destinataires peuvent être créées à partir d'utilisateurs de messagerie ou d'entrées de liste de distribution dans un conteneur de carnet d'adresses ou à partir de plusieurs points.</span><span class="sxs-lookup"><span data-stu-id="7dde4-124">Recipient lists can be created from messaging users or distribution list entries in an address book container or from one-offs.</span></span> <span data-ttu-id="7dde4-125">Les destinataires uniques sont créés en tant qu'entrées temporaires pour être utilisés uniquement pour l'adressage d'un seul message ou comme entrées à ajouter à un carnet d'adresses personnel.</span><span class="sxs-lookup"><span data-stu-id="7dde4-125">One-offs are recipients that are created either as temporary entries to be used only for addressing a single message or as entries to be added to a personal address book.</span></span> <span data-ttu-id="7dde4-126">Le format d'un identificateur d'entrée unique et d'une adresse est défini par MAPI.</span><span class="sxs-lookup"><span data-stu-id="7dde4-126">The format for a one-off entry identifier and address is defined by MAPI.</span></span> <span data-ttu-id="7dde4-127">Pour plus d'informations sur ces formats, consultez les [adresses ponctuelles](one-off-addresses.md) et les identificateurs d' [entrée ponctuelle](one-off-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="7dde4-127">For more information about these formats, see [One-Off Addresses](one-off-addresses.md) and [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span>
  
<span data-ttu-id="7dde4-128">Vous pouvez permettre aux utilisateurs de créer leurs listes de destinataires:</span><span class="sxs-lookup"><span data-stu-id="7dde4-128">You can enable users to build their recipient lists:</span></span>
  
- <span data-ttu-id="7dde4-129">Uniquement avec les entrées du carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="7dde4-129">Only with entries from the address book.</span></span>
    
- <span data-ttu-id="7dde4-130">Uniquement avec les entrées uniques.</span><span class="sxs-lookup"><span data-stu-id="7dde4-130">Only with one-off entries.</span></span>
    
- <span data-ttu-id="7dde4-131">Avec une combinaison de destinataires de carnet d'adresses et de personnes à un.</span><span class="sxs-lookup"><span data-stu-id="7dde4-131">With a combination of address book recipients and one-offs.</span></span>
    
 <span data-ttu-id="7dde4-132">**Pour créer une liste de destinataires à l'aide de la boîte de dialogue adresse commune**</span><span class="sxs-lookup"><span data-stu-id="7dde4-132">**To create a recipient list using the common address dialog box**</span></span>
  
1. <span data-ttu-id="7dde4-133">AlLouez une structure [ADRPARM](adrparm.md) et un pointeur vers une structure [ADRLIST](adrlist.md) .</span><span class="sxs-lookup"><span data-stu-id="7dde4-133">Allocate an [ADRPARM](adrparm.md) structure and a pointer to an [ADRLIST](adrlist.md) structure.</span></span> 
    
2. <span data-ttu-id="7dde4-134">Zéro de la mémoire dans la structure **ADRPARM** et définissez le pointeur **ADRLIST** sur null.</span><span class="sxs-lookup"><span data-stu-id="7dde4-134">Zero the memory in the **ADRPARM** structure and set the **ADRLIST** pointer to NULL.</span></span> 
    
3. <span data-ttu-id="7dde4-135">Appelez [IAddrBook:: Address](iaddrbook-address.md) pour afficher la boîte de dialogue d'adresses et remplir la structure **ADRPARM** .</span><span class="sxs-lookup"><span data-stu-id="7dde4-135">Call [IAddrBook::Address](iaddrbook-address.md) to display the address dialog box and populate the **ADRPARM** structure.</span></span> 
    
4. <span data-ttu-id="7dde4-136">Appelez [IMessage:: ModifyRecipients](imessage-modifyrecipients.md), en passant le pointeur **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="7dde4-136">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md), passing the **ADRLIST** pointer.</span></span> <span data-ttu-id="7dde4-137">Cette structure contient les propriétés de chacun des destinataires sélectionnés par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7dde4-137">This structure will contain the properties of each of the recipients selected by the user.</span></span> 
    
 <span data-ttu-id="7dde4-138">**Pour créer une liste de destinataires par programme**</span><span class="sxs-lookup"><span data-stu-id="7dde4-138">**To create a recipient list programmatically**</span></span>
  
1. <span data-ttu-id="7dde4-139">AlLouez une structure **ADRLIST** qui contient une structure [ADRENTRY](adrentry.md) pour chacun des destinataires à inclure dans la liste.</span><span class="sxs-lookup"><span data-stu-id="7dde4-139">Allocate an **ADRLIST** structure that contains one [ADRENTRY](adrentry.md) structure for each of the recipients to be included in the list.</span></span> <span data-ttu-id="7dde4-140">Rendez chaque structure **ADRENTRY** suffisamment importante pour contenir chacune des propriétés requises et **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7dde4-140">Make each **ADRENTRY** structure large enough to hold each of the required properties and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="7dde4-141">Pour chaque destinataire, définissez le tableau de valeurs de propriété pour son membre **aEntries** dans la structure **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="7dde4-141">For each recipient, set the property value array for its **aEntries** member in the **ADRLIST** structure.</span></span> 
    
3. <span data-ttu-id="7dde4-142">Appelez [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) avec l'indicateur MODRECIP_ADD défini.</span><span class="sxs-lookup"><span data-stu-id="7dde4-142">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md) with the MODRECIP_ADD flag set.</span></span> 
    

