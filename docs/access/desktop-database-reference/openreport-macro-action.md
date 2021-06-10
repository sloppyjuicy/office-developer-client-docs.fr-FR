---
title: OpenReport, action de macro
TOCTitle: OpenReport macro action
ms:assetid: cd35faf2-190d-ac48-cf59-81c1599eb764
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834462(v=office.15)
ms:contentKeyID: 48547758
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm188079
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cff57a185d226328792bef79072dfc46c6134f98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288349"
---
# <a name="openreport-macro-action"></a>OpenReport, action de macro

**S’applique à** : Access 2013, Office 2013

Faites appel à l'action **OuvrirEtat** pour ouvrir un état en mode Création ou Aperçu avant impression ou pour envoyer l'état directement à l'imprimante. Vous pouvez également limiter les enregistrements qui sont imprimés dans l'état.

## <a name="setting"></a>Paramètre

L’action **OuvrirEtat** possède les arguments suivants.

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
<td><p>Nom du rapport</p></td>
<td><p>Nom de l'état à ouvrir. La zone <strong>Nom de l'état</strong> de la section <strong>Arguments de l'action</strong> du volet <strong>Générateur de macro</strong> présente tous les états dans la base de données actuelle. Il s'agit d'un argument obligatoire. Si vous exécutez une macro contenant l'action OpenReport dans une base de données bibliothèque, Microsoft Access recherche d'abord l'état portant ce nom dans la base de données bibliothèque, puis dans la base de données actuelle.  </p></td>
</tr>
<tr class="even">
<td><p>Afficher</p></td>
<td><p>Affichage dans lequel s'ouvre l'état. Cliquez sur <strong>Imprimer</strong> (imprime l'état immédiatement), <strong>Création</strong> ou <strong>Aperçu avant impression</strong> dans la zone <strong>Affichage</strong>. La valeur par défaut est <strong>Imprimer</strong>.  </p></td>
</tr>
<tr class="odd">
<td><p>Nom du filtre</p></td>
<td><p>Filtre qui limite les enregistrements de l'état. Vous pouvez entrer le nom d'une requête existante quelconque ou d'un filtre enregistré en tant que requête. La requête doit toutefois inclure tous les champs de l'état que vous ouvrez, ou sa propriété <strong>TousLesChamps</strong> doit avoir la valeur <strong>Oui</strong>.  </p></td>
</tr>
<tr class="even">
<td><p>Condition Where</p></td>
<td><p>Clause ou expression WHERE SQL valable (sans le mot WHERE) utilisée par Access pour sélectionner des enregistrements dans la table ou requête sous-jacente de l'état. Si vous sélectionnez un filtre avec l’argument Nom du filtre, Access applique cette clause WHERE aux résultats du filtre. Pour ouvrir un état et limiter ses enregistrements à ceux spécifiés par la valeur d’un contrôle sur un formulaire, utilisez l’expression suivante :<br />
<strong>[</strong><em>nom_champ</em><strong>] = Formulaires ! [</strong><em>nom_formulaire</em><strong>]! [</strong><em>nom du contrôle sur le formulaire</em><strong>]</strong><br />
Remplacez <em>fieldname</em> par le nom d’un champ dans la table ou la requête sous-jacente de l’état que vous souhaitez ouvrir. Remplacez <em>nom_formulaire</em> et <em>nom_contrôle dans le formulaire</em> par le nom du formulaire et du contrôle dans le formulaire qui contient la valeur avec laquelle vous souhaitez que les enregistrements de l’état correspondent.</p>
<p><b>REMARQUE</b>: la longueur maximale de l’argument Condition Where est de 255 caractères. If you need to enter a more complex SQL WHERE clause longer than this, use the <b>OpenReport</b> method of the <b>DoCmd</b> object in a Visual Basic for Applications (VBA) module instead. You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</p>
</td>
</tr>
<tr class="odd">
<td><p>Mode Fenêtre</p></td>
<td><p>Mode dans lequel s'ouvre l'état. Cliquez sur <strong>Standard</strong>, <strong>Masqué</strong>, <strong>Icône</strong> ou <strong>Boîte de dialogue</strong> dans la zone <strong>Mode Fenêtre</strong>. La valeur par défaut est <strong>Standard</strong>.  </p>
<p><b>REMARQUE</b>: certains paramètres d’argument du mode Fenêtre ne s’appliquent pas lors de l’utilisation de documents à onglets. Pour passer à des fenêtres superposées :
<ol>
<li><p>Cliquez sur <strong>Options</strong>.</p></li>
<li><p>Dans la boîte dialogue <strong>Options Access</strong>, cliquez sur <strong>Base de données active</strong>.</p></li>
<li><p>Dans la section <strong>Options de l'application</strong>, sous <strong>Options de la fenêtre Document</strong>, cliquez sur <strong>Fenêtres superposées</strong>.</p></li>
<li><p>Cliquez <strong>sur OK,</strong>puis fermez et rouvrez la base de données.</p></li>
</ol>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Le paramètre **Print** de l'argument **View** imprime immédiatement l'état selon les paramètres d'imprimante actuels, sans ouvrir la boîte de dialogue **Imprimer**. Vous pouvez également utiliser l'action **OpenReport** pour ouvrir et configurer un état, puis utiliser l'action PrintOut pour l'imprimer. Par exemple, vous pouvez modifier l'état ou utiliser l'action **PrintOut** pour modifier les paramètres d'imprimante avant l'impression.

Le filtre et la condition WHERE que vous appliquez deviennent le paramètre de la propriété **Filtre** de l'état.

L'action **OuvrirEtat** équivaut à double-cliquer sur l'état dans le volet de navigation ou à cliquer avec le bouton droit sur l'état dans le volet de navigation et à choisir un affichage ou la commande **Imprimer**.

> [!TIP] 
> - Pour imprimer des états similaires pour différentes séries de données, utilisez un filtre ou une clause WHERE pour limiter les enregistrements imprimés dans l'état. Modifiez ensuite la macro pour appliquer un autre filtre ou modifiez l’argument Condition Where.
> 
> - Vous pouvez faire glisser un état depuis le volet de navigation vers une ligne d'action de macro. Ceci crée automatiquement une action **OuvrirEtat** qui ouvre l'état en mode État.

## <a name="example"></a>Exemple

L’exemple suivant montre comment utiliser l’action OpenReport pour transmettre un paramètre qui permet de filtrer un état lorsqu’il est ouvert. L’état **rptChapters** affiche les enregistrements de l’auteur spécifié en transmettant l’élément sélectionné dans la zone de liste modifiable **cboAuthors** au paramètre SelectedAuthor.

**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    OpenReport
        Report Name rptChapters
        View Report
        Filter Name
        Where Condition
        Window Mode Normal
    
    Parameters
        SelectedAuthor =[cboAuthor]
```
