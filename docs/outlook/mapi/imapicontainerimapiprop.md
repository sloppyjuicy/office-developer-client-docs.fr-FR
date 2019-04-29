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
# <a name="imapicontainer--imapiprop"></a><span data-ttu-id="81958-103">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="81958-103">IMAPIContainer : IMAPIProp</span></span>

  
  
<span data-ttu-id="81958-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81958-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81958-105">Gère les opérations de haut niveau sur des objets conteneur, tels que des carnets d'adresses, des listes de distribution et des dossiers.</span><span class="sxs-lookup"><span data-stu-id="81958-105">Manages high-level operations on container objects such as address books, distribution lists, and folders.</span></span> <span data-ttu-id="81958-106">Les interfaces [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md), [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md)et [IDistList: IMAPIContainer](idistlistimapicontainer.md) sont dérivées de **IMAPIContainer**.</span><span class="sxs-lookup"><span data-stu-id="81958-106">The [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), and [IDistList : IMAPIContainer](idistlistimapicontainer.md) interfaces are derived from **IMAPIContainer**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="81958-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="81958-107">Header file:</span></span>  <br/> |<span data-ttu-id="81958-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="81958-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="81958-109">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="81958-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="81958-110">Objets de dossier, de carnet d'adresses et de liste de distribution</span><span class="sxs-lookup"><span data-stu-id="81958-110">Folder, address book container, and distribution list objects</span></span>  <br/> |
|<span data-ttu-id="81958-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="81958-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="81958-112">Banque de messages, carnet d'adresses et fournisseurs de transport à distance</span><span class="sxs-lookup"><span data-stu-id="81958-112">Message store, address book, and remote transport providers</span></span>  <br/> |
|<span data-ttu-id="81958-113">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="81958-113">Called by:</span></span>  <br/> |<span data-ttu-id="81958-114">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="81958-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="81958-115">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="81958-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="81958-116">IID_IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="81958-116">IID_IMAPIContainer</span></span>  <br/> |
|<span data-ttu-id="81958-117">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="81958-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="81958-118">LPMAPICONTAINER</span><span class="sxs-lookup"><span data-stu-id="81958-118">LPMAPICONTAINER</span></span>  <br/> |
|<span data-ttu-id="81958-119">Modèle de transaction:</span><span class="sxs-lookup"><span data-stu-id="81958-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="81958-120">Classe abstraite, jamais implémentée</span><span class="sxs-lookup"><span data-stu-id="81958-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="81958-121">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="81958-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="81958-122">GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="81958-122">GetContentsTable</span></span>](imapicontainer-getcontentstable.md) <br/> |<span data-ttu-id="81958-123">Renvoie un pointeur vers la table des matières du conteneur.</span><span class="sxs-lookup"><span data-stu-id="81958-123">Returns a pointer to the container's contents table.</span></span>  <br/> |
|[<span data-ttu-id="81958-124">GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="81958-124">GetHierarchyTable</span></span>](imapicontainer-gethierarchytable.md) <br/> |<span data-ttu-id="81958-125">Renvoie un pointeur vers la table de hiérarchie du conteneur.</span><span class="sxs-lookup"><span data-stu-id="81958-125">Returns a pointer to the container's hierarchy table.</span></span>  <br/> |
|[<span data-ttu-id="81958-126">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="81958-126">OpenEntry</span></span>](imapicontainer-openentry.md) <br/> |<span data-ttu-id="81958-127">Ouvre un objet dans le conteneur, en renvoyant un pointeur d'interface pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="81958-127">Opens an object in the container, returning an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="81958-128">SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="81958-128">SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md) <br/> |<span data-ttu-id="81958-129">Établit les critères de recherche pour le conteneur.</span><span class="sxs-lookup"><span data-stu-id="81958-129">Establishes search criteria for the container.</span></span>  <br/> |
|[<span data-ttu-id="81958-130">GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="81958-130">GetSearchCriteria</span></span>](imapicontainer-getsearchcriteria.md) <br/> |<span data-ttu-id="81958-131">Obtient les critères de recherche pour le conteneur.</span><span class="sxs-lookup"><span data-stu-id="81958-131">Obtains the search criteria for the container.</span></span>  <br/> |
   
|<span data-ttu-id="81958-132">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="81958-132">**Required properties**</span></span>|<span data-ttu-id="81958-133">**Accès**</span><span class="sxs-lookup"><span data-stu-id="81958-133">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="81958-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="81958-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="81958-135">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="81958-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="81958-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="81958-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="81958-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="81958-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="81958-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="81958-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="81958-139">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="81958-139">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="81958-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81958-140">See also</span></span>



[<span data-ttu-id="81958-141">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="81958-141">MAPI Interfaces</span></span>](mapi-interfaces.md)

