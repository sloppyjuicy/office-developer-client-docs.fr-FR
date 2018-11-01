---
title: Bip, Action de Macro (référence de base de données du bureau Access)
TOCTitle: Beep Macro Action
ms:assetid: 5ca1600f-7934-3b3d-19fd-f305cda0e5d8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194572(v=office.15)
ms:contentKeyID: 48545092
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11853
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 284be6222d0b81e48a061afd1d87dd32c3985feb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867579"
---
# <a name="beep-macro-action"></a>Bip, action de macro


**S’applique à**: Access 2013, Office 2013

Utilisez l'action **Bip** pour émettre un signal sonore dans les haut-parleurs de l'ordinateur.

## <a name="setting"></a>Valeur

L'action **Bip** ne possède aucun argument.

## <a name="remarks"></a>Remarques

Vous pouvez utiliser l'action **Bip** pour signaler les occurrences suivantes :

  - des modifications importantes ont été apportées à l'écran ;

  - le type de données entré dans un contrôle est incorrect. Par exemple, l'utilisateur a entré des donnes numériques dans un contrôle zone de texte ;

  - une macro a atteint un point spécifique ou a terminé ses actions.

La fréquence et la durée du signal sonore dépendent du matériel, qui peut varier d'un ordinateur à un autre.

Pour exécuter l'action **Bip** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Beep** de l'objet **DoCmd**.

