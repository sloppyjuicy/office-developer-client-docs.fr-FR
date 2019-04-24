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
# <a name="xlrunningoncluster"></a>xlRunningOnCluster

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Renvoie une valeur qui indique si la fonction définie par l'utilisateur est exécutée sur un cluster. 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Paramètres

Cette fonction n'a pas d'argument.
  
## <a name="return-value"></a>Valeur renvoyée

Si la fonction est exécutée dans un processus Excel, renvoie 0 dans un **XLOPER12** de type **xltypeInt**. Si la fonction est exécutée sur un cluster, le type de retour et la valeur sont déterminés par le fournisseur de connecteur de cluster.
  
## <a name="requirements"></a>Configuration requise

Cette fonction est définie dans le fichier d'en-tête xlcall. h.
  
## <a name="see-also"></a>Voir aussi

- [Fonctions sécurisées pour le cluster](cluster-safe-functions.md)
- [Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

