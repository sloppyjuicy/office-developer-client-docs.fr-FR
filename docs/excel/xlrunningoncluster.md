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
ms.openlocfilehash: f42ccbeb94e1fc6b6cf880f1b32ee1bfeb24997e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782255"
---
# <a name="xlrunningoncluster"></a><span data-ttu-id="c4d15-104">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="c4d15-104">xlRunningOnCluster</span></span>

<span data-ttu-id="c4d15-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c4d15-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c4d15-106">Renvoie une valeur qui indique si la fonction définie par l’utilisateur est en cours d’exécution sur un cluster.</span><span class="sxs-lookup"><span data-stu-id="c4d15-106">Returns a value that indicates whether the user-defined function is running on a cluster.</span></span> 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="c4d15-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4d15-107">Parameters</span></span>

<span data-ttu-id="c4d15-108">Cette fonction ne comporte aucun argument.</span><span class="sxs-lookup"><span data-stu-id="c4d15-108">This function has no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="c4d15-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="c4d15-109">Return value</span></span>

<span data-ttu-id="c4d15-110">Si la fonction s’exécute dans un processus Excel, renvoie la valeur 0 dans un **XLOPER12** de type **xlTypeInt**.</span><span class="sxs-lookup"><span data-stu-id="c4d15-110">If the function is running in an Excel process, returns 0 in an **XLOPER12** of type **xlTypeInt**.</span></span> <span data-ttu-id="c4d15-111">Si la fonction s’exécute sur un cluster, le type de retour et la valeur est déterminée par le fournisseur de connecteur de cluster.</span><span class="sxs-lookup"><span data-stu-id="c4d15-111">If the function is running on a cluster, the return type and value is determined by the cluster connector provider.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="c4d15-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4d15-112">Requirements</span></span>

<span data-ttu-id="c4d15-113">Cette fonction est définie dans le fichier d’en-tête Xlcall.h.</span><span class="sxs-lookup"><span data-stu-id="c4d15-113">This function is defined in the Xlcall.h header file.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c4d15-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4d15-114">See also</span></span>

- [<span data-ttu-id="c4d15-115">Fonctions sécurisées pour le cluster</span><span class="sxs-lookup"><span data-stu-id="c4d15-115">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
- [<span data-ttu-id="c4d15-116">Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="c4d15-116">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

