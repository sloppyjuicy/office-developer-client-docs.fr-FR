---
title: Inscription d’un fournisseur
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: Cette rubrique décrit les emplacements du Registre Windows qui sont utilisés lorsque vous installez un fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: 3ec594ec94b045d2ceb583144781a5746b945b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787698"
---
# <a name="registering-a-provider"></a><span data-ttu-id="ecfc2-103">Inscription d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="ecfc2-103">Registering a provider</span></span>

<span data-ttu-id="ecfc2-104">Cette rubrique décrit les emplacements du Registre Windows qui sont utilisés lorsque vous installez un fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="ecfc2-104">This topic describes the Windows registry locations that are used when you install an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="com-registration"></a><span data-ttu-id="ecfc2-105">Enregistrement COM</span><span class="sxs-lookup"><span data-stu-id="ecfc2-105">COM registration</span></span>

<span data-ttu-id="ecfc2-106">Vous devez configurer le fournisseur OSC DLL à inscrire à l’aide de l’inscription automatique COM ou regsvr32 pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="ecfc2-106">You must configure the OSC provider DLL to register using COM self-registration or regsvr32 during installation.</span></span> <span data-ttu-id="ecfc2-107">Enregistrement COM de la DLL du fournisseur enregistre le fournisseur OSC sous le `HKEY_CLASSES_ROOT` ruche du Registre.</span><span class="sxs-lookup"><span data-stu-id="ecfc2-107">COM registration of the provider DLL registers the OSC provider under the `HKEY_CLASSES_ROOT` registry hive.</span></span> 
  
<span data-ttu-id="ecfc2-108">Un fournisseur OSC développé dans le code managé a un assembly de fournisseur COM visibles.</span><span class="sxs-lookup"><span data-stu-id="ecfc2-108">An OSC provider developed in managed code has a COM-visible provider assembly.</span></span> <span data-ttu-id="ecfc2-109">Vous devez utiliser un domaine d’application distinct pour le composant fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ecfc2-109">You should use a separate application domain for the provider component.</span></span> <span data-ttu-id="ecfc2-110">Sinon, le fournisseur OSC utilise le domaine d’application partagée par défaut qui est utilisé par d’autres composants et le fournisseur peut ne pas fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="ecfc2-110">Otherwise, the OSC provider uses the default shared application domain that is used by other components, and the provider may not operate as expected.</span></span>
  
## <a name="registering-provider-progid"></a><span data-ttu-id="ecfc2-111">Inscription du fournisseur ProgID</span><span class="sxs-lookup"><span data-stu-id="ecfc2-111">Registering provider ProgID</span></span>

<span data-ttu-id="ecfc2-112">Chaque fournisseur OSC doit enregistrer un identificateur programmatique (`ProgID`).</span><span class="sxs-lookup"><span data-stu-id="ecfc2-112">Each OSC provider must register a programmatic identifier (`ProgID`).</span></span> <span data-ttu-id="ecfc2-113">Le programme d’installation fournisseur peut choisir un des emplacements suivants pour ajouter ou supprimer la `ProgID`:</span><span class="sxs-lookup"><span data-stu-id="ecfc2-113">The provider installer can choose one of the following locations to add or remove the `ProgID`:</span></span>
  
- <span data-ttu-id="ecfc2-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Votre programme d’installation du fournisseur doit utiliser cet emplacement si le fournisseur est installé pour seulement l’utilisateur actuellement connecté.</span><span class="sxs-lookup"><span data-stu-id="ecfc2-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for only the currently logged-on user.</span></span>
    
- <span data-ttu-id="ecfc2-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Votre programme d’installation du fournisseur doit utiliser cet emplacement si le fournisseur n’est installé pour tous les utilisateurs sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ecfc2-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for all users on the computer.</span></span>
    
<span data-ttu-id="ecfc2-116">L’OSC recherche pour le fournisseur `ProgID` dans les emplacements ci-dessus, à moins que l’ordinateur client Outlook 32 bits sur un système d’exploitation de Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ecfc2-116">The OSC looks for the provider  `ProgID` in the above locations, unless the client computer has 32-bit Outlook running on a 64-bit Windows operating system.</span></span> <span data-ttu-id="ecfc2-117">Dans ce cas, votre programme d’installation du fournisseur doit cliquer sur un des emplacements suivants dans le `HKEY_CURRENT_USER` ou `HKEY_LOCAL_MACHINE` ruche :</span><span class="sxs-lookup"><span data-stu-id="ecfc2-117">In such a case, your provider installer should choose one of the following locations in the  `HKEY_CURRENT_USER` or  `HKEY_LOCAL_MACHINE` hive:</span></span> 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
<span data-ttu-id="ecfc2-118">Pour une version Click-to-Run d’Office, le programme d’installation de votre fournisseur doit cliquer sur un des emplacements suivants dans la ruche HKEY_CURRENT_USER ou HKEY_LOCAL_MACHINE :</span><span class="sxs-lookup"><span data-stu-id="ecfc2-118">For a Click-to-Run version of Office, your provider installer should choose one of the following locations in the HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE hive:</span></span>
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a><span data-ttu-id="ecfc2-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecfc2-119">See also</span></span>

- [<span data-ttu-id="ecfc2-120">Aide-mémoire d’installation</span><span class="sxs-lookup"><span data-stu-id="ecfc2-120">Installation Checklist</span></span>](installation-checklist.md)
- [<span data-ttu-id="ecfc2-121">Étapes rapides pour apprendre à développer un fournisseur</span><span class="sxs-lookup"><span data-stu-id="ecfc2-121">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="ecfc2-122">Déploiement d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="ecfc2-122">Deploying a Provider</span></span>](deploying-a-provider.md)

