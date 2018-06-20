---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 165be9eada54b2030471fc10e7a0bf0c7dcc7c8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782197"
---
# <a name="pingsession"></a><span data-ttu-id="1d6c2-103">PingSession</span><span class="sxs-lookup"><span data-stu-id="1d6c2-103">PingSession</span></span>

<span data-ttu-id="1d6c2-104">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1d6c2-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1d6c2-105">Vérifie si une session est valide.</span><span class="sxs-lookup"><span data-stu-id="1d6c2-105">Checks whether a session is valid.</span></span> <span data-ttu-id="1d6c2-106">Cette fonction est généralement appelée lorsque Excel doit déterminer si un ID de session précédemment retourné est toujours actif et peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="1d6c2-106">This function is typically called when Excel needs to determine if a previously returned session ID is still active and can be used.</span></span>
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="1d6c2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d6c2-107">Parameters</span></span>

<span data-ttu-id="1d6c2-108">_ID de session_</span><span class="sxs-lookup"><span data-stu-id="1d6c2-108">_SessionID_</span></span>
  
> <span data-ttu-id="1d6c2-109">ID de la session Ping.</span><span class="sxs-lookup"><span data-stu-id="1d6c2-109">The ID of the session to ping.</span></span> <span data-ttu-id="1d6c2-110">Cette valeur doit correspondre à un ID renvoyé par un appel précédent à la [méthode OpenSession](opensession.md).</span><span class="sxs-lookup"><span data-stu-id="1d6c2-110">This value must match an ID returned by a previous call to [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1d6c2-111">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="1d6c2-111">Return value</span></span>

<span data-ttu-id="1d6c2-112">**xlHpcRetSuccess** si l’argument _SessionId_ est valide ; dans le cas contraire **xlHpcRetInvalidSessionId**.</span><span class="sxs-lookup"><span data-stu-id="1d6c2-112">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; otherwise **xlHpcRetInvalidSessionId**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1d6c2-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d6c2-113">See also</span></span>

- [<span data-ttu-id="1d6c2-114">Méthode OpenSession</span><span class="sxs-lookup"><span data-stu-id="1d6c2-114">OpenSession</span></span>](opensession.md)
- [<span data-ttu-id="1d6c2-115">Fonctions du connecteur de Cluster Excel</span><span class="sxs-lookup"><span data-stu-id="1d6c2-115">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

