---
title: Test et débogage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0afceb1f-9086-4cc9-8ce4-fb9256a81a9c
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 96bc2e58482ba259b14e820f3380978f80c542c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787336"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="e4e99-103">Test et débogage</span><span class="sxs-lookup"><span data-stu-id="e4e99-103">Testing and Debugging</span></span>

  
  
<span data-ttu-id="e4e99-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e4e99-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e4e99-105">Tests des stratégies varient selon que vous développez un client ou fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="e4e99-105">Testing strategies differ depending on whether you are developing a client or service provider.</span></span> <span data-ttu-id="e4e99-106">Comme une application cliente requiert un ou plusieurs fournisseurs de services fonctionner, les clients doivent être testés dans un environnement comportant plusieurs ensembles de fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="e4e99-106">Because a client application requires one or more service providers to operate, clients should be tested in an environment with different sets of service providers.</span></span>
  
<span data-ttu-id="e4e99-107">Toutefois, les fournisseurs de services, doivent être testées de manière isolée avant l’intégration avec d’autres fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="e4e99-107">Service providers, however, should be tested in isolation before being integrated with other providers.</span></span> <span data-ttu-id="e4e99-108">MAPI fournit des outils qui sont destinées à tester les fonctionnalités d’un fournisseur de service d’un type particulier.</span><span class="sxs-lookup"><span data-stu-id="e4e99-108">MAPI provides tools that are meant to test the features of a service provider of a particular type.</span></span> <span data-ttu-id="e4e99-109">L’exemple d’application [MFCMAPI](http://go.microsoft.com/fwlink/?LinkId=124154) montre comment tester les fonctionnalités d’un fournisseur de carnet d’adresses et le fournisseur de magasin fonctionne avec un message.</span><span class="sxs-lookup"><span data-stu-id="e4e99-109">The [MFCMAPI](http://go.microsoft.com/fwlink/?LinkId=124154) sample application shows how to test the features of an address book provider and works with a message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e4e99-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4e99-110">See also</span></span>



[<span data-ttu-id="e4e99-111">Vue d'ensemble de la programmation MAPI</span><span class="sxs-lookup"><span data-stu-id="e4e99-111">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
  
[<span data-ttu-id="e4e99-112">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="e4e99-112">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

