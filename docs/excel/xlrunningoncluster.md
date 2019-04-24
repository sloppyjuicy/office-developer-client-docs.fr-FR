---
title: xlRunningOnCluster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- xlrunningoncluster
localization_priority: Normal
ms.assetid: 7662f255-4184-4af0-97f5-9a89347a201a
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f5c630c73899b07e2727a7d42b18eb1891797bab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310100"
---
# <a name="xlrunningoncluster"></a><span data-ttu-id="47a1b-104">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="47a1b-104">xlRunningOnCluster</span></span>

<span data-ttu-id="47a1b-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="47a1b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="47a1b-106">Renvoie une valeur qui indique si la fonction définie par l'utilisateur est exécutée sur un cluster.</span><span class="sxs-lookup"><span data-stu-id="47a1b-106">Returns a value that indicates whether the user-defined function is running on a cluster.</span></span> 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="47a1b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47a1b-107">Parameters</span></span>

<span data-ttu-id="47a1b-108">Cette fonction n'a pas d'argument.</span><span class="sxs-lookup"><span data-stu-id="47a1b-108">This function has no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="47a1b-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="47a1b-109">Return value</span></span>

<span data-ttu-id="47a1b-110">Si la fonction est exécutée dans un processus Excel, renvoie 0 dans un **XLOPER12** de type **xltypeInt**.</span><span class="sxs-lookup"><span data-stu-id="47a1b-110">If the function is running in an Excel process, returns 0 in an **XLOPER12** of type **xlTypeInt**.</span></span> <span data-ttu-id="47a1b-111">Si la fonction est exécutée sur un cluster, le type de retour et la valeur sont déterminés par le fournisseur de connecteur de cluster.</span><span class="sxs-lookup"><span data-stu-id="47a1b-111">If the function is running on a cluster, the return type and value is determined by the cluster connector provider.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="47a1b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47a1b-112">Requirements</span></span>

<span data-ttu-id="47a1b-113">Cette fonction est définie dans le fichier d'en-tête xlcall. h.</span><span class="sxs-lookup"><span data-stu-id="47a1b-113">This function is defined in the Xlcall.h header file.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="47a1b-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47a1b-114">See also</span></span>

- [<span data-ttu-id="47a1b-115">Fonctions sécurisées pour le cluster</span><span class="sxs-lookup"><span data-stu-id="47a1b-115">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
- [<span data-ttu-id="47a1b-116">Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="47a1b-116">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

