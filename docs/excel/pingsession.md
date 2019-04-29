---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0fa5fe57e537a7b8c7d880b934809a6f68ce27a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408361"
---
# <a name="pingsession"></a><span data-ttu-id="a10b5-103">PingSession</span><span class="sxs-lookup"><span data-stu-id="a10b5-103">PingSession</span></span>

<span data-ttu-id="a10b5-104">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a10b5-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a10b5-105">Vérifie si une session est valide.</span><span class="sxs-lookup"><span data-stu-id="a10b5-105">Checks whether a session is valid.</span></span> <span data-ttu-id="a10b5-106">Cette fonction est généralement appelée lorsque Excel doit déterminer si un ID de session précédemment renvoyé est toujours actif et peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="a10b5-106">This function is typically called when Excel needs to determine if a previously returned session ID is still active and can be used.</span></span>
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="a10b5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a10b5-107">Parameters</span></span>

<span data-ttu-id="a10b5-108">_SessionID_</span><span class="sxs-lookup"><span data-stu-id="a10b5-108">_SessionID_</span></span>
  
> <span data-ttu-id="a10b5-109">ID de la session à tester.</span><span class="sxs-lookup"><span data-stu-id="a10b5-109">The ID of the session to ping.</span></span> <span data-ttu-id="a10b5-110">Cette valeur doit correspondre à un ID renvoyé par un appel précédent à [OpenSession](opensession.md).</span><span class="sxs-lookup"><span data-stu-id="a10b5-110">This value must match an ID returned by a previous call to [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a10b5-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a10b5-111">Return value</span></span>

<span data-ttu-id="a10b5-112">**xlHpcRetSuccess** si l'argument _SessionID_ est valide; sinon **xlHpcRetInvalidSessionId**.</span><span class="sxs-lookup"><span data-stu-id="a10b5-112">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; otherwise **xlHpcRetInvalidSessionId**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a10b5-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a10b5-113">See also</span></span>

- [<span data-ttu-id="a10b5-114">OpenSession</span><span class="sxs-lookup"><span data-stu-id="a10b5-114">OpenSession</span></span>](opensession.md)
- [<span data-ttu-id="a10b5-115">Fonctions du connecteur de cluster Excel</span><span class="sxs-lookup"><span data-stu-id="a10b5-115">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

