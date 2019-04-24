---
title: Liaison aux fichiers DLL MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19fd4678-21d3-47a6-a439-1d4959cac407
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 394537a60f4cb9603024115ccea67570291d8ac6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270041"
---
# <a name="linking-to-the-mapi-dlls"></a><span data-ttu-id="1640d-103">Liaison aux fichiers DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="1640d-103">Linking to the MAPI DLLs</span></span>

  
  
<span data-ttu-id="1640d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1640d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1640d-105">Les clients MAPI peuvent établir des liens vers les dll MAPI de manière implicite ou explicitement à l'aide des fonctions Windows **LoadLibrary** et **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="1640d-105">MAPI clients can link to the MAPI DLLs implicitly, or explicitly by using the Windows functions **LoadLibrary** and **GetProcAddress**.</span></span> <span data-ttu-id="1640d-106">Pour plus d'informations sur la liaison explicite des dll MAPI, voir [lien vers des fonctions MAPI](how-to-link-to-mapi-functions.md).</span><span class="sxs-lookup"><span data-stu-id="1640d-106">For information on explicitly linking MAPI DLLs, see [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
  
<span data-ttu-id="1640d-107">MAPI fournit des instructions de définition de type dans le MAPIX. H pour chacune des fonctions suivantes:</span><span class="sxs-lookup"><span data-stu-id="1640d-107">MAPI provides type definition statements in the MAPIX.H header file for each of the following functions:</span></span>
  
[<span data-ttu-id="1640d-108">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="1640d-108">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="1640d-109">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="1640d-109">MAPIUninitialize</span></span>](mapiuninitialize.md)
  
[<span data-ttu-id="1640d-110">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="1640d-110">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="1640d-111">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="1640d-111">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="1640d-112">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="1640d-112">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="1640d-113">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1640d-113">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1640d-114">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="1640d-114">MAPIAdminProfiles</span></span>](mapiadminprofiles.md)
  
<span data-ttu-id="1640d-115">Utilisez ces définitions de types pour appeler correctement les points d'entrée correspondants si vous liez explicitement les dll MAPI.</span><span class="sxs-lookup"><span data-stu-id="1640d-115">Use these type definitions to correctly call the corresponding entry points if you link explicitly to the MAPI DLLs.</span></span>
  
<span data-ttu-id="1640d-116">Les fournisseurs de services peuvent contenir des fonctionnalités non MAPI (fonctionnalités totalement non liées à MAPI) dans leur DLL.</span><span class="sxs-lookup"><span data-stu-id="1640d-116">Service providers can contain non-MAPI functionality — features that are completely unrelated to MAPI — in their DLL.</span></span> <span data-ttu-id="1640d-117">Si vous devez utiliser ces fonctionnalités, appelez **LoadLibrary** avant d'utiliser la dll et **FreeLibrary** pour supprimer la dll de la mémoire après son utilisation.</span><span class="sxs-lookup"><span data-stu-id="1640d-117">If you need to use these features, call **LoadLibrary** before using the DLL and **FreeLibrary** to remove the DLL from memory after its use.</span></span> <span data-ttu-id="1640d-118">Comme MAPI n'est pas conscient des utilisations non-MAPI d'un fournisseur de services DLL, il n'existe aucune garantie que la DLL sera disponible si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1640d-118">Because MAPI is unaware of non-MAPI uses of a service provider DLL, there is no guarantee that the DLL will be available when needed.</span></span> <span data-ttu-id="1640d-119">MAPI publie une DLL de fournisseur de services lorsqu'il n'y a plus de client avec des sessions actives qui nécessitent ses services.</span><span class="sxs-lookup"><span data-stu-id="1640d-119">MAPI releases a service provider DLL when there are no longer any clients with active sessions that require its services.</span></span> 
  

