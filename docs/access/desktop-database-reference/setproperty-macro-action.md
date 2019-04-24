---
title: SetProperty, action de macro
TOCTitle: SetProperty macro action
ms:assetid: 58d2eac3-35b2-e9f8-47e0-62c9b52f2c24
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194340(v=office.15)
ms:contentKeyID: 48545004
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm139044
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c5972ad630efe3afe27565924c7c6a8a2230a9f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314573"
---
# <a name="setproperty-macro-action"></a>SetProperty, action de macro

**S’applique à** : Access 2013, Office 2013

L'action **DéfinirPropriété** permet de définir une propriété pour un contrôle dans un formulaire ou un état.

## <a name="setting"></a>Setting

L’action **DéfinirPropriété** utilise les arguments suivants :

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
<td><p>Nom du contrôle</p></td>
<td><p>Tapez le nom du champ ou du contrôle pour lequel vous souhaitez définir la valeur d’une propriété. Utilisez uniquement le nom du contrôle, et non la syntaxe complète. Laissez cet argument vide si vous souhaitez définir cette propriété pour le formulaire ou l’état actif.</p></td>
</tr>
<tr class="even">
<td><p>Propriété</p></td>
<td><p>Sélectionnez la propriété dont la valeur doit être définie. Consultez la section <strong>Remarques</strong> de cet article pour accéder à la liste des propriétés qui peuvent être définies via cette action.</p></td>
</tr>
<tr class="odd">
<td><p>Valeur</p></td>
<td><p>Tapez la valeur que vous souhaitez définir pour la propriété. Pour les propriétés dont la valeur doit être définie sur Oui ou Non, utilisez <strong>-1</strong> pour Oui et <strong>0</strong> pour Non.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

- L’action **DéfinirPropriété** permet de définir les propriétés suivantes pour un contrôle : **Activé**, **Visible**, **Verrouillé**, **Gauche**, **Haut**, **Largeur**, **Hauteur**, **Couleur texte**, **Couleur fond** ou **Légende**.

- Si vous entrez une valeur non admise pour l’argument ***Valeur***, aucune erreur ne se produit, mais il se peut que la valeur de la propriété soit modifiée dans Access, selon l’interprétation de l’argument.

- L'action **DéfinirPropriété** peut être utilisée dans une macro autonome, à condition de la faire précéder d'une action sélectionnant le formulaire ou l'état contenant le contrôle pour lequel la propriété est définie. Si le formulaire ou l'état n'est pas ouvert, vous pouvez utiliser les actions **OuvrirFormulaire** ou **OuvrirEtat** pour l'ouvrir et le sélectionner. Si le formulaire ou l'état est déjà ouvert, vous pouvez utiliser l'action **SélectionnerObjet** pour le sélectionner. Vous pouvez ensuite utiliser l'action **DéfinirPropriété** pour définir la propriété. La sélection de l'objet n'est pas nécessaire si vous utilisez l'action **DéfinirPropriété** dans une macro incorporée dans un contrôle du même formulaire ou du même état que le contrôle pour lequel vous définissez la propriété.

- To run the **SetProperty** action in a VBA module, use the **SetProperty** method of the **DoCmd** object.

## <a name="example"></a>Exemple

L'exemple suivant montre comment utiliser l'action SetProperty pour faire basculer la visibilité de la zone de texte **myTextBox** .

**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Submacro: TestVisible
        SetProperty
            Control Name Text40
            Property Visible
            Value =Not[Text40].[Visible]
    End Submacro
```
