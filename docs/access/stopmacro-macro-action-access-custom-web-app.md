---
title: Action de Macro ArrêtMacro (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: Vous pouvez utiliser l’action ArrêtMacro pour arrêter la macro en cours d’exécution.
ms.openlocfilehash: 54501b65eb1847287e810ae43742a2e6e5384264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781983"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a>Action de Macro ArrêtMacro (accès personnalisé web app)

Vous pouvez utiliser l’action **ArrêtMacro** pour arrêter la macro en cours d’exécution. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="setting"></a>Valeur

L’action **ArrêtMacro** ne possède aucun argument. 
  
## <a name="remarks"></a>Remarques

Vous utilisez généralement cette action quand une condition rend nécessaire pour arrêter la macro. Par exemple, vous pouvez créer une macro de l’interface utilisateur qui ouvre une vue affichant les totaux de la commande tous les jours à la date entrée dans la vue actuelle. Vous pouvez utiliser une expression conditionnelle pour vous assurer que le contrôle de Date de la commande dans la boîte de dialogue contient une date valide. Le cas contraire, l’action de **contrôle zonemessage** peut afficher un message d’erreur et l’action **ArrêtMacro** arrêter la macro d’interface utilisateur. 
  

