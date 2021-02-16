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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2ef3bc973e12bd5630cc00b3c512b748d4a16e86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409089"
---
# <a name="iattach--imapiprop"></a><span data-ttu-id="8dbb9-103">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8dbb9-103">IAttach : IMAPIProp</span></span>

  
  
<span data-ttu-id="8dbb9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8dbb9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8dbb9-105">Maintient et fournit l’accès aux propriétés des pièces jointes dans les messages.</span><span class="sxs-lookup"><span data-stu-id="8dbb9-105">Maintains and provides access to the properties of attachments in messages.</span></span> <span data-ttu-id="8dbb9-106">**L’interface IAttach** n’a aucune méthode unique.</span><span class="sxs-lookup"><span data-stu-id="8dbb9-106">The **IAttach** interface has no unique methods of its own.</span></span> <span data-ttu-id="8dbb9-107">Pour plus d’informations sur l’utilisation des pièces jointes, voir [Pièces jointes MAPI](mapi-attachments.md) et tables de pièces [jointes.](attachment-tables.md)</span><span class="sxs-lookup"><span data-stu-id="8dbb9-107">For more information about how to use attachments, see [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8dbb9-108">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8dbb9-108">Header file:</span></span>  <br/> |<span data-ttu-id="8dbb9-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8dbb9-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8dbb9-110">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="8dbb9-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="8dbb9-111">Objets de pièce jointe</span><span class="sxs-lookup"><span data-stu-id="8dbb9-111">Attachment objects</span></span>  <br/> |
|<span data-ttu-id="8dbb9-112">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="8dbb9-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="8dbb9-113">Fournisseurs de magasins de messages</span><span class="sxs-lookup"><span data-stu-id="8dbb9-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="8dbb9-114">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="8dbb9-114">Called by:</span></span>  <br/> |<span data-ttu-id="8dbb9-115">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="8dbb9-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="8dbb9-116">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="8dbb9-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8dbb9-117">IID_IAttachment</span><span class="sxs-lookup"><span data-stu-id="8dbb9-117">IID_IAttachment</span></span>  <br/> |
|<span data-ttu-id="8dbb9-118">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="8dbb9-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="8dbb9-119">LPATTACH</span><span class="sxs-lookup"><span data-stu-id="8dbb9-119">LPATTACH</span></span>  <br/> |
|<span data-ttu-id="8dbb9-120">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="8dbb9-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="8dbb9-121">Transacted</span><span class="sxs-lookup"><span data-stu-id="8dbb9-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8dbb9-122">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="8dbb9-122">Vtable order</span></span>

<span data-ttu-id="8dbb9-123">Cette interface n’a pas de méthode unique.</span><span class="sxs-lookup"><span data-stu-id="8dbb9-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="8dbb9-124">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="8dbb9-124">**Required properties**</span></span>|<span data-ttu-id="8dbb9-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="8dbb9-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8dbb9-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8dbb9-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8dbb9-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8dbb9-127">Read-only</span></span>  <br/> |
|<span data-ttu-id="8dbb9-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8dbb9-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8dbb9-129">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8dbb9-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="8dbb9-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8dbb9-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8dbb9-131">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8dbb9-131">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8dbb9-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8dbb9-132">See also</span></span>



[<span data-ttu-id="8dbb9-133">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="8dbb9-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

