---
title: DisplayHourglassPointer, action de macro
TOCTitle: DisplayHourglassPointer macro action
ms:assetid: 2c93039a-f75c-abeb-1dfa-e632a5bdf6f2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192103(v=office.15)
ms:contentKeyID: 48543957
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117200
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 0ae2c20d3e447c1f1d039accc686a216d704ccfd
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63626667"
---
# <a name="displayhourglasspointer-macro-action"></a>DisplayHourglassPointer, action de macro


**S’applique à** : Access 2013, Office 2013

Utilisez l'action **AfficherPointeurSablier** pour transformer le pointeur de la souris en icône de sablier (ou toute autre icône choisie) pendant l'exécution d'une macro. Cette action peut fournir une indication visuelle de l'exécution de la macro. Elle est particulièrement utile lorsque l'exécution d'une action de macro ou de la macro elle-même prend beaucoup de temps.

## <a name="setting"></a>Paramètres

L’action **AfficherPointeurSablier** utilise l'argument suivant :

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument de l’action</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Sablier actif</strong></p></td>
<td><p>Cliquez sur <strong>Oui</strong> (afficher l’icône) ou sur <strong>Non</strong> (afficher le pointeur de souris normal) dans la zone <strong>Sablier actif</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. La valeur par défaut est <strong>Oui</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Cette action est souvent utilisée lorsque l'écho est désactivé à l'aide de l'action **Écho**. Lorsque l’écho est éteint, Access suspend les mises à jour de l’écran jusqu’à ce que la macro soit terminée.

Access réinitialise automatiquement l'argument **Sablier actif** sur la valeur **Non** une fois la macro terminée.

> [!NOTE]
> - Dans Microsoft Windows, il s'agit de l'icône définie pour **Occupé** dans la boîte de dialogue **Propriétés de Souris** du Panneau de configuration de Windows. L'icône utilisée par défaut pour tous les systèmes d'exploitation Windows est un sablier animé.
> - Vous pouvez choisir toute autre icône.

Pour exécuter l'action **AfficherPointeurSablier** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Hourglass** de l'objet **DoCmd**.

