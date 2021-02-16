---
title: IMAPIContainer IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer
api_type:
- COM
ms.assetid: d83fdd83-3e86-43c8-a73f-8e9e01b53371
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8be3b1857d539f81e42d2ac3e5813afa73513a16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406121"
---
# <a name="imapicontainer--imapiprop"></a><span data-ttu-id="eafc5-103">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="eafc5-103">IMAPIContainer : IMAPIProp</span></span>

  
  
<span data-ttu-id="eafc5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eafc5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eafc5-105">Gère les opérations de haut niveau sur les objets conteneur tels que les carnets d’adresses, les listes de distribution et les dossiers.</span><span class="sxs-lookup"><span data-stu-id="eafc5-105">Manages high-level operations on container objects such as address books, distribution lists, and folders.</span></span> <span data-ttu-id="eafc5-106">Les interfaces [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)et [IDistList : IMAPIContainer](idistlistimapicontainer.md) sont dérivées d’IMAPIContainer . </span><span class="sxs-lookup"><span data-stu-id="eafc5-106">The [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), and [IDistList : IMAPIContainer](idistlistimapicontainer.md) interfaces are derived from **IMAPIContainer**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eafc5-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="eafc5-107">Header file:</span></span>  <br/> |<span data-ttu-id="eafc5-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eafc5-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="eafc5-109">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="eafc5-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="eafc5-110">Objets dossier, conteneur de carnet d’adresses et liste de distribution</span><span class="sxs-lookup"><span data-stu-id="eafc5-110">Folder, address book container, and distribution list objects</span></span>  <br/> |
|<span data-ttu-id="eafc5-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="eafc5-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="eafc5-112">Magasin de messages, carnet d’adresses et fournisseurs de transport distants</span><span class="sxs-lookup"><span data-stu-id="eafc5-112">Message store, address book, and remote transport providers</span></span>  <br/> |
|<span data-ttu-id="eafc5-113">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="eafc5-113">Called by:</span></span>  <br/> |<span data-ttu-id="eafc5-114">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="eafc5-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="eafc5-115">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="eafc5-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="eafc5-116">IID_IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="eafc5-116">IID_IMAPIContainer</span></span>  <br/> |
|<span data-ttu-id="eafc5-117">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="eafc5-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="eafc5-118">LPMAPICONTAINER</span><span class="sxs-lookup"><span data-stu-id="eafc5-118">LPMAPICONTAINER</span></span>  <br/> |
|<span data-ttu-id="eafc5-119">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="eafc5-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="eafc5-120">Classe abstraite, jamais implémentée</span><span class="sxs-lookup"><span data-stu-id="eafc5-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="eafc5-121">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="eafc5-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="eafc5-122">GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="eafc5-122">GetContentsTable</span></span>](imapicontainer-getcontentstable.md) <br/> |<span data-ttu-id="eafc5-123">Renvoie un pointeur vers la table des matières du conteneur.</span><span class="sxs-lookup"><span data-stu-id="eafc5-123">Returns a pointer to the container's contents table.</span></span>  <br/> |
|[<span data-ttu-id="eafc5-124">GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="eafc5-124">GetHierarchyTable</span></span>](imapicontainer-gethierarchytable.md) <br/> |<span data-ttu-id="eafc5-125">Renvoie un pointeur vers le tableau hiérarchique du conteneur.</span><span class="sxs-lookup"><span data-stu-id="eafc5-125">Returns a pointer to the container's hierarchy table.</span></span>  <br/> |
|[<span data-ttu-id="eafc5-126">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="eafc5-126">OpenEntry</span></span>](imapicontainer-openentry.md) <br/> |<span data-ttu-id="eafc5-127">Ouvre un objet dans le conteneur, renvoyant un pointeur d’interface pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="eafc5-127">Opens an object in the container, returning an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="eafc5-128">SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="eafc5-128">SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md) <br/> |<span data-ttu-id="eafc5-129">Établit des critères de recherche pour le conteneur.</span><span class="sxs-lookup"><span data-stu-id="eafc5-129">Establishes search criteria for the container.</span></span>  <br/> |
|[<span data-ttu-id="eafc5-130">GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="eafc5-130">GetSearchCriteria</span></span>](imapicontainer-getsearchcriteria.md) <br/> |<span data-ttu-id="eafc5-131">Obtient les critères de recherche pour le conteneur.</span><span class="sxs-lookup"><span data-stu-id="eafc5-131">Obtains the search criteria for the container.</span></span>  <br/> |
   
|<span data-ttu-id="eafc5-132">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="eafc5-132">**Required properties**</span></span>|<span data-ttu-id="eafc5-133">**Access**</span><span class="sxs-lookup"><span data-stu-id="eafc5-133">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eafc5-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eafc5-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eafc5-135">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eafc5-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="eafc5-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eafc5-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eafc5-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eafc5-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="eafc5-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eafc5-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eafc5-139">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="eafc5-139">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eafc5-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eafc5-140">See also</span></span>



[<span data-ttu-id="eafc5-141">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="eafc5-141">MAPI Interfaces</span></span>](mapi-interfaces.md)

