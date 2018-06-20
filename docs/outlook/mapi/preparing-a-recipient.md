---
title: Préparation d’un destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9573f10c-66e1-4e87-93f0-89687e906b8b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 51241009262471bf30f7d71e3108b896bbce8df7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786929"
---
# <a name="preparing-a-recipient"></a><span data-ttu-id="3ed30-103">Préparation d’un destinataire</span><span class="sxs-lookup"><span data-stu-id="3ed30-103">Preparing a Recipient</span></span>

  
  
<span data-ttu-id="3ed30-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3ed30-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3ed30-105">Une application cliente prépare les destinataires à convertir leurs identificateurs d’entrée à court terme identificateurs d’entrée à long terme et éventuellement l’ajout, modification ou réorganisation des propriétés.</span><span class="sxs-lookup"><span data-stu-id="3ed30-105">A client application prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span> <span data-ttu-id="3ed30-106">Vous pouvez préparer des destinataires qui font partie d’une liste de destinataires pour un message ou des destinataires qui ne sont pas liés à un message.</span><span class="sxs-lookup"><span data-stu-id="3ed30-106">You can prepare recipients that are part of a recipient list for a message or recipients that are unrelated to a message.</span></span> <span data-ttu-id="3ed30-107">En règle générale, les clients appeler [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) directement pour convertir les identificateurs d’entrée à court terme en identificateurs d’entrée à long terme pour les destinataires qui sont inclus dans la boîte de dialogue adresses.</span><span class="sxs-lookup"><span data-stu-id="3ed30-107">Typically, clients call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) directly to translate short-term entry identifiers into long-term entry identifiers for recipients that are included in the common address dialog box.</span></span> <span data-ttu-id="3ed30-108">Pour les destinataires qui sont associés à un message sortant, la préparation d’un destinataire est gérée par le processus de résolution de nom.</span><span class="sxs-lookup"><span data-stu-id="3ed30-108">For recipients that are associated with an outgoing message, recipient preparation is handled by the name resolution process.</span></span> 
  
<span data-ttu-id="3ed30-109">Pour préparer une liste de destinataires, appelez **IAddrBook::PrepareRecips**.</span><span class="sxs-lookup"><span data-stu-id="3ed30-109">To prepare a list of recipients, call **IAddrBook::PrepareRecips**.</span></span> <span data-ttu-id="3ed30-110">**PrepareRecips** accepte une structure [ADRLIST](adrlist.md) et une liste des balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="3ed30-110">**PrepareRecips** accepts an [ADRLIST](adrlist.md) structure and a list of property tags.</span></span> <span data-ttu-id="3ed30-111">La structure **ADRLIST** contient les destinataires à préparer tandis que la liste de balise de propriété représente les propriétés de chaque destinataire doit prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="3ed30-111">The **ADRLIST** structure contains the recipients to be prepared while the property tag list represents properties that each recipient should support.</span></span> <span data-ttu-id="3ed30-112">Tente de placer les propriétés qui sont incluses dans la liste de balise de propriété au début de la structure **ADRLIST** **PrepareRecips** .</span><span class="sxs-lookup"><span data-stu-id="3ed30-112">**PrepareRecips** attempts to place the properties that are included in the property tag list at the beginning of the **ADRLIST** structure.</span></span> <span data-ttu-id="3ed30-113">Si une des propriétés de la liste est manquante dans la structure **ADRLIST** , le fournisseur de carnet d’adresses pour fournir les appels MAPI.</span><span class="sxs-lookup"><span data-stu-id="3ed30-113">If any of the properties in the list are missing from the **ADRLIST** structure, MAPI calls the address book provider to supply them.</span></span> <span data-ttu-id="3ed30-114">Si vous devez uniquement vérifier les identificateurs d’entrée à long terme, passez la valeur NULL pour le paramètre _lpSPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="3ed30-114">If you only need to check for long-term entry identifiers, pass NULL for the  _lpSPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="3ed30-115">Par exemple, supposons que vous travaillez avec des cinq destinataires.</span><span class="sxs-lookup"><span data-stu-id="3ed30-115">For example, suppose you are working with five recipients.</span></span> <span data-ttu-id="3ed30-116">Tous les cinq destinataires apparaissent dans la structure **ADRLIST** avec les propriétés suivantes dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="3ed30-116">All five recipients appear in the **ADRLIST** structure with the following properties in the following order:</span></span> 
  
1. <span data-ttu-id="3ed30-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3ed30-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
2. <span data-ttu-id="3ed30-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3ed30-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="3ed30-119">**Clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3ed30-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
4. <span data-ttu-id="3ed30-120">**ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3ed30-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
5. <span data-ttu-id="3ed30-121">**TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3ed30-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
<span data-ttu-id="3ed30-122">Trois autres propriétés sont incluses dans la structure **ADRLIST** pour les deux premiers destinataires.</span><span class="sxs-lookup"><span data-stu-id="3ed30-122">Three other properties are included in the **ADRLIST** structure for the first two recipients.</span></span> 
  
1. <span data-ttu-id="3ed30-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3ed30-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span>
    
2. <span data-ttu-id="3ed30-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3ed30-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="3ed30-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3ed30-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span></span>
    
<span data-ttu-id="3ed30-126">Étant donné que tous les destinataires doivent avoir en tant que leurs trois premiers propriétés **TYPEADR_PR**, **PR_ENTRYID**et **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), créez un tableau de balise de propriété avec ces propriétés et le secret elle et la structure **ADRLIST** à **PrepareRecips**.</span><span class="sxs-lookup"><span data-stu-id="3ed30-126">Because all of the recipients need to have as their first three properties **PR_ADDRTYPE**, **PR_ENTRYID**, and **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), create a property tag array with these properties and pass it and the **ADRLIST** structure to **PrepareRecips**.</span></span> <span data-ttu-id="3ed30-127">**PrepareRecips** appelle la méthode **IMAPIProp::GetProps** de chaque destinataire pour récupérer **PR_HOME_TELEPHONE_NUMBER** , car il n’est pas partie de la structure **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="3ed30-127">**PrepareRecips** calls each recipient's **IMAPIProp::GetProps** method to retrieve **PR_HOME_TELEPHONE_NUMBER** because it is not currently part of the **ADRLIST** structure.</span></span> <span data-ttu-id="3ed30-128">**PrepareRecips** retourne la liste des destinataires représente une liste de destinataires fusionnée avec les propriétés incluses dans la structure **ADRLIST** apparaissant en premier pour chaque destinataire.</span><span class="sxs-lookup"><span data-stu-id="3ed30-128">When **PrepareRecips** returns, the recipient list represents a merged list of recipients with the properties included in the **ADRLIST** structure appearing first for each recipient.</span></span> 
  
<span data-ttu-id="3ed30-129">La liste de destinataires pour les destinataires 1 et 2 comprend des propriétés dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="3ed30-129">The recipient list for recipients 1 and 2 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="3ed30-130">**TYPEADR_PR**</span><span class="sxs-lookup"><span data-stu-id="3ed30-130">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="3ed30-131">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="3ed30-131">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="3ed30-132">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="3ed30-132">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="3ed30-133">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="3ed30-133">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="3ed30-134">**CLÉ PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="3ed30-134">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="3ed30-135">**ADRESSE_EMAIL_PR**</span><span class="sxs-lookup"><span data-stu-id="3ed30-135">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="3ed30-136">**TYPEADR_PR**</span><span class="sxs-lookup"><span data-stu-id="3ed30-136">**PR_ADDRTYPE**</span></span>
    
8. <span data-ttu-id="3ed30-137">**PR_ACCOUNT**</span><span class="sxs-lookup"><span data-stu-id="3ed30-137">**PR_ACCOUNT**</span></span>
    
9. <span data-ttu-id="3ed30-138">**PR_GIVEN_NAME**</span><span class="sxs-lookup"><span data-stu-id="3ed30-138">**PR_GIVEN_NAME**</span></span>
    
10. <span data-ttu-id="3ed30-139">**PR_SURNAME**</span><span class="sxs-lookup"><span data-stu-id="3ed30-139">**PR_SURNAME**</span></span>
    
<span data-ttu-id="3ed30-140">La liste de destinataires pour les destinataires 3, 4 et 5 comprend des propriétés dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="3ed30-140">The recipient list for recipients 3, 4, and 5 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="3ed30-141">**TYPEADR_PR**</span><span class="sxs-lookup"><span data-stu-id="3ed30-141">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="3ed30-142">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="3ed30-142">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="3ed30-143">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="3ed30-143">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="3ed30-144">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="3ed30-144">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="3ed30-145">**CLÉ PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="3ed30-145">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="3ed30-146">**ADRESSE_EMAIL_PR**</span><span class="sxs-lookup"><span data-stu-id="3ed30-146">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="3ed30-147">**TYPEADR_PR**</span><span class="sxs-lookup"><span data-stu-id="3ed30-147">**PR_ADDRTYPE**</span></span>
    
<span data-ttu-id="3ed30-148">Comme alternative à l’appel **IAddrBook::PrepareRecips** pour utiliser des propriétés, appelez la méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) de chaque destinataire et, si nécessaire, la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="3ed30-148">As an alternative to calling **IAddrBook::PrepareRecips** to work with properties, call each recipient's [IMAPIProp::GetProps](imapiprop-getprops.md) method and, if necessary, its [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="3ed30-149">Lorsque qu’un seul destinataire est impliqué, deux méthodes sont satisfaisants.</span><span class="sxs-lookup"><span data-stu-id="3ed30-149">When only one recipient is involved, either technique is satisfactory.</span></span> <span data-ttu-id="3ed30-150">Toutefois, lorsque plusieurs destinataires sont impliqués, l’appel **PrepareRecips** plutôt que les méthodes **IMAPIProp** gagne du temps et, si vous travaillez à distance, plusieurs appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="3ed30-150">However, when multiple recipients are involved, calling **PrepareRecips** rather than the **IMAPIProp** methods saves time and, if you are operating remotely, many remote procedure calls.</span></span> <span data-ttu-id="3ed30-151">**PrepareRecips** traite tous les destinataires dans un seul appel tandis que **GetProps** et **SetProps** émettre un appel pour chaque destinataire.</span><span class="sxs-lookup"><span data-stu-id="3ed30-151">**PrepareRecips** processes all recipients in a single call whereas **GetProps** and **SetProps** make one call for each recipient.</span></span> 
  

