---
title: Installation de l'exemple de complément d'État hors connexion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Dernière modification: juillet 06, 2012'
ms.openlocfilehash: b7b9ce539537e0759020ef7e3b4f6541a940d6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317212"
---
# <a name="installing-the-sample-offline-state-add-in"></a><span data-ttu-id="e5db6-103">Installation de l'exemple de complément d'État hors connexion</span><span class="sxs-lookup"><span data-stu-id="e5db6-103">Installing the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="e5db6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5db6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5db6-105">Cette rubrique décrit les étapes à suivre pour télécharger et installer l'exemple de complément d'État hors connexion.</span><span class="sxs-lookup"><span data-stu-id="e5db6-105">This topic takes you through the steps to download and install the Sample Offline State Add-in.</span></span> <span data-ttu-id="e5db6-106">L'exemple de complément d'État hors connexion est un complément COM qui ajoute un menu d' **État hors** connexion à Outlook et utilise l'API d'État hors connexion.</span><span class="sxs-lookup"><span data-stu-id="e5db6-106">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="e5db6-107">Le menu État hors connexion vous permet d'activer ou de désactiver l'analyse de l'État, de vérifier l'état actuel et de modifier l'état actuel.</span><span class="sxs-lookup"><span data-stu-id="e5db6-107">Through the Offline State menu you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="e5db6-108">Pour plus d'informations sur la façon dont le complément d'État hors connexion est implémenté, consultez la rubrique [configuration d'un complément d'État hors connexion](setting-up-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="e5db6-108">For more information about how the Offline State Add-in is implemented, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
## <a name="install-the-sample-offline-state-add-in"></a><span data-ttu-id="e5db6-109">Installer l'exemple de complément d'État hors connexion</span><span class="sxs-lookup"><span data-stu-id="e5db6-109">Install the Sample Offline State Add-in</span></span>

1. <span data-ttu-id="e5db6-110">Téléchargez l'exemple de complément d'État hors connexion ici: [exemples de code de référence auxiliaire Outlook 2007 et programme d'installation](https://www.microsoft.com/en-us/download/details.aspx?id=24102)redistribuable.</span><span class="sxs-lookup"><span data-stu-id="e5db6-110">Download the Sample Offline State Add-in here: [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="e5db6-111">Exécutez Visual Studio 2005 en tant qu'administrateur.</span><span class="sxs-lookup"><span data-stu-id="e5db6-111">Run Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="e5db6-112">Si votre ordinateur fonctionne sous Windows XP, vous devez être connecté en tant qu'administrateur.</span><span class="sxs-lookup"><span data-stu-id="e5db6-112">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="e5db6-113">Si votre ordinateur exécute Windows Vista, vous devez être connecté en tant qu'administrateur.</span><span class="sxs-lookup"><span data-stu-id="e5db6-113">If your computer is running Windows Vista, you must be logged in as an Administrator.</span></span> <span data-ttu-id="e5db6-114">Cliquez avec le bouton droit sur l'icône Visual Studio 2005, puis cliquez sur **exécuter en tant qu'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="e5db6-114">Right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
3. <span data-ttu-id="e5db6-115">Dans Visual Studio 2005, cliquez sur **fichier**, sur **ouvrir**, puis sur **projet/solution**.</span><span class="sxs-lookup"><span data-stu-id="e5db6-115">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
4. <span data-ttu-id="e5db6-116">Naviguez jusqu'à l'emplacement où vous avez enregistré l'exemple, cliquez sur **ConnectionStateAddin**, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="e5db6-116">Browse to the location where you saved the sample, click **ConnectionStateAddin**, and then click **Open**.</span></span>
    
5. <span data-ttu-id="e5db6-117">Dans le menu **Générer**, cliquez sur **Générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="e5db6-117">On the **Build** menu, click **Build Solution**.</span></span>
    
6. <span data-ttu-id="e5db6-118">Dans la boîte de dialogue **enregistrer le fichier sous** , cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="e5db6-118">In the **Save File As** dialog box, click **Save**.</span></span>
    
7. <span data-ttu-id="e5db6-119">Cliquez sur le menu **Démarrer** , cliquez sur **tous les programmes**, cliquez sur **accessoires**, cliquez avec le bouton droit sur **invite de commandes**, puis cliquez sur **exécuter en tant qu'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="e5db6-119">Click the **Start** menu, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="e5db6-120">Si vous exécutez Windows XP, vous devez être connecté en tant qu'administrateur.</span><span class="sxs-lookup"><span data-stu-id="e5db6-120">If you are running Windows XP, you must be logged in as an Administrator.</span></span> 
  
8. <span data-ttu-id="e5db6-121">Dans la boîte de dialogue **contrôle de compte d'utilisateur** , cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="e5db6-121">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
9. <span data-ttu-id="e5db6-122">Dans la fenêtre d' **invite de commandes** , accédez au dossier de débogage dans lequel vous avez enregistré l'exemple.</span><span class="sxs-lookup"><span data-stu-id="e5db6-122">In the **Command Prompt** window, change directories to the Debug folder where you saved the sample.</span></span> <span data-ttu-id="e5db6-123">Par exemple, si vous avez enregistré l'exemple sur le C:\ tapez **CD «C:\ConnectionStateAddin\Debug»** , puis appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="e5db6-123">For example, if you saved the sample on your C:\ drive, you would type **cd "C:\ConnectionStateAddin\Debug"** and then press **ENTER**.</span></span> 
    
10. <span data-ttu-id="e5db6-124">Tapez **regsvr32 OfflineStateAddin. dll** , puis appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="e5db6-124">Type **regsvr32 OfflineStateAddin.dll** and press **ENTER**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="e5db6-125">Pour désinstaller l'exemple de complément d'État hors connexion, tapez **regsvr32-u OfflineStateAddin. dll**</span><span class="sxs-lookup"><span data-stu-id="e5db6-125">To uninstall the Sample Offline State Add-in, type **regsvr32 -u OfflineStateAddin.dll**</span></span>
  
11. <span data-ttu-id="e5db6-126">Dans la boîte de dialogue **Regsrv32** , cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e5db6-126">In the **RegSrv32** dialog box, click **OK**.</span></span>
    
12. <span data-ttu-id="e5db6-127">ReDémarrez Outlook pour afficher le menu **État hors connexion** .</span><span class="sxs-lookup"><span data-stu-id="e5db6-127">Restart Outlook to see the **Offline State** menu.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e5db6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5db6-128">See also</span></span>



[<span data-ttu-id="e5db6-129">À propos de l’API d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="e5db6-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="e5db6-130">Installation de l’exemple de complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="e5db6-130">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="e5db6-131">À propos de l’exemple de complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="e5db6-131">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="e5db6-132">Configuration d’un complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="e5db6-132">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
  
[<span data-ttu-id="e5db6-133">Surveillance des modifications de l’état de connexion à l’aide d’un complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="e5db6-133">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[<span data-ttu-id="e5db6-134">Déconnexion d'un complément d'État hors connexion</span><span class="sxs-lookup"><span data-stu-id="e5db6-134">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

