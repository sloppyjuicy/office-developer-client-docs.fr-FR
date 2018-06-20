---
title: ExécuterMacro, Action de Macro (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: Vous pouvez utiliser l’action ExécuterMacro pour exécuter une macro de l’interface utilisateur.
ms.openlocfilehash: 68a59e246c0af8385a17aedcf3da771c720f8fd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781977"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a>ExécuterMacro, Action de Macro (accès personnalisé web app)

Vous pouvez utiliser l’action **ExécuterMacro** pour exécuter une macro de l’interface utilisateur. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="setting"></a>Valeur

L'action **ExécuterMacro** accepte les arguments suivants. 
  
|**Argument de l'action**|**Description**|
|:-----|:-----|
|**Nom de la macro** <br/> |Nom de la macro d’interface utilisateur à exécuter.  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque vous exécutez une macro d’interface utilisateur contenant l’action **ExécuterMacro** et qu’elle atteint l’action **ExécuterMacro** , Access exécute la macro appelée de l’interface utilisateur. Lorsque la macro d’interface utilisateur appelée est terminée, Access retourne à la macro d’interface utilisateur d’origine et exécute l’action suivante. 
  

