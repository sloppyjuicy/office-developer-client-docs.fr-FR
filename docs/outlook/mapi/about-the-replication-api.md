---
title: À propos de l’API de réplication
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: 532c01d6885e72753067b2d30bf2bd5f88207176
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329518"
---
# <a name="about-the-replication-api"></a><span data-ttu-id="bf140-103">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="bf140-103">About the Replication API</span></span>

  
  
<span data-ttu-id="bf140-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf140-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf140-105">L'API de réPlication fournit les fonctionnalités d'un fournisseur de banque de messages MAPI pour synchroniser les éléments Microsoft Outlook 2013 ou Microsoft Outlook 2010 entre un serveur et un magasin local. pst privé créé pour ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="bf140-105">The Replication API provides the functionality for a MAPI message store provider to synchronize Microsoft Outlook 2013 or Microsoft Outlook 2010 items between a server and a private .pst-based local store that is created for that provider.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bf140-106">Un fournisseur de banque de messages MAPI doit implémenter l'API de réPlication conformément aux instructions de [la rubrique à propos de la machine à États](about-the-replication-state-machine.md)de réplication.</span><span class="sxs-lookup"><span data-stu-id="bf140-106">A MAPI message store provider must implement the Replication API according to the instructions in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="bf140-107">Le fournisseur doit utiliser l'API uniquement sur un magasin personnel créé pour lui-même, et non sur des magasins personnels créés pour d'autres fournisseurs, car des magasins personnels créés pour d'autres fournisseurs ont déjà configuré leurs propres mécanismes de réplication avec le serveur respectif.</span><span class="sxs-lookup"><span data-stu-id="bf140-107">The provider must use the API only on a personal store created for itself, and not on personal stores created for other providers, because personal stores created for other providers may have already set up their own replication mechanisms with the respective server.</span></span> <span data-ttu-id="bf140-108">Par exemple, un fichier de dossiers en mode hors connexion (. ost) conserve sa propre relation de réplication avec un serveur Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="bf140-108">For example, an offline folder file (.ost) maintains its own replication relationship with a Microsoft Exchange server.</span></span> 
  
<span data-ttu-id="bf140-109">Pour utiliser l'API de réPlication, un fournisseur de banque de messages MAPI doit d'abord ouvrir et encapsuler un magasin local basé sur un fichier. pst en appelant **[NSTServiceEntry](nstserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="bf140-109">To use the Replication API, a MAPI message store provider must first open and wrap a .pst-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="bf140-110">Le fournisseur peut ensuite utiliser les principales interfaces de l'API **[IOSTX](iostxiunknown.md)** et **[IPSTX](ipstxiunknown.md)** pour effectuer la réplication.</span><span class="sxs-lookup"><span data-stu-id="bf140-110">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> <span data-ttu-id="bf140-111">**IPSTX** est fourni par l'interrogation sur [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)et **IOSTX** est fourni par **[IPSTX:: GetSyncObject](ipstx-getsyncobject.md)**.</span><span class="sxs-lookup"><span data-stu-id="bf140-111">**IPSTX** is provided by querying on [IMsgStore : IMAPIProp](imsgstoreimapiprop.md), and **IOSTX** is provided by **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**.</span></span> 
  
## <a name="the-iostx-interface"></a><span data-ttu-id="bf140-112">Interface IOSTX</span><span class="sxs-lookup"><span data-stu-id="bf140-112">The IOSTX Interface</span></span>

<span data-ttu-id="bf140-113">L'interface **IOSTX** est l'interface principale qui effectue la synchronisation dans l'API de réplication.</span><span class="sxs-lookup"><span data-stu-id="bf140-113">The **IOSTX** interface is the primary interface that performs synchronization in the Replication API.</span></span> <span data-ttu-id="bf140-114">**IOSTX** déplace le magasin local par le biais d'une série d'États, en récupérant des informations dans chaque État sur les modifications apportées à la banque locale, ainsi qu'en informant le magasin local des modifications apportées sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="bf140-114">**IOSTX** moves the local store through a series of states, retrieving information in each state about changes in the local store, as well as informing the local store of changes on the server.</span></span> <span data-ttu-id="bf140-115">L'API de réPlication spécifie également de nombreuses structures de données qui prennent en charge la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="bf140-115">The Replication API also specifies many data structures that support the synchronization.</span></span> 
  
<span data-ttu-id="bf140-116">Un fournisseur de banque, en tant que client pour cette API, utilise l'API de réPlication pour encapsuler le magasin local et parcourir ces États, en envoyant les modifications sur le magasin local (telles que les modifications apportées à la hiérarchie de dossiers ou l'ajout de nouveaux éléments) au serveur et en extrayant également informations sur les modifications sur le serveur et la fourniture de ces informations à l'interface **IOSTX** .</span><span class="sxs-lookup"><span data-stu-id="bf140-116">A store provider, as a client to this API, uses the Replication API to wrap the local store and move through these states, pushing changes on the local store (such as changes to the folder hierarchy or the addition of new items) to the server, and also retrieving information about changes on the server and providing that information to the **IOSTX** interface.</span></span> <span data-ttu-id="bf140-117">L'interface **IOSTX** adopte une synchronisation des modifications incrémentielles fournie par Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bf140-117">The **IOSTX** interface adopts Incremental Change Synchronization (ICS) provided by Microsoft Exchange Server.</span></span> <span data-ttu-id="bf140-118">Pour plus d'informations sur le partage de connexion Internet, consultez la rubrique [critères d'évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="bf140-118">For more information about ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span> <span data-ttu-id="bf140-119">Via **IOSTX**, le client utilise ICS pour surveiller et synchroniser les modifications incrémentielles apportées à la hiérarchie ou au contenu d'un magasin local.</span><span class="sxs-lookup"><span data-stu-id="bf140-119">Through **IOSTX**, the client uses ICS to monitor and synchronize incremental changes to the hierarchy or content on a local store.</span></span> 
  
## <a name="the-ipstx-interface"></a><span data-ttu-id="bf140-120">Interface IPSTX</span><span class="sxs-lookup"><span data-stu-id="bf140-120">The IPSTX Interface</span></span>

 <span data-ttu-id="bf140-121">**IPSTX** et cinq autres \* \* IPSTX *n* \* \* les interfaces qui héritent de **IPSTX** fournissent une fonctionnalité d'assistance qui peut être utilisée lors de l'exécution de la réplication via l'interface **IOSTX** .</span><span class="sxs-lookup"><span data-stu-id="bf140-121">**IPSTX** and five other \*\*IPSTX *n* \*\* interfaces that inherit from **IPSTX** provide helper functionality that can be used when performing replication through the **IOSTX** interface.</span></span> <span data-ttu-id="bf140-122">Par exemple, **[IPSTX:: EmulateSpooler](ipstx-emulatespooler.md)** vous permet de faire en sorte que le magasin local émule le gestionnaire de protocoles Outlook pour mettre en file d'attente les messages sortants vers un serveur.</span><span class="sxs-lookup"><span data-stu-id="bf140-122">For example, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** allows you to make the local store emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span> 
  
<span data-ttu-id="bf140-123">Pour plus d'informations sur les transitions d'état lors de la réplication, voir [à propos de la machine à États](about-the-replication-state-machine.md)de réplication.</span><span class="sxs-lookup"><span data-stu-id="bf140-123">For more information about state transitions during replication, see [About the Replication State Machine](about-the-replication-state-machine.md).</span></span>
  
## <a name="the-replication-api"></a><span data-ttu-id="bf140-124">API de réPlication</span><span class="sxs-lookup"><span data-stu-id="bf140-124">The Replication API</span></span>

<span data-ttu-id="bf140-125">L'API de réPlication fournit les defintions, les types de données et les interfaces suivants.</span><span class="sxs-lookup"><span data-stu-id="bf140-125">The Replication API provides the following defintions, data types, and interfaces.</span></span> <span data-ttu-id="bf140-126">Pour un exemple d'implémentation d'un fournisseur de magasin pour les fichiers de dossiers personnels (PST) encapsulés, voir [à propos de l'exemple de fournisseur de magasins PST encapsulé](about-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="bf140-126">For a sample implementation of a store provider for wrapped Personal Folders files (PST), see [About the Sample Wrapped PST Store Provider](about-the-sample-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="bf140-127">Définitions :</span><span class="sxs-lookup"><span data-stu-id="bf140-127">Definitions:</span></span>
  
- [<span data-ttu-id="bf140-128">Constantes pour l'API de réPlication</span><span class="sxs-lookup"><span data-stu-id="bf140-128">Constants for the Replication API</span></span>](mapi-constants.md)
    
<span data-ttu-id="bf140-129">Fonctions :</span><span class="sxs-lookup"><span data-stu-id="bf140-129">Functions:</span></span>
  
- <span data-ttu-id="bf140-130">**[NSTServiceEntry](nstserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-130">**[NSTServiceEntry](nstserviceentry.md)**</span></span>
    
<span data-ttu-id="bf140-131">Types de données:</span><span class="sxs-lookup"><span data-stu-id="bf140-131">Data types:</span></span>
  
- <span data-ttu-id="bf140-132">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-132">**[DNHIER](dnhier.md)**</span></span>
    
- <span data-ttu-id="bf140-133">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-133">**[DNTBL](dntbl.md)**</span></span>
    
- <span data-ttu-id="bf140-134">**[DNTBLE](dntble.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-134">**[DNTBLE](dntble.md)**</span></span>
    
- <span data-ttu-id="bf140-135">**[FEID](feid.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-135">**[FEID](feid.md)**</span></span>
    
- <span data-ttu-id="bf140-136">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-136">**[HDRSYNC](hdrsync.md)**</span></span>
    
- <span data-ttu-id="bf140-137">**[LTID](ltid.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-137">**[LTID](ltid.md)**</span></span>
    
- <span data-ttu-id="bf140-138">**[MEID](meid.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-138">**[MEID](meid.md)**</span></span>
    
- <span data-ttu-id="bf140-139">**[OLFI](olfi.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-139">**[OLFI](olfi.md)**</span></span>
    
- <span data-ttu-id="bf140-140">**[SKEY](skey.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-140">**[SKEY](skey.md)**</span></span>
    
- <span data-ttu-id="bf140-141">**[SYNCHRONI](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-141">**[SYNC](sync.md)**</span></span>
    
- <span data-ttu-id="bf140-142">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-142">**[SYNCCONT](synccont.md)**</span></span>
    
- <span data-ttu-id="bf140-143">**[SYNCSTATE](syncstate.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-143">**[SYNCSTATE](syncstate.md)**</span></span>
    
- <span data-ttu-id="bf140-144">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-144">**[UPDEL](updel.md)**</span></span>
    
- <span data-ttu-id="bf140-145">**[UPDELE](updele.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-145">**[UPDELE](updele.md)**</span></span>
    
- <span data-ttu-id="bf140-146">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-146">**[UPFLD](upfld.md)**</span></span>
    
- <span data-ttu-id="bf140-147">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-147">**[UPHIER](uphier.md)**</span></span>
    
- <span data-ttu-id="bf140-148">**[UPMOV](upmov.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-148">**[UPMOV](upmov.md)**</span></span>
    
- <span data-ttu-id="bf140-149">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-149">**[UPMSG](upmsg.md)**</span></span>
    
- <span data-ttu-id="bf140-150">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-150">**[UPREAD](upread.md)**</span></span>
    
- <span data-ttu-id="bf140-151">**[UPREADE](upreade.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-151">**[UPREADE](upreade.md)**</span></span>
    
- <span data-ttu-id="bf140-152">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-152">**[UPTBL](uptbl.md)**</span></span>
    
- <span data-ttu-id="bf140-153">**[UPTBLE](uptble.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-153">**[UPTBLE](uptble.md)**</span></span>
    
<span data-ttu-id="bf140-154">Interfaces :</span><span class="sxs-lookup"><span data-stu-id="bf140-154">Interfaces:</span></span>
  
- <span data-ttu-id="bf140-155">**[IOSTX](iostxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-155">**[IOSTX](iostxiunknown.md)**</span></span>
    
- <span data-ttu-id="bf140-156">**[IPSTX](ipstxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-156">**[IPSTX](ipstxiunknown.md)**</span></span>
    
- <span data-ttu-id="bf140-157">**[IPSTX2](ipstx2ipstx.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-157">**[IPSTX2](ipstx2ipstx.md)**</span></span>
    
- <span data-ttu-id="bf140-158">**[IPSTX3](ipstx3ipstx2.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-158">**[IPSTX3](ipstx3ipstx2.md)**</span></span>
    
- <span data-ttu-id="bf140-159">**[IPSTX4](ipstx4ipstx3.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-159">**[IPSTX4](ipstx4ipstx3.md)**</span></span>
    
- <span data-ttu-id="bf140-160">**[IPSTX5](ipstx5ipstx4.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-160">**[IPSTX5](ipstx5ipstx4.md)**</span></span>
    
- <span data-ttu-id="bf140-161">**[IPSTX6](ipstx6ipstx5.md)**</span><span class="sxs-lookup"><span data-stu-id="bf140-161">**[IPSTX6](ipstx6ipstx5.md)**</span></span>
    

