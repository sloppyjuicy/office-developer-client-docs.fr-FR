---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 096f57335572c3788fdf129dd3bcf4a76cf62b01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433009"
---
# <a name="calludf"></a><span data-ttu-id="f78e8-103">CallUDF</span><span class="sxs-lookup"><span data-stu-id="f78e8-103">CallUDF</span></span>

<span data-ttu-id="f78e8-104">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f78e8-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f78e8-105">Appelle une fonction définie par l'utilisateur dans un environnement informatique à hautes performances.</span><span class="sxs-lookup"><span data-stu-id="f78e8-105">Calls a user-defined function in a high-performance computing environment.</span></span>
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a><span data-ttu-id="f78e8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f78e8-106">Parameters</span></span>

<span data-ttu-id="f78e8-107">_Session_</span><span class="sxs-lookup"><span data-stu-id="f78e8-107">_SessionId_</span></span>
  
> <span data-ttu-id="f78e8-108">ID de la session dans laquelle effectuer l'appel.</span><span class="sxs-lookup"><span data-stu-id="f78e8-108">The ID of the session in which to make the call.</span></span>
    
<span data-ttu-id="f78e8-109">_XLLName_</span><span class="sxs-lookup"><span data-stu-id="f78e8-109">_XLLName_</span></span>
  
> <span data-ttu-id="f78e8-110">Nom de la XLL qui contient la fonction définie par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f78e8-110">The name of the XLL that contains the user-defined function.</span></span>
    
<span data-ttu-id="f78e8-111">_UDFName_</span><span class="sxs-lookup"><span data-stu-id="f78e8-111">_UDFName_</span></span>
  
> <span data-ttu-id="f78e8-112">Nom de la fonction définie par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f78e8-112">The name of the user-defined function.</span></span>
    
<span data-ttu-id="f78e8-113">_CallBackAddr_</span><span class="sxs-lookup"><span data-stu-id="f78e8-113">_CallBackAddr_</span></span>
  
> <span data-ttu-id="f78e8-114">Fonction que le connecteur doit appeler lorsque la fonction définie par l'utilisateur est terminée.</span><span class="sxs-lookup"><span data-stu-id="f78e8-114">The function that the connector should call when the user-defined function is finished.</span></span>
    
<span data-ttu-id="f78e8-115">_pxAsyncHandle_</span><span class="sxs-lookup"><span data-stu-id="f78e8-115">_pxAsyncHandle_</span></span>
  
> <span data-ttu-id="f78e8-116">Le handle asynchrone utilisé par Excel et le connecteur pour effectuer le suivi de l'appel de fonction défini par l'utilisateur en attente.</span><span class="sxs-lookup"><span data-stu-id="f78e8-116">The asynchronous handle used by Excel and the connector to track the pending user-defined function call.</span></span> <span data-ttu-id="f78e8-117">Le connecteur l'utilise ultérieurement lorsque l'appel est terminé, lorsqu'il rappelle dans Excel à l'aide du pointeur de fonction transmis dans l'argument _CallBackAddr_ .</span><span class="sxs-lookup"><span data-stu-id="f78e8-117">The connector uses it later when the call is finished, when it calls back into Excel using the function pointer passed in the  _CallBackAddr_ argument.</span></span> 
    
<span data-ttu-id="f78e8-118">_ArgCount_</span><span class="sxs-lookup"><span data-stu-id="f78e8-118">_ArgCount_</span></span>
  
> <span data-ttu-id="f78e8-119">Nombre d'arguments à transmettre à la fonction définie par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f78e8-119">The number of arguments to pass to the user-defined function.</span></span> <span data-ttu-id="f78e8-120">La valeur maximale autorisée est 255.</span><span class="sxs-lookup"><span data-stu-id="f78e8-120">The maximum value allowed is 255.</span></span>
    
<span data-ttu-id="f78e8-121">_Paramètre1_</span><span class="sxs-lookup"><span data-stu-id="f78e8-121">_Parameter1_</span></span>
  
> <span data-ttu-id="f78e8-122">Valeur à transmettre à la fonction définie par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f78e8-122">A value to pass to the user-defined function.</span></span> <span data-ttu-id="f78e8-123">Répétez cet argument pour chaque paramètre indiqué par _ArgCount_.</span><span class="sxs-lookup"><span data-stu-id="f78e8-123">Repeat this argument for each parameter indicated by  _ArgCount_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f78e8-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f78e8-124">Return value</span></span>

<span data-ttu-id="f78e8-125">**xlHpcRetSuccess** si l'appel de la FDU est initié avec succès; **xlHpcRetInvalidSessionId** si l'argument _SessionID_ n'est pas valide; **xlHpcRetCallFailed** sur d'autres défaillances, y compris le délai d'expiration. Si l'appel renvoie tout code d'erreur (à l'exception de **xlHpcRetSuccess**), Excel considère que l'appel de la FDU a échoué, annule la _pxAsyncHandle_et ne s'attend pas à un rappel.</span><span class="sxs-lookup"><span data-stu-id="f78e8-125">**xlHpcRetSuccess** if the UDF call is successfully initiated; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures, including time-out. If the call returns any error code (anything except **xlHpcRetSuccess**), then Excel considers the UDF call to have failed, invalidates the  _pxAsyncHandle_, and does not expect a callback to occur.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f78e8-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="f78e8-126">Remarks</span></span>

<span data-ttu-id="f78e8-127">Cette fonction s'exécute de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="f78e8-127">This function executes asynchronously.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f78e8-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f78e8-128">See also</span></span>

- [<span data-ttu-id="f78e8-129">Fonctions du connecteur de cluster Excel</span><span class="sxs-lookup"><span data-stu-id="f78e8-129">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

