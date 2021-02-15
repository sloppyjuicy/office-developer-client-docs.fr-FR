---
title: SetWarnings, action de macro
TOCTitle: SetWarnings macro action
ms:assetid: ff95b919-b1ee-c0a0-851d-71894851bb1d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837313(v=office.15)
ms:contentKeyID: 48548965
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165020
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: acf541bde41c282b752532cb74d5ec4fa4a13ca9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308658"
---
# <a name="setwarnings-macro-action"></a>SetWarnings, action de macro

**S’applique à** : Access 2013, Office 2013

L'action **Avertissements** permet d'activer ou de désactiver les messages système.

> [!NOTE]
> Cette action ne sera pas autorisée si la base de données n’est pas approuvée. 

## <a name="setting"></a>Setting

L’action **Avertissements** utilise les arguments suivants :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument de l’action</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Avertissements actifs</strong></p></td>
<td><p>Spécifie si les messages système sont affichés. Cliquez sur <strong>Oui</strong> pour activer les messages système ou sur <strong>Non</strong> pour les désactiver dans la zone <strong>Avertissements actifs</strong> de la section <strong>Arguments de l’action</strong> du Générateur de macro. La valeur par défaut est <strong>Non</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous pouvez utiliser cette action pour empêcher que les avertissements modaux et les boîtes de message n’interrompent la macro. Néanmoins, des messages d’erreur sont toujours affichés, et Microsoft Access affiche les boîtes de dialogue nécessitant la saisie de données, et non l’activation d’un bouton (tel que **OK**, **Annuler**, **Oui** ou **Non**) , par exemple, une boîte de dialogue dans laquelle vous devez entrer des chaînes de texte ou sélectionner une ou plusieurs options.

Exécuter cette action avec l'argument **Avertissements actifs** défini sur **Non** équivaut à appuyer sur la touche Entrée chaque fois qu'un avertissement ou une boîte de message s'affiche. En règle générale, la réponse à l'avertissement ou au message s'effectue en cliquant sur **OK** ou sur le bouton **Oui**.

À la fin de l'exécution de la macro, l'affichage des messages système est automatiquement réactivé dans Access.

Cette action est souvent utilisée conjointement avec l'action **Écho**, qui masque les résultats d'une macro jusqu'à la fin de son exécution. Vous pouvez également utiliser l'action **Avertissements** pour masquer les avertissements et les boîtes de message.

> [!WARNING]
> [!ATTENTION] Bien que l'action **Avertissements** permette de simplifier les interactions avec les macros, il est conseillé d'agir prudemment lors de la désactivation des messages système. Dans certains cas, vous choisirez d'interrompre l'exécution d'une macro lors de l'affichage d'un avertissement. Par conséquent, à moins d'être certain des résultats de toutes les actions de macro, l'utilisation de cette action n'est pas conseillée.

Pour exécuter l'action **Avertissements** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **SetWarnings** de l'objet **DoCmd**.

