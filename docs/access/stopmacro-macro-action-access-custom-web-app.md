---
title: StopMacro Macro Action (Application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: Vous pouvez utiliser l’action ArrêterMacro pour arrêter la macro en cours d’exécution.
ms.openlocfilehash: 9aabe8a0f3b8625ca91614fb431d1038fcca9cc9
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62179941"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a>StopMacro Macro Action (Application web personnalisée Access)

Vous pouvez utiliser l’action **ArrêterMacro** pour arrêter la macro en cours d’exécution. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="setting"></a>Paramètre

**L’action StopMacro** ne comprend aucun argument. 
  
## <a name="remarks"></a>Remarques

Cette action est généralement utilisée lorsqu’une condition rend nécessaire l’arrêt de la macro. Par exemple, vous pouvez créer une macro d’interface utilisateur qui ouvre une vue affichant les totaux de la commande quotidienne pour la date entrée dans l’affichage actuel. Vous pouvez utiliser une expression conditionnelle pour vous assurer que le contrôle Date de commande de la boîte de dialogue contient une date valide. Si ce n’est pas le cas, l’action **MessageBox** peut afficher un message d’erreur et l’action **ArrêterMacro** peut arrêter la macro d’interface utilisateur. 
  

