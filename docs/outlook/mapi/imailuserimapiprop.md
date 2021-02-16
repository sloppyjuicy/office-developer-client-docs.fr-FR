---
title: IMailUser IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMailUser
api_type:
- COM
ms.assetid: 74c25870-62d9-484a-9a99-4dc35c52479e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a0e109fe95120483e700bab5b82f6d7cb75e2e28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436593"
---
# <a name="imailuser--imapiprop"></a><span data-ttu-id="3f68e-103">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3f68e-103">IMailUser : IMAPIProp</span></span>

  
  
<span data-ttu-id="3f68e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f68e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f68e-105">Permet d’accéder aux nombreuses propriétés associées aux utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="3f68e-105">Provides access to the many properties that are associated with messaging users.</span></span> <span data-ttu-id="3f68e-106">**L’interface IMailUser est** implémentée par les objets utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="3f68e-106">The **IMailUser** interface is implemented by messaging user objects.</span></span> <span data-ttu-id="3f68e-107">**IMailUser** hérite de l’interface [IMAPIProp : IUnknown](imapipropiunknown.md) et n’a aucune méthode unique propre.</span><span class="sxs-lookup"><span data-stu-id="3f68e-107">**IMailUser** inherits from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface and has no unique methods of its own.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3f68e-108">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="3f68e-108">Header file:</span></span>  <br/> |<span data-ttu-id="3f68e-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3f68e-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3f68e-110">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="3f68e-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="3f68e-111">Objets utilisateur de messagerie</span><span class="sxs-lookup"><span data-stu-id="3f68e-111">Messaging user objects</span></span>  <br/> |
|<span data-ttu-id="3f68e-112">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="3f68e-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="3f68e-113">Fournisseurs de carnets d’adresses</span><span class="sxs-lookup"><span data-stu-id="3f68e-113">Address book providers</span></span>  <br/> |
|<span data-ttu-id="3f68e-114">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="3f68e-114">Called by:</span></span>  <br/> |<span data-ttu-id="3f68e-115">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="3f68e-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="3f68e-116">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="3f68e-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3f68e-117">IID_IMailUser</span><span class="sxs-lookup"><span data-stu-id="3f68e-117">IID_IMailUser</span></span>  <br/> |
|<span data-ttu-id="3f68e-118">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="3f68e-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="3f68e-119">LPMAILUSER</span><span class="sxs-lookup"><span data-stu-id="3f68e-119">LPMAILUSER</span></span>  <br/> |
|<span data-ttu-id="3f68e-120">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="3f68e-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="3f68e-121">Transacted</span><span class="sxs-lookup"><span data-stu-id="3f68e-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3f68e-122">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="3f68e-122">Vtable order</span></span>

<span data-ttu-id="3f68e-123">Cette interface n’a pas de méthode unique.</span><span class="sxs-lookup"><span data-stu-id="3f68e-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="3f68e-124">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="3f68e-124">**Required properties**</span></span>|<span data-ttu-id="3f68e-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="3f68e-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3f68e-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f68e-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3f68e-127">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3f68e-127">Read/write</span></span>  <br/> |
|<span data-ttu-id="3f68e-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f68e-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3f68e-129">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3f68e-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="3f68e-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f68e-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3f68e-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f68e-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="3f68e-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f68e-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3f68e-133">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3f68e-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="3f68e-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f68e-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3f68e-135">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f68e-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="3f68e-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f68e-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3f68e-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f68e-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="3f68e-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f68e-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3f68e-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f68e-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="3f68e-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f68e-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3f68e-141">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f68e-141">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f68e-142">Remarques</span><span class="sxs-lookup"><span data-stu-id="3f68e-142">Remarks</span></span>

<span data-ttu-id="3f68e-143">Cinq des propriétés requises sont appelées propriétés d’adresse de base pour les destinataires :</span><span class="sxs-lookup"><span data-stu-id="3f68e-143">Five of the required properties are known as the base address properties for recipients:</span></span>
  
- <span data-ttu-id="3f68e-144">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="3f68e-144">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="3f68e-145">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="3f68e-145">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="3f68e-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="3f68e-146">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="3f68e-147">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="3f68e-147">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="3f68e-148">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="3f68e-148">**PR_SEARCH_KEY**</span></span>
    
<span data-ttu-id="3f68e-149">Ces propriétés sont considérées comme spéciales, car de nombreux autres groupes de propriétés similaires reposent sur ce groupe de base.</span><span class="sxs-lookup"><span data-stu-id="3f68e-149">These properties are considered special because many other groups of similar properties are built upon this base group.</span></span> <span data-ttu-id="3f68e-150">Les autres groupes sont utilisés pour décrire un destinataire dans différents rôles, tels que l’expéditeur d’origine ou l’expéditeur délégué d’un message.</span><span class="sxs-lookup"><span data-stu-id="3f68e-150">The other groups are used to describe a recipient in various roles, such as a message's original or delegate sender.</span></span> <span data-ttu-id="3f68e-151">Pour plus d’informations sur ces propriétés et leur utilisation, voir [Types d’adresses MAPI.](mapi-address-types.md)</span><span class="sxs-lookup"><span data-stu-id="3f68e-151">For more information about these properties and how to use them, see [MAPI Address Types](mapi-address-types.md).</span></span>
  
<span data-ttu-id="3f68e-152">Les utilisateurs de messagerie peuvent afficher une collection de leurs propriétés en PR_DETAILS_TABLE **la** propriété ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3f68e-152">Messaging users can display a collection of their properties by supporting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="3f68e-153">**PR_DETAILS_TABLE** est un tableau d’affichage qui décrit la disposition d’une boîte de dialogue détails ou d’une page de propriétés à onglets qui affiche les informations de propriété du destinataire.</span><span class="sxs-lookup"><span data-stu-id="3f68e-153">**PR_DETAILS_TABLE** is a display table that describes the layout of a details dialog box or a tabbed property page that displays recipient property information.</span></span> <span data-ttu-id="3f68e-154">MAPI crée des boîtes de dialogue de détails lorsqu’un client appelle la méthode [IAddrBook::D etails.](iaddrbook-details.md)</span><span class="sxs-lookup"><span data-stu-id="3f68e-154">MAPI creates details dialog boxes when a client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="3f68e-155">Les objets utilisateur de messagerie peuvent être associés à d’autres propriétés facultatives.</span><span class="sxs-lookup"><span data-stu-id="3f68e-155">Messaging user objects can have other optional properties associated with them.</span></span> <span data-ttu-id="3f68e-156">MAPI définit de nombreuses propriétés qui fournissent des informations d’adressa ment supplémentaires sur un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="3f68e-156">MAPI defines many properties that provide additional addressing information about a messaging user.</span></span> <span data-ttu-id="3f68e-157">Toutes ces propriétés sont des chaînes de caractères.</span><span class="sxs-lookup"><span data-stu-id="3f68e-157">All of these properties are character strings.</span></span> <span data-ttu-id="3f68e-158">La liste suivante présente les propriétés les plus couramment utilisées :</span><span class="sxs-lookup"><span data-stu-id="3f68e-158">The following list shows the more commonly used properties:</span></span>
  
- <span data-ttu-id="3f68e-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f68e-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span> 
    
- <span data-ttu-id="3f68e-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f68e-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span></span> 
    
- <span data-ttu-id="3f68e-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f68e-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="3f68e-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f68e-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="3f68e-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f68e-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="3f68e-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f68e-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span></span> 
    
- <span data-ttu-id="3f68e-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3f68e-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span></span> 
    
<span data-ttu-id="3f68e-166">Pour obtenir la liste complète des propriétés, voir [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md).</span><span class="sxs-lookup"><span data-stu-id="3f68e-166">For a complete list of properties, see [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3f68e-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f68e-167">See also</span></span>



[<span data-ttu-id="3f68e-168">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="3f68e-168">MAPI Interfaces</span></span>](mapi-interfaces.md)

