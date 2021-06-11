---
title: Utilisation des utilitaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d8ec18ee7b80d8603266cf827f9484ee85bdb03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409985"
---
# <a name="using-the-mapi-utilities"></a><span data-ttu-id="790a9-103">Utilisation des utilitaires MAPI</span><span class="sxs-lookup"><span data-stu-id="790a9-103">Using the MAPI Utilities</span></span>

  
  
<span data-ttu-id="790a9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="790a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="790a9-105">Les utilitaires MAPI sont composés d’objets de données de table et de données de propriétés, ainsi que de diverses fonctions pour prendre en charge diverses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="790a9-105">The MAPI utilities are made up of table data and property data objects and a variety of functions to support miscellaneous features.</span></span> <span data-ttu-id="790a9-106">Il est possible pour un client de n’avoir besoin que de ces utilitaires et de ne pas avoir à se connecter au sous-système MAPI pour établir une connexion avec les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="790a9-106">It is possible for a client to need only these utilities and not have to log on to the MAPI subsystem to establish a connection with service providers.</span></span> <span data-ttu-id="790a9-107">Si votre client s’inscrit dans cette catégorie, appelez la fonction API [ScInitMapiUtil](scinitmapiutil.md) plutôt que [la fonction MAPIInitialize](mapiinitialize.md) au moment de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="790a9-107">If your client fits into this category, call the API function [ScInitMapiUtil](scinitmapiutil.md) rather than the [MAPIInitialize](mapiinitialize.md) function at initialization time.</span></span> 
  
 <span data-ttu-id="790a9-108">**ScInitMapiUtil** permet aux clients d’utiliser des fonctions utilitaires qui nécessitent des allocateurs MAPI, mais qui ne demandent pas explicitement les allocateurs.</span><span class="sxs-lookup"><span data-stu-id="790a9-108">**ScInitMapiUtil** enables clients to use utility functions that require MAPI allocators, but that do not ask for the allocators explicitly.</span></span> <span data-ttu-id="790a9-109">Au moment de l’arrêt, appelez [DeinitMapiUtil](deinitmapiutil.md) pour libérer des ressources plutôt que [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="790a9-109">When it is time to shut down, call [DeinitMapiUtil](deinitmapiutil.md) to free resources rather than [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="790a9-110">Les clients qui n’appellent **jamais MAPIInitialize** ne doivent pas appeler **MAPIUninitialize**.</span><span class="sxs-lookup"><span data-stu-id="790a9-110">Clients that never call **MAPIInitialize** should not call **MAPIUninitialize**.</span></span>
  
<span data-ttu-id="790a9-111">Si vous avez appelé **ScInitMapiUtil** plutôt que **MAPIInitialize** et que vous utilisez des tableaux par le biais des méthodes **ITableData** plutôt que par le biais des méthodes **IMAPITable,** sachez que les notifications de tableau ne fonctionneront pas.</span><span class="sxs-lookup"><span data-stu-id="790a9-111">If you have called **ScInitMapiUtil** rather than **MAPIInitialize** and are using tables through the **ITableData** methods rather than through the **IMAPITable** methods, be aware that table notifications will not work.</span></span> <span data-ttu-id="790a9-112">Les notifications nécessitent l’utilisation des bibliothèques MAPI et [de IMAPITable : IUnknown](imapitableiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="790a9-112">Notifications require the use of the MAPI libraries and [IMAPITable : IUnknown](imapitableiunknown.md).</span></span>
  

