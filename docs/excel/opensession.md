---
title: Méthode OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 782843f11643e203488b313181d224443a1d36c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782184"
---
# <a name="opensession"></a><span data-ttu-id="e04bd-103">Méthode OpenSession</span><span class="sxs-lookup"><span data-stu-id="e04bd-103">OpenSession</span></span>

<span data-ttu-id="e04bd-104">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e04bd-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e04bd-105">Crée une session dans laquelle les fonctions définies par l’utilisateur peuvent être exécutées.</span><span class="sxs-lookup"><span data-stu-id="e04bd-105">Creates a session in which user-defined functions can be executed.</span></span>
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a><span data-ttu-id="e04bd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e04bd-106">Parameters</span></span>

<span data-ttu-id="e04bd-107">_Paramètres_</span><span class="sxs-lookup"><span data-stu-id="e04bd-107">_Params_</span></span>
  
> <span data-ttu-id="e04bd-108">Pointeur vers une chaîne UNICODE délimitée par des paramètres pour la session.</span><span class="sxs-lookup"><span data-stu-id="e04bd-108">A pointer to semicolon-delimited UNICODE string of parameters for the session.</span></span> <span data-ttu-id="e04bd-109">Excel n’utilise pas cet argument.</span><span class="sxs-lookup"><span data-stu-id="e04bd-109">Excel does not use this argument.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e04bd-110">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="e04bd-110">Return value</span></span>

<span data-ttu-id="e04bd-111">Un ID de session à utiliser dans les autres appels vers le connecteur de cluster, si la session a été créée avec succès ; dans le cas contraire **xlHpcRetCallFailed**.</span><span class="sxs-lookup"><span data-stu-id="e04bd-111">A session ID to use in other calls to the cluster connector, if the session was successfully created; otherwise **xlHpcRetCallFailed**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e04bd-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e04bd-112">See also</span></span>

- [<span data-ttu-id="e04bd-113">Fonctions du connecteur de Cluster Excel</span><span class="sxs-lookup"><span data-stu-id="e04bd-113">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

