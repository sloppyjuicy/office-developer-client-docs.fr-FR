---
title: Fonctionnalité requise pour les fournisseurs de transport
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
# <a name="required-functionality-for-transport-providers"></a><span data-ttu-id="fbbb1-103">Fonctionnalité requise pour les fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="fbbb1-103">Required Functionality for Transport Providers</span></span>

  
  
<span data-ttu-id="fbbb1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fbbb1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fbbb1-105">Chaque fournisseur de transport MAPI doit:</span><span class="sxs-lookup"><span data-stu-id="fbbb1-105">Every MAPI transport provider must:</span></span>
  
- <span data-ttu-id="fbbb1-106">Suivez les instructions générales relatives à l'utilisation de MAPI et d'autres fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="fbbb1-106">Follow the general guidelines for working with MAPI and other service providers.</span></span> <span data-ttu-id="fbbb1-107">Pour plus d'informations, consultez la rubrique [MAPI Application Development](mapi-application-development.md) and [MAPI service](mapi-service-providers.md)Providers.</span><span class="sxs-lookup"><span data-stu-id="fbbb1-107">For more information, see [MAPI Application Development](mapi-application-development.md) and [MAPI Service Providers](mapi-service-providers.md).</span></span>
    
- <span data-ttu-id="fbbb1-108">Sa DLL de fournisseur de transport expose à MAPI sa fonction d'initialisation [XPProviderInit](xpproviderinit.md) .</span><span class="sxs-lookup"><span data-stu-id="fbbb1-108">Have its transport provider DLL expose to MAPI its [XPProviderInit](xpproviderinit.md) initialization function.</span></span> 
    
- <span data-ttu-id="fbbb1-109">Exposer à l'interface MAPI son implémentation des interfaces [IXPProvider: IUnknown](ixpprovideriunknown.md) et [IXPLogon: IUnknown](ixplogoniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="fbbb1-109">Expose to MAPI its implementation of the [IXPProvider : IUnknown](ixpprovideriunknown.md) and [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces.</span></span> 
    
- <span data-ttu-id="fbbb1-110">Exposer aux applications MAPI et client son implémentation de l'interface [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="fbbb1-110">Expose to MAPI and client applications its implementation of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="fbbb1-111">Pour plus d'informations sur l'implémentation de **IMAPIStatus**, voir [Status implémentation Object](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="fbbb1-111">For more information about implementing **IMAPIStatus**, see [Status Object Implementation](status-object-implementation.md).</span></span> 
    
- <span data-ttu-id="fbbb1-112">Implémentez une boîte de dialogue de feuille de propriétés pour la configuration.</span><span class="sxs-lookup"><span data-stu-id="fbbb1-112">Implement a property sheet dialog box for configuration.</span></span> <span data-ttu-id="fbbb1-113">Pour plus d'informations sur l'implémentation des feuilles de propriétés, voir implémentation de la [feuille de propriétés](property-sheet-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="fbbb1-113">For more information about implementing property sheets, see [Property Sheet Implementation](property-sheet-implementation.md).</span></span>
    

