---
title: xlRunningOnCluster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- xlrunningoncluster
ms.localizationpriority: medium
ms.assetid: 7662f255-4184-4af0-97f5-9a89347a201a
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a5c8a231a1b3dbb7288999f0ac782a89c2b6a943
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576610"
---
# <a name="xlrunningoncluster"></a>xlRunningOnCluster

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Renvoie une valeur qui indique si la fonction définie par l’utilisateur est en cours d’exécution sur un cluster. 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Paramètres

Cette fonction n’a pas d’arguments.
  
## <a name="return-value"></a>Valeur renvoyée

Si la fonction est en cours d’Excel, renvoie 0 dans une **XLOPER12** de type **xlTypeInt**. Si la fonction est en cours d’exécution sur un cluster, le type de retour et la valeur sont déterminés par le fournisseur de connecteur de cluster.
  
## <a name="requirements"></a>Configuration requise

Cette fonction est définie dans le fichier d’en-tête Xlcall.h.
  
## <a name="see-also"></a>Voir aussi

- [Fonctions sécurisées pour le cluster](cluster-safe-functions.md)
- [Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

