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
ms.openlocfilehash: 0905fbe2ba584aef49c50152aaf448267d477c10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348957"
---
# <a name="iabcontainer--imapicontainer"></a><span data-ttu-id="b8ed4-103">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="b8ed4-103">IABContainer : IMAPIContainer</span></span>

<span data-ttu-id="b8ed4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8ed4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8ed4-105">Fournit l'accès aux conteneurs du carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="b8ed4-105">Provides access to address book containers.</span></span> <span data-ttu-id="b8ed4-106">Les applications MAPI et clientes appellent les méthodes de **IABContainer** pour effectuer la résolution de noms et pour créer, copier et supprimer des destinataires.</span><span class="sxs-lookup"><span data-stu-id="b8ed4-106">MAPI and client applications call the methods of **IABContainer** to perform name resolution and to create, copy, and delete recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b8ed4-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b8ed4-107">Header file:</span></span>  <br/> |<span data-ttu-id="b8ed4-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b8ed4-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b8ed4-109">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="b8ed4-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="b8ed4-110">Objets conteneur du carnet d'adresses</span><span class="sxs-lookup"><span data-stu-id="b8ed4-110">Address book container objects</span></span>  <br/> |
|<span data-ttu-id="b8ed4-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="b8ed4-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="b8ed4-112">Fournisseurs de carnets d'adresses</span><span class="sxs-lookup"><span data-stu-id="b8ed4-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="b8ed4-113">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="b8ed4-113">Called by:</span></span>  <br/> |<span data-ttu-id="b8ed4-114">Applications MAPI et clientes</span><span class="sxs-lookup"><span data-stu-id="b8ed4-114">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="b8ed4-115">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="b8ed4-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b8ed4-116">IID_IABContainer</span><span class="sxs-lookup"><span data-stu-id="b8ed4-116">IID_IABContainer</span></span>  <br/> |
|<span data-ttu-id="b8ed4-117">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="b8ed4-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="b8ed4-118">LPABCONT</span><span class="sxs-lookup"><span data-stu-id="b8ed4-118">LPABCONT</span></span>  <br/> |
|<span data-ttu-id="b8ed4-119">Modèle de transaction:</span><span class="sxs-lookup"><span data-stu-id="b8ed4-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="b8ed4-120">Traitées</span><span class="sxs-lookup"><span data-stu-id="b8ed4-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b8ed4-121">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="b8ed4-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b8ed4-122">CreateEntry</span><span class="sxs-lookup"><span data-stu-id="b8ed4-122">CreateEntry</span></span>](iabcontainer-createentry.md) <br/> |<span data-ttu-id="b8ed4-123">Crée une nouvelle entrée, qui peut être un utilisateur de messagerie, une liste de distribution ou un autre conteneur.</span><span class="sxs-lookup"><span data-stu-id="b8ed4-123">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>  <br/> |
|[<span data-ttu-id="b8ed4-124">CopyEntries</span><span class="sxs-lookup"><span data-stu-id="b8ed4-124">CopyEntries</span></span>](iabcontainer-copyentries.md) <br/> |<span data-ttu-id="b8ed4-125">Copie une ou plusieurs entrées, généralement les utilisateurs de messagerie ou les listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="b8ed4-125">Copies one or more entries, typically messaging users or distribution lists.</span></span>  <br/> |
|[<span data-ttu-id="b8ed4-126">DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="b8ed4-126">DeleteEntries</span></span>](iabcontainer-deleteentries.md) <br/> |<span data-ttu-id="b8ed4-127">Supprime une ou plusieurs entrées, généralement les utilisateurs de messagerie, les listes de distribution ou d'autres conteneurs.</span><span class="sxs-lookup"><span data-stu-id="b8ed4-127">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>  <br/> |
|[<span data-ttu-id="b8ed4-128">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="b8ed4-128">ResolveNames</span></span>](iabcontainer-resolvenames.md) <br/> |<span data-ttu-id="b8ed4-129">Effectue la résolution de noms pour une ou plusieurs entrées de destinataires.</span><span class="sxs-lookup"><span data-stu-id="b8ed4-129">Performs name resolution for one or more recipient entries.</span></span>  <br/> |
   
|<span data-ttu-id="b8ed4-130">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="b8ed4-130">**Required properties**</span></span>|<span data-ttu-id="b8ed4-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="b8ed4-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b8ed4-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8ed4-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b8ed4-133">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="b8ed4-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="b8ed4-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8ed4-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b8ed4-135">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="b8ed4-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="b8ed4-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8ed4-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b8ed4-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8ed4-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="b8ed4-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8ed4-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b8ed4-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8ed4-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="b8ed4-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8ed4-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b8ed4-141">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8ed4-141">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="b8ed4-142">**Propriétés facultatives**</span><span class="sxs-lookup"><span data-stu-id="b8ed4-142">**Optional properties**</span></span>|<span data-ttu-id="b8ed4-143">**Access**</span><span class="sxs-lookup"><span data-stu-id="b8ed4-143">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b8ed4-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8ed4-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b8ed4-145">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8ed4-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="b8ed4-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8ed4-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b8ed4-147">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8ed4-147">Read-only</span></span>  <br/> |
|<span data-ttu-id="b8ed4-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8ed4-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b8ed4-149">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8ed4-149">Read-only</span></span>  <br/> |
|<span data-ttu-id="b8ed4-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8ed4-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b8ed4-151">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8ed4-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="b8ed4-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8ed4-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b8ed4-153">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8ed4-153">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8ed4-154">Remarques</span><span class="sxs-lookup"><span data-stu-id="b8ed4-154">Remarks</span></span>

<span data-ttu-id="b8ed4-155">L'interface **IABContainer** hérite indirectement de l'interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) via les interfaces [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) et [IMAPIProp: IUnknown](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="b8ed4-155">The **IABContainer** interface inherits indirectly from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface through the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) and [IMAPIProp : IUnknown](imapipropiunknown.md) interfaces.</span></span> <span data-ttu-id="b8ed4-156">Les fournisseurs de carnets d'adresses implémentent l'interface **IABContainer** .</span><span class="sxs-lookup"><span data-stu-id="b8ed4-156">Address book providers implement the **IABContainer** interface.</span></span> 
  
<span data-ttu-id="b8ed4-157">Un conteneur de carnet d'adresses peut contenir n'importe quel nombre d'objets utilisateur de messagerie, de listes de distribution et d'autres conteneurs du carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="b8ed4-157">Any number of messaging user objects, distribution lists, and other address book containers can exist in an address book container.</span></span> <span data-ttu-id="b8ed4-158">Comme avec tout conteneur, les clients ou fournisseurs de services peuvent utiliser un conteneur de carnet d'adresses pour ouvrir l'une de ses entrées ou récupérer une table de hiérarchie ou une table de contenu.</span><span class="sxs-lookup"><span data-stu-id="b8ed4-158">As with any container, clients or service providers can use an address book container to open one of its entries or to retrieve a hierarchy table or contents table.</span></span> <span data-ttu-id="b8ed4-159">Les conteneurs du carnet d'adresses fournissent également une résolution de nom et, en fonction du fournisseur, la possibilité d'ajouter, de supprimer ou de modifier des entrées.</span><span class="sxs-lookup"><span data-stu-id="b8ed4-159">Address book containers also provide name resolution and, depending on the provider, the ability to add, remove, or modify entries.</span></span>
  
<span data-ttu-id="b8ed4-160">MAPI définit un conteneur de carnet d'adresses spécial appelé carnet d'adresses personnel (PAB) contenant les entrées copiées à partir d'autres conteneurs.</span><span class="sxs-lookup"><span data-stu-id="b8ed4-160">MAPI defines a special address book container called the personal address book (PAB) that holds entries copied from other containers.</span></span> <span data-ttu-id="b8ed4-161">Un PAB est toujours modifiable.</span><span class="sxs-lookup"><span data-stu-id="b8ed4-161">A PAB is always modifiable.</span></span> <span data-ttu-id="b8ed4-162">Les utilisateurs renseignent généralement leur PAB avec des entrées désignant les destinataires avec lesquels ils communiquent le plus souvent.</span><span class="sxs-lookup"><span data-stu-id="b8ed4-162">Users typically populate their PAB with entries designating the recipients with which they most frequently communicate.</span></span> <span data-ttu-id="b8ed4-163">Un PAB peut également contenir des adresses uniques et des destinataires qui ne font pas encore partie d'un conteneur de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="b8ed4-163">A PAB can also hold one-off addresses and new recipients not yet a part of any address book container.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b8ed4-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8ed4-164">See also</span></span>

- [<span data-ttu-id="b8ed4-165">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="b8ed4-165">MAPI Interfaces</span></span>](mapi-interfaces.md)

