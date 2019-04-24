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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2ef3bc973e12bd5630cc00b3c512b748d4a16e86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341621"
---
# <a name="iattach--imapiprop"></a><span data-ttu-id="b2ef8-103">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b2ef8-103">IAttach : IMAPIProp</span></span>

  
  
<span data-ttu-id="b2ef8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2ef8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2ef8-105">Conserve et permet d'accéder aux propriétés des pièces jointes dans les messages.</span><span class="sxs-lookup"><span data-stu-id="b2ef8-105">Maintains and provides access to the properties of attachments in messages.</span></span> <span data-ttu-id="b2ef8-106">L'interface **IAttach** ne possède pas de méthodes uniques.</span><span class="sxs-lookup"><span data-stu-id="b2ef8-106">The **IAttach** interface has no unique methods of its own.</span></span> <span data-ttu-id="b2ef8-107">Pour plus d'informations sur l'utilisation des pièces jointes, consultez la rubrique [MAPI Attachments](mapi-attachments.md) and [Attachment tables](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b2ef8-107">For more information about how to use attachments, see [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2ef8-108">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b2ef8-108">Header file:</span></span>  <br/> |<span data-ttu-id="b2ef8-109">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b2ef8-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b2ef8-110">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="b2ef8-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="b2ef8-111">Objets Attachment</span><span class="sxs-lookup"><span data-stu-id="b2ef8-111">Attachment objects</span></span>  <br/> |
|<span data-ttu-id="b2ef8-112">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="b2ef8-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="b2ef8-113">Fournisseurs de banques de messages</span><span class="sxs-lookup"><span data-stu-id="b2ef8-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="b2ef8-114">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="b2ef8-114">Called by:</span></span>  <br/> |<span data-ttu-id="b2ef8-115">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="b2ef8-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="b2ef8-116">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="b2ef8-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b2ef8-117">IID_IAttachment</span><span class="sxs-lookup"><span data-stu-id="b2ef8-117">IID_IAttachment</span></span>  <br/> |
|<span data-ttu-id="b2ef8-118">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="b2ef8-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="b2ef8-119">LPATTACH</span><span class="sxs-lookup"><span data-stu-id="b2ef8-119">LPATTACH</span></span>  <br/> |
|<span data-ttu-id="b2ef8-120">Modèle de transaction:</span><span class="sxs-lookup"><span data-stu-id="b2ef8-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="b2ef8-121">Traitées</span><span class="sxs-lookup"><span data-stu-id="b2ef8-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b2ef8-122">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="b2ef8-122">Vtable order</span></span>

<span data-ttu-id="b2ef8-123">Cette interface n'a pas de méthodes uniques.</span><span class="sxs-lookup"><span data-stu-id="b2ef8-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="b2ef8-124">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="b2ef8-124">**Required properties**</span></span>|<span data-ttu-id="b2ef8-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="b2ef8-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b2ef8-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b2ef8-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b2ef8-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2ef8-127">Read-only</span></span>  <br/> |
|<span data-ttu-id="b2ef8-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b2ef8-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b2ef8-129">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="b2ef8-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="b2ef8-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b2ef8-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b2ef8-131">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="b2ef8-131">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b2ef8-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2ef8-132">See also</span></span>



[<span data-ttu-id="b2ef8-133">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="b2ef8-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

