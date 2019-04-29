---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e4df0c5772f28ab4ab8d84eaddfe4409a88061b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421836"
---
# <a name="opensession"></a><span data-ttu-id="7231f-103">OpenSession</span><span class="sxs-lookup"><span data-stu-id="7231f-103">OpenSession</span></span>

<span data-ttu-id="7231f-104">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7231f-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7231f-105">Crée une session dans laquelle des fonctions définies par l'utilisateur peuvent être exécutées.</span><span class="sxs-lookup"><span data-stu-id="7231f-105">Creates a session in which user-defined functions can be executed.</span></span>
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a><span data-ttu-id="7231f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7231f-106">Parameters</span></span>

<span data-ttu-id="7231f-107">_Paramètres_</span><span class="sxs-lookup"><span data-stu-id="7231f-107">_Params_</span></span>
  
> <span data-ttu-id="7231f-108">Pointeur vers une chaîne UNICODE délimitée par des points-virgules de paramètres pour la session.</span><span class="sxs-lookup"><span data-stu-id="7231f-108">A pointer to semicolon-delimited UNICODE string of parameters for the session.</span></span> <span data-ttu-id="7231f-109">Excel n'utilise pas cet argument.</span><span class="sxs-lookup"><span data-stu-id="7231f-109">Excel does not use this argument.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7231f-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7231f-110">Return value</span></span>

<span data-ttu-id="7231f-111">Un ID de session à utiliser dans d'autres appels vers le connecteur de cluster, si la session a été correctement créée; sinon **xlHpcRetCallFailed**.</span><span class="sxs-lookup"><span data-stu-id="7231f-111">A session ID to use in other calls to the cluster connector, if the session was successfully created; otherwise **xlHpcRetCallFailed**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7231f-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7231f-112">See also</span></span>

- [<span data-ttu-id="7231f-113">Fonctions du connecteur de cluster Excel</span><span class="sxs-lookup"><span data-stu-id="7231f-113">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

