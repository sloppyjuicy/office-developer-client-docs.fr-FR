---
title: Invalidation d’un objet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 9c0ba8f1f0bf31bb892f380df310cd9fa7a8a24f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784339"
---
# <a name="invalidating-an-object"></a><span data-ttu-id="fd431-103">Invalidation d’un objet</span><span class="sxs-lookup"><span data-stu-id="fd431-103">Invalidating an Object</span></span>

  
  
<span data-ttu-id="fd431-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fd431-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fd431-105">Dans le cadre du processus d’arrêt de votre fournisseur, vous voudrez peut-être invalider un objet.</span><span class="sxs-lookup"><span data-stu-id="fd431-105">As part of your provider's shutdown process, you might want to invalidate an object.</span></span> <span data-ttu-id="fd431-106">Invalidation d’un objet implique de remplacer son vtable avec un vtable qui contient des implémentations pour les trois méthodes **IUnknown** : **QueryInterface**, **AddRef**et **Release**.</span><span class="sxs-lookup"><span data-stu-id="fd431-106">Invalidating an object involves replacing its vtable with a vtable that contains implementations for the three **IUnknown** methods: **AddRef**, **Release**, and **QueryInterface**.</span></span> <span data-ttu-id="fd431-107">Invalider un objet en appelant [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), une méthode qui est incluse dans l’objet de prise en charge de chacun des trois types de fournisseurs courantes.</span><span class="sxs-lookup"><span data-stu-id="fd431-107">Invalidate an object by calling [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), a method that is included in the support object of each of the three common provider types.</span></span> <span data-ttu-id="fd431-108">Fournisseurs de rendre généralement cet appel dans l’implémentation de la méthode de **fermeture de session** de l’objet de leur ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="fd431-108">Providers typically make this call in the implementation of their logon object's **Logoff** method.</span></span> 
  
<span data-ttu-id="fd431-109">Invalidation d’un objet donne MAPI la responsabilité ultime pour libérer la mémoire associée à un objet.</span><span class="sxs-lookup"><span data-stu-id="fd431-109">Invalidating an object gives MAPI the ultimate responsibility for freeing the memory associated with an object.</span></span> <span data-ttu-id="fd431-110">Vous pouvez libérer toutes les ressources liées à un objet, puis appelez **MakeInvalid** pour invalider toutes les méthodes dans les interfaces héritées.</span><span class="sxs-lookup"><span data-stu-id="fd431-110">You can free all of the resources connected with an object and then call **MakeInvalid** to invalidate all of the methods in its inherited interfaces.</span></span> <span data-ttu-id="fd431-111">Les appels à une de ces méthodes renvoient MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="fd431-111">Calls to any of these methods will return MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="fd431-112">À l’aide de **MakeInvalid** est une option choisir de nombreux fournisseurs de services d’ignorer.</span><span class="sxs-lookup"><span data-stu-id="fd431-112">Using **MakeInvalid** is an option that many service providers choose to ignore.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fd431-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd431-113">See also</span></span>



[<span data-ttu-id="fd431-114">Arrêt d’un fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="fd431-114">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

