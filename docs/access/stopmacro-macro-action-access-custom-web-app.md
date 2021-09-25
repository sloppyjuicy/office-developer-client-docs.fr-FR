---
title: StopMacro Macro Action (Application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: Vous pouvez utiliser l’action ArrêterMacro pour arrêter la macro en cours d’exécution.
ms.openlocfilehash: 873937805bb96584dc08708cf2fe4eeadeec8b03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614730"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a>StopMacro Macro Action (Application web personnalisée Access)

Vous pouvez utiliser l’action **ArrêterMacro** pour arrêter la macro en cours d’exécution. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="setting"></a>Paramètre

**L’action StopMacro** ne comprend aucun argument. 
  
## <a name="remarks"></a>Remarques

Cette action est généralement utilisée lorsqu’une condition rend nécessaire l’arrêt de la macro. Par exemple, vous pouvez créer une macro d’interface utilisateur qui ouvre une vue affichant les totaux de commande quotidiens pour la date entrée dans l’affichage actuel. Vous pouvez utiliser une expression conditionnelle pour vous assurer que le contrôle Date de commande de la boîte de dialogue contient une date valide. Si ce n’est pas le cas, l’action **MessageBox** peut afficher un message d’erreur et l’action **ArrêterMacro** peut arrêter la macro d’interface utilisateur. 
  

