---
title: SingleStep, action de macro
TOCTitle: SingleStep macro action
ms:assetid: 2836fe1d-fb9b-6b42-acfd-c52e468161d4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191989(v=office.15)
ms:contentKeyID: 48543855
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm47687
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9e934b290472dc4bb0ad8619b2ada6992b4215c0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726273"
---
# <a name="singlestep-macro-action"></a>SingleStep, action de macro

**S’applique à**: Access 2013, Office 2013

L'action **PasAPas** permet d'interrompre l'exécution d'une macro et d'ouvrir la boîte de dialogue **Pas à pas**.

## <a name="setting"></a>Valeur

L'action **PasAPas** n'utilise aucun argument.

## <a name="remarks"></a>Remarques

- L'action **PasAPas** permet de résoudre les dysfonctionnements d'une macro. Vous pouvez ajouter l'action **PasAPas** à une macro juste avant l'exécution d'une action que vous suspectez d'être la cause du problème. L'action interrompt l'exécution de la macro et ouvre la boîte de dialogue **Pas à pas**. Cette boîte de dialogue affiche les informations associées à l'action de la macro active, telles que le nom de la macro, les conditions spécifiées, le nom de l'action, les arguments et, le cas échéant, le numéro de l'erreur. Dans la boîte de dialogue, cliquez sur **Pas à pas** pour atteindre la prochaine action de macro, **Arrêter toutes les macros**, pour interrompre la macro active et, le cas échéant, les autres macros en cours d'exécution, ou cliquez sur **Continuer** pour arrêter la méthode Pas à pas et revenir à l'exécution normale de la macro.

- Utiliser l'action **PasAPas** équivaut à cliquer sur **Pas à pas** dans le groupe **Outils** de l'onglet **Créer** du Générateur de macro. La différence entre ce mode et l'exécution de l'action **PasAPas** est la suivante : en exécutant l'action, vous pouvez placer celle-ci dans la macro, à l'endroit précis où vous souhaitez démarrer le mode Pas à pas. Cette méthode vous évite de devoir passer en revue les actions précédentes avant d'accéder à celle que vous souhaitez examiner. En revanche, lorsque vous cliquez sur **Pas à pas** dans le Générateur de macro, vous devez le faire avant l'exécution de la macro. Dans ce cas, le mode Pas à pas démarre au niveau de la première action dans la macro.

> [!NOTE]
> [!REMARQUE] Si vous utilisez le mode pas à pas jusqu'à la fin d'une macro, sans cliquer sur **Continuer**, ce mode restera actif jusqu'à la fin de l'exécution de la macro. Les éventuelles macros suivantes seront également exécutées en mode Pas à pas. Pour désactiver le mode Pas à pas, cliquez sur **Continuer** dans la boîte de dialogue **Pas à pas** ou, dans une macro ouverte en mode Création, cliquez sur **Pas à pas** dans le groupe **Outils** de l'onglet **Créer** pour annuler la sélection.
