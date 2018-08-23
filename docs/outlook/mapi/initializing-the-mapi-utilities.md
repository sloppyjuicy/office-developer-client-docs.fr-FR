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
ms.openlocfilehash: d0507a26b9ae5ae018111e2771e3af8b25761786
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567670"
---
# <a name="initializing-the-mapi-utilities"></a><span data-ttu-id="a1193-103">Initialisation des utilitaires MAPI</span><span class="sxs-lookup"><span data-stu-id="a1193-103">Initializing the MAPI Utilities</span></span>

  
  
<span data-ttu-id="a1193-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1193-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1193-105">Si la seule partie de MAPI que vous devrez utiliser sont les utilitaires, les interfaces et les fonctions déclarées dans MAPIUTIL de MAPI. Fichier d’en-tête H telles que **IPropData** et **ITableData** — vous n’avez pas besoin d’appeler **exécuter MAPIInitialize** pour l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="a1193-105">If the only part of MAPI that you need to use are the utilities — the interfaces and functions declared in MAPI's MAPIUTIL.H header file such as **IPropData** and **ITableData** — you do not need to call **MAPIInitialize** for initialization.</span></span> <span data-ttu-id="a1193-106">Pour plus d’informations, voir [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md)et [exécuter MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="a1193-106">For more information, see [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md), and [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="a1193-107">Au lieu de cela, appelez la fonction **ScInitMapiUtil** .</span><span class="sxs-lookup"><span data-stu-id="a1193-107">Instead, call the **ScInitMapiUtil** function.</span></span> <span data-ttu-id="a1193-108">Pour plus d’informations, voir [ScInitMapiUtil](scinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="a1193-108">For more information, see [ScInitMapiUtil](scinitmapiutil.md).</span></span> <span data-ttu-id="a1193-109">**ScInitMapiUtil** permet aux applications de client à utiliser les fonctions utilitaires et des méthodes qui requièrent des allocateurs MAPI, mais qui ne demandent pas les explicitement.</span><span class="sxs-lookup"><span data-stu-id="a1193-109">**ScInitMapiUtil** enables client applications to use utility functions and methods that require MAPI allocators, but that do not ask for them explicitly.</span></span> 
  
<span data-ttu-id="a1193-110">Au moment de l’arrêt, passer un appel à **DeinitMapiUtil** pour libérer des ressources liées aux utilitaires.</span><span class="sxs-lookup"><span data-stu-id="a1193-110">At shutdown time, make a call to **DeinitMapiUtil** to free resources connected to the utilities.</span></span> <span data-ttu-id="a1193-111">N’appelez pas **MAPIUninitialize**.</span><span class="sxs-lookup"><span data-stu-id="a1193-111">Do not call **MAPIUninitialize**.</span></span> <span data-ttu-id="a1193-112">Pour plus d’informations, voir [DeinitMapiUtil](deinitmapiutil.md) et [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="a1193-112">For more information, see [DeinitMapiUtil](deinitmapiutil.md) and [MAPIUninitialize](mapiuninitialize.md).</span></span>
  
<span data-ttu-id="a1193-113">Sachez que l’interface **ITableData** ne gère pas les notifications de table pour les clients qui ont appelé **ScInitMapiUtil** plutôt que **d’exécuter MAPIInitialize**.</span><span class="sxs-lookup"><span data-stu-id="a1193-113">Be aware that the **ITableData** interface does not support table notifications for clients that have called **ScInitMapiUtil** rather than **MAPIInitialize**.</span></span> 
  

