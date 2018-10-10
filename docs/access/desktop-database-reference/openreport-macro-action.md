---
title: OuvrirEtat, action de macro
TOCTitle: OpenReport Macro Action
ms:assetid: cd35faf2-190d-ac48-cf59-81c1599eb764
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834462(v=office.15)
ms:contentKeyID: 48547758
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm188079
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 06828474aee961dd6df02f29c7d046805a1c764c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470223"
---
# <a name="openreport-macro-action"></a>OuvrirEtat, action de macro

**S’applique à**: Access 2013 | Office 2013

Faites appel à l'action **OuvrirEtat** pour ouvrir un état en mode Création ou Aperçu avant impression ou pour envoyer l'état directement à l'imprimante. Vous pouvez également limiter les enregistrements qui sont imprimés dans l'état.

## <a name="setting"></a>Paramètre

L'action **OuvrirEtat** possède les arguments suivants.

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
<td><p>Nom de l’état</p></td>
<td><p>Nom de l'état à ouvrir. La zone <strong>Nom de l'état</strong> de la section <strong>Arguments de l'action</strong> du volet <strong>Générateur de macro</strong> présente tous les états dans la base de données actuelle. Il s'agit d'un argument obligatoire. Si vous exécutez une macro contenant l'action OpenReport dans une base de données bibliothèque, Microsoft Access recherche d'abord l'état portant ce nom dans la base de données bibliothèque, puis dans la base de données actuelle.  </p></td>
</tr>
<tr class="even">
<td><p>Vue</p></td>
<td><p>Affichage dans lequel s'ouvre l'état. Cliquez sur <strong>Imprimer</strong> (imprime l'état immédiatement), <strong>Création</strong> ou <strong>Aperçu avant impression</strong> dans la zone <strong>Affichage</strong>. La valeur par défaut est <strong>Imprimer</strong>.  </p></td>
</tr>
<tr class="odd">
<td><p>Filter Name</p></td>
<td><p>Filtre qui limite les enregistrements de l'état. Vous pouvez entrer le nom d'une requête existante quelconque ou d'un filtre enregistré en tant que requête. La requête doit toutefois inclure tous les champs de l'état que vous ouvrez, ou sa propriété <strong>TousLesChamps</strong> doit avoir la valeur <strong>Oui</strong>.  </p></td>
</tr>
<tr class="even">
<td><p>Where Condition</p></td>
<td><p>Clause ou expression WHERE SQL valable (sans le mot WHERE) utilisée par Access pour sélectionner des enregistrements dans la table ou requête sous-jacente de l'état. Si vous sélectionnez un filtre avec l’argument nom du filtre, Access applique cette clause WHERE aux résultats du filtre. Pour ouvrir un état et limiter ses enregistrements à ceux spécifiés par la valeur d’un contrôle d’un formulaire, utilisez l’expression suivante :<br />
<strong>[</strong><em>nomchamp</em><strong>] = Forms![</strong><em>nomformulaire</em><strong>]![</strong><em>nomcontrôle formulaire</em><strong>]</strong><br />
Remplacez <em>fieldname</em> par le nom d’un champ dans la table ou requête sous-jacente du rapport que vous souhaitez ouvrir. Remplacez <em>formname</em> et <em>NomContrôle formulaire</em> par le nom du formulaire et le contrôle du formulaire qui contient la valeur à laquelle les enregistrements du rapport doivent correspondre.</p>
<p><b>Remarque</b>: la longueur maximale de l’argument Condition Where est de 255 caractères. Si vous devez entrer une clause SQL WHERE plus complexe et plus longue, utilisez la méthode <b>OpenReport</b> de l’objet <b>DoCmd</b> dans un Visual Basic pour le module d’Applications (VBA) à la place. Vous pouvez entrer des instructions de clause SQL WHERE jusqu'à 32 768 caractères dans VBA.</p>
</td>
</tr>
<tr class="odd">
<td><p>Window Mode</p></td>
<td><p>Mode dans lequel s'ouvre l'état. Cliquez sur <strong>Standard</strong>, <strong>Masqué</strong>, <strong>Icône</strong> ou <strong>Boîte de dialogue</strong> dans la zone <strong>Mode Fenêtre</strong>. La valeur par défaut est <strong>Standard</strong>.  </p>
<p><b>Remarque</b>: paramètres de l’argument Mode fenêtre certains ne s’appliquent pas à l’aide des documents à onglets. Pour activer des fenêtres superposées :
<ol>
<li><p>Cliquez sur <strong>Options</strong>.</p></li>
<li><p>Dans la boîte dialogue <strong>Options Access</strong>, cliquez sur <strong>Base de données active</strong>.</p></li>
<li><p>Dans la section <strong>Options de l'application</strong>, sous <strong>Options de la fenêtre Document</strong>, cliquez sur <strong>Fenêtres superposées</strong>.</p></li>
<li><p>Cliquez sur <strong>OK</strong>, puis fermez et rouvrez la base de données.</p></li>
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
> - Pour imprimer des états similaires pour différentes séries de données, utilisez un filtre ou une clause WHERE pour limiter les enregistrements imprimés dans l'état. Ensuite, modifiez la macro pour appliquer un autre filtre ou modifier l’argument Condition Where.
> 
> - Vous pouvez faire glisser un état depuis le volet de navigation vers une ligne d'action de macro. Ceci crée automatiquement une action **OuvrirEtat** qui ouvre l'état en mode État.

## <a name="example"></a>Exemple

L'exemple suivant montre comment utiliser l'action OpenReport pour transmettre un paramètre qui permet de filtrer un état lorsqu'il est ouvert. Le rapport **rptChapters** affiche les enregistrements de l’auteur spécifié en transmettant l’élément sélectionné dans la zone de liste déroulante **cboAuthors** pour le paramètre SelectedAuthor.

**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
