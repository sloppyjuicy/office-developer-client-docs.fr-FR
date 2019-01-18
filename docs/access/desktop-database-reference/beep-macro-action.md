---
title: Bip, action de macro (référence de base de données du bureau Access)
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
localization_priority: Normal
ms.openlocfilehash: 96051d8389f4b8ba7005c75ccdb5e2780ba17138
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721471"
---
# <a name="beep-macro-action"></a>Beep, action de macro


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

