---
title: Exemple de fournisseur de banque de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 25c606531aa9a7436306a1b87c32aab49fd975db
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593913"
---
# <a name="message-store-provider-sample"></a><span data-ttu-id="7f481-103">Exemple de fournisseur de banque de messages</span><span class="sxs-lookup"><span data-stu-id="7f481-103">Message Store Provider Sample</span></span>

  
  
<span data-ttu-id="7f481-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f481-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f481-105">Le fournisseur de banque PST encapsulé exemple utilise un fournisseur de fichier (.pst) de dossiers personnels en tant que serveur principal pour le stockage des données.</span><span class="sxs-lookup"><span data-stu-id="7f481-105">The Sample Wrapped PST Store Provider uses a Personal Folders file (PST) provider as the back end for storing data.</span></span> <span data-ttu-id="7f481-106">Le fournisseur de banque PST encapsulé doit être utilisé avec l’API de réplication.</span><span class="sxs-lookup"><span data-stu-id="7f481-106">The wrapped PST store provider should be used together with the Replication API.</span></span> 
  
<span data-ttu-id="7f481-107">L’API de réplication permet de répliquer des éléments d’un référentiel de données principale dans le magasin de fichiers PST de Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="7f481-107">The Replication API enables you to replicate items from a back-end data repository into a Microsoft Outlook PST store.</span></span> <span data-ttu-id="7f481-108">Vous utilisez l’API de réplication pour répliquer les données dans une banque de dossiers personnels dédiée et garder une trace de l’état de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="7f481-108">You use the Replication API to replicate the data into a dedicated PST store and keep track of the synchronization state.</span></span> <span data-ttu-id="7f481-109">Pour plus d’informations, consultez la rubrique [Sur l’API de réplication](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="7f481-109">For more information, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="7f481-110">La plupart des fonctions dans le fournisseur de banque PST encapsulé exemple transmettre leurs arguments directement au fournisseur sous-jacent PST.</span><span class="sxs-lookup"><span data-stu-id="7f481-110">Most of the functions in the Sample Wrapped PST Store Provider pass their arguments directly to the underlying PST provider.</span></span> <span data-ttu-id="7f481-111">Certaines fonctions requièrent une implémentation spéciale et sont décrites dans les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="7f481-111">Certain functions require special implementation and are described in the following topics.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f481-112">Fichier exécutable :</span><span class="sxs-lookup"><span data-stu-id="7f481-112">Executable:</span></span>  <br/> |<span data-ttu-id="7f481-113">WrpPST32.dll</span><span class="sxs-lookup"><span data-stu-id="7f481-113">WrpPST32.dll</span></span>  <br/> |
|<span data-ttu-id="7f481-114">Répertoire de code source :</span><span class="sxs-lookup"><span data-stu-id="7f481-114">Source code directory:</span></span>  <br/> |<span data-ttu-id="7f481-115">SampleWrappedPSTStoreProvider\WrapPST</span><span class="sxs-lookup"><span data-stu-id="7f481-115">SampleWrappedPSTStoreProvider\WrapPST</span></span>  <br/> |
|<span data-ttu-id="7f481-116">Langue :</span><span class="sxs-lookup"><span data-stu-id="7f481-116">Language:</span></span>  <br/> |<span data-ttu-id="7f481-117">C++</span><span class="sxs-lookup"><span data-stu-id="7f481-117">C++</span></span>  <br/> |
|<span data-ttu-id="7f481-118">Plateformes :</span><span class="sxs-lookup"><span data-stu-id="7f481-118">Platforms:</span></span>  <br/> |<span data-ttu-id="7f481-119">Microsoft Visual Studio 2008 pour compiler pour Windows Vista, Windows Server 2008, Windows XP SP2 et Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="7f481-119">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="7f481-120">Fonctionnalités prises en charge</span><span class="sxs-lookup"><span data-stu-id="7f481-120">Supported Features</span></span>

<span data-ttu-id="7f481-121">Cet exemple prend en charge de Microsoft Outlook 2010 64 bits et maintenant a été modifié pour Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="7f481-121">This sample supports Microsoft Outlook 2010 64-bit and has now been revised for Outlook 2013.</span></span> <span data-ttu-id="7f481-122">Consultez les rubriques suivantes pour plus d’informations :</span><span class="sxs-lookup"><span data-stu-id="7f481-122">See the following topics for additional information:</span></span>
  
- [<span data-ttu-id="7f481-123">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="7f481-123">About the Replication API</span></span>](about-the-replication-api.md)
    
- [<span data-ttu-id="7f481-124">Initialisation d’un fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="7f481-124">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="7f481-125">Connexion à un fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="7f481-125">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="7f481-126">Utilisation d’un fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="7f481-126">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="7f481-127">Arrêt d’un fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="7f481-127">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)
    
 <span data-ttu-id="7f481-128">**Pour installer le fournisseur de banque exemple encapsulé PST**</span><span class="sxs-lookup"><span data-stu-id="7f481-128">**To install the Sample Wrapped PST Store Provider**</span></span>
  
1. <span data-ttu-id="7f481-129">Pour télécharger l’exemple entourées de fournisseur PST, voir [télécharger les exemples de MAPI Outlook](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="7f481-129">To download the Sample Wrapped PST Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="7f481-130">Recherchez le dossier où vous avez enregistré les exemples de MAPI Outlook.</span><span class="sxs-lookup"><span data-stu-id="7f481-130">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="7f481-131">Avec le bouton droit la **OutlookMAPISamples -\<numéro de version\> ** zip du dossier, puis cliquez sur **Extraire tout**.</span><span class="sxs-lookup"><span data-stu-id="7f481-131">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and then click **Extract All**.</span></span>
    
3. <span data-ttu-id="7f481-132">Cliquez sur **Parcourir**, sélectionnez l’emplacement où vous souhaitez enregistrer l’exemple, puis cliquez sur **Extraire**.</span><span class="sxs-lookup"><span data-stu-id="7f481-132">Click **Browse**, select the location where you want to save the sample, and then click **Extract**.</span></span>
    
4. <span data-ttu-id="7f481-133">Exécutez Microsoft Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="7f481-133">Run Microsoft Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="7f481-134">Dans Microsoft Visual Studio 2008, cliquez sur **fichier**, sélectionnez **Ouvrir**, puis cliquez sur **Projet/Solution**.</span><span class="sxs-lookup"><span data-stu-id="7f481-134">In Microsoft Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="7f481-135">Accédez à l’emplacement où vous avez enregistré l’exemple et cliquez sur **WrapPST.vcproj**, puis cliquez sur **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="7f481-135">Browse to the location where you saved the sample, click **WrapPST.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="7f481-136">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="7f481-136">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="7f481-137">Dans la boîte de dialogue **Enregistrer le fichier sous** , cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7f481-137">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="7f481-138">Dans le dossier où vous avez enregistré l’exemple, cliquez sur le fichier **install.bat** , puis sur **Exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="7f481-138">In the folder where you saved the sample, right-click the **install.bat** file and then click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="7f481-139">Dans la boîte de dialogue **Contrôle de compte d’utilisateur** , cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="7f481-139">In the **User Account Control** dialog box, click **Continue**.</span></span>
    

