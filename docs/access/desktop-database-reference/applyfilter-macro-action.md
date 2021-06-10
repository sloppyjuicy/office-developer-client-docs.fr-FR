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
localization_priority: Normal
ms.openlocfilehash: e79ab56778f9429e7f1a985f0f81864ae4363606
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296996"
---
# <a name="applyfilter-macro-action"></a>ApplyFilter, action de macro

**S’applique à** : Access 2013, Office 2013

Utilisez l'action **AppliquerFiltre** pour appliquer un filtre, une requête ou une clause SQL WHERE à une table, un formulaire ou un état de manière à restreindre ou trier les enregistrements de la table ou bien les enregistrements de la table ou de la requête sous-jacente du formulaire ou de l'état. Dans le cas d'un état, utilisez cette action uniquement dans une macro spécifiée par la propriété de type événement **SurOuverture** de cet état.

> [!NOTE]
> [!REMARQUE] Vous pouvez utiliser cette action pour appliquer une clause WHERE SQL seulement lorsque vous appliquez un filtre serveur. Il n'est pas possible d'appliquer un filtre serveur à une source d'enregistrement d'une procédure stockée.

## <a name="setting"></a>Paramètre

L’action **AppliquerFiltre** possède les arguments suivants.

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
<td><p>Nom d’un filtre ou d’une requête qui restreint ou trie les enregistrements de la table, du formulaire ou du rapport. Vous pouvez entrer le nom d’une requête existante ou d’un filtre <strong></strong> qui a été enregistré en tant que requête dans la zone Nom du filtre de la section Arguments de <strong>l’action</strong> du volet Générateur de <strong>macro.</strong></p><p><strong>REMARQUE</strong>: lorsque vous utilisez cette action pour appliquer un filtre serveur, l’argument Nom du filtre doit être vide.</p></td>
</tr>
<tr class="even">
<td><p>Condition Where</p></td>
<td><p>Clause SQL WHERE (sans le mot WHERE) valide ou expression qui restreint les enregistrements de la table, du formulaire ou de l’état.</p>
<p><b>REMARQUE</b>: dans une expression d’argument Condition Where, le côté gauche de l’expression contient généralement un nom de champ de la table ou de la requête sous-jacente pour le formulaire ou l’état. La partie droite de l’expression contient généralement les critères que vous souhaitez appliquer à ce champ pour restreindre ou trier les enregistrements. Ces critères peuvent ainsi être le nom d’un contrôle dans un autre formulaire qui contient la valeur à laquelle doivent correspondre les enregistrements dans le premier formulaire. Le nom du contrôle doit être complet, comme dans l’exemple suivant :</p>
<p><strong>Formulaires</strong>! <em>formname</em>! <em>controlname</em> Les noms de champs doivent être entourés de guillemets doubles et les littéraux de chaîne doivent être entourés de guillemets simples. L’argument Condition Where est limité à 255 caractères. Si vous avez besoin d’entrer une clause SQL WHERE plus longue, utilisez la méthode <strong>ApplyFilter</strong> de l’objet <strong>DoCmd</strong> dans un module Visual Basic pour Applications (VBA). Dans VBA, les instructions de clause SQL WHERE peuvent contenir jusqu’à 32 768 caractères.</p></td>
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

When you save a table or form, Access saves any filter currently defined in that object, but won't apply the filter automatically the next time the object is opened (although it will automatically apply any sort you applied to the object before it was saved). If you want to apply a filter automatically when a form is first opened, specify a macro containing the **ApplyFilter** action or an event procedure containing the **ApplyFilter** method of the **DoCmd** object as the **OnOpen** event property setting of the form. You can also apply a filter by using the **OpenForm** or **OpenReport** action, or their corresponding methods. To apply a filter automatically when a table is first opened, you can open the table by using a macro containing the **OpenTable** action, followed immediately by the **ApplyFilter** action.

## <a name="example"></a>Exemple

L’exemple suivant montre comment utiliser l’action AppliquerFiltre pour filtrer le formulaire frm Foods lors de son ouverture.

**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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



