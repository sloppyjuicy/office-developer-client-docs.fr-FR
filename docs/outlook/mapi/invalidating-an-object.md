---
title: Invalidation d'un objet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: bf7ef15ccfd9cd015771785bda9d6ad79415736b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317198"
---
# <a name="invalidating-an-object"></a><span data-ttu-id="993d4-103">Invalidation d'un objet</span><span class="sxs-lookup"><span data-stu-id="993d4-103">Invalidating an Object</span></span>

  
  
<span data-ttu-id="993d4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="993d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="993d4-105">Dans le cadre du processus d'arrêt de votre fournisseur, il se peut que vous souhaitiez invalider un objet.</span><span class="sxs-lookup"><span data-stu-id="993d4-105">As part of your provider's shutdown process, you might want to invalidate an object.</span></span> <span data-ttu-id="993d4-106">L'invalidation d'un objet implique le remplacement de sa vtable par un vtable qui contient des implémentations pour les trois méthodes **IUnknown** : **AddRef**, **Release**et **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="993d4-106">Invalidating an object involves replacing its vtable with a vtable that contains implementations for the three **IUnknown** methods: **AddRef**, **Release**, and **QueryInterface**.</span></span> <span data-ttu-id="993d4-107">Invalidez un objet en appelant [IMAPISupport:: MakeInvalid](imapisupport-makeinvalid.md), une méthode incluse dans l'objet de prise en charge de chacun des trois types de fournisseurs courants.</span><span class="sxs-lookup"><span data-stu-id="993d4-107">Invalidate an object by calling [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), a method that is included in the support object of each of the three common provider types.</span></span> <span data-ttu-id="993d4-108">Les fournisseurs effectuent généralement cet appel dans l'implémentation de la méthode de **fermeture** de session de leur objet d'ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="993d4-108">Providers typically make this call in the implementation of their logon object's **Logoff** method.</span></span> 
  
<span data-ttu-id="993d4-109">L'invalidation d'un objet confère à MAPI la responsabilité ultime de la libération de la mémoire associée à un objet.</span><span class="sxs-lookup"><span data-stu-id="993d4-109">Invalidating an object gives MAPI the ultimate responsibility for freeing the memory associated with an object.</span></span> <span data-ttu-id="993d4-110">Vous pouvez libérer toutes les ressources connectées à un objet, puis appeler **MakeInvalid** pour invalider toutes les méthodes dans ses interfaces héritées.</span><span class="sxs-lookup"><span data-stu-id="993d4-110">You can free all of the resources connected with an object and then call **MakeInvalid** to invalidate all of the methods in its inherited interfaces.</span></span> <span data-ttu-id="993d4-111">Les appels à l'une de ces méthodes renvoient MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="993d4-111">Calls to any of these methods will return MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="993d4-112">L'utilisation de **MakeInvalid** est une option que de nombreux fournisseurs de services choisissent d'ignorer.</span><span class="sxs-lookup"><span data-stu-id="993d4-112">Using **MakeInvalid** is an option that many service providers choose to ignore.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="993d4-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="993d4-113">See also</span></span>



[<span data-ttu-id="993d4-114">Arrêt d'un fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="993d4-114">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

