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
# <a name="idistlist--imapicontainer"></a><span data-ttu-id="f18c6-103">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="f18c6-103">IDistList : IMAPIContainer</span></span>

  
  
<span data-ttu-id="f18c6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f18c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f18c6-105">Permet d’accéder aux listes de distribution dans les conteneurs de carnet d’adresses modifiables.</span><span class="sxs-lookup"><span data-stu-id="f18c6-105">Provides access to distribution lists in modifiable address book containers.</span></span> <span data-ttu-id="f18c6-106">**IDistList peut** créer, copier et supprimer des listes de distribution, en plus d’effectuer une résolution de nom.</span><span class="sxs-lookup"><span data-stu-id="f18c6-106">**IDistList** can create, copy, and delete distribution lists, in addition to performing name resolution.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f18c6-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f18c6-107">Header file:</span></span>  <br/> |<span data-ttu-id="f18c6-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f18c6-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f18c6-109">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="f18c6-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="f18c6-110">Objets de liste de distribution</span><span class="sxs-lookup"><span data-stu-id="f18c6-110">Distribution list objects</span></span>  <br/> |
|<span data-ttu-id="f18c6-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="f18c6-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="f18c6-112">Fournisseurs de carnets d’adresses</span><span class="sxs-lookup"><span data-stu-id="f18c6-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="f18c6-113">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="f18c6-113">Called by:</span></span>  <br/> |<span data-ttu-id="f18c6-114">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="f18c6-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="f18c6-115">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="f18c6-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="f18c6-116">IID_IDistList</span><span class="sxs-lookup"><span data-stu-id="f18c6-116">IID_IDistList</span></span>  <br/> |
|<span data-ttu-id="f18c6-117">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="f18c6-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="f18c6-118">LPDISTLIST</span><span class="sxs-lookup"><span data-stu-id="f18c6-118">LPDISTLIST</span></span>  <br/> |
|<span data-ttu-id="f18c6-119">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="f18c6-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="f18c6-120">Transacted</span><span class="sxs-lookup"><span data-stu-id="f18c6-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="f18c6-121">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="f18c6-121">Vtable order</span></span>

<span data-ttu-id="f18c6-122">Cette interface n’a pas de méthode unique.</span><span class="sxs-lookup"><span data-stu-id="f18c6-122">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="f18c6-123">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="f18c6-123">**Required properties**</span></span>|<span data-ttu-id="f18c6-124">**Access**</span><span class="sxs-lookup"><span data-stu-id="f18c6-124">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f18c6-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f18c6-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f18c6-126">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f18c6-126">Read/write</span></span>  <br/> |
|<span data-ttu-id="f18c6-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f18c6-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f18c6-128">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f18c6-128">Read/write</span></span>  <br/> |
|<span data-ttu-id="f18c6-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f18c6-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f18c6-130">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f18c6-130">Read-only</span></span>  <br/> |
|<span data-ttu-id="f18c6-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f18c6-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f18c6-132">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f18c6-132">Read-only</span></span>  <br/> |
|<span data-ttu-id="f18c6-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f18c6-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f18c6-134">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f18c6-134">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f18c6-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="f18c6-135">Remarks</span></span>

<span data-ttu-id="f18c6-136">**L’interface IDistList** hérite d’IMAPIContainer et inclut les mêmes méthodes que les conteneurs de carnet d’adresses. [](imapicontainerimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="f18c6-136">The **IDistList** interface inherits from [IMAPIContainer](imapicontainerimapiprop.md) and includes the same methods as address book containers.</span></span> <span data-ttu-id="f18c6-137">Par conséquent, étant donné que les méthodes de l’interface **IDistList** sont identiques à celles de l’interface [IABContainer,](iabcontainerimapicontainer.md) elles ne sont pas dupliquées ici.</span><span class="sxs-lookup"><span data-stu-id="f18c6-137">Therefore, because the methods of the **IDistList** interface are identical to those of the [IABContainer](iabcontainerimapicontainer.md) interface, they are not duplicated here.</span></span> 
  
<span data-ttu-id="f18c6-138">Une liste de distribution ou un objet qui implémente **IDistList** est une collection d’objets utilisateur de messagerie ou de destinataires individuels.</span><span class="sxs-lookup"><span data-stu-id="f18c6-138">A distribution list or object that implements **IDistList** is a collection of messaging user objects, or individual recipients.</span></span> <span data-ttu-id="f18c6-139">Une liste de distribution peut se composer de tous les objets utilisateur de messagerie, ou d’un utilisateur de messagerie et de certaines listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="f18c6-139">A distribution list can consist of all messaging user objects, or some messaging user and some distribution lists.</span></span> 
  
<span data-ttu-id="f18c6-140">Il existe généralement deux types de listes de distribution :</span><span class="sxs-lookup"><span data-stu-id="f18c6-140">There are typically two types of distribution lists:</span></span>
  
- <span data-ttu-id="f18c6-141">Listes de distribution étendues par le système de messagerie sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="f18c6-141">Distribution lists that are expanded by the underlying messaging system.</span></span> <span data-ttu-id="f18c6-142">Ce type de liste a une adresse, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), et est traité comme s’il s’agit d’un destinataire individuel.</span><span class="sxs-lookup"><span data-stu-id="f18c6-142">This type of list has an address, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and is treated the same as if it were an individual recipient.</span></span> 
    
- <span data-ttu-id="f18c6-143">Listes de distribution qui existent dans un conteneur local et qui sont étendues par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="f18c6-143">Distribution lists that exist in a local container and are expanded by the client application.</span></span>
    
<span data-ttu-id="f18c6-144">Les propriétés facultatives de la liste de distribution sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f18c6-144">Optional distribution list properties include the following:</span></span>
  
- <span data-ttu-id="f18c6-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f18c6-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="f18c6-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f18c6-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="f18c6-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f18c6-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span></span> 
    
<span data-ttu-id="f18c6-148">Notez **que PR_ADDRTYPE** est obligatoire, mais **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) ne l’est pas.</span><span class="sxs-lookup"><span data-stu-id="f18c6-148">Notice that **PR_ADDRTYPE** is required, but **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is not.</span></span> <span data-ttu-id="f18c6-149">En effet, une liste de distribution sans adresse de messagerie peut toujours recevoir des messages, mais sa liste de membres doit être étendue.</span><span class="sxs-lookup"><span data-stu-id="f18c6-149">That is because a distribution list without an email address can still receive messages, but its member list must be expanded.</span></span> <span data-ttu-id="f18c6-150">Si la **PR_ADDRTYPE** est définie sur MAPIPDL, MAPI effectue l’expansion.</span><span class="sxs-lookup"><span data-stu-id="f18c6-150">If the **PR_ADDRTYPE** property is set to MAPIPDL, MAPI performs the expansion.</span></span> <span data-ttu-id="f18c6-151">Si **PR_ADDRTYPE** est une valeur autre que MAPIPDL, le fournisseur de transport effectue l’expansion.</span><span class="sxs-lookup"><span data-stu-id="f18c6-151">If **PR_ADDRTYPE** is a value other than MAPIPDL, the transport provider performs the expansion.</span></span> 
  
<span data-ttu-id="f18c6-152">Pour plus d’informations sur l’utilisation des méthodes **IDistList,** voir les entrées de référence pour les méthodes parallèles de **IABContainer**.</span><span class="sxs-lookup"><span data-stu-id="f18c6-152">For additional information about how to use the **IDistList** methods, see the reference entries for the parallel methods of **IABContainer**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f18c6-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f18c6-153">See also</span></span>



[<span data-ttu-id="f18c6-154">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="f18c6-154">MAPI Interfaces</span></span>](mapi-interfaces.md)

