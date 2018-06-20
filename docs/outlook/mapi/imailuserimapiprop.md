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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0c70d16d294426d30f3ac5f00b6bc46992386a86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783693"
---
# <a name="imailuser--imapiprop"></a><span data-ttu-id="c03ec-103">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c03ec-103">IMailUser : IMAPIProp</span></span>

  
  
<span data-ttu-id="c03ec-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c03ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c03ec-105">Permet d’accéder aux nombreuses propriétés qui sont associés à des utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="c03ec-105">Provides access to the many properties that are associated with messaging users.</span></span> <span data-ttu-id="c03ec-106">L’interface **IMailUser** est implémentée par les objets utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="c03ec-106">The **IMailUser** interface is implemented by messaging user objects.</span></span> <span data-ttu-id="c03ec-107">**IMailUser** hérite de la [IMAPIProp : IUnknown](imapipropiunknown.md) interface et n’a aucune méthode unique qui lui est propre.</span><span class="sxs-lookup"><span data-stu-id="c03ec-107">**IMailUser** inherits from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface and has no unique methods of its own.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c03ec-108">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c03ec-108">Header file:</span></span>  <br/> |<span data-ttu-id="c03ec-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c03ec-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c03ec-110">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="c03ec-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="c03ec-111">Objets utilisateur de messagerie</span><span class="sxs-lookup"><span data-stu-id="c03ec-111">Messaging user objects</span></span>  <br/> |
|<span data-ttu-id="c03ec-112">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="c03ec-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="c03ec-113">Fournisseurs de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="c03ec-113">Address book providers</span></span>  <br/> |
|<span data-ttu-id="c03ec-114">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="c03ec-114">Called by:</span></span>  <br/> |<span data-ttu-id="c03ec-115">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="c03ec-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="c03ec-116">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="c03ec-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c03ec-117">IID_IMailUser</span><span class="sxs-lookup"><span data-stu-id="c03ec-117">IID_IMailUser</span></span>  <br/> |
|<span data-ttu-id="c03ec-118">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="c03ec-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="c03ec-119">LPMAILUSER</span><span class="sxs-lookup"><span data-stu-id="c03ec-119">LPMAILUSER</span></span>  <br/> |
|<span data-ttu-id="c03ec-120">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="c03ec-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="c03ec-121">Traitées</span><span class="sxs-lookup"><span data-stu-id="c03ec-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c03ec-122">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="c03ec-122">Vtable order</span></span>

<span data-ttu-id="c03ec-123">Cette interface n’a pas de méthodes uniques.</span><span class="sxs-lookup"><span data-stu-id="c03ec-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="c03ec-124">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="c03ec-124">**Required properties**</span></span>|<span data-ttu-id="c03ec-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="c03ec-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c03ec-126">**TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c03ec-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c03ec-127">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="c03ec-127">Read/write</span></span>  <br/> |
|<span data-ttu-id="c03ec-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c03ec-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c03ec-129">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="c03ec-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="c03ec-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c03ec-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c03ec-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c03ec-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="c03ec-132">**ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c03ec-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c03ec-133">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="c03ec-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="c03ec-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c03ec-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c03ec-135">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c03ec-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="c03ec-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c03ec-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c03ec-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c03ec-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="c03ec-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c03ec-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c03ec-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c03ec-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="c03ec-140">**Clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c03ec-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c03ec-141">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c03ec-141">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c03ec-142">Remarques</span><span class="sxs-lookup"><span data-stu-id="c03ec-142">Remarks</span></span>

<span data-ttu-id="c03ec-143">Cinq propriétés requises sont appelées les propriétés d’adresse de base pour les destinataires :</span><span class="sxs-lookup"><span data-stu-id="c03ec-143">Five of the required properties are known as the base address properties for recipients:</span></span>
  
- <span data-ttu-id="c03ec-144">**TYPEADR_PR**</span><span class="sxs-lookup"><span data-stu-id="c03ec-144">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="c03ec-145">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="c03ec-145">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="c03ec-146">**ADRESSE_EMAIL_PR**</span><span class="sxs-lookup"><span data-stu-id="c03ec-146">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="c03ec-147">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="c03ec-147">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="c03ec-148">**CLÉ PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="c03ec-148">**PR_SEARCH_KEY**</span></span>
    
<span data-ttu-id="c03ec-149">Ces propriétés sont considérés comme spéciale car de nombreux autres groupes de propriétés similaires sont créées d’après ce groupe de base.</span><span class="sxs-lookup"><span data-stu-id="c03ec-149">These properties are considered special because many other groups of similar properties are built upon this base group.</span></span> <span data-ttu-id="c03ec-150">Les autres groupes sont utilisés pour décrire un destinataire dans différents rôles, comme un message s d’origine ou déléguer l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="c03ec-150">The other groups are used to describe a recipient in various roles, such as a message's original or delegate sender.</span></span> <span data-ttu-id="c03ec-151">Pour plus d’informations sur ces propriétés et comment les utiliser, voir [Types d’adresses MAPI](mapi-address-types.md).</span><span class="sxs-lookup"><span data-stu-id="c03ec-151">For more information about these properties and how to use them, see [MAPI Address Types](mapi-address-types.md).</span></span>
  
<span data-ttu-id="c03ec-152">Les utilisateurs de messagerie peut afficher une collection de leurs propriétés en prenant en charge la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c03ec-152">Messaging users can display a collection of their properties by supporting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="c03ec-153">**PR_DETAILS_TABLE** est une table d’affichage qui décrit la disposition d’une boîte de dialogue Détails ou une page de propriétés à onglets qui affiche des informations sur les propriétés de destinataire.</span><span class="sxs-lookup"><span data-stu-id="c03ec-153">**PR_DETAILS_TABLE** is a display table that describes the layout of a details dialog box or a tabbed property page that displays recipient property information.</span></span> <span data-ttu-id="c03ec-154">MAPI crée les boîtes de dialogue Détails lorsqu’un client appelle la méthode [IAddrBook::Details](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="c03ec-154">MAPI creates details dialog boxes when a client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="c03ec-155">Objets d’utilisateur de messagerie peuvent avoir les propriétés facultatives associées.</span><span class="sxs-lookup"><span data-stu-id="c03ec-155">Messaging user objects can have other optional properties associated with them.</span></span> <span data-ttu-id="c03ec-156">MAPI définit de nombreuses propriétés qui fournissent des informations d’adressage supplémentaires à propos d’un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="c03ec-156">MAPI defines many properties that provide additional addressing information about a messaging user.</span></span> <span data-ttu-id="c03ec-157">Toutes ces propriétés sont des chaînes de caractères.</span><span class="sxs-lookup"><span data-stu-id="c03ec-157">All of these properties are character strings.</span></span> <span data-ttu-id="c03ec-158">La liste suivante affiche les propriétés les plus couramment utilisées :</span><span class="sxs-lookup"><span data-stu-id="c03ec-158">The following list shows the more commonly used properties:</span></span>
  
- <span data-ttu-id="c03ec-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c03ec-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span> 
    
- <span data-ttu-id="c03ec-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c03ec-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span></span> 
    
- <span data-ttu-id="c03ec-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c03ec-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="c03ec-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c03ec-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="c03ec-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c03ec-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="c03ec-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c03ec-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span></span> 
    
- <span data-ttu-id="c03ec-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c03ec-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span></span> 
    
<span data-ttu-id="c03ec-166">Pour obtenir une liste complète des propriétés, voir [Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md).</span><span class="sxs-lookup"><span data-stu-id="c03ec-166">For a complete list of properties, see [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c03ec-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c03ec-167">See also</span></span>



[<span data-ttu-id="c03ec-168">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="c03ec-168">MAPI Interfaces</span></span>](mapi-interfaces.md)

