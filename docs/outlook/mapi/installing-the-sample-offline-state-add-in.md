---
title: Installation de l’exemple de add-in d’état hors connexion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Last modified: July 06, 2012'
ms.openlocfilehash: b7b9ce539537e0759020ef7e3b4f6541a940d6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317212"
---
# <a name="installing-the-sample-offline-state-add-in"></a><span data-ttu-id="2e163-103">Installation de l’exemple de add-in d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="2e163-103">Installing the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="2e163-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e163-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e163-105">Cette rubrique vous fait suivre les étapes de téléchargement et d’installation de l’exemple de add-in d’état hors connexion.</span><span class="sxs-lookup"><span data-stu-id="2e163-105">This topic takes you through the steps to download and install the Sample Offline State Add-in.</span></span> <span data-ttu-id="2e163-106">L’exemple de compl?ment d’état hors ligne est un compl?ment COM qui ajoute un **menu** d’état hors connexion Outlook et utilise l’API d’état hors connexion.</span><span class="sxs-lookup"><span data-stu-id="2e163-106">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="2e163-107">Le menu État hors connexion vous permet d’activer ou de désactiver la surveillance de l’état, de vérifier l’état actuel et de modifier l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="2e163-107">Through the Offline State menu you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="2e163-108">Pour plus d’informations sur la façon dont le add-in d’état hors connexion est implémenté, voir [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="2e163-108">For more information about how the Offline State Add-in is implemented, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
## <a name="install-the-sample-offline-state-add-in"></a><span data-ttu-id="2e163-109">Installer l’exemple de add-in d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="2e163-109">Install the Sample Offline State Add-in</span></span>

1. <span data-ttu-id="2e163-110">Téléchargez l’exemple de add-in d’état hors connexion ici [: Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span><span class="sxs-lookup"><span data-stu-id="2e163-110">Download the Sample Offline State Add-in here: [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="2e163-111">Exécutez Visual Studio 2005 en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="2e163-111">Run Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="2e163-112">Si votre ordinateur exécute Windows XP, vous devez être connecté en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="2e163-112">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="2e163-113">Si votre ordinateur exécute Windows Vista, vous devez être connecté en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="2e163-113">If your computer is running Windows Vista, you must be logged in as an Administrator.</span></span> <span data-ttu-id="2e163-114">Cliquez avec le bouton droit sur Visual Studio icône 2005 et cliquez **sur Exécuter en tant qu’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="2e163-114">Right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
3. <span data-ttu-id="2e163-115">Dans Visual Studio 2005, cliquez sur **Fichier,** sélectionnez **Ouvrir,** puis cliquez sur **Project/Solution.**</span><span class="sxs-lookup"><span data-stu-id="2e163-115">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
4. <span data-ttu-id="2e163-116">Accédez à l’emplacement où vous avez enregistré l’exemple, cliquez **sur ConnectionStateAddin,** puis cliquez sur **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="2e163-116">Browse to the location where you saved the sample, click **ConnectionStateAddin**, and then click **Open**.</span></span>
    
5. <span data-ttu-id="2e163-117">Dans le menu **Générer**, cliquez sur **Générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="2e163-117">On the **Build** menu, click **Build Solution**.</span></span>
    
6. <span data-ttu-id="2e163-118">Dans la **boîte de dialogue Enregistrer le fichier sous,** cliquez sur **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="2e163-118">In the **Save File As** dialog box, click **Save**.</span></span>
    
7. <span data-ttu-id="2e163-119">Cliquez sur **le** menu Démarrer, cliquez sur **Tous** les programmes, cliquez sur **Accessoires,** cliquez avec le bouton droit sur Invite de **commandes,** puis cliquez sur Exécuter en **tant qu’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="2e163-119">Click the **Start** menu, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="2e163-120">Si vous exécutez Windows XP, vous devez être connecté en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="2e163-120">If you are running Windows XP, you must be logged in as an Administrator.</span></span> 
  
8. <span data-ttu-id="2e163-121">Dans la boîte **de dialogue Contrôle de compte** d’utilisateur, cliquez sur **Continuer.**</span><span class="sxs-lookup"><span data-stu-id="2e163-121">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
9. <span data-ttu-id="2e163-122">Dans la **fenêtre Invite de** commandes, modifiez les répertoires vers le dossier Débogage dans lequel vous avez enregistré l’exemple.</span><span class="sxs-lookup"><span data-stu-id="2e163-122">In the **Command Prompt** window, change directories to the Debug folder where you saved the sample.</span></span> <span data-ttu-id="2e163-123">Par exemple, si vous avez enregistré l’exemple sur votre C:\ lecteur, vous tapez **cd « C:\ConnectionStateAddin\Debug »,** puis appuyez sur **Entrée**.</span><span class="sxs-lookup"><span data-stu-id="2e163-123">For example, if you saved the sample on your C:\ drive, you would type **cd "C:\ConnectionStateAddin\Debug"** and then press **ENTER**.</span></span> 
    
10. <span data-ttu-id="2e163-124">Tapez **regsvr32 OfflineStateAddin.dll** appuyez sur **Entrée**.</span><span class="sxs-lookup"><span data-stu-id="2e163-124">Type **regsvr32 OfflineStateAddin.dll** and press **ENTER**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="2e163-125">Pour désinstaller l’exemple de add-in d’état hors connexion, tapez **regsvr32 -u OfflineStateAddin.dll**</span><span class="sxs-lookup"><span data-stu-id="2e163-125">To uninstall the Sample Offline State Add-in, type **regsvr32 -u OfflineStateAddin.dll**</span></span>
  
11. <span data-ttu-id="2e163-126">Dans la **boîte de dialogue RegSrv32,** cliquez sur **OK.**</span><span class="sxs-lookup"><span data-stu-id="2e163-126">In the **RegSrv32** dialog box, click **OK**.</span></span>
    
12. <span data-ttu-id="2e163-127">Redémarrez Outlook pour voir le menu **État** hors connexion.</span><span class="sxs-lookup"><span data-stu-id="2e163-127">Restart Outlook to see the **Offline State** menu.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2e163-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e163-128">See also</span></span>



[<span data-ttu-id="2e163-129">À propos de l’API d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="2e163-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="2e163-130">Installation de l’exemple de complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="2e163-130">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="2e163-131">À propos de l’exemple de complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="2e163-131">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="2e163-132">Configuration d’un complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="2e163-132">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
  
[<span data-ttu-id="2e163-133">Surveillance des modifications de l’état de connexion à l’aide d’un complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="2e163-133">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[<span data-ttu-id="2e163-134">Déconnexion d’un add-in d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="2e163-134">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

