---
title: IDistList IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IDistList
api_type:
- COM
ms.assetid: bd8e1ddb-3027-428b-8964-81614f80282d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7fee3c84d6a4d4a94397f5197f45637b0c7dd2be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783679"
---
# <a name="idistlist--imapicontainer"></a><span data-ttu-id="a405c-103">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="a405c-103">IDistList : IMAPIContainer</span></span>

  
  
<span data-ttu-id="a405c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a405c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a405c-105">Fournit des conteneurs du carnet d’accès aux listes de distribution dans la zone Adresse modifiable.</span><span class="sxs-lookup"><span data-stu-id="a405c-105">Provides access to distribution lists in modifiable address book containers.</span></span> <span data-ttu-id="a405c-106">**IDistList** peut créer, copier et supprimer des listes de distribution, en plus de la résolution de nom.</span><span class="sxs-lookup"><span data-stu-id="a405c-106">**IDistList** can create, copy, and delete distribution lists, in addition to performing name resolution.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a405c-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a405c-107">Header file:</span></span>  <br/> |<span data-ttu-id="a405c-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a405c-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a405c-109">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="a405c-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="a405c-110">Objets de liste de distribution</span><span class="sxs-lookup"><span data-stu-id="a405c-110">Distribution list objects</span></span>  <br/> |
|<span data-ttu-id="a405c-111">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="a405c-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="a405c-112">Fournisseurs de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="a405c-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="a405c-113">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="a405c-113">Called by:</span></span>  <br/> |<span data-ttu-id="a405c-114">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="a405c-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="a405c-115">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="a405c-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a405c-116">IID_IDistList</span><span class="sxs-lookup"><span data-stu-id="a405c-116">IID_IDistList</span></span>  <br/> |
|<span data-ttu-id="a405c-117">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="a405c-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="a405c-118">LPDISTLIST</span><span class="sxs-lookup"><span data-stu-id="a405c-118">LPDISTLIST</span></span>  <br/> |
|<span data-ttu-id="a405c-119">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="a405c-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="a405c-120">Traitées</span><span class="sxs-lookup"><span data-stu-id="a405c-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a405c-121">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="a405c-121">Vtable order</span></span>

<span data-ttu-id="a405c-122">Cette interface n’a pas de méthodes uniques.</span><span class="sxs-lookup"><span data-stu-id="a405c-122">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="a405c-123">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="a405c-123">**Required properties**</span></span>|<span data-ttu-id="a405c-124">**Access**</span><span class="sxs-lookup"><span data-stu-id="a405c-124">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a405c-125">**TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a405c-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a405c-126">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="a405c-126">Read/write</span></span>  <br/> |
|<span data-ttu-id="a405c-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a405c-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a405c-128">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="a405c-128">Read/write</span></span>  <br/> |
|<span data-ttu-id="a405c-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a405c-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a405c-130">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a405c-130">Read-only</span></span>  <br/> |
|<span data-ttu-id="a405c-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a405c-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a405c-132">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a405c-132">Read-only</span></span>  <br/> |
|<span data-ttu-id="a405c-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a405c-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a405c-134">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a405c-134">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a405c-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="a405c-135">Remarks</span></span>

<span data-ttu-id="a405c-136">L’interface **IDistList** hérite de [IMAPIContainer](imapicontainerimapiprop.md) et inclut les mêmes méthodes que les conteneurs de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="a405c-136">The **IDistList** interface inherits from [IMAPIContainer](imapicontainerimapiprop.md) and includes the same methods as address book containers.</span></span> <span data-ttu-id="a405c-137">Par conséquent, étant donné que les méthodes de l’interface **IDistList** sont identiques à celles de l’interface [IABContainer](iabcontainerimapicontainer.md) , ils ne sont pas dupliquées ici.</span><span class="sxs-lookup"><span data-stu-id="a405c-137">Therefore, because the methods of the **IDistList** interface are identical to those of the [IABContainer](iabcontainerimapicontainer.md) interface, they are not duplicated here.</span></span> 
  
<span data-ttu-id="a405c-138">Une liste de distribution ou un objet qui implémente **IDistList** est une collection d’objets utilisateur de la messagerie ou des destinataires individuels.</span><span class="sxs-lookup"><span data-stu-id="a405c-138">A distribution list or object that implements **IDistList** is a collection of messaging user objects, or individual recipients.</span></span> <span data-ttu-id="a405c-139">Une liste de distribution peut se composer de tous les objets utilisateur messagerie, ou un utilisateur de messagerie et des listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="a405c-139">A distribution list can consist of all messaging user objects, or some messaging user and some distribution lists.</span></span> 
  
<span data-ttu-id="a405c-140">Il existe généralement deux types de listes de distribution :</span><span class="sxs-lookup"><span data-stu-id="a405c-140">There are typically two types of distribution lists:</span></span>
  
- <span data-ttu-id="a405c-141">Listes de distribution sont développés par le système de messagerie sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="a405c-141">Distribution lists that are expanded by the underlying messaging system.</span></span> <span data-ttu-id="a405c-142">Ce type de liste possède une adresse, **ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) et est traité comme s’il s’agissait d’une personne de la même.</span><span class="sxs-lookup"><span data-stu-id="a405c-142">This type of list has an address, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and is treated the same as if it were an individual recipient.</span></span> 
    
- <span data-ttu-id="a405c-143">Listes de distribution qui existent dans un conteneur local et sont développés par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="a405c-143">Distribution lists that exist in a local container and are expanded by the client application.</span></span>
    
<span data-ttu-id="a405c-144">Propriétés de liste de distribution facultatifs sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="a405c-144">Optional distribution list properties include the following:</span></span>
  
- <span data-ttu-id="a405c-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a405c-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="a405c-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a405c-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="a405c-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a405c-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span></span> 
    
<span data-ttu-id="a405c-148">Notez que **TYPEADR_PR** est requis, mais n’est pas **ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a405c-148">Notice that **PR_ADDRTYPE** is required, but **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is not.</span></span> <span data-ttu-id="a405c-149">C’est parce qu’une liste de distribution sans une adresse de messagerie peut toujours recevoir des messages, mais sa liste de membres doit être développée.</span><span class="sxs-lookup"><span data-stu-id="a405c-149">That is because a distribution list without an email address can still receive messages, but its member list must be expanded.</span></span> <span data-ttu-id="a405c-150">Si la propriété **TYPEADR_PR** est définie à MAPIPDL, MAPI effectue le développement.</span><span class="sxs-lookup"><span data-stu-id="a405c-150">If the **PR_ADDRTYPE** property is set to MAPIPDL, MAPI performs the expansion.</span></span> <span data-ttu-id="a405c-151">Si **TYPEADR_PR** est une valeur autre que MAPIPDL, le fournisseur de transport effectue le développement.</span><span class="sxs-lookup"><span data-stu-id="a405c-151">If **PR_ADDRTYPE** is a value other than MAPIPDL, the transport provider performs the expansion.</span></span> 
  
<span data-ttu-id="a405c-152">Pour plus d’informations sur la façon d’utiliser les méthodes **IDistList** , voir les entrées de référence pour les méthodes parallèles de **IABContainer**.</span><span class="sxs-lookup"><span data-stu-id="a405c-152">For additional information about how to use the **IDistList** methods, see the reference entries for the parallel methods of **IABContainer**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a405c-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a405c-153">See also</span></span>



[<span data-ttu-id="a405c-154">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="a405c-154">MAPI Interfaces</span></span>](mapi-interfaces.md)

