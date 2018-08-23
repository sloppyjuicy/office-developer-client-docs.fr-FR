---
title: Liaison aux fichiers DLL MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19fd4678-21d3-47a6-a439-1d4959cac407
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 428e92dd783368374fa07c8df9629d60e83dd217
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582027"
---
# <a name="linking-to-the-mapi-dlls"></a><span data-ttu-id="ef79d-103">Liaison aux fichiers DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="ef79d-103">Linking to the MAPI DLLs</span></span>

  
  
<span data-ttu-id="ef79d-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef79d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef79d-105">Clients MAPI peuvent lier aux DLL MAPI implicite ou explicite en utilisant les fonctions Windows **LoadLibrary** et **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="ef79d-105">MAPI clients can link to the MAPI DLLs implicitly, or explicitly by using the Windows functions **LoadLibrary** and **GetProcAddress**.</span></span> <span data-ttu-id="ef79d-106">Pour plus d’informations sur la liaison explicitement DLL MAPI, voir [lien vers des fonctions MAPI](how-to-link-to-mapi-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ef79d-106">For information on explicitly linking MAPI DLLs, see [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
  
<span data-ttu-id="ef79d-107">MAPI fournit des instructions de définition de type dans le MAPIX. Fichier d’en-tête H pour chacune des fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="ef79d-107">MAPI provides type definition statements in the MAPIX.H header file for each of the following functions:</span></span>
  
[<span data-ttu-id="ef79d-108">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="ef79d-108">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="ef79d-109">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="ef79d-109">MAPIUninitialize</span></span>](mapiuninitialize.md)
  
[<span data-ttu-id="ef79d-110">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="ef79d-110">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="ef79d-111">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="ef79d-111">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="ef79d-112">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="ef79d-112">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="ef79d-113">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ef79d-113">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ef79d-114">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="ef79d-114">MAPIAdminProfiles</span></span>](mapiadminprofiles.md)
  
<span data-ttu-id="ef79d-115">Utilisez ces définitions de type à appeler correctement les points d’entrée correspondante si la liaison explicitement les DLL MAPI.</span><span class="sxs-lookup"><span data-stu-id="ef79d-115">Use these type definitions to correctly call the corresponding entry points if you link explicitly to the MAPI DLLs.</span></span>
  
<span data-ttu-id="ef79d-116">Fournisseurs de services peuvent contenir des fonctionnalités non MAPI — fonctionnalités qui ne sont pas complètement liées à MAPI — dans leur DLL.</span><span class="sxs-lookup"><span data-stu-id="ef79d-116">Service providers can contain non-MAPI functionality — features that are completely unrelated to MAPI — in their DLL.</span></span> <span data-ttu-id="ef79d-117">Si vous avez besoin d’utiliser ces fonctionnalités, appeler **LoadLibrary** avant d’utiliser la DLL et **FreeLibrary** pour supprimer la DLL de la mémoire après son utilisation.</span><span class="sxs-lookup"><span data-stu-id="ef79d-117">If you need to use these features, call **LoadLibrary** before using the DLL and **FreeLibrary** to remove the DLL from memory after its use.</span></span> <span data-ttu-id="ef79d-118">MAPI n’a pas connaissance d’utilisations non MAPI d’un fournisseur de service DLL, il n’aucune garantie que la DLL sera disponible lorsqu’elle est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ef79d-118">Because MAPI is unaware of non-MAPI uses of a service provider DLL, there is no guarantee that the DLL will be available when needed.</span></span> <span data-ttu-id="ef79d-119">MAPI libère un fournisseur de services DLL quand il y a plus aucun tous les clients avec des sessions actives nécessitant ses services.</span><span class="sxs-lookup"><span data-stu-id="ef79d-119">MAPI releases a service provider DLL when there are no longer any clients with active sessions that require its services.</span></span> 
  

