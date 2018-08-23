---
title: IAttach IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttach
api_type:
- COM
ms.assetid: f47e20e1-2a30-4c9e-8ca6-e8c5e72f44a1
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ce9c8b189991e4102fcc9d17b88747d4ce55efec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570911"
---
# <a name="iattach--imapiprop"></a><span data-ttu-id="e81d0-103">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e81d0-103">IAttach : IMAPIProp</span></span>

  
  
<span data-ttu-id="e81d0-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e81d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e81d0-105">Gère et donne accès aux propriétés des pièces jointes des messages.</span><span class="sxs-lookup"><span data-stu-id="e81d0-105">Maintains and provides access to the properties of attachments in messages.</span></span> <span data-ttu-id="e81d0-106">L’interface **IAttach** a aucune méthode unique qui lui est propre.</span><span class="sxs-lookup"><span data-stu-id="e81d0-106">The **IAttach** interface has no unique methods of its own.</span></span> <span data-ttu-id="e81d0-107">Pour plus d’informations sur l’utilisation des pièces jointes, voir [Les pièces jointes MAPI](mapi-attachments.md) et les [Tables des pièces jointes](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e81d0-107">For more information about how to use attachments, see [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e81d0-108">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e81d0-108">Header file:</span></span>  <br/> |<span data-ttu-id="e81d0-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e81d0-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e81d0-110">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="e81d0-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="e81d0-111">Objets Attachment</span><span class="sxs-lookup"><span data-stu-id="e81d0-111">Attachment objects</span></span>  <br/> |
|<span data-ttu-id="e81d0-112">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="e81d0-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="e81d0-113">Fournisseurs de banque de messages</span><span class="sxs-lookup"><span data-stu-id="e81d0-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="e81d0-114">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="e81d0-114">Called by:</span></span>  <br/> |<span data-ttu-id="e81d0-115">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="e81d0-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="e81d0-116">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="e81d0-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e81d0-117">IID_IAttachment</span><span class="sxs-lookup"><span data-stu-id="e81d0-117">IID_IAttachment</span></span>  <br/> |
|<span data-ttu-id="e81d0-118">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="e81d0-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="e81d0-119">LPATTACH</span><span class="sxs-lookup"><span data-stu-id="e81d0-119">LPATTACH</span></span>  <br/> |
|<span data-ttu-id="e81d0-120">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="e81d0-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="e81d0-121">Traitées</span><span class="sxs-lookup"><span data-stu-id="e81d0-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e81d0-122">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="e81d0-122">Vtable order</span></span>

<span data-ttu-id="e81d0-123">Cette interface n’a pas de méthodes uniques.</span><span class="sxs-lookup"><span data-stu-id="e81d0-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="e81d0-124">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="e81d0-124">**Required properties**</span></span>|<span data-ttu-id="e81d0-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="e81d0-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e81d0-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e81d0-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e81d0-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e81d0-127">Read-only</span></span>  <br/> |
|<span data-ttu-id="e81d0-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e81d0-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e81d0-129">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="e81d0-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="e81d0-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e81d0-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e81d0-131">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="e81d0-131">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e81d0-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e81d0-132">See also</span></span>



[<span data-ttu-id="e81d0-133">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="e81d0-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

