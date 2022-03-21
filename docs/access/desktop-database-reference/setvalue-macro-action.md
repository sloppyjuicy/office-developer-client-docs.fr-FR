---
title: Action de macro SetValue
TOCTitle: SetValue macro action
ms:assetid: a08be0c1-a053-45f9-b4ae-709fedc58e8b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820771(v=office.15)
ms:contentKeyID: 48546712
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 9ac89c53c0e326e430634f9837ba85f2e3bcca54
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63631950"
---
# <a name="setvalue-macro-action"></a>Action de macro SetValue

**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser l'action **DéfinirValeur** pour définir la valeur d'un champ, d'un contrôle ou d'une propriété Microsoft Access dans un formulaire, un formulaire feuille de données ou un état.

> [!NOTE]
> - Vous ne pouvez pas utiliser l’action **DéfinirValeur** pour définir la valeur d’une propriété Access qui renvoie un objet.
> - Cette action ne sera pas autorisée si la base de données n’est pas approuvée. 

## <a name="setting"></a>Setting

L’action **DéfinirValeur** utilise les arguments suivants.

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
<td><p><strong>Item</strong></p></td>
<td><p>Nom du champ, du contrôle ou de la propriété dont vous souhaitez définir la valeur. Entrez le nom du champ, du contrôle ou de la propriété dans la zone <strong>Élément</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Vous devez utiliser la syntaxe complète pour faire référence à cet élément, telle que <em>nom_contrôle</em> (pour un contrôle dans le formulaire ou l’état à partir duquel la macro a été appelée) ou <strong>Forms</strong>!<em>nom_formulaire</em>!<em>nom_contrôle</em>. Cet argument est obligatoire.</p></td>
</tr>
<tr class="even">
<td><p><strong>Expression</strong></p></td>
<td><p>Expression utilisée par Access pour définir la valeur de cet élément. Vous devez toujours utiliser la syntaxe complète pour faire référence à des objets dans l’expression. Par exemple, pour augmenter la valeur d’un contrôle Salaire dans un formulaire Employés de 10 pour cent, utilisez Forms!Employees!Salary*1.1.. Il s’agit d’un argument obligatoire.</p><p><strong>REMARQUE</strong> : Vous ne devez pas utiliser le signe égal (=) avant l'expression dans cet argument. Si vous le faites, Access évalue l'expression et utilise ensuite cette valeur comme expression dans cet argument. Cela peut produire des résultats inattendus si l'expression est une chaîne de caractères.</p>
<p>Par exemple, si vous tapez <strong>=&quot;Chaîne1&quot;</strong> pour cet argument, Access évalue d’abord l’expression comme Chaîne1. Il utilise ensuite Chaîne1 comme expression dans cet argument, s’attendant à trouver un contrôle ou une propriété nommé Chaîne1 dans le formulaire ou l’état qui a appelé la macro.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Dans une base de données Access (.mdb ou .accdb), cliquez sur le bouton **Générer** pour utiliser le Générateur d'expression et créer une expression pour l'un de ces arguments.

## <a name="remarks"></a>Remarques

Vous pouvez utiliser cette action pour définir une valeur pour un champ ou un contrôle dans un formulaire, un formulaire feuille de données ou un état. Vous pouvez également définir la valeur de presque toutes les propriétés de contrôle, de formulaire et d’état dans n’importe quel affichage. Pour déterminer si une propriété spécifique peut être configurée à l’aide d’une macro et les affichages pouvant être définis, consultez la rubrique d’aide relative à cette propriété dans Visual Basic Editor.

Vous pouvez également définir la valeur d’un champ dans la table sous-jacente d’un formulaire, même si le formulaire ne contient pas de contrôle lié au champ. Utilisez la syntaxe **Formulaires**\!*nomformulaire*\!*nomchamp* dans la zone **Élément** pour définir la valeur d’un tel champ. Vous pouvez également faire référence à un champ dans la table sous-jacente d’un rapport en utilisant la syntaxe **Reports**\!*nomrapport*\!*nomchamp*, mais il doit y avoir un contrôle dans le rapport lié à ce champ, ou le champ doit être référencé dans un contrôle calculé sur le rapport.

Si vous définissez la valeur d'un contrôle dans un formulaire, l'action **DéfinirValeur** ne déclenche pas les règles de validation au niveau du formulaire du contrôle, mais elle déclenche les règles de validation au niveau de la table du champ sous-jacent si le contrôle est un contrôle lié. L'action **DéfinirValeur** déclenche également le recalcul, mais ce dernier peut ne pas avoir lieu immédiatement. Pour déclencher la mise à jour immédiate et forcer l'exécution du recalcul, utilisez l'action **RedessinerObjet**. La valeur que vous définissez dans un contrôle à l'aide de l'action **DéfinirValeur** est également non affectée par un masque de saisie défini dans la propriété **InputMask** du contrôle ou du champ sous-jacent.

Pour modifier la valeur d'un contrôle, vous pouvez utiliser l'action **DéfinirValeur** dans une macro spécifiée par la propriété de type événement **AfterUpdate** du contrôle. Toutefois, vous ne pouvez pas utiliser l'action **DéfinirValeur** dans une macro spécifiée par la propriété de type événement **BeforeUpdate** d'un contrôle pour modifier la valeur du contrôle (bien que vous puissiez utiliser l'action **DéfinirValeur** pour modifier la valeur d'autres contrôles). Vous pouvez également utiliser l'action **DéfinirValeur** dans une macro spécifiée par la propriété **AvantMAJ** ou **AprèsMAJ** d'un formulaire pour modifier la valeur de tous les contrôles de l'enregistrement actif.

> [!NOTE]
> Vous ne pouvez pas utiliser l’action **DéfinirValeur** pour définir la valeur des contrôles suivants :
> - Les contrôles dépendants et les contrôles calculés dans des états.
> - Les contrôles calculés dans des formulaires.

> [!TIP]
> Vous pouvez utiliser l’action **DéfinirValeur** pour masquer ou afficher un formulaire en mode Formulaire. Entrez **Formulaires**!*nomformulaire***.Visible** dans la zone **Élément**, et **Non** ou **Oui** dans la zone **Expression**. La définition de la propriété **Visible** d’un formulaire modal sur **Non** masque le formulaire et le rend non modal. La définition de la propriété sur **Oui** affiche le formulaire et le rend à nouveau modal.

La modification de la valeur ou l'ajout des nouvelles données dans un contrôle à l'aide de l'action **DéfinirValeur** dans une macro ne déclenche pas des événements tels que **AvantMAJ**, **AvantInsertion** ou **Modifier** qui se produisent lorsque vous modifiez ou entrez des données dans ces contrôles dans l'interface utilisateur. Ces événements ne se produisent pas non plus si vous définissez la valeur du contrôle à l'aide d'un module Visual Basic pour Applications (VBA).

Cette action n’est pas disponible dans un module VBA. Définissez la valeur directement en langage VBA.

## <a name="example"></a>Exemple

**Définissez la valeur d’un contrôle en utilisant une macro**

La macro suivante ouvre le formulaire Ajouter des produits à partir d'un bouton dans le formulaire Fournisseurs. Elle présente l'utilisation des actions **Écho**, **FermerFenêtre**, **OuvrirFormulaire**, **DéfinirValeur** et **AtteindreContrôle**. L'action **DéfinirValeur** définit le contrôle N° fournisseur dans le formulaire Produits sur le fournisseur actif dans le formulaire Fournisseurs. L'action **AtteindreContrôle** déplace ensuite le focus vers le champ N° catégorie, où vous pouvez commencer à entrer des données pour le nouveau produit. Cette macro doit être associée au bouton Ajouter des produits dans le formulaire Fournisseurs.

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Action</p></th>
<th><p>Arguments : Paramètre</p></th>
<th><p>Commentaire</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Écho sur</strong>: <strong>Non</strong></p></td>
<td><p>Arrêter l’actualisation de l’écran pendant l’exécution de la macro.</p></td>
</tr>
<tr class="even">
<td><p><strong>FermerFenêtre</strong></p></td>
<td><p><strong>Type d’objet</strong> : <strong>FormulaireNom de l’objet</strong> : Liste des produits <strong>Enregistrer</strong> : <strong>Non</strong></p></td>
<td><p>Fermer le formulaire Liste des produits.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OuvrirFormulaire</strong></p></td>
<td><p><strong>Nom du formulaire</strong> : Produits <strong>Affichage</strong> : <strong>FormulaireMode de données</strong> : <strong>AjouterMode Fenêtre</strong> :<strong>Normal</strong></p></td>
<td><p>Ouvrir le formulaire Produits.</p></td>
</tr>
<tr class="even">
<td><p><strong>DéfinirValeur</strong></p></td>
<td><p><strong>Élément</strong>: [Forms]![Produits]! [N° fournisseur] <strong>Expression</strong>: N° fournisseur    </p></td>
<td><p>Définissez le contrôle N° fournisseur sur le fournisseur actuel dans le formulaire Fournisseurs.</p></td>
</tr>
<tr class="odd">
<td><p><strong>AtteindreContrôle</strong></p></td>
<td><p><strong>Nom du contrôle</strong>: N° catégorie</p></td>
<td><p>Accédez au contrôle N° catégorie.</p></td>
</tr>
</tbody>
</table>

