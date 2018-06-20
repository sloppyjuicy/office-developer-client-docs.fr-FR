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
# <a name="xlrunningoncluster"></a>xlRunningOnCluster

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Renvoie une valeur qui indique si la fonction définie par l’utilisateur est en cours d’exécution sur un cluster. 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Paramètres

Cette fonction ne comporte aucun argument.
  
## <a name="return-value"></a>Valeur renvoy�e

Si la fonction s’exécute dans un processus Excel, renvoie la valeur 0 dans un **XLOPER12** de type **xlTypeInt**. Si la fonction s’exécute sur un cluster, le type de retour et la valeur est déterminée par le fournisseur de connecteur de cluster.
  
## <a name="requirements"></a>Configuration requise

Cette fonction est définie dans le fichier d’en-tête Xlcall.h.
  
## <a name="see-also"></a>Voir aussi

- [Fonctions sécurisées pour le cluster](cluster-safe-functions.md)
- [Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

