---
title: Fonctionnalités requises pour les fournisseurs de Transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: eb5d70c31f28df16593fb020f13124ea217476ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787019"
---
# <a name="required-functionality-for-transport-providers"></a><span data-ttu-id="e6ca6-103">Fonctionnalités requises pour les fournisseurs de Transport</span><span class="sxs-lookup"><span data-stu-id="e6ca6-103">Required Functionality for Transport Providers</span></span>

  
  
<span data-ttu-id="e6ca6-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e6ca6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e6ca6-105">Chaque fournisseur de transport MAPI doit :</span><span class="sxs-lookup"><span data-stu-id="e6ca6-105">Every MAPI transport provider must:</span></span>
  
- <span data-ttu-id="e6ca6-106">Suivez les instructions générales pour l’utilisation de MAPI et d’autres fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="e6ca6-106">Follow the general guidelines for working with MAPI and other service providers.</span></span> <span data-ttu-id="e6ca6-107">Pour plus d’informations, voir [Développement d’applications MAPI](mapi-application-development.md) et les [Fournisseurs de services MAPI](mapi-service-providers.md).</span><span class="sxs-lookup"><span data-stu-id="e6ca6-107">For more information, see [MAPI Application Development](mapi-application-development.md) and [MAPI Service Providers](mapi-service-providers.md).</span></span>
    
- <span data-ttu-id="e6ca6-108">Avoir son fournisseur de transport exposent DLL MAPI sa fonction d’initialisation de [XPProviderInit](xpproviderinit.md) .</span><span class="sxs-lookup"><span data-stu-id="e6ca6-108">Have its transport provider DLL expose to MAPI its [XPProviderInit](xpproviderinit.md) initialization function.</span></span> 
    
- <span data-ttu-id="e6ca6-109">Exposer à MAPI son implémentation de la [IXPProvider : IUnknown](ixpprovideriunknown.md) et [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces.</span><span class="sxs-lookup"><span data-stu-id="e6ca6-109">Expose to MAPI its implementation of the [IXPProvider : IUnknown](ixpprovideriunknown.md) and [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces.</span></span> 
    
- <span data-ttu-id="e6ca6-110">Exposer aux applications MAPI et client son implémentation de la [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span><span class="sxs-lookup"><span data-stu-id="e6ca6-110">Expose to MAPI and client applications its implementation of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="e6ca6-111">Pour plus d’informations sur l’implémentation de **IMAPIStatus**, voir [Implémentation d’objet état](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="e6ca6-111">For more information about implementing **IMAPIStatus**, see [Status Object Implementation](status-object-implementation.md).</span></span> 
    
- <span data-ttu-id="e6ca6-112">Implémenter une boîte de dialogue de feuille de propriété de configuration.</span><span class="sxs-lookup"><span data-stu-id="e6ca6-112">Implement a property sheet dialog box for configuration.</span></span> <span data-ttu-id="e6ca6-113">Pour plus d’informations sur l’implémentation de feuilles de propriétés, voir [Implémentation de feuille de propriétés](property-sheet-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="e6ca6-113">For more information about implementing property sheets, see [Property Sheet Implementation](property-sheet-implementation.md).</span></span>
    

