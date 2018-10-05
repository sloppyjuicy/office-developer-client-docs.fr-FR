---
title: Installation de l’exemple de fournisseur d’archive PST encapsulée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90ce0ea3-ba73-cb57-0fa9-8898bc4ac9de
description: 'Derni�re modification�: jeudi 5 juillet 2012'
ms.openlocfilehash: a1574de555eb74d06c4dbe721e7e013ac59d3071
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397764"
---
# <a name="installing-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="4891f-103">Installation de l’exemple de fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="4891f-103">Installing the Sample Wrapped PST Store Provider</span></span>

  
  
<span data-ttu-id="4891f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4891f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4891f-105">Cette rubrique présente les étapes pour télécharger et installer le fournisseur de banque exemple encapsulé PST.</span><span class="sxs-lookup"><span data-stu-id="4891f-105">This topic takes you through the steps to download and install the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="4891f-106">L’exemple encapsulé PST stocker de fournisseur, WrapPST, implémente un fournisseur de banque PST encapsulé est destiné à être utilisé conjointement avec l’API de réplication.</span><span class="sxs-lookup"><span data-stu-id="4891f-106">The Sample Wrapped PST Store Provider, WrapPST, implements a wrapped PST store provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="4891f-107">Pour plus d’informations sur l’API de réplication, consultez la rubrique [Sur l’API de réplication](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="4891f-107">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="4891f-108">Installer l’exemple de fournisseur de banque de dossiers personnels encapsulé</span><span class="sxs-lookup"><span data-stu-id="4891f-108">Install the Sample Wrapped PST Store Provider</span></span>

1. <span data-ttu-id="4891f-109">Pour télécharger le fournisseur de banque exemple encapsulé PST, voir [exemples de Code de référence Outlook 2007 supplémentaire et programme d’installation redistribuable](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span><span class="sxs-lookup"><span data-stu-id="4891f-109">To download the Sample Wrapped PST Store Provider, see [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="4891f-110">Ouvrez le dossier **SampleWrappedPSTStoreProvider** , puis cliquez sur **Extraire tous les fichiers**.</span><span class="sxs-lookup"><span data-stu-id="4891f-110">Open the **SampleWrappedPSTStoreProvider** folder and click **Extract All Files**.</span></span>
    
3. <span data-ttu-id="4891f-111">Cliquez sur **Parcourir**, sélectionnez l’emplacement où vous souhaitez enregistrer l’exemple et cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="4891f-111">Click **Browse**, select the location where you want to save the sample, and click **OK**.</span></span>
    
4. <span data-ttu-id="4891f-112">Cliquez sur **Extraire**.</span><span class="sxs-lookup"><span data-stu-id="4891f-112">Click **Extract**.</span></span> <span data-ttu-id="4891f-113">Le dossier que vous avez sélectionné apparaît et contient les fichiers extraits.</span><span class="sxs-lookup"><span data-stu-id="4891f-113">The folder you selected appears and contains the extracted files.</span></span>
    
5. <span data-ttu-id="4891f-114">Ouvrez Visual Studio 2005 en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="4891f-114">Open Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="4891f-115">Si votre ordinateur exécute Windows XP, vous devez être connecté en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="4891f-115">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="4891f-116">Si votre ordinateur exécute Windows Vista, vous devez être connecté en comme un administrateur et que vous devez avec le bouton droit de l’icône de Visual Studio 2005, cliquez sur **Exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="4891f-116">If your computer is running Windows Vista, you must be logged in as an Administrator and you must right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
6. <span data-ttu-id="4891f-117">Dans Visual Studio 2005, cliquez sur **fichier**, sélectionnez **Ouvrir**, puis cliquez sur **Projet/Solution**.</span><span class="sxs-lookup"><span data-stu-id="4891f-117">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
7. <span data-ttu-id="4891f-118">Accédez à l’emplacement où vous avez enregistré l’exemple et cliquez sur **WrapPST**, puis cliquez sur **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="4891f-118">Browse to the location where you saved the sample, click **WrapPST**, and then click **Open**.</span></span>
    
8. <span data-ttu-id="4891f-119">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="4891f-119">On the **Build** menu, click **Build Solution**.</span></span>
    
9. <span data-ttu-id="4891f-120">Dans la boîte de dialogue **Enregistrer le fichier sous** , cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4891f-120">In the **Save File As** dialog box, click **Save**.</span></span>
    
10. <span data-ttu-id="4891f-121">Dans le dossier où vous avez enregistré l’exemple, cliquez sur le fichier **Install.bat** et cliquez sur **Exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="4891f-121">In the folder where you saved the sample, right-click the **Install.bat** file and click **Run as administrator**.</span></span>
    
11. <span data-ttu-id="4891f-122">Dans la boîte de dialogue **Contrôle de compte d’utilisateur** , cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="4891f-122">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4891f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4891f-123">See also</span></span>



[<span data-ttu-id="4891f-124">À propos de l’exemple de fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="4891f-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="4891f-125">Initialisation d’un fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="4891f-125">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="4891f-126">Connexion à un fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="4891f-126">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="4891f-127">Utilisation d’un fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="4891f-127">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="4891f-128">Arrêt d’un fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="4891f-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

