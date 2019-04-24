---
title: Inscription d’un fournisseur
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: Cette rubrique décrit les emplacements de Registre Windows qui sont utilisés lors de l'installation d'un fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: a5f76850f9bebcba3c2bff31e799a3b012d6b91a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329210"
---
# <a name="registering-a-provider"></a><span data-ttu-id="e0da4-103">Inscription d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="e0da4-103">Registering a provider</span></span>

<span data-ttu-id="e0da4-104">Cette rubrique décrit les emplacements de Registre Windows qui sont utilisés lors de l'installation d'un fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="e0da4-104">This topic describes the Windows registry locations that are used when you install an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="com-registration"></a><span data-ttu-id="e0da4-105">Inscription COM</span><span class="sxs-lookup"><span data-stu-id="e0da4-105">COM registration</span></span>

<span data-ttu-id="e0da4-106">Vous devez configurer la DLL du fournisseur OSC pour enregistrer à l'aide de l'auto-enregistrement COM ou de regsvr32 lors de l'installation.</span><span class="sxs-lookup"><span data-stu-id="e0da4-106">You must configure the OSC provider DLL to register using COM self-registration or regsvr32 during installation.</span></span> <span data-ttu-id="e0da4-107">L'inscription COM de la DLL du fournisseur enregistre le fournisseur OSC sous `HKEY_CLASSES_ROOT` la ruche de registre.</span><span class="sxs-lookup"><span data-stu-id="e0da4-107">COM registration of the provider DLL registers the OSC provider under the `HKEY_CLASSES_ROOT` registry hive.</span></span> 
  
<span data-ttu-id="e0da4-108">Un fournisseur OSC développé dans le code managé dispose d'un assembly de fournisseur visible par COM.</span><span class="sxs-lookup"><span data-stu-id="e0da4-108">An OSC provider developed in managed code has a COM-visible provider assembly.</span></span> <span data-ttu-id="e0da4-109">Vous devez utiliser un domaine d'application distinct pour le composant fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e0da4-109">You should use a separate application domain for the provider component.</span></span> <span data-ttu-id="e0da4-110">Dans le cas contraire, le fournisseur OSC utilise le domaine d'application partagé par défaut qui est utilisé par d'autres composants, et le fournisseur peut ne pas fonctionner comme prévu.</span><span class="sxs-lookup"><span data-stu-id="e0da4-110">Otherwise, the OSC provider uses the default shared application domain that is used by other components, and the provider may not operate as expected.</span></span>
  
## <a name="registering-provider-progid"></a><span data-ttu-id="e0da4-111">Inscription du ProgID du fournisseur</span><span class="sxs-lookup"><span data-stu-id="e0da4-111">Registering provider ProgID</span></span>

<span data-ttu-id="e0da4-112">Chaque fournisseur OSC doit inscrire un identificateur programmatique (`ProgID`).</span><span class="sxs-lookup"><span data-stu-id="e0da4-112">Each OSC provider must register a programmatic identifier (`ProgID`).</span></span> <span data-ttu-id="e0da4-113">Le programme d'installation du fournisseur peut choisir l'un des emplacements suivants pour ajouter `ProgID`ou supprimer:</span><span class="sxs-lookup"><span data-stu-id="e0da4-113">The provider installer can choose one of the following locations to add or remove the `ProgID`:</span></span>
  
- <span data-ttu-id="e0da4-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Le programme d'installation de votre fournisseur doit utiliser cet emplacement si le fournisseur est installé uniquement pour l'utilisateur actuellement connecté.</span><span class="sxs-lookup"><span data-stu-id="e0da4-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for only the currently logged-on user.</span></span>
    
- <span data-ttu-id="e0da4-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Le programme d'installation de votre fournisseur doit utiliser cet emplacement si le fournisseur est installé pour tous les utilisateurs sur l'ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e0da4-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for all users on the computer.</span></span>
    
<span data-ttu-id="e0da4-116">Le OSC recherche le fournisseur `ProgID` aux emplacements ci-dessus, sauf si l'ordinateur client dispose d'Outlook 32 bits s'exécutant sur un système d'exploitation Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e0da4-116">The OSC looks for the provider  `ProgID` in the above locations, unless the client computer has 32-bit Outlook running on a 64-bit Windows operating system.</span></span> <span data-ttu-id="e0da4-117">Dans ce cas, le programme d'installation de votre fournisseur doit choisir l'un des emplacements `HKEY_CURRENT_USER` suivants `HKEY_LOCAL_MACHINE` dans la ruche ou:</span><span class="sxs-lookup"><span data-stu-id="e0da4-117">In such a case, your provider installer should choose one of the following locations in the  `HKEY_CURRENT_USER` or  `HKEY_LOCAL_MACHINE` hive:</span></span> 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
<span data-ttu-id="e0da4-118">Pour une version «démarrer en un clic» d'Office, le programme d'installation de votre fournisseur doit choisir l'un des emplacements suivants dans la ruche HKEY_CURRENT_USER ou HKEY_LOCAL_MACHINE:</span><span class="sxs-lookup"><span data-stu-id="e0da4-118">For a Click-to-Run version of Office, your provider installer should choose one of the following locations in the HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE hive:</span></span>
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a><span data-ttu-id="e0da4-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0da4-119">See also</span></span>

- [<span data-ttu-id="e0da4-120">Liste de vérification de l'installation</span><span class="sxs-lookup"><span data-stu-id="e0da4-120">Installation Checklist</span></span>](installation-checklist.md)
- [<span data-ttu-id="e0da4-121">Étapes rapides pour apprendre à développer un fournisseur</span><span class="sxs-lookup"><span data-stu-id="e0da4-121">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="e0da4-122">Déploiement d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="e0da4-122">Deploying a Provider</span></span>](deploying-a-provider.md)

