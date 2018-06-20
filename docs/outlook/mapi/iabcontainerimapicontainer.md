---
title: IABContainer IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer
api_type:
- COM
ms.assetid: 1f5ce6e0-b79a-4da2-b014-8c00cd72912e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0eb6d62b64595474957415e94275d0ac52cc2b6b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783577"
---
# <a name="iabcontainer--imapicontainer"></a><span data-ttu-id="614ff-103">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="614ff-103">IABContainer : IMAPIContainer</span></span>

<span data-ttu-id="614ff-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="614ff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="614ff-105">Donne accès aux conteneurs de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="614ff-105">Provides access to address book containers.</span></span> <span data-ttu-id="614ff-106">Applications clientes et MAPI appellent les méthodes **IABContainer** pour effectuer la résolution de noms et pour créer, copier et supprimer des destinataires.</span><span class="sxs-lookup"><span data-stu-id="614ff-106">MAPI and client applications call the methods of **IABContainer** to perform name resolution and to create, copy, and delete recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="614ff-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="614ff-107">Header file:</span></span>  <br/> |<span data-ttu-id="614ff-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="614ff-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="614ff-109">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="614ff-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="614ff-110">Objets conteneur de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="614ff-110">Address book container objects</span></span>  <br/> |
|<span data-ttu-id="614ff-111">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="614ff-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="614ff-112">Fournisseurs de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="614ff-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="614ff-113">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="614ff-113">Called by:</span></span>  <br/> |<span data-ttu-id="614ff-114">Applications MAPI et client</span><span class="sxs-lookup"><span data-stu-id="614ff-114">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="614ff-115">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="614ff-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="614ff-116">IID_IABContainer</span><span class="sxs-lookup"><span data-stu-id="614ff-116">IID_IABContainer</span></span>  <br/> |
|<span data-ttu-id="614ff-117">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="614ff-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="614ff-118">LPABCONT</span><span class="sxs-lookup"><span data-stu-id="614ff-118">LPABCONT</span></span>  <br/> |
|<span data-ttu-id="614ff-119">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="614ff-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="614ff-120">Traitées</span><span class="sxs-lookup"><span data-stu-id="614ff-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="614ff-121">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="614ff-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="614ff-122">CreateEntry</span><span class="sxs-lookup"><span data-stu-id="614ff-122">CreateEntry</span></span>](iabcontainer-createentry.md) <br/> |<span data-ttu-id="614ff-123">Crée une nouvelle entrée, qui peut être un utilisateur de messagerie, une liste de distribution ou un autre conteneur.</span><span class="sxs-lookup"><span data-stu-id="614ff-123">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>  <br/> |
|[<span data-ttu-id="614ff-124">CopyEntries</span><span class="sxs-lookup"><span data-stu-id="614ff-124">CopyEntries</span></span>](iabcontainer-copyentries.md) <br/> |<span data-ttu-id="614ff-125">Copie une ou plusieurs entrées, les utilisateurs de messagerie en général ou des listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="614ff-125">Copies one or more entries, typically messaging users or distribution lists.</span></span>  <br/> |
|[<span data-ttu-id="614ff-126">DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="614ff-126">DeleteEntries</span></span>](iabcontainer-deleteentries.md) <br/> |<span data-ttu-id="614ff-127">Supprime une ou plusieurs entrées, généralement autres conteneurs, listes de distribution ou les utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="614ff-127">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>  <br/> |
|[<span data-ttu-id="614ff-128">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="614ff-128">ResolveNames</span></span>](iabcontainer-resolvenames.md) <br/> |<span data-ttu-id="614ff-129">Effectue la résolution de noms pour une ou plusieurs entrées de destinataire.</span><span class="sxs-lookup"><span data-stu-id="614ff-129">Performs name resolution for one or more recipient entries.</span></span>  <br/> |
   
|<span data-ttu-id="614ff-130">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="614ff-130">**Required properties**</span></span>|<span data-ttu-id="614ff-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="614ff-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="614ff-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="614ff-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="614ff-133">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="614ff-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="614ff-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="614ff-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="614ff-135">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="614ff-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="614ff-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="614ff-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="614ff-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="614ff-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="614ff-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="614ff-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="614ff-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="614ff-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="614ff-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="614ff-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="614ff-141">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="614ff-141">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="614ff-142">**Propriétés facultatives**</span><span class="sxs-lookup"><span data-stu-id="614ff-142">**Optional properties**</span></span>|<span data-ttu-id="614ff-143">**Access**</span><span class="sxs-lookup"><span data-stu-id="614ff-143">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="614ff-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="614ff-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="614ff-145">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="614ff-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="614ff-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="614ff-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="614ff-147">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="614ff-147">Read-only</span></span>  <br/> |
|<span data-ttu-id="614ff-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="614ff-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="614ff-149">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="614ff-149">Read-only</span></span>  <br/> |
|<span data-ttu-id="614ff-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="614ff-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="614ff-151">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="614ff-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="614ff-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="614ff-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="614ff-153">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="614ff-153">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="614ff-154">Remarques</span><span class="sxs-lookup"><span data-stu-id="614ff-154">Remarks</span></span>

<span data-ttu-id="614ff-155">L’interface **IABContainer** indirectement hérite de l’interface [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) par le biais de la [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) et [IMAPIProp : IUnknown](imapipropiunknown.md) interfaces.</span><span class="sxs-lookup"><span data-stu-id="614ff-155">The **IABContainer** interface inherits indirectly from the [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) interface through the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) and [IMAPIProp : IUnknown](imapipropiunknown.md) interfaces.</span></span> <span data-ttu-id="614ff-156">Fournisseurs de carnet d’adresses implémentent l’interface **IABContainer** .</span><span class="sxs-lookup"><span data-stu-id="614ff-156">Address book providers implement the **IABContainer** interface.</span></span> 
  
<span data-ttu-id="614ff-157">N’importe quel nombre d’autres conteneurs de carnet d’adresses, des listes de distribution et les objets utilisateur de messagerie peut exister dans un conteneur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="614ff-157">Any number of messaging user objects, distribution lists, and other address book containers can exist in an address book container.</span></span> <span data-ttu-id="614ff-158">Comme avec n’importe quel conteneur, clients ou fournisseurs de services peuvent utiliser un conteneur de carnet d’adresses pour ouvrir une de ses entrées ou récupérer une table de hiérarchie ou une table de contenu.</span><span class="sxs-lookup"><span data-stu-id="614ff-158">As with any container, clients or service providers can use an address book container to open one of its entries or to retrieve a hierarchy table or contents table.</span></span> <span data-ttu-id="614ff-159">Conteneurs également fournissent la résolution de nom et, selon le fournisseur, la possibilité d’ajouter, supprimer ou modifier des entrées de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="614ff-159">Address book containers also provide name resolution and, depending on the provider, the ability to add, remove, or modify entries.</span></span>
  
<span data-ttu-id="614ff-160">MAPI définit un conteneur de carnet d’adresses spécial appelé le carnet d’adresses personnel (CAP) qui contient les entrées copiées à partir d’autres conteneurs.</span><span class="sxs-lookup"><span data-stu-id="614ff-160">MAPI defines a special address book container called the personal address book (PAB) that holds entries copied from other containers.</span></span> <span data-ttu-id="614ff-161">Un carnet d’adresses personnel est toujours modifiable.</span><span class="sxs-lookup"><span data-stu-id="614ff-161">A PAB is always modifiable.</span></span> <span data-ttu-id="614ff-162">Les utilisateurs remplir généralement leur carnet d’adresses personnel avec des entrées de désigner les destinataires dont ils communiquent plus fréquemment.</span><span class="sxs-lookup"><span data-stu-id="614ff-162">Users typically populate their PAB with entries designating the recipients with which they most frequently communicate.</span></span> <span data-ttu-id="614ff-163">Un carnet d’adresses personnel peut également contenir des adresses uniques et les nouveaux destinataires n’est pas encore partie de n’importe quel conteneur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="614ff-163">A PAB can also hold one-off addresses and new recipients not yet a part of any address book container.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="614ff-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="614ff-164">See also</span></span>

- [<span data-ttu-id="614ff-165">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="614ff-165">MAPI Interfaces</span></span>](mapi-interfaces.md)

