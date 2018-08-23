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
ms.openlocfilehash: 4612b6f345d59d988013671758c6d0579aaa127d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569532"
---
# <a name="using-the-mapi-utilities"></a><span data-ttu-id="0fd22-103">Utilisation des utilitaires MAPI</span><span class="sxs-lookup"><span data-stu-id="0fd22-103">Using the MAPI Utilities</span></span>

  
  
<span data-ttu-id="0fd22-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fd22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fd22-105">Les utilitaires MAPI sont composés des données de la table et les objets de données de propriété et une variété de fonctions pour prendre en charge diverses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="0fd22-105">The MAPI utilities are made up of table data and property data objects and a variety of functions to support miscellaneous features.</span></span> <span data-ttu-id="0fd22-106">Il est possible d’un client ont besoin seulement ces utilitaires et n’ont pas à se connecter au sous-système MAPI pour établir une connexion avec des fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="0fd22-106">It is possible for a client to need only these utilities and not have to log on to the MAPI subsystem to establish a connection with service providers.</span></span> <span data-ttu-id="0fd22-107">Si votre client appartient à cette catégorie, appelez la fonction API [ScInitMapiUtil](scinitmapiutil.md) au lieu de la fonction [exécuter MAPIInitialize](mapiinitialize.md) lors de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="0fd22-107">If your client fits into this category, call the API function [ScInitMapiUtil](scinitmapiutil.md) rather than the [MAPIInitialize](mapiinitialize.md) function at initialization time.</span></span> 
  
 <span data-ttu-id="0fd22-108">**ScInitMapiUtil** permet aux clients d’utiliser des fonctions utilitaires qui requièrent allocateurs MAPI, mais qui ne demandent pas les allocateurs explicitement.</span><span class="sxs-lookup"><span data-stu-id="0fd22-108">**ScInitMapiUtil** enables clients to use utility functions that require MAPI allocators, but that do not ask for the allocators explicitly.</span></span> <span data-ttu-id="0fd22-109">Lorsqu’il est temps d’arrêter, appelez [DeinitMapiUtil](deinitmapiutil.md) pour libérer des ressources plutôt que [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="0fd22-109">When it is time to shut down, call [DeinitMapiUtil](deinitmapiutil.md) to free resources rather than [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="0fd22-110">Les clients qui appellent jamais **exécuter MAPIInitialize** ne doivent pas appeler **MAPIUninitialize**.</span><span class="sxs-lookup"><span data-stu-id="0fd22-110">Clients that never call **MAPIInitialize** should not call **MAPIUninitialize**.</span></span>
  
<span data-ttu-id="0fd22-111">Si vous avez appelé **ScInitMapiUtil** plutôt que **d’exécuter MAPIInitialize** et utilisez des tables via les méthodes **ITableData** plutôt que par les méthodes **IMAPITable** , sachez que les notifications de table ne fonctionnent pas.</span><span class="sxs-lookup"><span data-stu-id="0fd22-111">If you have called **ScInitMapiUtil** rather than **MAPIInitialize** and are using tables through the **ITableData** methods rather than through the **IMAPITable** methods, be aware that table notifications will not work.</span></span> <span data-ttu-id="0fd22-112">Les notifications requièrent l’utilisation des bibliothèques de MAPI et [IMAPITable : IUnknown](imapitableiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="0fd22-112">Notifications require the use of the MAPI libraries and [IMAPITable : IUnknown](imapitableiunknown.md).</span></span>
  

