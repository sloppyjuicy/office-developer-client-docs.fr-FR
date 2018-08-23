---
title: Création d’une liste de destinataires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6de805da2aadd8ac40ca984c5f336d5ca7906248
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590126"
---
# <a name="creating-a-recipient-list"></a><span data-ttu-id="721a6-103">Création d’une liste de destinataires</span><span class="sxs-lookup"><span data-stu-id="721a6-103">Creating a Recipient List</span></span>

  
  
<span data-ttu-id="721a6-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="721a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="721a6-105">Une liste de destinataires est une structure [ADRLIST](adrlist.md) qui contient un tableau de structures de valeur de propriété pour chaque destinataire du message — destination pour le message.</span><span class="sxs-lookup"><span data-stu-id="721a6-105">A recipient list is an [ADRLIST](adrlist.md) structure that contains an array of property value structures for each message recipient — destination for the message.</span></span> <span data-ttu-id="721a6-106">Un destinataire peut représenter un utilisateur, un ordinateur ou un dossier.</span><span class="sxs-lookup"><span data-stu-id="721a6-106">A recipient can represent a human user, a machine, or a folder.</span></span> <span data-ttu-id="721a6-107">Tous les messages soient envoyées nécessitent au moins un destinataire qui a été par le biais du processus de résolution de nom, un processus pour s’assurer que la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) est incluse dans le tableau de valeurs de propriété du destinataire.</span><span class="sxs-lookup"><span data-stu-id="721a6-107">All messages to be sent require at least one recipient that has been through the name resolution process — a process for ensuring that the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included in the recipient's property value array.</span></span> 
  
<span data-ttu-id="721a6-108">Les propriétés d’un destinataire sont une combinaison de propriétés de carnet d’adresses et les propriétés de message.</span><span class="sxs-lookup"><span data-stu-id="721a6-108">The properties of a recipient are a combination of address book properties and message properties.</span></span> <span data-ttu-id="721a6-109">Propriétés de destinataire peuvent s’appliquent à tous les messages pour un destinataire particulier ou uniquement pour le message en cours.</span><span class="sxs-lookup"><span data-stu-id="721a6-109">Recipient properties can apply either to all messages for a particular recipient or only to the current message.</span></span> <span data-ttu-id="721a6-110">Les deux messages magasin et fournisseurs de transport peuvent définir des propriétés de destinataire.</span><span class="sxs-lookup"><span data-stu-id="721a6-110">Both message store and transport providers can set recipient properties.</span></span> 
  
<span data-ttu-id="721a6-111">Chaque destinataire doit avoir un ensemble de propriétés dans le tableau de valeurs de propriété au moment où que le message est prêt à être envoyé.</span><span class="sxs-lookup"><span data-stu-id="721a6-111">Each recipient must have a core set of properties in its property value array by the time the message is ready to be sent.</span></span> <span data-ttu-id="721a6-112">Le jeu de propriétés de destinataire requis sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="721a6-112">The required set of recipient properties include:</span></span>
  
- <span data-ttu-id="721a6-113">**TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="721a6-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="721a6-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="721a6-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="721a6-115">**ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="721a6-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="721a6-116">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="721a6-116">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="721a6-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="721a6-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="721a6-118">**Clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="721a6-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="721a6-119">Ces propriétés sont utilisées pour accéder au destinataire, lui envoyer des messages et comparer à d’autres personnes.</span><span class="sxs-lookup"><span data-stu-id="721a6-119">These properties are used to access the recipient, send messages to it, and to compare it to others.</span></span> <span data-ttu-id="721a6-120">Toutes ces propriétés doivent être immédiatement disponibles.</span><span class="sxs-lookup"><span data-stu-id="721a6-120">Not all of these properties need to be available right away.</span></span> <span data-ttu-id="721a6-121">Vous pouvez ajouter un destinataire à l’origine sans connaître son identificateur d’entrée, compter sur le processus de résolution de noms à assigner à cette propriété.</span><span class="sxs-lookup"><span data-stu-id="721a6-121">You can add a recipient initially without knowing its entry identifier, relying on the name resolution process to assign this property.</span></span> <span data-ttu-id="721a6-122">À un moment donné avant d’envoyer un message, appelez [IAddrBook::ResolveName](iaddrbook-resolvename.md) pour vous assurer que tous les destinataires dans votre liste des destinataires sont résolus.</span><span class="sxs-lookup"><span data-stu-id="721a6-122">At some point before you send a message, call [IAddrBook::ResolveName](iaddrbook-resolvename.md) to make sure that all of the recipients in your recipient list are resolved.</span></span> <span data-ttu-id="721a6-123">Pour plus d’informations, voir [résolution de nom d’un destinataire](resolving-a-recipient-name.md).</span><span class="sxs-lookup"><span data-stu-id="721a6-123">For more information, see [Resolving a Recipient Name](resolving-a-recipient-name.md).</span></span>
  
<span data-ttu-id="721a6-124">Listes de destinataires peuvent être créés à partir d’utilisateurs ou des entrées de liste de distribution dans un conteneur de carnet d’adresses de messagerie ou uniques.</span><span class="sxs-lookup"><span data-stu-id="721a6-124">Recipient lists can be created from messaging users or distribution list entries in an address book container or from one-offs.</span></span> <span data-ttu-id="721a6-125">Uniques sont des destinataires qui sont créés comme des entrées temporaires à utiliser uniquement pour adresser un message unique ou comme des entrées à ajouter à un carnet d’adresses personnel.</span><span class="sxs-lookup"><span data-stu-id="721a6-125">One-offs are recipients that are created either as temporary entries to be used only for addressing a single message or as entries to be added to a personal address book.</span></span> <span data-ttu-id="721a6-126">Le format d’un identificateur d’entrée unique et une adresse est défini par MAPI.</span><span class="sxs-lookup"><span data-stu-id="721a6-126">The format for a one-off entry identifier and address is defined by MAPI.</span></span> <span data-ttu-id="721a6-127">Pour plus d’informations sur ces formats, voir [Adresses uniques](one-off-addresses.md) et des [Identificateurs uniques d’entrée](one-off-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="721a6-127">For more information about these formats, see [One-Off Addresses](one-off-addresses.md) and [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span>
  
<span data-ttu-id="721a6-128">Vous pouvez permettre aux utilisateurs créer leurs listes de destinataires :</span><span class="sxs-lookup"><span data-stu-id="721a6-128">You can enable users to build their recipient lists:</span></span>
  
- <span data-ttu-id="721a6-129">Uniquement avec les entrées du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="721a6-129">Only with entries from the address book.</span></span>
    
- <span data-ttu-id="721a6-130">Uniquement avec les entrées uniques.</span><span class="sxs-lookup"><span data-stu-id="721a6-130">Only with one-off entries.</span></span>
    
- <span data-ttu-id="721a6-131">Avec une combinaison de destinataires de carnet d’adresses et uniques.</span><span class="sxs-lookup"><span data-stu-id="721a6-131">With a combination of address book recipients and one-offs.</span></span>
    
 <span data-ttu-id="721a6-132">**Pour créer une liste de destinataires à l’aide de la boîte de dialogue adresse**</span><span class="sxs-lookup"><span data-stu-id="721a6-132">**To create a recipient list using the common address dialog box**</span></span>
  
1. <span data-ttu-id="721a6-133">Allouez une structure [ADRPARM](adrparm.md) et un pointeur vers une structure [ADRLIST](adrlist.md) .</span><span class="sxs-lookup"><span data-stu-id="721a6-133">Allocate an [ADRPARM](adrparm.md) structure and a pointer to an [ADRLIST](adrlist.md) structure.</span></span> 
    
2. <span data-ttu-id="721a6-134">Zéro de la mémoire dans la structure **ADRPARM** et définir le pointeur **ADRLIST** NULL.</span><span class="sxs-lookup"><span data-stu-id="721a6-134">Zero the memory in the **ADRPARM** structure and set the **ADRLIST** pointer to NULL.</span></span> 
    
3. <span data-ttu-id="721a6-135">Appelez [IAddrBook::Address](iaddrbook-address.md) pour afficher la boîte de dialogue adresse et remplir la structure **ADRPARM** .</span><span class="sxs-lookup"><span data-stu-id="721a6-135">Call [IAddrBook::Address](iaddrbook-address.md) to display the address dialog box and populate the **ADRPARM** structure.</span></span> 
    
4. <span data-ttu-id="721a6-136">Appelez [IMessage::ModifyRecipients](imessage-modifyrecipients.md), en passant le pointeur **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="721a6-136">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md), passing the **ADRLIST** pointer.</span></span> <span data-ttu-id="721a6-137">Cette structure contient les propriétés de chacun des destinataires sélectionnés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="721a6-137">This structure will contain the properties of each of the recipients selected by the user.</span></span> 
    
 <span data-ttu-id="721a6-138">**Pour créer une liste de destinataires par programme**</span><span class="sxs-lookup"><span data-stu-id="721a6-138">**To create a recipient list programmatically**</span></span>
  
1. <span data-ttu-id="721a6-139">Allouez une structure **ADRLIST** qui contient une structure [ADRENTRY](adrentry.md) pour chacun des destinataires à inclure dans la liste.</span><span class="sxs-lookup"><span data-stu-id="721a6-139">Allocate an **ADRLIST** structure that contains one [ADRENTRY](adrentry.md) structure for each of the recipients to be included in the list.</span></span> <span data-ttu-id="721a6-140">Vérifiez chaque structure **ADRENTRY** suffisante pour contenir chacune des propriétés requises et **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="721a6-140">Make each **ADRENTRY** structure large enough to hold each of the required properties and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="721a6-141">Pour chaque destinataire, définissez le tableau de valeurs de propriété pour ses membres **aEntries** dans la structure **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="721a6-141">For each recipient, set the property value array for its **aEntries** member in the **ADRLIST** structure.</span></span> 
    
3. <span data-ttu-id="721a6-142">Appelez [IMessage::ModifyRecipients](imessage-modifyrecipients.md) avec l’indicateur MODRECIP_ADD.</span><span class="sxs-lookup"><span data-stu-id="721a6-142">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md) with the MODRECIP_ADD flag set.</span></span> 
    

