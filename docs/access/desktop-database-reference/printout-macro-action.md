---
title: PrintOut, action de macro
TOCTitle: PrintOut macro action
ms:assetid: 13688158-1cf1-4b2e-d90a-271c8890e413
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845432(v=office.15)
ms:contentKeyID: 48543368
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm1697
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: b74abfe54be45db52e9854d73a5bf99b98c6d9eb
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63630566"
---
# <a name="printout-macro-action"></a>PrintOut, action de macro

**S’applique à** : Access 2013, Office 2013

Faites appel à l'action **Imprimer** pour imprimer l'objet actif dans la base de données ouverte. Vous pouvez imprimer des feuilles de données, des états, des formulaires, des pages d'accès aux données et des modules.

> [!NOTE]
> Cette action ne sera pas autorisée si la base de données n’est pas approuvée. 

## <a name="setting"></a>Setting

L’action **Imprimer** possède les arguments suivants.

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
<td><p><strong>Imprimer</strong></p></td>
<td><p>Étendue d’impression. Cliquez sur <strong>Tout</strong> (l’utilisateur peut imprimer l’intégralité de l’objet), sur <strong>Sélection</strong> (l’utilisateur peut imprimer la partie de l’objet qui est sélectionnée) ou sur <strong>Pages</strong> (l’utilisateur peut spécifier une série de pages dans les arguments <strong>De la page</strong> et <strong>À la page</strong>) dans la zone <strong>Imprimer</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. La valeur par défaut est <strong>Tout</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>De la page</strong></p></td>
<td><p>Première page à imprimer. L’impression commence en haut de cette page. Cet argument est obligatoire si vous sélectionnez l’option <strong>Pages</strong> dans la zone <strong>Imprimer</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>À la page</strong></p></td>
<td><p>Dernière page à imprimer. L’impression s’arrête à la fin de cette page. Cet argument est obligatoire si vous sélectionnez l’option <strong>Pages</strong> dans la zone <strong>Imprimer</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Qualité de l’impression</strong></p></td>
<td><p>Qualité d’impression. Cliquez sur <strong>Haute</strong>, <strong>Moyenne</strong>, <strong>Basse</strong> ou <strong>Brouillon</strong>. Plus la qualité est basse, plus l’impression de l’objet est rapide. <strong>Haute</strong> est la valeur par défaut.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Copies</strong></p></td>
<td><p>Nombre de copies à imprimer. La valeur par défaut est 1.</p></td>
</tr>
<tr class="even">
<td><p><strong>Copies triées</strong></p></td>
<td><p>Cliquez sur <strong>Oui</strong> (les copies imprimées sont triées) ou <strong>Non</strong> (elles ne sont pas triées). L’impression de l’objet peut être plus rapide si cet argument a la valeur <strong>Non</strong>. La valeur par défaut est <strong>Oui</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Cette action équivaut à sélectionner un objet, à cliquer sur l'onglet **Fichier**, puis à cliquer sur **Imprimer**. Toutefois, avec cette action, aucune boîte de dialogue **Imprimer** ne s'ouvre.

> [!TIP]
> [!CONSEIL] Si vous utilisez fréquemment des paramètres d'impression spécifiques, créez une macro contenant une action **Imprimer** reprenant ces paramètres dans ses arguments.

Les arguments à spécifier pour cette action correspondent aux options de la boîte de dialogue **Imprimer**. Toutefois, à la différence de l'action **TrouverEnregistrement** et la boîte de dialogue **Rechercher et remplacer**, les paramètres des arguments ne sont pas partagés avec les options de la boîte de dialogue **Imprimer**.

Pour exécuter l'action **Imprimer** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **PrintOut** de l'objet **DoCmd**.

