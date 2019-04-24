---
title: Exemple de fournisseur de banque de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: eb51881aac6e1953a21686857944ba2a15d0dca2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356937"
---
# <a name="message-store-provider-sample"></a><span data-ttu-id="bc281-103">Exemple de fournisseur de banque de messages</span><span class="sxs-lookup"><span data-stu-id="bc281-103">Message Store Provider Sample</span></span>

  
  
<span data-ttu-id="bc281-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc281-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc281-105">L'exemple de fournisseur de banque d'informations PST encapsulé utilise un fournisseur de fichiers de dossiers personnels (PST) comme serveur principal pour le stockage des données.</span><span class="sxs-lookup"><span data-stu-id="bc281-105">The Sample Wrapped PST Store Provider uses a Personal Folders file (PST) provider as the back end for storing data.</span></span> <span data-ttu-id="bc281-106">Le fournisseur de magasins PST encapsulé doit être utilisé avec l'API de réPlication.</span><span class="sxs-lookup"><span data-stu-id="bc281-106">The wrapped PST store provider should be used together with the Replication API.</span></span> 
  
<span data-ttu-id="bc281-107">L'API de réPlication vous permet de répliquer des éléments à partir d'un référentiel de données principal dans un magasin Microsoft Outlook PST.</span><span class="sxs-lookup"><span data-stu-id="bc281-107">The Replication API enables you to replicate items from a back-end data repository into a Microsoft Outlook PST store.</span></span> <span data-ttu-id="bc281-108">L'API de réPlication permet de répliquer les données dans un magasin PST dédié et de suivre l'état de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="bc281-108">You use the Replication API to replicate the data into a dedicated PST store and keep track of the synchronization state.</span></span> <span data-ttu-id="bc281-109">Pour plus d'informations, consultez [la rubrique à propos de l'API](about-the-replication-api.md)de réplication.</span><span class="sxs-lookup"><span data-stu-id="bc281-109">For more information, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="bc281-110">La plupart des fonctions dans l'exemple de fournisseur de magasins PST encapsulé passent leurs arguments directement au fournisseur PST sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="bc281-110">Most of the functions in the Sample Wrapped PST Store Provider pass their arguments directly to the underlying PST provider.</span></span> <span data-ttu-id="bc281-111">Certaines fonctions nécessitent une implémentation spéciale et sont décrites dans les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="bc281-111">Certain functions require special implementation and are described in the following topics.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bc281-112">Exécutable</span><span class="sxs-lookup"><span data-stu-id="bc281-112">Executable:</span></span>  <br/> |<span data-ttu-id="bc281-113">WrpPST32. dll</span><span class="sxs-lookup"><span data-stu-id="bc281-113">WrpPST32.dll</span></span>  <br/> |
|<span data-ttu-id="bc281-114">Répertoire de code source:</span><span class="sxs-lookup"><span data-stu-id="bc281-114">Source code directory:</span></span>  <br/> |<span data-ttu-id="bc281-115">SampleWrappedPSTStoreProvider\WrapPST</span><span class="sxs-lookup"><span data-stu-id="bc281-115">SampleWrappedPSTStoreProvider\WrapPST</span></span>  <br/> |
|<span data-ttu-id="bc281-116">Langue</span><span class="sxs-lookup"><span data-stu-id="bc281-116">Language:</span></span>  <br/> |<span data-ttu-id="bc281-117">C++</span><span class="sxs-lookup"><span data-stu-id="bc281-117">C++</span></span>  <br/> |
|<span data-ttu-id="bc281-118">Formes</span><span class="sxs-lookup"><span data-stu-id="bc281-118">Platforms:</span></span>  <br/> |<span data-ttu-id="bc281-119">Microsoft Visual Studio 2008 pour la compilation pour Windows Vista, Windows Server 2008, Windows XP SP2 et Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="bc281-119">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="bc281-120">Fonctionnalités prises en charge</span><span class="sxs-lookup"><span data-stu-id="bc281-120">Supported Features</span></span>

<span data-ttu-id="bc281-121">Cet exemple prend en charge Microsoft Outlook 2010 64 bits et est maintenant révisé pour Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="bc281-121">This sample supports Microsoft Outlook 2010 64-bit and has now been revised for Outlook 2013.</span></span> <span data-ttu-id="bc281-122">Pour plus d'informations, consultez les rubriques suivantes:</span><span class="sxs-lookup"><span data-stu-id="bc281-122">See the following topics for additional information:</span></span>
  
- [<span data-ttu-id="bc281-123">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="bc281-123">About the Replication API</span></span>](about-the-replication-api.md)
    
- [<span data-ttu-id="bc281-124">Initialisation d'un fournisseur de magasins PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="bc281-124">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="bc281-125">Connexion à un fournisseur de magasins PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="bc281-125">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="bc281-126">Utilisation d'un fournisseur de magasins PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="bc281-126">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="bc281-127">Arrêt d'un fournisseur de magasins PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="bc281-127">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)
    
 <span data-ttu-id="bc281-128">**Pour installer l'exemple de fournisseur de magasins PST encapsulé**</span><span class="sxs-lookup"><span data-stu-id="bc281-128">**To install the Sample Wrapped PST Store Provider**</span></span>
  
1. <span data-ttu-id="bc281-129">Pour télécharger l'exemple de fournisseur de fichiers PST encapsulés, consultez [la rubrique téléchargement des exemples MAPI Outlook](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="bc281-129">To download the Sample Wrapped PST Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="bc281-130">Recherchez le dossier dans lequel vous avez enregistré les exemples MAPI Outlook.</span><span class="sxs-lookup"><span data-stu-id="bc281-130">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="bc281-131">Cliquez avec le bouton droit sur le dossier zip de **\<\> numéro de version OutlookMAPISamples** , puis cliquez sur **extraire tout**.</span><span class="sxs-lookup"><span data-stu-id="bc281-131">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and then click **Extract All**.</span></span>
    
3. <span data-ttu-id="bc281-132">Cliquez sur **Parcourir**, sélectionnez l'emplacement où vous souhaitez enregistrer l'exemple, puis cliquez sur **extraire**.</span><span class="sxs-lookup"><span data-stu-id="bc281-132">Click **Browse**, select the location where you want to save the sample, and then click **Extract**.</span></span>
    
4. <span data-ttu-id="bc281-133">Exécutez Microsoft Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="bc281-133">Run Microsoft Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="bc281-134">Dans Microsoft Visual Studio 2008, cliquez sur **fichier**, sur **ouvrir**, puis sur **projet/solution**.</span><span class="sxs-lookup"><span data-stu-id="bc281-134">In Microsoft Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="bc281-135">Naviguez jusqu'à l'emplacement où vous avez enregistré l'exemple, cliquez sur **WrapPST. vcproj**, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="bc281-135">Browse to the location where you saved the sample, click **WrapPST.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="bc281-136">Dans le menu **Générer**, cliquez sur **Générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="bc281-136">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="bc281-137">Dans la boîte de dialogue **enregistrer le fichier sous** , cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="bc281-137">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="bc281-138">Dans le dossier où vous avez enregistré l'exemple, cliquez avec le bouton droit sur le fichier **install. bat** , puis cliquez sur **exécuter en tant qu'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="bc281-138">In the folder where you saved the sample, right-click the **install.bat** file and then click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="bc281-139">Dans la boîte de dialogue **contrôle de compte d'utilisateur** , cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="bc281-139">In the **User Account Control** dialog box, click **Continue**.</span></span>
    

