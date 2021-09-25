---
title: StopAllMacros, action de macro
TOCTitle: StopAllMacros macro action
ms:assetid: 6afbf906-03b8-6e68-bbc9-7a4b141cf1c5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195440(v=office.15)
ms:contentKeyID: 48545442
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm104968
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 7a80017a58f0d0e1c1f9e50fbeb751e587822dcd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601785"
---
# <a name="stopallmacros-macro-action"></a>StopAllMacros, action de macro


**S’applique à** : Access 2013, Office 2013

L’action **ArrêtToutesMacros** permet d’arrêter toutes les macros en cours d’exécution.

## <a name="setting"></a>Paramètre

L’action **ArrêtToutesMacros** n’utilise aucun argument.

## <a name="remarks"></a>Remarques

Cette action est généralement utilisée lorsqu’une condition d’erreur nécessite l’arrêt de toutes les macros. Vous pouvez utiliser une expression conditionnelle dans la ligne d’action de la macro contenant cette action. Lorsque l’expression renvoie la valeur **True** (–1), Microsoft Access arrête l’exécution de toutes les macros.

C'est le cas, par exemple, lorsque l'affichage d'une boîte de message constitue l'une des actions complexes d'une macro, parmi lesquelles l'exécution d'autres macros. Si l'utilisateur clique sur **Annuler** dans cette boîte de message, l'action **ArrêtToutesMacros** peut entraîner l'arrêt de toutes les macros en cours d'exécution.

Si les actions **Écho** ou **Avertissements** ont été utilisées par une macro pour désactiver un écho ou l'affichage des messages système, l'action **ArrêtToutesMacros** les réactivera automatiquement.

Cette action n'est pas disponible dans les modules Visual Basic pour Applications (VBA).

