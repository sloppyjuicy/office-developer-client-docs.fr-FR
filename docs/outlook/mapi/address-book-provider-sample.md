---
title: Exemple de fournisseur de carnets d’adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fa2a447d0757e75c95d7dc3d9b1dd16b8c7a8084
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394719"
---
# <a name="address-book-provider-sample"></a><span data-ttu-id="d8238-103">Exemple de fournisseur de carnets d’adresses</span><span class="sxs-lookup"><span data-stu-id="d8238-103">Address Book Provider Sample</span></span>

  
  
<span data-ttu-id="d8238-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8238-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8238-105">Cet exemple prend en charge un seul conteneur en lecture seule pour les noms complets et les adresses de messagerie, qui sont lues à partir d’un fichier binaire plat.</span><span class="sxs-lookup"><span data-stu-id="d8238-105">This sample supports a single read-only container for display names and email addresses, which are read from a flat binary file.</span></span> <span data-ttu-id="d8238-106">L’exemple prend en charge les modèles uniques et toutes les options de configuration à l’exception de l’Assistant profil.</span><span class="sxs-lookup"><span data-stu-id="d8238-106">The sample supports one-off templates and all configuration options except the Profile Wizard.</span></span>
  
<span data-ttu-id="d8238-107">Vous pouvez télécharger cet exemple à partir des [Exemples de Code Outlook MAPI (Messaging API)](https://go.microsoft.com/fwlink/?LinkId=129740
).</span><span class="sxs-lookup"><span data-stu-id="d8238-107">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](https://go.microsoft.com/fwlink/?LinkId=129740
).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d8238-108">Fichier exécutable :</span><span class="sxs-lookup"><span data-stu-id="d8238-108">Executable:</span></span>  <br/> |<span data-ttu-id="d8238-109">SABP32.dll</span><span class="sxs-lookup"><span data-stu-id="d8238-109">SABP32.dll</span></span>  <br/> |
| <span data-ttu-id="d8238-110">Répertoire de code source :</span><span class="sxs-lookup"><span data-stu-id="d8238-110">Source code directory:</span></span>  <br/> |<span data-ttu-id="d8238-111">SampleAddressBookProvider\SABP</span><span class="sxs-lookup"><span data-stu-id="d8238-111">SampleAddressBookProvider\SABP</span></span>  <br/> |
|<span data-ttu-id="d8238-112">Langue :</span><span class="sxs-lookup"><span data-stu-id="d8238-112">Language:</span></span>  <br/> |<span data-ttu-id="d8238-113">C++</span><span class="sxs-lookup"><span data-stu-id="d8238-113">C++</span></span>  <br/> |
|<span data-ttu-id="d8238-114">Plateformes :</span><span class="sxs-lookup"><span data-stu-id="d8238-114">Platforms:</span></span>  <br/> |<span data-ttu-id="d8238-115">Microsoft Visual Studio 2008 pour compiler pour Windows Vista, Windows Server 2008, Windows XP SP2 et Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="d8238-115">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="d8238-116">Fonctionnalités prises en charge</span><span class="sxs-lookup"><span data-stu-id="d8238-116">Supported Features</span></span>

<span data-ttu-id="d8238-117">Cet exemple prend en charge les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="d8238-117">This sample supports the following features:</span></span>
  
- <span data-ttu-id="d8238-118">Restrictions de table.</span><span class="sxs-lookup"><span data-stu-id="d8238-118">Table restrictions.</span></span> <span data-ttu-id="d8238-119">L’exemple implémente résolution-correspondance de préfixe et de nom ambigu.</span><span class="sxs-lookup"><span data-stu-id="d8238-119">The sample implements prefix-match and ambiguous-name resolution.</span></span> <span data-ttu-id="d8238-120">Il n’implémente pas la langue de restriction MAPI complète et restrictions sont pris en charge uniquement sur le nom complet.</span><span class="sxs-lookup"><span data-stu-id="d8238-120">It does not implement the full MAPI restriction language, and restrictions are supported only on the display name.</span></span>
    
- <span data-ttu-id="d8238-121">Une table d’affichage Détails pour les utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="d8238-121">A details display table for messaging users.</span></span> 
    
- <span data-ttu-id="d8238-122">Adresses uniques.</span><span class="sxs-lookup"><span data-stu-id="d8238-122">One-off addresses.</span></span>
    
- <span data-ttu-id="d8238-123">Une boîte de dialogue Recherche avancée.</span><span class="sxs-lookup"><span data-stu-id="d8238-123">An advanced search dialog box.</span></span>
    
- <span data-ttu-id="d8238-124">Un [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span><span class="sxs-lookup"><span data-stu-id="d8238-124">An [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="d8238-125">Cette interface est partiellement pris en charge ; ses méthodes **IMAPIProp** sont délégués à l’interface **IPropData** .</span><span class="sxs-lookup"><span data-stu-id="d8238-125">This interface is partially supported; its **IMAPIProp** methods are delegated to the **IPropData** interface.</span></span> <span data-ttu-id="d8238-126">Pour plus d’informations, voir la [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span><span class="sxs-lookup"><span data-stu-id="d8238-126">For more information, see the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="d8238-127">Configuration interactive et par programmation.</span><span class="sxs-lookup"><span data-stu-id="d8238-127">Interactive and programmatic configuration.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="d8238-128">Fonctionnalités non prises en charge</span><span class="sxs-lookup"><span data-stu-id="d8238-128">Unsupported Features</span></span>

<span data-ttu-id="d8238-129">Cet exemple ne prend pas en charge les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="d8238-129">This sample does not support the following features:</span></span>
  
- <span data-ttu-id="d8238-130">Tri.</span><span class="sxs-lookup"><span data-stu-id="d8238-130">Sorting.</span></span>
    
- <span data-ttu-id="d8238-131">Listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="d8238-131">Distribution lists.</span></span>
    
- <span data-ttu-id="d8238-132">Création, suppression et modification des entrées.</span><span class="sxs-lookup"><span data-stu-id="d8238-132">Creating, deleting, and modifying entries.</span></span>
    
- <span data-ttu-id="d8238-133">Propriétés à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="d8238-133">Properties with multiple values.</span></span>
    
- <span data-ttu-id="d8238-134">Propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="d8238-134">Named properties.</span></span>
    
- <span data-ttu-id="d8238-135">Faire la distinction entre le prénom et le nom dans les noms complets.</span><span class="sxs-lookup"><span data-stu-id="d8238-135">Distinguishing between first and last names in display names.</span></span>
    
 <span data-ttu-id="d8238-136">**Pour installer l’exemple de fournisseur de carnet d’adresses**</span><span class="sxs-lookup"><span data-stu-id="d8238-136">**To install the Sample Address Book Provider**</span></span>
  
1. <span data-ttu-id="d8238-137">Pour télécharger l’exemple de fournisseur de carnet d’adresses, voir [le téléchargement d’exemples MAPI Outlook](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="d8238-137">To download the Sample Address Book Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="d8238-138">Recherchez le dossier où vous avez enregistré les exemples de MAPI Outlook.</span><span class="sxs-lookup"><span data-stu-id="d8238-138">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="d8238-139">Avec le bouton droit la \*\*OutlookMAPISamples -\<numéro de version\> \*\* zip du dossier, puis cliquez sur **Extraire tout**.</span><span class="sxs-lookup"><span data-stu-id="d8238-139">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="d8238-140">Cliquez sur **Parcourir**, sélectionnez l’emplacement où vous souhaitez enregistrer l’exemple et cliquez sur **Extraire**.</span><span class="sxs-lookup"><span data-stu-id="d8238-140">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="d8238-141">Exécutez Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="d8238-141">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="d8238-142">Dans Visual Studio 2008, cliquez sur **fichier**, sélectionnez **Ouvrir**, puis cliquez sur **Projet/Solution**.</span><span class="sxs-lookup"><span data-stu-id="d8238-142">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="d8238-143">Accédez à l’emplacement où vous avez enregistré l’exemple et cliquez sur **SABP.vcproj**, puis cliquez sur **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="d8238-143">Browse to the location where you saved the sample, click **SABP.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="d8238-144">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="d8238-144">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="d8238-145">Dans la boîte de dialogue **Enregistrer le fichier sous** , cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="d8238-145">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="d8238-146">Dans le dossier où vous avez enregistré l’exemple, cliquez sur le fichier **install.bat** et cliquez sur **Exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="d8238-146">In the folder where you saved the sample, right-click the **install.bat** file and click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="d8238-147">Dans la boîte de dialogue **Contrôle de compte d’utilisateur** , cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="d8238-147">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="d8238-148">**Install.bat** cette méthode copie la DLL dans le dossier d’installation par défaut de Microsoft Office, C:\Program Files\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="d8238-148">**Install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="d8238-149">Si vous avez installé des produits Office dans un autre emplacement, cliquez sur **Install.bat** , cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="d8238-149">If you have installed Office products in a different location, right-click **Install.bat** and click **Edit**.</span></span> <span data-ttu-id="d8238-150">Le fichier s’ouvre dans le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="d8238-150">The file opens in Notepad.</span></span> <span data-ttu-id="d8238-151">Remplacez le chemin d’installation par défaut par le chemin d’installation sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d8238-151">Replace the default installation path with the installation path used on your computer.</span></span> 
  

