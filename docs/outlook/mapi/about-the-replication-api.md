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
# <a name="about-the-replication-api"></a><span data-ttu-id="378a7-103">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="378a7-103">About the Replication API</span></span>

  
  
<span data-ttu-id="378a7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="378a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="378a7-105">L’API de réplication fournit la fonctionnalité permettant à un fournisseur de banque de messages MAPI de synchroniser des éléments Microsoft Outlook 2013 ou Microsoft Outlook 2010 entre un serveur et un magasin local .pst privé créé pour ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="378a7-105">The Replication API provides the functionality for a MAPI message store provider to synchronize Microsoft Outlook 2013 or Microsoft Outlook 2010 items between a server and a private .pst-based local store that is created for that provider.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="378a7-106">Un fournisseur de magasin de messages MAPI doit implémenter l’API de réplication conformément aux instructions de la machine à états de [réplication.](about-the-replication-state-machine.md)</span><span class="sxs-lookup"><span data-stu-id="378a7-106">A MAPI message store provider must implement the Replication API according to the instructions in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="378a7-107">Le fournisseur doit utiliser l’API uniquement sur un magasin personnel créé pour lui-même, et non sur les magasins personnels créés pour d’autres fournisseurs, car les magasins personnels créés pour d’autres fournisseurs ont peut-être déjà mis en place leurs propres mécanismes de réplication avec le serveur respectif.</span><span class="sxs-lookup"><span data-stu-id="378a7-107">The provider must use the API only on a personal store created for itself, and not on personal stores created for other providers, because personal stores created for other providers may have already set up their own replication mechanisms with the respective server.</span></span> <span data-ttu-id="378a7-108">Par exemple, un fichier de dossier hors connexion (.ost) conserve sa propre relation de réplication avec un serveur Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="378a7-108">For example, an offline folder file (.ost) maintains its own replication relationship with a Microsoft Exchange server.</span></span> 
  
<span data-ttu-id="378a7-109">Pour utiliser l’API de réplication, un fournisseur de magasin de messages MAPI doit d’abord ouvrir et encapsuler un magasin local .pst en appelant **[NSTServiceEntry](nstserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="378a7-109">To use the Replication API, a MAPI message store provider must first open and wrap a .pst-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="378a7-110">Le fournisseur peut ensuite utiliser les interfaces principales de l’API, **[IOSTX](iostxiunknown.md)** et **[IPSTX](ipstxiunknown.md)**, pour effectuer la réplication.</span><span class="sxs-lookup"><span data-stu-id="378a7-110">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> <span data-ttu-id="378a7-111">**IPSTX est** fourni par l’interrogation sur [IMsgStore : IMAPIProp](imsgstoreimapiprop.md)et **IOSTX** est fourni par **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**.</span><span class="sxs-lookup"><span data-stu-id="378a7-111">**IPSTX** is provided by querying on [IMsgStore : IMAPIProp](imsgstoreimapiprop.md), and **IOSTX** is provided by **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**.</span></span> 
  
## <a name="the-iostx-interface"></a><span data-ttu-id="378a7-112">The IOSTX Interface</span><span class="sxs-lookup"><span data-stu-id="378a7-112">The IOSTX Interface</span></span>

<span data-ttu-id="378a7-113">**L’interface IOSTX** est l’interface principale qui effectue la synchronisation dans l’API de réplication.</span><span class="sxs-lookup"><span data-stu-id="378a7-113">The **IOSTX** interface is the primary interface that performs synchronization in the Replication API.</span></span> <span data-ttu-id="378a7-114">**IOSTX** déplace le magasin local à travers une série d’états, en récupérant des informations dans chaque état sur les modifications apportées au magasin local, ainsi qu’en informant le magasin local des modifications sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="378a7-114">**IOSTX** moves the local store through a series of states, retrieving information in each state about changes in the local store, as well as informing the local store of changes on the server.</span></span> <span data-ttu-id="378a7-115">L’API de réplication spécifie également de nombreuses structures de données qui la prise en charge de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="378a7-115">The Replication API also specifies many data structures that support the synchronization.</span></span> 
  
<span data-ttu-id="378a7-116">Un fournisseur de magasin, en tant que client de cette API, utilise l’API de réplication pour encapsuler le magasin local et passer par ces états, en pushant les modifications sur le magasin local (telles que les modifications apportées à la hiérarchie de dossiers ou l’ajout de nouveaux éléments) au serveur, et en récupérant également des informations sur les modifications apportées au serveur et en fournissant ces informations à l’interface **IOSTX.**</span><span class="sxs-lookup"><span data-stu-id="378a7-116">A store provider, as a client to this API, uses the Replication API to wrap the local store and move through these states, pushing changes on the local store (such as changes to the folder hierarchy or the addition of new items) to the server, and also retrieving information about changes on the server and providing that information to the **IOSTX** interface.</span></span> <span data-ttu-id="378a7-117">**L’interface IOSTX** adopte la synchronisation des changements incrémentielles (ICS) fournie par Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="378a7-117">The **IOSTX** interface adopts Incremental Change Synchronization (ICS) provided by Microsoft Exchange Server.</span></span> <span data-ttu-id="378a7-118">Pour plus d’informations sur ICS, voir [Critères d’évaluation ICS.](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="378a7-118">For more information about ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span> <span data-ttu-id="378a7-119">Via **IOSTX,** le client utilise ICS pour surveiller et synchroniser les modifications incrémentielles apportées à la hiérarchie ou au contenu sur un magasin local.</span><span class="sxs-lookup"><span data-stu-id="378a7-119">Through **IOSTX**, the client uses ICS to monitor and synchronize incremental changes to the hierarchy or content on a local store.</span></span> 
  
## <a name="the-ipstx-interface"></a><span data-ttu-id="378a7-120">The IPSTX Interface</span><span class="sxs-lookup"><span data-stu-id="378a7-120">The IPSTX Interface</span></span>

 <span data-ttu-id="378a7-121">**IPSTX** et cinq autres interfaces \*\*IPSTX *n* \*\* qui héritent **d’IPSTX** fournissent des fonctionnalités d’aide qui peuvent être utilisées lors de la réplication via l’interface **IOSTX.**</span><span class="sxs-lookup"><span data-stu-id="378a7-121">**IPSTX** and five other \*\*IPSTX *n* \*\* interfaces that inherit from **IPSTX** provide helper functionality that can be used when performing replication through the **IOSTX** interface.</span></span> <span data-ttu-id="378a7-122">Par exemple, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** vous permet de faire en sorte que le magasin local émule le gestionnaire de protocole Outlook pour qu’il stocke des messages sortants sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="378a7-122">For example, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** allows you to make the local store emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span> 
  
<span data-ttu-id="378a7-123">Pour plus d’informations sur les transitions d’état pendant la réplication, voir À propos de [la machine à états de réplication.](about-the-replication-state-machine.md)</span><span class="sxs-lookup"><span data-stu-id="378a7-123">For more information about state transitions during replication, see [About the Replication State Machine](about-the-replication-state-machine.md).</span></span>
  
## <a name="the-replication-api"></a><span data-ttu-id="378a7-124">API de réplication</span><span class="sxs-lookup"><span data-stu-id="378a7-124">The Replication API</span></span>

<span data-ttu-id="378a7-125">L’API de réplication fournit les définitions, les types de données et les interfaces suivants.</span><span class="sxs-lookup"><span data-stu-id="378a7-125">The Replication API provides the following defintions, data types, and interfaces.</span></span> <span data-ttu-id="378a7-126">Pour un exemple d’implémentation d’un fournisseur de magasin pour les fichiers de dossiers personnels wrapped (PST), voir à propos de l’exemple de fournisseur de magasin [PST Wrapped](about-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="378a7-126">For a sample implementation of a store provider for wrapped Personal Folders files (PST), see [About the Sample Wrapped PST Store Provider](about-the-sample-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="378a7-127">Définitions :</span><span class="sxs-lookup"><span data-stu-id="378a7-127">Definitions:</span></span>
  
- [<span data-ttu-id="378a7-128">Constantes de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="378a7-128">Constants for the Replication API</span></span>](mapi-constants.md)
    
<span data-ttu-id="378a7-129">Fonctions :</span><span class="sxs-lookup"><span data-stu-id="378a7-129">Functions:</span></span>
  
- <span data-ttu-id="378a7-130">**[NSTServiceEntry](nstserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-130">**[NSTServiceEntry](nstserviceentry.md)**</span></span>
    
<span data-ttu-id="378a7-131">Types de données :</span><span class="sxs-lookup"><span data-stu-id="378a7-131">Data types:</span></span>
  
- <span data-ttu-id="378a7-132">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-132">**[DNHIER](dnhier.md)**</span></span>
    
- <span data-ttu-id="378a7-133">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-133">**[DNTBL](dntbl.md)**</span></span>
    
- <span data-ttu-id="378a7-134">**[DNTBLE](dntble.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-134">**[DNTBLE](dntble.md)**</span></span>
    
- <span data-ttu-id="378a7-135">**[FEID](feid.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-135">**[FEID](feid.md)**</span></span>
    
- <span data-ttu-id="378a7-136">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-136">**[HDRSYNC](hdrsync.md)**</span></span>
    
- <span data-ttu-id="378a7-137">**[LTID](ltid.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-137">**[LTID](ltid.md)**</span></span>
    
- <span data-ttu-id="378a7-138">**[MEID](meid.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-138">**[MEID](meid.md)**</span></span>
    
- <span data-ttu-id="378a7-139">**[OLFI](olfi.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-139">**[OLFI](olfi.md)**</span></span>
    
- <span data-ttu-id="378a7-140">**[SKEY](skey.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-140">**[SKEY](skey.md)**</span></span>
    
- <span data-ttu-id="378a7-141">**[SYNC](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-141">**[SYNC](sync.md)**</span></span>
    
- <span data-ttu-id="378a7-142">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-142">**[SYNCCONT](synccont.md)**</span></span>
    
- <span data-ttu-id="378a7-143">**[SYNCSTATE](syncstate.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-143">**[SYNCSTATE](syncstate.md)**</span></span>
    
- <span data-ttu-id="378a7-144">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-144">**[UPDEL](updel.md)**</span></span>
    
- <span data-ttu-id="378a7-145">**[UPDELE](updele.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-145">**[UPDELE](updele.md)**</span></span>
    
- <span data-ttu-id="378a7-146">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-146">**[UPFLD](upfld.md)**</span></span>
    
- <span data-ttu-id="378a7-147">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-147">**[UPHIER](uphier.md)**</span></span>
    
- <span data-ttu-id="378a7-148">**[UPMOV](upmov.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-148">**[UPMOV](upmov.md)**</span></span>
    
- <span data-ttu-id="378a7-149">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-149">**[UPMSG](upmsg.md)**</span></span>
    
- <span data-ttu-id="378a7-150">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-150">**[UPREAD](upread.md)**</span></span>
    
- <span data-ttu-id="378a7-151">**[UPREADE](upreade.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-151">**[UPREADE](upreade.md)**</span></span>
    
- <span data-ttu-id="378a7-152">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-152">**[UPTBL](uptbl.md)**</span></span>
    
- <span data-ttu-id="378a7-153">**[UPTBLE](uptble.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-153">**[UPTBLE](uptble.md)**</span></span>
    
<span data-ttu-id="378a7-154">Interfaces :</span><span class="sxs-lookup"><span data-stu-id="378a7-154">Interfaces:</span></span>
  
- <span data-ttu-id="378a7-155">**[IOSTX](iostxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-155">**[IOSTX](iostxiunknown.md)**</span></span>
    
- <span data-ttu-id="378a7-156">**[IPSTX](ipstxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-156">**[IPSTX](ipstxiunknown.md)**</span></span>
    
- <span data-ttu-id="378a7-157">**[IPSTX2](ipstx2ipstx.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-157">**[IPSTX2](ipstx2ipstx.md)**</span></span>
    
- <span data-ttu-id="378a7-158">**[IPSTX3](ipstx3ipstx2.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-158">**[IPSTX3](ipstx3ipstx2.md)**</span></span>
    
- <span data-ttu-id="378a7-159">**[IPSTX4](ipstx4ipstx3.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-159">**[IPSTX4](ipstx4ipstx3.md)**</span></span>
    
- <span data-ttu-id="378a7-160">**[IPSTX5](ipstx5ipstx4.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-160">**[IPSTX5](ipstx5ipstx4.md)**</span></span>
    
- <span data-ttu-id="378a7-161">**[IPSTX6](ipstx6ipstx5.md)**</span><span class="sxs-lookup"><span data-stu-id="378a7-161">**[IPSTX6](ipstx6ipstx5.md)**</span></span>
    

