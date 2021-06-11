---
title: Exemple de fournisseur de carnet d’adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fa2a447d0757e75c95d7dc3d9b1dd16b8c7a8084
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331107"
---
# <a name="address-book-provider-sample"></a><span data-ttu-id="fca0f-103">Exemple de fournisseur de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="fca0f-103">Address Book Provider Sample</span></span>

  
  
<span data-ttu-id="fca0f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fca0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fca0f-105">Cet exemple prend en charge un conteneur en lecture seule unique pour les noms complets et les adresses e-mail, qui sont lus à partir d’un fichier binaire plat.</span><span class="sxs-lookup"><span data-stu-id="fca0f-105">This sample supports a single read-only container for display names and email addresses, which are read from a flat binary file.</span></span> <span data-ttu-id="fca0f-106">L’exemple prend en charge les modèles unique et toutes les options de configuration à l’exception de l’Assistant Profil.</span><span class="sxs-lookup"><span data-stu-id="fca0f-106">The sample supports one-off templates and all configuration options except the Profile Wizard.</span></span>
  
<span data-ttu-id="fca0f-107">Vous pouvez télécharger cet exemple à partir [Outlook de code MAPI (Messaging API).](https://go.microsoft.com/fwlink/?LinkId=129740
)</span><span class="sxs-lookup"><span data-stu-id="fca0f-107">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](https://go.microsoft.com/fwlink/?LinkId=129740
).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fca0f-108">Exécutable :</span><span class="sxs-lookup"><span data-stu-id="fca0f-108">Executable:</span></span>  <br/> |<span data-ttu-id="fca0f-109">SABP32.dll</span><span class="sxs-lookup"><span data-stu-id="fca0f-109">SABP32.dll</span></span>  <br/> |
| <span data-ttu-id="fca0f-110">Répertoire de code source :</span><span class="sxs-lookup"><span data-stu-id="fca0f-110">Source code directory:</span></span>  <br/> |<span data-ttu-id="fca0f-111">SampleAddressBookProvider\SABP</span><span class="sxs-lookup"><span data-stu-id="fca0f-111">SampleAddressBookProvider\SABP</span></span>  <br/> |
|<span data-ttu-id="fca0f-112">Langue :</span><span class="sxs-lookup"><span data-stu-id="fca0f-112">Language:</span></span>  <br/> |<span data-ttu-id="fca0f-113">C++</span><span class="sxs-lookup"><span data-stu-id="fca0f-113">C++</span></span>  <br/> |
|<span data-ttu-id="fca0f-114">Plateformes :</span><span class="sxs-lookup"><span data-stu-id="fca0f-114">Platforms:</span></span>  <br/> |<span data-ttu-id="fca0f-115">Microsoft Visual Studio 2008 à compiler pour Windows Vista, Windows Server 2008, Windows XP SP2 et Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="fca0f-115">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="fca0f-116">Fonctionnalités prise en charge</span><span class="sxs-lookup"><span data-stu-id="fca0f-116">Supported Features</span></span>

<span data-ttu-id="fca0f-117">Cet exemple prend en charge les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="fca0f-117">This sample supports the following features:</span></span>
  
- <span data-ttu-id="fca0f-118">Restrictions de tableau.</span><span class="sxs-lookup"><span data-stu-id="fca0f-118">Table restrictions.</span></span> <span data-ttu-id="fca0f-119">L’exemple implémente la correspondance de préfixe et la résolution de nom ambigu.</span><span class="sxs-lookup"><span data-stu-id="fca0f-119">The sample implements prefix-match and ambiguous-name resolution.</span></span> <span data-ttu-id="fca0f-120">Il n’implémente pas le langage de restriction MAPI complet et les restrictions sont uniquement prise en charge sur le nom complet.</span><span class="sxs-lookup"><span data-stu-id="fca0f-120">It does not implement the full MAPI restriction language, and restrictions are supported only on the display name.</span></span>
    
- <span data-ttu-id="fca0f-121">Tableau d’affichage des détails pour les utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="fca0f-121">A details display table for messaging users.</span></span> 
    
- <span data-ttu-id="fca0f-122">Adresses one-off.</span><span class="sxs-lookup"><span data-stu-id="fca0f-122">One-off addresses.</span></span>
    
- <span data-ttu-id="fca0f-123">Boîte de dialogue de recherche avancée.</span><span class="sxs-lookup"><span data-stu-id="fca0f-123">An advanced search dialog box.</span></span>
    
- <span data-ttu-id="fca0f-124">Interface [IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="fca0f-124">An [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="fca0f-125">Cette interface est partiellement prise en charge . ses **méthodes IMAPIProp** sont déléguées à l’interface **IPropData.**</span><span class="sxs-lookup"><span data-stu-id="fca0f-125">This interface is partially supported; its **IMAPIProp** methods are delegated to the **IPropData** interface.</span></span> <span data-ttu-id="fca0f-126">Pour plus d’informations, voir [l’interface IPropData : IMAPIProp.](ipropdataimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="fca0f-126">For more information, see the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="fca0f-127">Configuration interactive et par programmation.</span><span class="sxs-lookup"><span data-stu-id="fca0f-127">Interactive and programmatic configuration.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="fca0f-128">Fonctionnalités non pris en compte</span><span class="sxs-lookup"><span data-stu-id="fca0f-128">Unsupported Features</span></span>

<span data-ttu-id="fca0f-129">Cet exemple ne prend pas en charge les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="fca0f-129">This sample does not support the following features:</span></span>
  
- <span data-ttu-id="fca0f-130">Tri.</span><span class="sxs-lookup"><span data-stu-id="fca0f-130">Sorting.</span></span>
    
- <span data-ttu-id="fca0f-131">Listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="fca0f-131">Distribution lists.</span></span>
    
- <span data-ttu-id="fca0f-132">Création, suppression et modification d’entrées.</span><span class="sxs-lookup"><span data-stu-id="fca0f-132">Creating, deleting, and modifying entries.</span></span>
    
- <span data-ttu-id="fca0f-133">Propriétés avec plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="fca0f-133">Properties with multiple values.</span></span>
    
- <span data-ttu-id="fca0f-134">Propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="fca0f-134">Named properties.</span></span>
    
- <span data-ttu-id="fca0f-135">Distinction entre le prénom et le nom de famille dans les noms d’affichage.</span><span class="sxs-lookup"><span data-stu-id="fca0f-135">Distinguishing between first and last names in display names.</span></span>
    
 <span data-ttu-id="fca0f-136">**Pour installer l’exemple de fournisseur de carnet d’adresses**</span><span class="sxs-lookup"><span data-stu-id="fca0f-136">**To install the Sample Address Book Provider**</span></span>
  
1. <span data-ttu-id="fca0f-137">Pour télécharger l’exemple de fournisseur de carnet d’adresses, consultez [la Outlook exemples MAPI.](downloading-the-outlook-mapi-samples.md)</span><span class="sxs-lookup"><span data-stu-id="fca0f-137">To download the Sample Address Book Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="fca0f-138">Recherchez le dossier dans lequel vous avez enregistré Outlook exemples MAPI.</span><span class="sxs-lookup"><span data-stu-id="fca0f-138">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="fca0f-139">Cliquez avec le bouton droit sur le dossier zip du numéro de **\< \> version d’OutlookMAPISamples,** puis cliquez sur **Extraire tout.**</span><span class="sxs-lookup"><span data-stu-id="fca0f-139">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="fca0f-140">Cliquez **sur Parcourir,** sélectionnez l’emplacement où vous souhaitez enregistrer l’exemple, puis cliquez sur **Extraire.**</span><span class="sxs-lookup"><span data-stu-id="fca0f-140">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="fca0f-141">Exécutez Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="fca0f-141">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="fca0f-142">Dans Visual Studio 2008, cliquez sur **Fichier,** sélectionnez **Ouvrir,** puis cliquez sur **Project/Solution**.</span><span class="sxs-lookup"><span data-stu-id="fca0f-142">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="fca0f-143">Accédez à l’emplacement où vous avez enregistré l’exemple, cliquez sur **SABP.vcproj,** puis cliquez sur **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="fca0f-143">Browse to the location where you saved the sample, click **SABP.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="fca0f-144">Dans le menu **Générer**, cliquez sur **Générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="fca0f-144">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="fca0f-145">Dans la **boîte de dialogue Enregistrer le fichier sous,** cliquez sur **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="fca0f-145">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="fca0f-146">Dans le dossier où vous avez enregistré l’exemple, cliquez avec le bouton droit sur **le fichierinstall.bat** puis cliquez sur Exécuter en tant **qu’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="fca0f-146">In the folder where you saved the sample, right-click the **install.bat** file and click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="fca0f-147">Dans la boîte **de dialogue Contrôle de compte** d’utilisateur, cliquez sur **Continuer.**</span><span class="sxs-lookup"><span data-stu-id="fca0f-147">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="fca0f-148">**Install.bat** copie le .dll dans le dossier d Microsoft Office d’installation par défaut, C:\Program Files\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="fca0f-148">**Install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="fca0f-149">Si vous avez installé Office produits à un autre emplacement, cliquez avec le bouton droit sur **Install.bat** puis cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="fca0f-149">If you have installed Office products in a different location, right-click **Install.bat** and click **Edit**.</span></span> <span data-ttu-id="fca0f-150">Le fichier s’ouvre en Bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="fca0f-150">The file opens in Notepad.</span></span> <span data-ttu-id="fca0f-151">Remplacez le chemin d’installation par défaut par le chemin d’installation utilisé sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fca0f-151">Replace the default installation path with the installation path used on your computer.</span></span> 
  

