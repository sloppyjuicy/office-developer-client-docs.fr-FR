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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 463d81a6692b6071cada0ad22e7343020563e41c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431546"
---
# <a name="idistlist--imapicontainer"></a><span data-ttu-id="07bee-103">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="07bee-103">IDistList : IMAPIContainer</span></span>

  
  
<span data-ttu-id="07bee-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07bee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07bee-105">Permet d'accéder à des listes de distribution dans des conteneurs de carnet d'adresses modifiables.</span><span class="sxs-lookup"><span data-stu-id="07bee-105">Provides access to distribution lists in modifiable address book containers.</span></span> <span data-ttu-id="07bee-106">**IDistList** peut créer, copier et supprimer des listes de distribution, en plus d'effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="07bee-106">**IDistList** can create, copy, and delete distribution lists, in addition to performing name resolution.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07bee-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="07bee-107">Header file:</span></span>  <br/> |<span data-ttu-id="07bee-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="07bee-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="07bee-109">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="07bee-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="07bee-110">Objets de liste de distribution</span><span class="sxs-lookup"><span data-stu-id="07bee-110">Distribution list objects</span></span>  <br/> |
|<span data-ttu-id="07bee-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="07bee-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="07bee-112">Fournisseurs de carnets d'adresses</span><span class="sxs-lookup"><span data-stu-id="07bee-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="07bee-113">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="07bee-113">Called by:</span></span>  <br/> |<span data-ttu-id="07bee-114">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="07bee-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="07bee-115">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="07bee-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="07bee-116">IID_IDistList</span><span class="sxs-lookup"><span data-stu-id="07bee-116">IID_IDistList</span></span>  <br/> |
|<span data-ttu-id="07bee-117">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="07bee-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="07bee-118">LPDISTLIST</span><span class="sxs-lookup"><span data-stu-id="07bee-118">LPDISTLIST</span></span>  <br/> |
|<span data-ttu-id="07bee-119">Modèle de transaction:</span><span class="sxs-lookup"><span data-stu-id="07bee-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="07bee-120">Traitées</span><span class="sxs-lookup"><span data-stu-id="07bee-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="07bee-121">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="07bee-121">Vtable order</span></span>

<span data-ttu-id="07bee-122">Cette interface n'a pas de méthodes uniques.</span><span class="sxs-lookup"><span data-stu-id="07bee-122">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="07bee-123">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="07bee-123">**Required properties**</span></span>|<span data-ttu-id="07bee-124">**Accès**</span><span class="sxs-lookup"><span data-stu-id="07bee-124">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="07bee-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="07bee-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="07bee-126">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="07bee-126">Read/write</span></span>  <br/> |
|<span data-ttu-id="07bee-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="07bee-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="07bee-128">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="07bee-128">Read/write</span></span>  <br/> |
|<span data-ttu-id="07bee-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="07bee-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="07bee-130">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="07bee-130">Read-only</span></span>  <br/> |
|<span data-ttu-id="07bee-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="07bee-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="07bee-132">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="07bee-132">Read-only</span></span>  <br/> |
|<span data-ttu-id="07bee-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="07bee-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="07bee-134">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="07bee-134">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07bee-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="07bee-135">Remarks</span></span>

<span data-ttu-id="07bee-136">L'interface **IDistList** hérite de [IMAPIContainer](imapicontainerimapiprop.md) et inclut les mêmes méthodes que les conteneurs de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="07bee-136">The **IDistList** interface inherits from [IMAPIContainer](imapicontainerimapiprop.md) and includes the same methods as address book containers.</span></span> <span data-ttu-id="07bee-137">Par conséquent, étant donné que les méthodes de l'interface **IDistList** sont identiques à celles de l'interface [IABContainer](iabcontainerimapicontainer.md) , elles ne sont pas dupliquées ici.</span><span class="sxs-lookup"><span data-stu-id="07bee-137">Therefore, because the methods of the **IDistList** interface are identical to those of the [IABContainer](iabcontainerimapicontainer.md) interface, they are not duplicated here.</span></span> 
  
<span data-ttu-id="07bee-138">Une liste de distribution ou un objet qui implémente **IDistList** est une collection d'objets utilisateur de messagerie ou de destinataires individuels.</span><span class="sxs-lookup"><span data-stu-id="07bee-138">A distribution list or object that implements **IDistList** is a collection of messaging user objects, or individual recipients.</span></span> <span data-ttu-id="07bee-139">Une liste de distribution peut être constituée de tous les objets utilisateur de messagerie ou d'un utilisateur de messagerie et de certaines listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="07bee-139">A distribution list can consist of all messaging user objects, or some messaging user and some distribution lists.</span></span> 
  
<span data-ttu-id="07bee-140">Il existe généralement deux types de listes de distribution:</span><span class="sxs-lookup"><span data-stu-id="07bee-140">There are typically two types of distribution lists:</span></span>
  
- <span data-ttu-id="07bee-141">Listes de distribution qui sont développées par le système de messagerie sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="07bee-141">Distribution lists that are expanded by the underlying messaging system.</span></span> <span data-ttu-id="07bee-142">Ce type de liste a une adresse, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) et est traité de la même manière que s'il s'agissait d'un destinataire individuel.</span><span class="sxs-lookup"><span data-stu-id="07bee-142">This type of list has an address, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and is treated the same as if it were an individual recipient.</span></span> 
    
- <span data-ttu-id="07bee-143">Les listes de distribution qui existent dans un conteneur local et sont développées par l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="07bee-143">Distribution lists that exist in a local container and are expanded by the client application.</span></span>
    
<span data-ttu-id="07bee-144">Les propriétés de liste de distribution facultatives sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="07bee-144">Optional distribution list properties include the following:</span></span>
  
- <span data-ttu-id="07bee-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="07bee-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="07bee-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="07bee-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="07bee-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="07bee-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span></span> 
    
<span data-ttu-id="07bee-148">Notez que **PR_ADDRTYPE** est requis, mais que **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) ne l'est pas.</span><span class="sxs-lookup"><span data-stu-id="07bee-148">Notice that **PR_ADDRTYPE** is required, but **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is not.</span></span> <span data-ttu-id="07bee-149">En effet, une liste de distribution sans adresse de messagerie peut toujours recevoir des messages, mais sa liste de membres doit être développée.</span><span class="sxs-lookup"><span data-stu-id="07bee-149">That is because a distribution list without an email address can still receive messages, but its member list must be expanded.</span></span> <span data-ttu-id="07bee-150">Si la propriété **PR_ADDRTYPE** est définie sur MAPIPDL, MAPI effectue l'expansion.</span><span class="sxs-lookup"><span data-stu-id="07bee-150">If the **PR_ADDRTYPE** property is set to MAPIPDL, MAPI performs the expansion.</span></span> <span data-ttu-id="07bee-151">Si **PR_ADDRTYPE** est une valeur autre que MAPIPDL, le fournisseur de transport effectue l'expansion.</span><span class="sxs-lookup"><span data-stu-id="07bee-151">If **PR_ADDRTYPE** is a value other than MAPIPDL, the transport provider performs the expansion.</span></span> 
  
<span data-ttu-id="07bee-152">Pour plus d'informations sur l'utilisation des méthodes **IDistList** , voir les entrées de référence pour les méthodes parallèles de **IABContainer**.</span><span class="sxs-lookup"><span data-stu-id="07bee-152">For additional information about how to use the **IDistList** methods, see the reference entries for the parallel methods of **IABContainer**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="07bee-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07bee-153">See also</span></span>



[<span data-ttu-id="07bee-154">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="07bee-154">MAPI Interfaces</span></span>](mapi-interfaces.md)

