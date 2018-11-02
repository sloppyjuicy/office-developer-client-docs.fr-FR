---
title: SetValue, action de macro
TOCTitle: SetValue macro action
ms:assetid: a08be0c1-a053-45f9-b4ae-709fedc58e8b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820771(v=office.15)
ms:contentKeyID: 48546712
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6f407c5da2ca669025d5aec47685e6eb9732c72c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927101"
---
# <a name="setvalue-macro-action"></a>SetValue, action de macro


**S’applique à**: Access 2013, Office 2013


Vous pouvez utiliser l'action **DéfinirValeur** pour définir la valeur d'un champ, d'un contrôle ou d'une propriété Microsoft Access dans un formulaire, un formulaire feuille de données ou un état.


> [!NOTE]
> <P>[!REMARQUE] Vous ne pouvez pas utiliser l'action <STRONG>DéfinirValeur</STRONG> pour définir la valeur d'une propriété Access qui renvoie un objet.</P>




> [!NOTE]
> <P>[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.</P>



## <a name="setting"></a>Paramètre

L'action **DéfinirValeur** utilise les arguments suivants.

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
<td><p><strong>Item</strong></p></td>
<td><p>Nom du champ, du contrôle ou de la propriété dont vous souhaitez définir la valeur. Entrez le nom du champ, du contrôle ou de la propriété dans la zone <strong>Élément</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Vous devez utiliser la syntaxe complète pour faire référence à cet élément, telle que <em>nom_contrôle</em> (pour un contrôle dans le formulaire ou l’état à partir duquel la macro a été appelée) ou <strong>Forms</strong>!<em>nom_formulaire</em>!<em>nom_contrôle</em>. Cet argument est obligatoire.</p></td>
</tr>
<tr class="even">
<td><p><strong>Expression</strong></p></td>
<td><p>Expression utilisée par Access pour définir la valeur de cet élément. Vous devez toujours utiliser la syntaxe complète pour faire référence à des objets dans l’expression. Par exemple, pour augmenter la valeur d’un contrôle Salaire dans un formulaire Employés de 10 pour cent, utilisez Forms!Employees!Salary*1.1.. Il s’agit d’un argument obligatoire.</p>

> [!NOTE]
> <P>Vous ne devez pas utiliser un signe égal (<STRONG>=</STRONG>) avant l’expression dans cet argument. Si vous le faites, Access évalue l’expression, puis utilise cette valeur comme expression dans cet argument. Cela peut produire des résultats inattendus si l’expression est une chaîne.</P>


<p>Par exemple, si vous tapez <strong> = &quot;chaîne1&quot; </strong> à cet argument, Access évalue l’expression comme chaîne1 d’abord. Il utilise ensuite Chaîne1 comme expression dans cet argument, s’attendant à trouver un contrôle ou la propriété nommé Chaîne1 dans le formulaire ou l’état qui a appelé la macro.</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>[!REMARQUE] Dans une base de données Access (.mdb ou .accdb), cliquez sur le bouton <STRONG>Générer</STRONG> pour utiliser le Générateur d'expression et créer une expression pour l'un de ces arguments.</P>



## <a name="remarks"></a>Remarques

Vous pouvez utiliser cette action pour définir une valeur pour un champ ou un contrôle dans un formulaire, un formulaire feuille de données ou un état. Vous pouvez également définir la valeur de presque toutes les propriétés de contrôle, de formulaire et d'état dans n'importe quel affichage. Pour déterminer si une propriété spécifique peut être configurée à l'aide d'une macro et les affichages pouvant être définis, consultez la rubrique d'aide relative à cette propriété dans Visual Basic Editor.

Vous pouvez également définir la valeur d'un champ dans la table sous-jacente d'un formulaire, même si le formulaire ne contient pas de contrôle lié au champ. Utilisez la syntaxe **Forms**\!*formname*\!*fieldname* dans la zone **élément** pour définir la valeur pour ce champ. Vous pouvez également faire référence à un champ de table sous-jacente d’un état à l’aide de la syntaxe de **rapports**\!*reportname*\!*fieldname*, mais il doit exister un contrôle dépendant de ce champ ou le champ doit être référencé en une contrôle calculé dans l’état.

Si vous définissez la valeur d'un contrôle dans un formulaire, l'action **DéfinirValeur** ne déclenche pas les règles de validation au niveau du formulaire du contrôle, mais elle déclenche les règles de validation au niveau de la table du champ sous-jacent si le contrôle est un contrôle lié. L'action **DéfinirValeur** déclenche également le recalcul, mais ce dernier peut ne pas avoir lieu immédiatement. Pour déclencher la mise à jour immédiate et forcer l'exécution du recalcul, utilisez l'action **RedessinerObjet**. La valeur que vous définissez dans un contrôle à l'aide de l'action **DéfinirValeur** est également non affectée par un masque de saisie défini dans la propriété **InputMask** du contrôle ou du champ sous-jacent.

Pour modifier la valeur d'un contrôle, vous pouvez utiliser l'action **DéfinirValeur** dans une macro spécifiée par la propriété de type événement **AfterUpdate** du contrôle. Toutefois, vous ne pouvez pas utiliser l'action **DéfinirValeur** dans une macro spécifiée par la propriété de type événement **BeforeUpdate** d'un contrôle pour modifier la valeur du contrôle (bien que vous puissiez utiliser l'action **DéfinirValeur** pour modifier la valeur d'autres contrôles). Vous pouvez également utiliser l'action **DéfinirValeur** dans une macro spécifiée par la propriété **AvantMAJ** ou **AprèsMAJ** d'un formulaire pour modifier la valeur de tous les contrôles de l'enregistrement actif.


> [!NOTE]
> <P>Vous ne pouvez pas utiliser l’action <STRONG>DéfinirValeur</STRONG> pour définir la valeur des contrôles suivants :</P>
> <UL>
> <LI>
> <P>Les contrôles dépendants et les contrôles calculés dans des états.</P>
> <LI>
> <P>Les contrôles calculés dans des formulaires.</P></LI></UL>




> [!TIP]
> <P>Vous pouvez utiliser l’action <STRONG>DéfinirValeur</STRONG> pour masquer ou afficher un formulaire en mode Formulaire. Entrez <STRONG>Forms</STRONG>!<EM>nom_formulaire</EM><STRONG>.Visible</STRONG> dans la zone <STRONG>Élément</STRONG>, et <STRONG>Non</STRONG> ou <STRONG>Oui</STRONG> dans la zone <STRONG>Expression</STRONG>. La définition de la propriété <STRONG>Visible</STRONG> d’un formulaire modal sur <STRONG>Non</STRONG> masque le formulaire et le rend non modal. La définition de la propriété sur <STRONG>Oui</STRONG> affiche le formulaire et le rend à nouveau modal.</P>



La modification de la valeur ou l'ajout des nouvelles données dans un contrôle à l'aide de l'action **DéfinirValeur** dans une macro ne déclenche pas des événements tels que **AvantMAJ**, **AvantInsertion** ou **Modifier** qui se produisent lorsque vous modifiez ou entrez des données dans ces contrôles dans l'interface utilisateur. Ces événements ne se produisent pas non plus si vous définissez la valeur du contrôle à l'aide d'un module Visual Basic pour Applications (VBA).

Cette action n'est pas disponible dans un module VBA. Définissez la valeur directement en langage VBA.

## <a name="example"></a>Exemple

**Définissez la valeur d'un contrôle en utilisant une macro**

La macro suivante ouvre le formulaire Ajouter des produits à partir d'un bouton dans le formulaire Fournisseurs. Elle présente l'utilisation des actions **Écho**, **FermerFenêtre**, **OuvrirFormulaire**, **DéfinirValeur** et **AtteindreContrôle**. L'action **DéfinirValeur** définit le contrôle N° fournisseur dans le formulaire Produits sur le fournisseur actif dans le formulaire Fournisseurs. L'action **AtteindreContrôle** déplace ensuite le focus vers le champ N° catégorie, où vous pouvez commencer à entrer des données pour le nouveau produit. Cette macro doit être associée au bouton Ajouter des produits dans le formulaire Fournisseurs.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
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
<td><p><strong>Écho</strong></p></td>
<td><p><strong>Écho sur</strong>: <strong>Non</strong></p></td>
<td><p>Arrêter l'actualisation de l'écran pendant l'exécution de la macro.</p></td>
</tr>
<tr class="even">
<td><p><strong>FermerFenêtre</strong></p></td>
<td><p><strong>Type d’objet</strong>: <strong>FormObject nom</strong>: produit liste <strong>Enregistrer</strong>: <strong>non</strong></p></td>
<td><p>Fermer le formulaire Liste des produits.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OuvrirFormulaire</strong></p></td>
<td><p><strong>Nom du formulaire</strong>: <strong>affichage</strong>des produits : <strong>Mode FormData</strong>: <strong>Mode fenêtre Ajouter</strong>: <strong>Normal</strong></p></td>
<td><p>Ouvrir le formulaire Produits.</p></td>
</tr>
<tr class="even">
<td><p><strong>DéfinirValeur</strong></p></td>
<td><p><strong>Élément</strong>: [Forms]![Produits]! [N° fournisseur] <strong>Expression</strong>: N° fournisseur  </p></td>
<td><p>Définissez le contrôle N° fournisseur sur le fournisseur actuel dans le formulaire Fournisseurs.</p></td>
</tr>
<tr class="odd">
<td><p><strong>AtteindreContrôle</strong></p></td>
<td><p><strong>Nom du contrôle</strong>: N° catégorie</p></td>
<td><p>Accédez au contrôle N° catégorie.</p></td>
</tr>
</tbody>
</table>

