---
title: Initialisation des utilitaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5c5a9355e9edec28e08986ccd055fc43eec7b974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420947"
---
# <a name="initializing-the-mapi-utilities"></a><span data-ttu-id="106bf-103">Initialisation des utilitaires MAPI</span><span class="sxs-lookup"><span data-stu-id="106bf-103">Initializing the MAPI Utilities</span></span>

  
  
<span data-ttu-id="106bf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="106bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="106bf-105">Si la seule partie de MAPI que vous devez utiliser est les utilitaires, les interfaces et les fonctions déclarées dans la MAPIUTIL de MAPI. H, par exemple **IPropData** et **ITableData** , il n'est pas nécessaire d'appeler **MAPIInitialize** pour l'initialisation.</span><span class="sxs-lookup"><span data-stu-id="106bf-105">If the only part of MAPI that you need to use are the utilities — the interfaces and functions declared in MAPI's MAPIUTIL.H header file such as **IPropData** and **ITableData** — you do not need to call **MAPIInitialize** for initialization.</span></span> <span data-ttu-id="106bf-106">Pour plus d'informations, voir [IPropData: IMAPIProp](ipropdataimapiprop.md), [ITableData: IUnknown](itabledataiunknown.md)et [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="106bf-106">For more information, see [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md), and [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="106bf-107">À la place, appelez la fonction **ScInitMapiUtil** .</span><span class="sxs-lookup"><span data-stu-id="106bf-107">Instead, call the **ScInitMapiUtil** function.</span></span> <span data-ttu-id="106bf-108">Pour plus d'informations, consultez la rubrique [ScInitMapiUtil](scinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="106bf-108">For more information, see [ScInitMapiUtil](scinitmapiutil.md).</span></span> <span data-ttu-id="106bf-109">**ScInitMapiUtil** permet aux applications clientes d'utiliser des fonctions et des méthodes utilitaires qui nécessitent des allocateurs MAPI, mais qui ne les demandent pas explicitement.</span><span class="sxs-lookup"><span data-stu-id="106bf-109">**ScInitMapiUtil** enables client applications to use utility functions and methods that require MAPI allocators, but that do not ask for them explicitly.</span></span> 
  
<span data-ttu-id="106bf-110">Au moment de l'arrêt, effectuez un appel à **DeinitMapiUtil** pour libérer les ressources connectées aux utilitaires.</span><span class="sxs-lookup"><span data-stu-id="106bf-110">At shutdown time, make a call to **DeinitMapiUtil** to free resources connected to the utilities.</span></span> <span data-ttu-id="106bf-111">N'appelez pas **MAPIUninitialize**.</span><span class="sxs-lookup"><span data-stu-id="106bf-111">Do not call **MAPIUninitialize**.</span></span> <span data-ttu-id="106bf-112">Pour plus d'informations, voir [DeinitMapiUtil](deinitmapiutil.md) et [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="106bf-112">For more information, see [DeinitMapiUtil](deinitmapiutil.md) and [MAPIUninitialize](mapiuninitialize.md).</span></span>
  
<span data-ttu-id="106bf-113">N'oubliez pas que l'interface **ITableData** ne prend pas en charge les notifications de table pour les clients qui ont appelé **ScInitMapiUtil** et non **MAPIInitialize**.</span><span class="sxs-lookup"><span data-stu-id="106bf-113">Be aware that the **ITableData** interface does not support table notifications for clients that have called **ScInitMapiUtil** rather than **MAPIInitialize**.</span></span> 
  

