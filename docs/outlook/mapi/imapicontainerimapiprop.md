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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e24f5ebd73a4652876282099f1460762c150b94d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783701"
---
# <a name="imapicontainer--imapiprop"></a><span data-ttu-id="d46d5-103">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d46d5-103">IMAPIContainer : IMAPIProp</span></span>

  
  
<span data-ttu-id="d46d5-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d46d5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d46d5-105">Gère les opérations de haut niveau sur les objets conteneur tels que des carnets d’adresses, des listes de distribution et des dossiers.</span><span class="sxs-lookup"><span data-stu-id="d46d5-105">Manages high-level operations on container objects such as address books, distribution lists, and folders.</span></span> <span data-ttu-id="d46d5-106">La [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), et [IDistList : IMAPIContainer](idistlistimapicontainer.md) **IMAPIContainer**proviennent des interfaces.</span><span class="sxs-lookup"><span data-stu-id="d46d5-106">The [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), and [IDistList : IMAPIContainer](idistlistimapicontainer.md) interfaces are derived from **IMAPIContainer**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d46d5-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d46d5-107">Header file:</span></span>  <br/> |<span data-ttu-id="d46d5-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d46d5-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d46d5-109">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="d46d5-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="d46d5-110">Dossier conteneur de carnet d’adresses et les objets de liste de distribution</span><span class="sxs-lookup"><span data-stu-id="d46d5-110">Folder, address book container, and distribution list objects</span></span>  <br/> |
|<span data-ttu-id="d46d5-111">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="d46d5-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="d46d5-112">Banque de messages, carnet d’adresses et fournisseurs de transport à distance</span><span class="sxs-lookup"><span data-stu-id="d46d5-112">Message store, address book, and remote transport providers</span></span>  <br/> |
|<span data-ttu-id="d46d5-113">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="d46d5-113">Called by:</span></span>  <br/> |<span data-ttu-id="d46d5-114">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="d46d5-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="d46d5-115">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="d46d5-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d46d5-116">IID_IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="d46d5-116">IID_IMAPIContainer</span></span>  <br/> |
|<span data-ttu-id="d46d5-117">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="d46d5-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="d46d5-118">LPMAPICONTAINER</span><span class="sxs-lookup"><span data-stu-id="d46d5-118">LPMAPICONTAINER</span></span>  <br/> |
|<span data-ttu-id="d46d5-119">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="d46d5-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="d46d5-120">Classe abstraite, jamais implémentée</span><span class="sxs-lookup"><span data-stu-id="d46d5-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d46d5-121">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="d46d5-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="d46d5-122">GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="d46d5-122">GetContentsTable</span></span>](imapicontainer-getcontentstable.md) <br/> |<span data-ttu-id="d46d5-123">Retourne un pointeur vers la table des matières du conteneur.</span><span class="sxs-lookup"><span data-stu-id="d46d5-123">Returns a pointer to the container's contents table.</span></span>  <br/> |
|[<span data-ttu-id="d46d5-124">GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="d46d5-124">GetHierarchyTable</span></span>](imapicontainer-gethierarchytable.md) <br/> |<span data-ttu-id="d46d5-125">Retourne un pointeur vers la table de hiérarchie du conteneur.</span><span class="sxs-lookup"><span data-stu-id="d46d5-125">Returns a pointer to the container's hierarchy table.</span></span>  <br/> |
|[<span data-ttu-id="d46d5-126">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="d46d5-126">OpenEntry</span></span>](imapicontainer-openentry.md) <br/> |<span data-ttu-id="d46d5-127">Ouvre un objet dans le conteneur, en retournant un pointeur d’interface pour l’accès des autres.</span><span class="sxs-lookup"><span data-stu-id="d46d5-127">Opens an object in the container, returning an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="d46d5-128">SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="d46d5-128">SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md) <br/> |<span data-ttu-id="d46d5-129">Définit les critères de recherche pour le conteneur.</span><span class="sxs-lookup"><span data-stu-id="d46d5-129">Establishes search criteria for the container.</span></span>  <br/> |
|[<span data-ttu-id="d46d5-130">GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="d46d5-130">GetSearchCriteria</span></span>](imapicontainer-getsearchcriteria.md) <br/> |<span data-ttu-id="d46d5-131">Obtient les critères de recherche pour le conteneur.</span><span class="sxs-lookup"><span data-stu-id="d46d5-131">Obtains the search criteria for the container.</span></span>  <br/> |
   
|<span data-ttu-id="d46d5-132">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="d46d5-132">**Required properties**</span></span>|<span data-ttu-id="d46d5-133">**Access**</span><span class="sxs-lookup"><span data-stu-id="d46d5-133">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d46d5-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d46d5-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d46d5-135">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d46d5-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="d46d5-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d46d5-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d46d5-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d46d5-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="d46d5-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d46d5-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d46d5-139">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="d46d5-139">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d46d5-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d46d5-140">See also</span></span>



[<span data-ttu-id="d46d5-141">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="d46d5-141">MAPI Interfaces</span></span>](mapi-interfaces.md)

