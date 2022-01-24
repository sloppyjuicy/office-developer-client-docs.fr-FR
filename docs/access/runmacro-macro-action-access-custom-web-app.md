---
title: RunMacro Macro Action (Application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: Vous pouvez utiliser l’action ExécuterMacro pour exécuter une macro d’interface utilisateur.
ms.openlocfilehash: fcc79a2d359fe50f6d8d0689e4d7e83ce5b77588
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62179542"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a>RunMacro Macro Action (Application web personnalisée Access)

Vous pouvez utiliser l’action **ExécuterMacro** pour exécuter une macro d’interface utilisateur. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="setting"></a>Paramètre

L’action **ExécuterMacro** accepte les arguments suivants. 
  
|**Argument de l'action**|**Description**|
|:-----|:-----|
|**Nom macro** <br/> |Nom de la macro d’interface utilisateur à exécuter.  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque vous exécutez une macro d’interface utilisateur contenant l’action **ExécuterMacro** et qu’elle atteint l’action **ExécuterMacro,** Access exécute la macro d’interface utilisateur appelée. Lorsque la macro d’interface utilisateur appelée est terminée, Access revient à la macro d’interface utilisateur d’origine et exécute l’action suivante. 
  

