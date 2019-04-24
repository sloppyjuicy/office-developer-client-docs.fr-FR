---
title: RunDataMacro, action de macro (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: Vous pouvez utiliser l'action RunDataMacro pour exécuter une macro de données autonome.
ms.openlocfilehash: 68c0e5a3837039bdab1165e686adb3bdf2a5b6f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304241"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a>RunDataMacro, action de macro (application Web personnalisée Access)

Vous pouvez utiliser l'action **RunDataMacro** pour exécuter une macro de données autonome. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="setting"></a>Paramètre

L’action **ExécuterMacroDonnées** utilise l’argument suivant. 
  
|**Argument de l'action**|**Description**|
|:-----|:-----|
| _Nom macro_ <br/> |Nom de la macro de données à exécuter.  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque vous sélectionnez la macro de données à exécuter dans le concepteur de macros, Access détermine si elle requiert des paramètres. Si la macro de données nécessite des paramètres, des zones de texte s'affichent à l'endroit où vous pouvez taper les arguments.
  
Lorsque vous exécutez une macro qui contient l'action **ExécuterMacroDonnées** et qu'elle atteint l'action **ExécuterMacroDonnées**, Access exécute la macro de données appelée. Lorsque celle-ci a terminé de s'exécuter, Access retourne à la macro d'origine et exécute l'action suivante. 
  

