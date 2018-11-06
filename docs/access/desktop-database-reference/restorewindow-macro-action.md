---
title: RestoreWindow, action de macro
TOCTitle: RestoreWindow macro action
ms:assetid: 507a6452-2be0-a523-1201-0108d2b9d23c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193815(v=office.15)
ms:contentKeyID: 48544796
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11103
f1_categories:
- Office.Version=v15
ms.openlocfilehash: dfd7877ff1db960afcbf864f1e72ff01b12e8f09
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998951"
---
# <a name="restorewindow-macro-action"></a>RestoreWindow, action de macro

**S’applique à**: Access 2013, Office 2013

Vous pouvez utiliser l'action **RestaurerFenêtre** pour rétablir la taille initiale d'une fenêtre agrandie ou réduite.

> [!NOTE]
> [!REMARQUE] Cette action ne peut pas être appliquée à des fenêtres Code de Visual Basic Editor. Pour plus d'informations sur la modification des fenêtres Code, consultez la rubrique de la propriété **WindowState**.

## <a name="setting"></a>Paramètre

L'action **RestaurerFenêtre** ne possède aucun argument.

## <a name="remarks"></a>Notes

Cette action s'applique à l'objet sélectionné. Si un objet a été réduit, vous pouvez d'abord le sélectionner avec l'action **SélectionnerObjet** et rétablir sa taille initiale avec l'action **RestaurerFenêtre**.

Vous pouvez utiliser l'action **DéplacerEtDimensionnerFenêtre** pour déplacer ou dimensionner une fenêtre que vous avez restaurée.

L'action **RestaurerFenêtre** équivaut à cliquer sur le bouton **Restaurer** dans le coin supérieur droit de la fenêtre ou à cliquer sur la commande Restaurer dans le menu **Restaurer** du menu **Contrôle** de la fenêtre.

Pour exécuter l'action **RestaurerFenêtre** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Restore** de l'objet **DoCmd**.

