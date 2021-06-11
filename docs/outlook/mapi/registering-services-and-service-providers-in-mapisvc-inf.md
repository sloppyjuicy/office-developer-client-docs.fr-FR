---
title: Inscription des services et des fournisseurs de services dans MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Last modified: July 18, 2013'
ms.openlocfilehash: adc6318ab36818b4c423bb6b1dc1b083b3fb54eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328370"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a><span data-ttu-id="8895f-103">Inscription des services et des fournisseurs de services dans MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="8895f-103">Registering Services and Service Providers in MapiSvc.inf</span></span>

 
  
<span data-ttu-id="8895f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8895f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8895f-105">L’installation d’un nouveau fournisseur sur un système nécessite la mise à jour du fichier MapiSvc.inf pour pointer vers le nouveau fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8895f-105">Installing a new provider on a system requires updating the MapiSvc.inf file to point to the new provider.</span></span> <span data-ttu-id="8895f-106">Les propriétés standard définies lors de la configuration, notamment les suivantes, indiquent à MAPI où trouver la bibliothèque de liens dynamiques (.dll) du fournisseur :</span><span class="sxs-lookup"><span data-stu-id="8895f-106">Standard properties set during configuration, which include the following, inform MAPI where to find the provider's dynamic-link library (.dll):</span></span>
  
- <span data-ttu-id="8895f-107">Le **PR_SERVICE_DLL_NAME** est spécifié dans la section **[Message Service].**</span><span class="sxs-lookup"><span data-stu-id="8895f-107">The **PR_SERVICE_DLL_NAME** is specified in the **[Message Service]** section.</span></span> 
    
- <span data-ttu-id="8895f-108">Le **PR_PROVIDER_DLL_NAME** est spécifié dans la section **[Fournisseur de services].**</span><span class="sxs-lookup"><span data-stu-id="8895f-108">The **PR_PROVIDER_DLL_NAME** is specified in the **[Service Provider]** section.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="8895f-109">L’objectif est que vous définissez le nom de l'.dll de votre fournisseur (sans le suffixe « 32 »).</span><span class="sxs-lookup"><span data-stu-id="8895f-109">The expectation is that you set the name of your provider's .dll (without the suffix "32").</span></span> <span data-ttu-id="8895f-110">MAPI charge ensuite votre fournisseur en le cherchant sur le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="8895f-110">MAPI then loads your provider by looking for it on the path.</span></span> 
  
## <a name="putting-a-path-in-mapisvcinf"></a><span data-ttu-id="8895f-111">Mise d’un chemin d’accès dans MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="8895f-111">Putting a Path in MapiSvc.inf</span></span>

<span data-ttu-id="8895f-112">La plupart des applications s’installent sous Program Files, nécessitant une mise à jour de la variable de chemin d’accès pour permettre aux fournisseurs MAPI de fonctionner.</span><span class="sxs-lookup"><span data-stu-id="8895f-112">Most applications install under Program Files, requiring an update to the path variable to allow MAPI providers to work.</span></span> <span data-ttu-id="8895f-113">Avec quelques restrictions, Microsoft Outlook 2010 et Outlook 2013 peuvent prendre en charge les chemins d’accès complets aux fournisseurs MAPI.</span><span class="sxs-lookup"><span data-stu-id="8895f-113">With a few restrictions Microsoft Outlook 2010 and Outlook 2013 can accommodate full paths to MAPI providers.</span></span>
  
<span data-ttu-id="8895f-114">Lors de l’inscription de votre fournisseur dans MapiSvc.inf, vous pouvez placer le chemin d’accès complet au fournisseur dans les propriétés MAPI PR_SERVICE_DLL_NAME **et** **PR_PROVIDER_DLL_NAME**.</span><span class="sxs-lookup"><span data-stu-id="8895f-114">When registering your provider in MapiSvc.inf, you could put the full path to the provider in the MAPI properties **PR_SERVICE_DLL_NAME** and **PR_PROVIDER_DLL_NAME**.</span></span>
  
<span data-ttu-id="8895f-115">Dans l’une ou l’autre des propriétés, le chemin d’accès complet doit être sans le suffixe « 32 », car MAPI continue à l’ajouter au nom de fichier avant de chercher votre fichier.</span><span class="sxs-lookup"><span data-stu-id="8895f-115">In either property, the full path must be without the suffix "32", because MAPI continues to append that to the filename before looking for your file.</span></span> <span data-ttu-id="8895f-116">Cela signifie que si vous inscrivez le chemin d’accès « c:\mypath\myprovider.dll », MAPI tentera de charger « c:\mypath\myprovider32.dll ».</span><span class="sxs-lookup"><span data-stu-id="8895f-116">This means that if you register the path "c:\mypath\myprovider.dll", MAPI will attempt to load "c:\mypath\myprovider32.dll".</span></span>
  
<span data-ttu-id="8895f-117">Étant donné que le MAPI de Outlook n’a pas été initialement conçu pour prendre en charge les chemins d’accès complets, il réalise cette insertion du suffixe « 32 » en cherchant la première période dans la chaîne, ce qui signifie que les chemins qui contiennent d’autres périodes ne peuvent pas fonctionner, vous ne pouvez donc pas utiliser des chemins d’accès tels que « c:\my.path\myprovider.dll » ou « c:\mypath\my.provider.dll ».</span><span class="sxs-lookup"><span data-stu-id="8895f-117">Because Outlook's MAPI was not originally designed to accommodate full paths, it accomplishes this insertion of the "32" suffix by looking for the first period in the string, which means that paths that contain other periods cannot work, so you cannot use paths such as "c:\my.path\myprovider.dll" or "c:\mypath\my.provider.dll".</span></span>
  
<span data-ttu-id="8895f-118">Parfois, dans un fournisseur de magasins, vous générez des identificateurs d’entrée à l’aide de la fonction **WrapStoreEntryID,** qui prend comme paramètre le nom de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8895f-118">Sometimes in a store provider you will generate entry identifiers using the **WrapStoreEntryID** function, which takes as a parameter the name of your provider.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="8895f-119">Si vous utilisez des chemins d’accès complets dans MapiSvc.inf, vous devez utiliser le même chemin d’accès dans tous les appels à **WrapStoreEntryID**.</span><span class="sxs-lookup"><span data-stu-id="8895f-119">If you are using full paths in MapiSvc.inf, you must use the same path in any calls to **WrapStoreEntryID**.</span></span> 
  
<span data-ttu-id="8895f-120">En outre, le chemin d’accès que vous utilisez peut être converti vers et à partir d’Unicode à l’aide de la page de code fournie par la [fonction GetACP.](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/)</span><span class="sxs-lookup"><span data-stu-id="8895f-120">Additionally, the path you use may be converted to and from Unicode using the code page provided by the [GetACP](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) function.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="8895f-121">Vous échouerez si vous choisissez un chemin d’accès qui contient des caractères qui ne peuvent pas résister à un tel aller-retour à travers les fonctions [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) et [WideCharToMultiByte.](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/)</span><span class="sxs-lookup"><span data-stu-id="8895f-121">You will experience failure if you choose a path that contains characters that cannot survive such a roundtrip through the [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) and [WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) functions.</span></span> 
  
<span data-ttu-id="8895f-122">Pour une démonstration de cette fonctionnalité, l’exemple [PST Wrapped](https://github.com/stephenegriffin/Outlook2010CodeSamples) sur GitHub a été révisé : la fonctionnalité pertinente est **dans MergeWithMapiSvc** et **GenerateProviderPath**.</span><span class="sxs-lookup"><span data-stu-id="8895f-122">For a demonstration of this functionality, the [Wrapped PST sample](https://github.com/stephenegriffin/Outlook2010CodeSamples) on GitHub has been revised - the pertinent functionality is in **MergeWithMapiSvc** and **GenerateProviderPath**.</span></span>
  

