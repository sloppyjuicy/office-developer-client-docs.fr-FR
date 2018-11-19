---
title: ApplyFilter, action de macro
TOCTitle: ApplyFilter macro action
ms:assetid: c63988c4-4506-cc51-98f7-478d1f3fe668
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823130(v=office.15)
ms:contentKeyID: 48547623
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm79035
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f6f0511a1358e8d9b0d0ee820e83cf59d2400345
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025966"
---
# <a name="applyfilter-macro-action"></a>ApplyFilter, action de macro

**S’applique à**: Access 2013, Office 2013

Utilisez l'action **AppliquerFiltre** pour appliquer un filtre, une requête ou une clause SQL WHERE à une table, un formulaire ou un état de manière à restreindre ou trier les enregistrements de la table ou bien les enregistrements de la table ou de la requête sous-jacente du formulaire ou de l'état. Dans le cas d'un état, utilisez cette action uniquement dans une macro spécifiée par la propriété de type événement **SurOuverture** de cet état.

> [!NOTE]
> [!REMARQUE] Vous pouvez utiliser cette action pour appliquer une clause WHERE SQL seulement lorsque vous appliquez un filtre serveur. Il n'est pas possible d'appliquer un filtre serveur à une source d'enregistrement d'une procédure stockée.

## <a name="setting"></a>Valeur

L'action **AppliquerFiltre** possède les arguments suivants.

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
<td><p>Nom du filtre</p></td>
<td><p>Le nom d’un filtre ou une requête qui limite ou trie les enregistrements de la table, formulaire ou état. Vous pouvez entrer le nom d’une requête existante ou un filtre qui a été enregistré en tant que requête dans la zone <strong>Nom du filtre</strong> dans la section <strong>Arguments de l’Action</strong> du volet <strong>Générateur de Macro</strong> .</p><p><strong>Remarque</strong>: lorsque vous utilisez cette action pour appliquer un filtre serveur, l’argument nom du filtre doit être vide.</p></td>
</tr>
<tr class="even">
<td><p>Where Condition</p></td>
<td><p>Clause SQL WHERE (sans le mot WHERE) valide ou expression qui restreint les enregistrements de la table, du formulaire ou de l’état. 

</p>
<p><b>Remarque</b>: dans une expression Condition Where argument, le côté gauche de l’expression contient généralement un nom de champ de la table ou requête sous-jacente pour le formulaire ou état. Le côté droit de l’expression contient généralement les critères que vous voulez appliquer à ce champ pour restreindre ou trier les enregistrements. Par exemple, les critères peuvent être le nom d’un contrôle sur un autre formulaire qui contient la valeur que vous souhaitez que les enregistrements dans le premier formulaire doivent correspondre. Le nom du contrôle doit être qualifié complet, par exemple :</p>
<p><strong>Formulaires</strong>! <em>formname</em>! <em>controlname</em> Noms de champs doivent être placés entre guillemets doubles et les littéraux de chaîne doivent être placés entre guillemets simples. La longueur maximale de l’argument Condition Where est de 255 caractères. Si vous devez entrer une clause SQL WHERE plus longue, utilisez la méthode <strong>ApplyFilter</strong> de l’objet <strong>DoCmd</strong> dans un Visual Basic pour le module d’Applications (VBA). Vous pouvez entrer des instructions de clause SQL WHERE jusqu'à 32 768 caractères dans VBA.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!REMARQUE] Utilisez l'argument Nom du filtre si vous avez déjà défini un filtre qui fournit les données appropriées. Utilisez l'argument Condition Where pour entrer directement les critères de restriction. Si vous utilisez les deux arguments, Microsoft Office Access 2007 applique la clause WHERE aux résultats du filtre. Vous devez utiliser au moins l'un de ces deux arguments.

## <a name="remarks"></a>Remarques

Vous pouvez appliquer un filtre ou une requête à un formulaire en mode Formulaire ou Feuille de données.

Le filtre et la condition WHERE que vous appliquez deviennent les paramètres de la propriété **Filtre** ou **FiltreServeur** du formulaire ou de l'état.

Pour les tables et les formulaires, cette action équivaut à cliquer sur **Appliquer le filtre/tri** ou **Appliquer un filtre serveur** dans le menu **Enregistrements**. La commande de menu applique le dernier filtre créé à la table ou au formulaire, alors que l'action **AppliquerFiltre** applique un filtre ou une requête spécifique.

Dans une base de données Access, si vous pointez sur **Filtrer** dans le menu **Enregistrements**, puis cliquez sur **Filtre/tri avancé** après avoir exécuté l'action **AppliquerFiltre**, la fenêtre Filtre/tri avancé affiche les critères de filtre sélectionnés avec cette action.

Pour supprimer un filtre et afficher tous les enregistrements d'une table ou d'un formulaire dans une base de données Office Access 2007, utilisez l'action **AfficherTousEnreg** ou la commande **Afficher tous les enregistrements** du menu **Enregistrements**. Pour supprimer un filtre dans un projet Access (.adp), vous pouvez revenir dans la fenêtre Filtrer par formulaire sur serveur et supprimer tous les critères de filtre, puis cliquer sur **Appliquer un filtre serveur** dans le menu **Enregistrements** de la barre d'outils ou définir la propriété **FiltreParFormulaireSurServeur** sur **Faux** (0).

Lorsque vous enregistrez une table ou un formulaire, Access enregistre tout filtre actuellement défini dans cet objet, mais il ne l’applique pas automatiquement à la prochaine ouverture de l’objet (même si en revanche, il applique tout tri que vous avez appliqué à l’objet avant de l’enregistrer). Si vous souhaitez appliquer automatiquement un filtre à la première ouverture d’un formulaire, vous devez spécifier une macro contenant l’action AppliquerFiltre ou une procédure événementielle contenant la méthode ApplyFilter de l’objet DoCmd comme paramètre de la propriété de type événement SurOuverture du formulaire. Vous pouvez également appliquer un filtre à l’aide de l’action OuvrirFormulaire ou OuvrirEtat, ou des méthodes correspondantes (OpenForm et OpenReport). Pour appliquer automatiquement un filtre à la première ouverture d’une table, ouvrez la table à l’aide d’une macro contenant l’action OuvrirTable, immédiatement suivie de l’action AppliquerFiltre.

## <a name="example"></a>Exemple

L’exemple suivant montre comment utiliser l’action AppliquerFiltre pour filtrer le formulaire frmFoods lors de son ouverture.

**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    ApplyFilter
        Filter Name
        Where Condition=[display_name] Link "*cheese*"
        Control Name
```



