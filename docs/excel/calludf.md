---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 1d55f22de88b274d0403f81717d0fddefbea0219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782007"
---
# <a name="calludf"></a><span data-ttu-id="d7bd7-103">CallUDF</span><span class="sxs-lookup"><span data-stu-id="d7bd7-103">CallUDF</span></span>

<span data-ttu-id="d7bd7-104">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d7bd7-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d7bd7-105">Appelle une fonction définie par l’utilisateur dans un environnement informatique hautes performances.</span><span class="sxs-lookup"><span data-stu-id="d7bd7-105">Calls a user-defined function in a high-performance computing environment.</span></span>
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a><span data-ttu-id="d7bd7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7bd7-106">Parameters</span></span>

<span data-ttu-id="d7bd7-107">_ID de session_</span><span class="sxs-lookup"><span data-stu-id="d7bd7-107">_SessionId_</span></span>
  
> <span data-ttu-id="d7bd7-108">ID de la session dans laquelle effectuer l’appel.</span><span class="sxs-lookup"><span data-stu-id="d7bd7-108">The ID of the session in which to make the call.</span></span>
    
<span data-ttu-id="d7bd7-109">_XLLName_</span><span class="sxs-lookup"><span data-stu-id="d7bd7-109">_XLLName_</span></span>
  
> <span data-ttu-id="d7bd7-110">Le nom de la ressource XLL contenant la fonction définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d7bd7-110">The name of the XLL that contains the user-defined function.</span></span>
    
<span data-ttu-id="d7bd7-111">_UDFName_</span><span class="sxs-lookup"><span data-stu-id="d7bd7-111">_UDFName_</span></span>
  
> <span data-ttu-id="d7bd7-112">Nom de la fonction définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d7bd7-112">The name of the user-defined function.</span></span>
    
<span data-ttu-id="d7bd7-113">_CallBackAddr_</span><span class="sxs-lookup"><span data-stu-id="d7bd7-113">_CallBackAddr_</span></span>
  
> <span data-ttu-id="d7bd7-114">La fonction que le connecteur doit appeler lorsque la fonction définie par l’utilisateur est terminée.</span><span class="sxs-lookup"><span data-stu-id="d7bd7-114">The function that the connector should call when the user-defined function is finished.</span></span>
    
<span data-ttu-id="d7bd7-115">_pxAsyncHandle_</span><span class="sxs-lookup"><span data-stu-id="d7bd7-115">_pxAsyncHandle_</span></span>
  
> <span data-ttu-id="d7bd7-116">La poignée asynchrone utilisée par Excel et le connecteur pour effectuer le suivi de l’appel en attente de fonction définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d7bd7-116">The asynchronous handle used by Excel and the connector to track the pending user-defined function call.</span></span> <span data-ttu-id="d7bd7-117">Le connecteur utilise plus tard lors de l’appel est terminé, lorsqu’il rappelle dans Excel à l’aide du pointeur de fonction passés dans l’argument _CallBackAddr_ .</span><span class="sxs-lookup"><span data-stu-id="d7bd7-117">The connector uses it later when the call is finished, when it calls back into Excel using the function pointer passed in the  _CallBackAddr_ argument.</span></span> 
    
<span data-ttu-id="d7bd7-118">_ArgCount_</span><span class="sxs-lookup"><span data-stu-id="d7bd7-118">_ArgCount_</span></span>
  
> <span data-ttu-id="d7bd7-119">Le nombre d’arguments à transmettre à la fonction définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d7bd7-119">The number of arguments to pass to the user-defined function.</span></span> <span data-ttu-id="d7bd7-120">La valeur maximale autorisée est de 255.</span><span class="sxs-lookup"><span data-stu-id="d7bd7-120">The maximum value allowed is 255.</span></span>
    
<span data-ttu-id="d7bd7-121">_Parameter1_</span><span class="sxs-lookup"><span data-stu-id="d7bd7-121">_Parameter1_</span></span>
  
> <span data-ttu-id="d7bd7-122">Une valeur à passer à la fonction définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d7bd7-122">A value to pass to the user-defined function.</span></span> <span data-ttu-id="d7bd7-123">Répétez cet argument pour chaque paramètre indiqué par _ArgCount_.</span><span class="sxs-lookup"><span data-stu-id="d7bd7-123">Repeat this argument for each parameter indicated by  _ArgCount_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d7bd7-124">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="d7bd7-124">Return value</span></span>

<span data-ttu-id="d7bd7-125">**xlHpcRetSuccess** si l’appel des UDF est démarré ; **xlHpcRetInvalidSessionId** si l’argument _SessionId_ n’est pas valide ; **xlHpcRetCallFailed** sur les autres erreurs, y compris le délai d’expiration. Si l’appel retourne un code d’erreur (n’est pas **xlHpcRetSuccess**), puis Excel considère que l’appel des UDF a échoué, invalide le _pxAsyncHandle_et n’attend pas un rappel se produise.</span><span class="sxs-lookup"><span data-stu-id="d7bd7-125">**xlHpcRetSuccess** if the UDF call is successfully initiated; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures, including time-out. If the call returns any error code (anything except **xlHpcRetSuccess**), then Excel considers the UDF call to have failed, invalidates the  _pxAsyncHandle_, and does not expect a callback to occur.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d7bd7-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="d7bd7-126">Remarks</span></span>

<span data-ttu-id="d7bd7-127">Cette fonction s’exécute en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="d7bd7-127">This function executes asynchronously.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d7bd7-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7bd7-128">See also</span></span>

- [<span data-ttu-id="d7bd7-129">Fonctions du connecteur de Cluster Excel</span><span class="sxs-lookup"><span data-stu-id="d7bd7-129">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

