---
title: L’installation de l’exemple en mode hors connexion d’état complément
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Dernière modification : 06 juillet 2012'
ms.openlocfilehash: 00232f290c367c4bab1854bfe3909abc7b03cef8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784338"
---
# <a name="installing-the-sample-offline-state-add-in"></a><span data-ttu-id="73938-103">L’installation de l’exemple en mode hors connexion d’état complément</span><span class="sxs-lookup"><span data-stu-id="73938-103">Installing the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="73938-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="73938-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="73938-105">Cette rubrique présente les étapes pour télécharger et installer le complément exemple hors connexion état.</span><span class="sxs-lookup"><span data-stu-id="73938-105">This topic takes you through the steps to download and install the Sample Offline State Add-in.</span></span> <span data-ttu-id="73938-106">Le complément exemple hors connexion état est un complément COM qui ajoute un menu **État hors connexion** dans Outlook et utilise l’API de l’état en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="73938-106">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="73938-107">Via le menu état hors connexion, vous pouvez activer ou désactiver l’analyse de l’état, vérifiez l’état actuel et modifier l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="73938-107">Through the Offline State menu you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="73938-108">Pour plus d’informations sur la façon dont le complément état hors connexion est implémenté, voir [définition d’une en mode hors connexion de l’état Add-in](setting-up-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="73938-108">For more information about how the Offline State Add-in is implemented, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
## <a name="install-the-sample-offline-state-add-in"></a><span data-ttu-id="73938-109">Installer l’exemple en mode hors connexion d’état complément</span><span class="sxs-lookup"><span data-stu-id="73938-109">Install the Sample Offline State Add-in</span></span>

1. <span data-ttu-id="73938-110">Télécharger l’exemple hors connexion état complément ici : [exemples de Code de référence Outlook 2007 supplémentaire et programme d’installation redistribuable](http://www.microsoft.com/en-us/download/details.aspx?id=24102).</span><span class="sxs-lookup"><span data-stu-id="73938-110">Download the Sample Offline State Add-in here: [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](http://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="73938-111">Exécutez Visual Studio 2005 en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="73938-111">Run Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="73938-112">Si votre ordinateur exécute Windows XP, vous devez être connecté en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="73938-112">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="73938-113">Si votre ordinateur exécute Windows Vista, vous devez être connecté en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="73938-113">If your computer is running Windows Vista, you must be logged in as an Administrator.</span></span> <span data-ttu-id="73938-114">Cliquez sur l’icône de Visual Studio 2005, cliquez sur **Exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="73938-114">Right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
3. <span data-ttu-id="73938-115">Dans Visual Studio 2005, cliquez sur **fichier**, sélectionnez **Ouvrir**, puis cliquez sur **Projet/Solution**.</span><span class="sxs-lookup"><span data-stu-id="73938-115">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
4. <span data-ttu-id="73938-116">Accédez à l’emplacement où vous avez enregistré l’exemple et cliquez sur **ConnectionStateAddin**, puis cliquez sur **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="73938-116">Browse to the location where you saved the sample, click **ConnectionStateAddin**, and then click **Open**.</span></span>
    
5. <span data-ttu-id="73938-117">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="73938-117">On the **Build** menu, click **Build Solution**.</span></span>
    
6. <span data-ttu-id="73938-118">Dans la boîte de dialogue **Enregistrer le fichier sous** , cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="73938-118">In the **Save File As** dialog box, click **Save**.</span></span>
    
7. <span data-ttu-id="73938-119">Cliquez sur le menu **Démarrer** , sur **Tous les programmes**, sur **Accessoires**, avec le bouton droit **invite de commandes**, puis cliquez sur **Exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="73938-119">Click the **Start** menu, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="73938-120">Si vous exécutez Windows XP, vous devez être connecté en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="73938-120">If you are running Windows XP, you must be logged in as an Administrator.</span></span> 
  
8. <span data-ttu-id="73938-121">Dans la boîte de dialogue **Contrôle de compte d’utilisateur** , cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="73938-121">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
9. <span data-ttu-id="73938-122">Dans la fenêtre **d’invite de commandes** , accédez au dossier où vous avez enregistré l’exemple Debug.</span><span class="sxs-lookup"><span data-stu-id="73938-122">In the **Command Prompt** window, change directories to the Debug folder where you saved the sample.</span></span> <span data-ttu-id="73938-123">Par exemple, si vous avez enregistré l’exemple sur votre lecteur C:\, vous souhaite tapez **cd « C:\ConnectionStateAddin\Debug »** , puis appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="73938-123">For example, if you saved the sample on your C:\ drive, you would type **cd "C:\ConnectionStateAddin\Debug"** and then press **ENTER**.</span></span> 
    
10. <span data-ttu-id="73938-124">Tapez **regsvr32 OfflineStateAddin.dll** et appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="73938-124">Type **regsvr32 OfflineStateAddin.dll** and press **ENTER**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="73938-125">Pour désinstaller le complément exemple hors connexion état, tapez **regsvr32-u OfflineStateAddin.dll**</span><span class="sxs-lookup"><span data-stu-id="73938-125">To uninstall the Sample Offline State Add-in, type **regsvr32 -u OfflineStateAddin.dll**</span></span>
  
11. <span data-ttu-id="73938-126">Dans la boîte de dialogue **RegSrv32** , cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="73938-126">In the **RegSrv32** dialog box, click **OK**.</span></span>
    
12. <span data-ttu-id="73938-127">Redémarrez Outlook pour afficher le menu **d’État hors connexion** .</span><span class="sxs-lookup"><span data-stu-id="73938-127">Restart Outlook to see the **Offline State** menu.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="73938-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73938-128">See also</span></span>



[<span data-ttu-id="73938-129">À propos de l’API d’état en mode hors connexion</span><span class="sxs-lookup"><span data-stu-id="73938-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="73938-130">L’installation de l’exemple en mode hors connexion d’état complément</span><span class="sxs-lookup"><span data-stu-id="73938-130">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="73938-131">À propos de l’exemple en mode hors connexion-dans l’état</span><span class="sxs-lookup"><span data-stu-id="73938-131">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="73938-132">Configuration d’un complément en mode hors connexion d’état</span><span class="sxs-lookup"><span data-stu-id="73938-132">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
  
[<span data-ttu-id="73938-133">Analyse l’état de connexion change utilisant un complément en mode hors connexion d’état</span><span class="sxs-lookup"><span data-stu-id="73938-133">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[<span data-ttu-id="73938-134">Déconnexion d’un complément en mode hors connexion d’état</span><span class="sxs-lookup"><span data-stu-id="73938-134">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

