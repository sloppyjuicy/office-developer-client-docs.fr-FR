---
title: Préparation d'un destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9573f10c-66e1-4e87-93f0-89687e906b8b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bb6bc8b8d0199ab07d5dad353dbc25da240593e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419876"
---
# <a name="preparing-a-recipient"></a><span data-ttu-id="9848e-103">Préparation d'un destinataire</span><span class="sxs-lookup"><span data-stu-id="9848e-103">Preparing a Recipient</span></span>

  
  
<span data-ttu-id="9848e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9848e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9848e-105">Une application cliente prépare les destinataires en convertissant leurs identificateurs d'entrée à court terme en identificateurs d'entrée à long terme et éventuellement en ajoutant, en modifiant ou en réorganisant des propriétés.</span><span class="sxs-lookup"><span data-stu-id="9848e-105">A client application prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span> <span data-ttu-id="9848e-106">Vous pouvez préparer des destinataires qui font partie d'une liste de destinataires pour un message ou des destinataires qui ne sont pas liés à un message.</span><span class="sxs-lookup"><span data-stu-id="9848e-106">You can prepare recipients that are part of a recipient list for a message or recipients that are unrelated to a message.</span></span> <span data-ttu-id="9848e-107">En règle générale, les clients appellent [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) directement pour traduire des identificateurs d'entrée à court terme dans des identificateurs d'entrée à long terme pour les destinataires inclus dans la boîte de dialogue adresse commune.</span><span class="sxs-lookup"><span data-stu-id="9848e-107">Typically, clients call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) directly to translate short-term entry identifiers into long-term entry identifiers for recipients that are included in the common address dialog box.</span></span> <span data-ttu-id="9848e-108">Pour les destinataires associés à un message sortant, la préparation des destinataires est gérée par le processus de résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="9848e-108">For recipients that are associated with an outgoing message, recipient preparation is handled by the name resolution process.</span></span> 
  
<span data-ttu-id="9848e-109">Pour préparer une liste de destinataires, appelez **IAddrBook::P reparerecips**.</span><span class="sxs-lookup"><span data-stu-id="9848e-109">To prepare a list of recipients, call **IAddrBook::PrepareRecips**.</span></span> <span data-ttu-id="9848e-110">**PrepareRecips** accepte une structure [ADRLIST](adrlist.md) et une liste de balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="9848e-110">**PrepareRecips** accepts an [ADRLIST](adrlist.md) structure and a list of property tags.</span></span> <span data-ttu-id="9848e-111">La structure **ADRLIST** contient les destinataires à préparer tandis que la liste des balises de propriétés représente les propriétés que chaque destinataire doit prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="9848e-111">The **ADRLIST** structure contains the recipients to be prepared while the property tag list represents properties that each recipient should support.</span></span> <span data-ttu-id="9848e-112">**PrepareRecips** tente de placer les propriétés qui sont incluses dans la liste de balises de propriété au début de la structure **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="9848e-112">**PrepareRecips** attempts to place the properties that are included in the property tag list at the beginning of the **ADRLIST** structure.</span></span> <span data-ttu-id="9848e-113">Si certaines propriétés de la liste sont absentes de la structure **ADRLIST** , MAPI appelle le fournisseur de carnet d'adresses pour les fournir.</span><span class="sxs-lookup"><span data-stu-id="9848e-113">If any of the properties in the list are missing from the **ADRLIST** structure, MAPI calls the address book provider to supply them.</span></span> <span data-ttu-id="9848e-114">Si vous devez uniquement vérifier les identificateurs d'entrée à long terme, transmettez la valeur NULL pour le paramètre _lpSPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="9848e-114">If you only need to check for long-term entry identifiers, pass NULL for the  _lpSPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="9848e-115">Par exemple, supposons que vous travaillez avec cinq destinataires.</span><span class="sxs-lookup"><span data-stu-id="9848e-115">For example, suppose you are working with five recipients.</span></span> <span data-ttu-id="9848e-116">Les cinq destinataires s'affichent dans la structure **ADRLIST** avec les propriétés suivantes dans l'ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="9848e-116">All five recipients appear in the **ADRLIST** structure with the following properties in the following order:</span></span> 
  
1. <span data-ttu-id="9848e-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9848e-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
2. <span data-ttu-id="9848e-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9848e-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="9848e-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9848e-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
4. <span data-ttu-id="9848e-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9848e-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
5. <span data-ttu-id="9848e-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9848e-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
<span data-ttu-id="9848e-122">Trois autres propriétés sont incluses dans la structure **ADRLIST** pour les deux premiers destinataires.</span><span class="sxs-lookup"><span data-stu-id="9848e-122">Three other properties are included in the **ADRLIST** structure for the first two recipients.</span></span> 
  
1. <span data-ttu-id="9848e-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9848e-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span>
    
2. <span data-ttu-id="9848e-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9848e-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="9848e-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9848e-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span></span>
    
<span data-ttu-id="9848e-126">Étant donné que tous les destinataires doivent avoir les trois premières propriétés **PR_ADDRTYPE**, **PR_ENTRYID**et **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), créez un tableau de balises de propriété avec ces propriétés et transmettez et la structure **ADRLIST** à **PrepareRecips**.</span><span class="sxs-lookup"><span data-stu-id="9848e-126">Because all of the recipients need to have as their first three properties **PR_ADDRTYPE**, **PR_ENTRYID**, and **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), create a property tag array with these properties and pass it and the **ADRLIST** structure to **PrepareRecips**.</span></span> <span data-ttu-id="9848e-127">**PrepareRecips** appelle la méthode **IMAPIProp:: GetProps** de chaque destinataire pour extraire **PR_HOME_TELEPHONE_NUMBER** car elle ne fait actuellement pas partie de la structure **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="9848e-127">**PrepareRecips** calls each recipient's **IMAPIProp::GetProps** method to retrieve **PR_HOME_TELEPHONE_NUMBER** because it is not currently part of the **ADRLIST** structure.</span></span> <span data-ttu-id="9848e-128">Lorsque **PrepareRecips** renvoie, la liste de destinataires représente une liste fusionnée de destinataires avec les propriétés incluses dans la structure **ADRLIST** apparaissant en premier pour chaque destinataire.</span><span class="sxs-lookup"><span data-stu-id="9848e-128">When **PrepareRecips** returns, the recipient list represents a merged list of recipients with the properties included in the **ADRLIST** structure appearing first for each recipient.</span></span> 
  
<span data-ttu-id="9848e-129">La liste des destinataires 1 et 2 des destinataires inclut des propriétés dans l'ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="9848e-129">The recipient list for recipients 1 and 2 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="9848e-130">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="9848e-130">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="9848e-131">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="9848e-131">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="9848e-132">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="9848e-132">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="9848e-133">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="9848e-133">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="9848e-134">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="9848e-134">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="9848e-135">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="9848e-135">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="9848e-136">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="9848e-136">**PR_ADDRTYPE**</span></span>
    
8. <span data-ttu-id="9848e-137">**PR_ACCOUNT**</span><span class="sxs-lookup"><span data-stu-id="9848e-137">**PR_ACCOUNT**</span></span>
    
9. <span data-ttu-id="9848e-138">**PR_GIVEN_NAME**</span><span class="sxs-lookup"><span data-stu-id="9848e-138">**PR_GIVEN_NAME**</span></span>
    
10. <span data-ttu-id="9848e-139">**PR_SURNAME**</span><span class="sxs-lookup"><span data-stu-id="9848e-139">**PR_SURNAME**</span></span>
    
<span data-ttu-id="9848e-140">La liste des destinataires pour les destinataires 3, 4 et 5 inclut des propriétés dans l'ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="9848e-140">The recipient list for recipients 3, 4, and 5 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="9848e-141">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="9848e-141">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="9848e-142">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="9848e-142">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="9848e-143">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="9848e-143">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="9848e-144">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="9848e-144">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="9848e-145">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="9848e-145">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="9848e-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="9848e-146">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="9848e-147">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="9848e-147">**PR_ADDRTYPE**</span></span>
    
<span data-ttu-id="9848e-148">En guise d'alternative à l'appel de **IAddrBook::P reparerecips** pour utiliser les propriétés, appelez la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de chaque destinataire et, si nécessaire, sa méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="9848e-148">As an alternative to calling **IAddrBook::PrepareRecips** to work with properties, call each recipient's [IMAPIProp::GetProps](imapiprop-getprops.md) method and, if necessary, its [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="9848e-149">Lorsqu'un seul destinataire est impliqué, l'une ou l'autre technique est satisfaisante.</span><span class="sxs-lookup"><span data-stu-id="9848e-149">When only one recipient is involved, either technique is satisfactory.</span></span> <span data-ttu-id="9848e-150">Toutefois, lorsque plusieurs destinataires sont impliqués, le fait d'appeler **PrepareRecips** plutôt que les méthodes **IMAPIProp** permet de gagner du temps et, si vous utilisez à distance, de nombreux appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="9848e-150">However, when multiple recipients are involved, calling **PrepareRecips** rather than the **IMAPIProp** methods saves time and, if you are operating remotely, many remote procedure calls.</span></span> <span data-ttu-id="9848e-151">**PrepareRecips** traite tous les destinataires dans un appel unique, tandis que **GetProps** et **SetProps** effectuent un appel pour chaque destinataire.</span><span class="sxs-lookup"><span data-stu-id="9848e-151">**PrepareRecips** processes all recipients in a single call whereas **GetProps** and **SetProps** make one call for each recipient.</span></span> 
  

