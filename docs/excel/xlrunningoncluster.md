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
ms.openlocfilehash: dcbaae6c926e44aced6ac8e164db21f072252510
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198718"
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
  
## <a name="requirements"></a>Conditions requises

Cette fonction est définie dans le fichier d’en-tête Xlcall.h.
  
## <a name="see-also"></a>Voir aussi

- [Fonctions sécurisées pour le cluster](cluster-safe-functions.md)
- [Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

