---
title: Fonctionnalités requises pour les fournisseurs de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7f9768d47cf740bdf50b439ee3af4b0d2a191602
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404441"
---
# <a name="required-functionality-for-transport-providers"></a><span data-ttu-id="cb755-103">Fonctionnalités requises pour les fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="cb755-103">Required Functionality for Transport Providers</span></span>

  
  
<span data-ttu-id="cb755-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb755-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb755-105">Chaque fournisseur de transport MAPI doit :</span><span class="sxs-lookup"><span data-stu-id="cb755-105">Every MAPI transport provider must:</span></span>
  
- <span data-ttu-id="cb755-106">Suivez les instructions générales pour travailler avec MAPI et d’autres fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="cb755-106">Follow the general guidelines for working with MAPI and other service providers.</span></span> <span data-ttu-id="cb755-107">Pour plus d’informations, voir [Développement d’applications MAPI](mapi-application-development.md) et Fournisseurs de [services MAPI.](mapi-service-providers.md)</span><span class="sxs-lookup"><span data-stu-id="cb755-107">For more information, see [MAPI Application Development](mapi-application-development.md) and [MAPI Service Providers](mapi-service-providers.md).</span></span>
    
- <span data-ttu-id="cb755-108">Exposer la DLL de son fournisseur de transport à MAPI avec sa fonction d’initialisation [XPProviderInit.](xpproviderinit.md)</span><span class="sxs-lookup"><span data-stu-id="cb755-108">Have its transport provider DLL expose to MAPI its [XPProviderInit](xpproviderinit.md) initialization function.</span></span> 
    
- <span data-ttu-id="cb755-109">Exposez à MAPI son implémentation des interfaces [IXPProvider : IUnknown](ixpprovideriunknown.md) et [IXPLogon : IUnknown.](ixplogoniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="cb755-109">Expose to MAPI its implementation of the [IXPProvider : IUnknown](ixpprovideriunknown.md) and [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces.</span></span> 
    
- <span data-ttu-id="cb755-110">Exposer à MAPI et aux applications clientes son implémentation de l’interface [IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="cb755-110">Expose to MAPI and client applications its implementation of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="cb755-111">Pour plus d’informations sur l’implémentation **d’IMAPIStatus,** voir [Status Object Implementation](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="cb755-111">For more information about implementing **IMAPIStatus**, see [Status Object Implementation](status-object-implementation.md).</span></span> 
    
- <span data-ttu-id="cb755-112">Implémenter une boîte de dialogue feuille de propriétés pour la configuration.</span><span class="sxs-lookup"><span data-stu-id="cb755-112">Implement a property sheet dialog box for configuration.</span></span> <span data-ttu-id="cb755-113">Pour plus d’informations sur l’implémentation des feuilles de propriétés, voir [Implémentation de la feuille de propriétés.](property-sheet-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="cb755-113">For more information about implementing property sheets, see [Property Sheet Implementation](property-sheet-implementation.md).</span></span>
    

