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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 38094895fed03884b138b02d4aa1ed87bcc6ea9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575699"
---
# <a name="imapicontainer--imapiprop"></a><span data-ttu-id="4b590-103">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4b590-103">IMAPIContainer : IMAPIProp</span></span>

  
  
<span data-ttu-id="4b590-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b590-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b590-105">Gère les opérations de haut niveau sur les objets conteneur tels que des carnets d’adresses, des listes de distribution et des dossiers.</span><span class="sxs-lookup"><span data-stu-id="4b590-105">Manages high-level operations on container objects such as address books, distribution lists, and folders.</span></span> <span data-ttu-id="4b590-106">La [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), et [IDistList : IMAPIContainer](idistlistimapicontainer.md) **IMAPIContainer**proviennent des interfaces.</span><span class="sxs-lookup"><span data-stu-id="4b590-106">The [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), and [IDistList : IMAPIContainer](idistlistimapicontainer.md) interfaces are derived from **IMAPIContainer**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4b590-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="4b590-107">Header file:</span></span>  <br/> |<span data-ttu-id="4b590-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4b590-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4b590-109">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="4b590-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="4b590-110">Dossier conteneur de carnet d’adresses et les objets de liste de distribution</span><span class="sxs-lookup"><span data-stu-id="4b590-110">Folder, address book container, and distribution list objects</span></span>  <br/> |
|<span data-ttu-id="4b590-111">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="4b590-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="4b590-112">Banque de messages, carnet d’adresses et fournisseurs de transport à distance</span><span class="sxs-lookup"><span data-stu-id="4b590-112">Message store, address book, and remote transport providers</span></span>  <br/> |
|<span data-ttu-id="4b590-113">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="4b590-113">Called by:</span></span>  <br/> |<span data-ttu-id="4b590-114">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="4b590-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="4b590-115">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="4b590-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4b590-116">IID_IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="4b590-116">IID_IMAPIContainer</span></span>  <br/> |
|<span data-ttu-id="4b590-117">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="4b590-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="4b590-118">LPMAPICONTAINER</span><span class="sxs-lookup"><span data-stu-id="4b590-118">LPMAPICONTAINER</span></span>  <br/> |
|<span data-ttu-id="4b590-119">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="4b590-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="4b590-120">Classe abstraite, jamais implémentée</span><span class="sxs-lookup"><span data-stu-id="4b590-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4b590-121">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="4b590-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4b590-122">GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="4b590-122">GetContentsTable</span></span>](imapicontainer-getcontentstable.md) <br/> |<span data-ttu-id="4b590-123">Retourne un pointeur vers la table des matières du conteneur.</span><span class="sxs-lookup"><span data-stu-id="4b590-123">Returns a pointer to the container's contents table.</span></span>  <br/> |
|[<span data-ttu-id="4b590-124">GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="4b590-124">GetHierarchyTable</span></span>](imapicontainer-gethierarchytable.md) <br/> |<span data-ttu-id="4b590-125">Retourne un pointeur vers la table de hiérarchie du conteneur.</span><span class="sxs-lookup"><span data-stu-id="4b590-125">Returns a pointer to the container's hierarchy table.</span></span>  <br/> |
|[<span data-ttu-id="4b590-126">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="4b590-126">OpenEntry</span></span>](imapicontainer-openentry.md) <br/> |<span data-ttu-id="4b590-127">Ouvre un objet dans le conteneur, en retournant un pointeur d’interface pour l’accès des autres.</span><span class="sxs-lookup"><span data-stu-id="4b590-127">Opens an object in the container, returning an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="4b590-128">SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="4b590-128">SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md) <br/> |<span data-ttu-id="4b590-129">Définit les critères de recherche pour le conteneur.</span><span class="sxs-lookup"><span data-stu-id="4b590-129">Establishes search criteria for the container.</span></span>  <br/> |
|[<span data-ttu-id="4b590-130">GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="4b590-130">GetSearchCriteria</span></span>](imapicontainer-getsearchcriteria.md) <br/> |<span data-ttu-id="4b590-131">Obtient les critères de recherche pour le conteneur.</span><span class="sxs-lookup"><span data-stu-id="4b590-131">Obtains the search criteria for the container.</span></span>  <br/> |
   
|<span data-ttu-id="4b590-132">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="4b590-132">**Required properties**</span></span>|<span data-ttu-id="4b590-133">**Access**</span><span class="sxs-lookup"><span data-stu-id="4b590-133">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4b590-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4b590-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4b590-135">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b590-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="4b590-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4b590-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4b590-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b590-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="4b590-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4b590-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4b590-139">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="4b590-139">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4b590-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b590-140">See also</span></span>



[<span data-ttu-id="4b590-141">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="4b590-141">MAPI Interfaces</span></span>](mapi-interfaces.md)

