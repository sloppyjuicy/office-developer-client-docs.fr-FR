---
title: Bip, action de macro (référence de base de données de bureau Access)
TOCTitle: Beep macro action
ms:assetid: 5ca1600f-7934-3b3d-19fd-f305cda0e5d8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194572(v=office.15)
ms:contentKeyID: 48545092
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11853
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 9384b4b10b5d370518b760eb1c0f7edf9d162eeb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607128"
---
# <a name="beep-macro-action"></a>Beep, action de macro


**S’applique à** : Access 2013, Office 2013

Utilisez l’action **Bip** pour émettre un signal sonore dans les haut-parleurs de l’ordinateur.

## <a name="setting"></a>Paramètre

L’action **Bip** ne possède aucun argument.

## <a name="remarks"></a>Remarques

Vous pouvez utiliser l’action **Bip** pour signaler les occurrences suivantes :

  - des modifications importantes ont été apportées à l'écran ;

  - le type de données entré dans un contrôle est incorrect. Par exemple, l'utilisateur a entré des donnes numériques dans un contrôle zone de texte ;

  - une macro a atteint un point spécifique ou a terminé ses actions.

La fréquence et la durée du signal sonore dépendent du matériel, qui peut varier d'un ordinateur à un autre.

Pour exécuter l'action **Bip** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Beep** de l'objet **DoCmd**.

