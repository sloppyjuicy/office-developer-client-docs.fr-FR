---
title: OpenForm, action de macro
TOCTitle: OpenForm macro action
ms:assetid: c519a9d7-99d4-4765-ad96-59c3fe1be9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823095(v=office.15)
ms:contentKeyID: 48547604
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c45f71ed079badfaa6843b5a12734bb82a2e553a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611909"
---
# <a name="openform-macro-action"></a>OpenForm, action de macro

**S’applique à** : Access 2013, Office 2013

Faites appel à l'action **OuvrirFormulaire** pour ouvrir un formulaire en mode Formulaire, Création, Aperçu avant impression ou Feuille de données. Vous pouvez sélectionner des modes d'affichage et de saisie des données pour le formulaire et limiter les enregistrements affichés par celui-ci.

## <a name="setting"></a>Paramètre

L’action **OuvrirFormulaire** utilise les arguments suivants.

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
<td><p><strong>Nom du formulaire</strong></p></td>
<td><p>Nom du formulaire à ouvrir. La zone <strong>Nom du formulaire</strong> dans la section <strong>Arguments de l'action</strong> du volet Générateur de macro présente tous les formulaires dans la base de données actuelle. Il s'agit d'un argument obligatoire. Si vous exécutez une macro contenant l'action <strong>OuvrirFormulaire</strong> dans une base de données bibliothèque, Microsoft Access recherche d'abord le formulaire portant ce nom dans la base de données bibliothèque, puis dans la base de données actuelle.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Affichage</strong></p></td>
<td><p>Affichage dans lequel le formulaire s'ouvre. Cliquez sur <strong>Formulaire</strong>, <strong>Création</strong>, <strong>Aperçu avant impression</strong>, <strong>Feuille de données</strong>, <strong>Tableau croisé dynamique</strong> ou <strong>Graphique croisé dynamique</strong> dans la zone <strong>Affichage</strong>. La valeur par défaut est <strong>Formulaire</strong>.  </p><p><strong>REMARQUE</strong>: le paramètre <STRONG>d’argument</STRONG> Affichage remplace les paramètres des propriétés <STRONG>DefaultView</STRONG> et <STRONG>ViewsAllowed du</STRONG> formulaire. For example, if a form's <STRONG>ViewsAllowed</STRONG> property is set to <STRONG>Datasheet</STRONG>, you can still use the <STRONG>OpenForm</STRONG> action to open the form in Form view.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Nom du filtre</strong></p></td>
<td><p>Filtre qui limite ou trie les enregistrements du formulaire. Vous pouvez entrer le nom d'une requête existante ou d'un filtre enregistré en tant que requête. La requête doit toutefois inclure tous les champs du formulaire que vous ouvrez, ou sa propriété <strong>OutputAllFields</strong> doit avoir la valeur <strong>Oui</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Condition Where</strong></p></td>
<td><p>Clause ou expression WHERE SQL valable (sans le mot WHERE) utilisée par Access pour sélectionner des enregistrements dans la table ou requête sous-jacente du formulaire. Si vous sélectionnez un filtre avec l'argument <strong>Filter Name</strong>, Access applique cette clause WHERE aux résultats du filtre. Pour ouvrir un formulaire et limiter ses enregistrements à ceux spécifiés par la valeur d’un contrôle dans un autre formulaire, utilisez l’expression suivante <strong>: [</strong><em>nom_champ</em><strong>] = Formulaires![</strong> <em>formname</em><strong>]! [</strong><em>nom_contrôle sur</em>un autre formulaire<strong>]</strong> Remplacez <em>nom_champ</em> par le nom d’un champ dans la table ou la requête sous-jacente du formulaire que vous souhaitez ouvrir. Remplacez <em>nom_formulaire</em> et <em>nom_contrôle</em> dans l’autre formulaire par le nom de l’autre formulaire et du contrôle dans l’autre formulaire qui contient la valeur avec laquelle vous souhaitez que les enregistrements du premier formulaire correspondent.</p><p><strong>REMARQUE</strong>: la longueur maximale de l’argument <STRONG>Condition Where</STRONG> est de 255 caractères. If you need to enter a more complex SQL WHERE clause longer than this, use the <STRONG>OpenForm</STRONG> method of the <STRONG>DoCmd</STRONG> object in a Visual Basic for Applications (VBA) module instead. You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Mode Données</strong></p></td>
<td><p>Mode de saisie de données du formulaire. S'applique uniquement aux formulaires ouverts en mode Formulaire ou Feuille de données. Cliquez sur <strong>Ajouter</strong> (l'utilisateur ne peut pas modifier les enregistrements existants, mais peut en ajouter de nouveaux), <strong>Modifier</strong> (l'utilisateur peut modifier les enregistrements existants et en ajouter de nouveaux) ou <strong>Lecture seule</strong> (l'utilisateur peut uniquement consulter les enregistrements). La valeur par défaut est <strong>Modifier</strong>. <strong>Notes</strong></p>
<ul>
<li><p>Le paramètre d'argument <strong>Mode Données</strong> remplace les paramètres des propriétés <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong> et <strong>DataEntry</strong> du formulaire. Par exemple, si la propriété <strong>AllowEdits</strong> d'un formulaire est définie sur <strong>Non</strong>, vous pouvez toujours utiliser l'action <strong>OuvrirFormulaire</strong> pour ouvrir le formulaire en mode Édition.  </p></li>
<li><p>Si vous laissez cet argument vide, Access ouvre le formulaire dans le mode d'entrée de données défini par les propriétés <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong> et <strong>DataEntry</strong> du formulaire.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Mode Fenêtre</strong></p></td>
<td><p>Mode de fenêtre dans laquelle le formulaire s'ouvre. Cliquez sur <strong>Normal</strong> (le formulaire s'ouvre dans le mode défini par ses propriétés), <strong>Masqué</strong> (le formulaire est masqué), <strong>Icône</strong> (le formulaire s'ouvre à la taille réduite sous la forme d'une barre de titre en bas de l'écran) ou <strong>Boîte de dialogue</strong> (les propriétés <strong>Modal</strong> et <strong>PopUp</strong> du formulaire sont définies sur <strong>Oui</strong>). La valeur par défaut est <strong>Normal</strong>.  </p><p><strong>REMARQUE</strong>: certains paramètres <STRONG>d’argument</STRONG> du mode Fenêtre ne s’appliquent pas lors de l’utilisation de documents à onglets. Pour passer à des fenêtres superposées :</p>
<ol>
<li><p>Cliquez sur l’onglet Fichier, puis sur <strong>Options.</strong></p></li>
<li><p>Dans la boîte dialogue <strong>Options Access</strong>, cliquez sur <strong>Base de données active</strong>.</p></li>
<li><p>Dans la section <strong>Options de l’application</strong>, sous <strong>Options de la fenêtre Document</strong>, cliquez sur <strong>Fenêtres superposées</strong>.</p></li>
<li><p>Cliquez sur <strong>OK</strong>, puis fermez et rouvrez la base de données.</p></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Cette action équivaut à double-cliquer sur un formulaire dans le volet de navigation ou à cliquer avec le bouton droit sur le formulaire dans le volet de navigation et à choisir un affichage.

Un formulaire peut être modal (il doit être fermé ou masqué avant que l'utilisateur puisse effectuer une autre action) ou non modal (l'utilisateur peut accéder à d'autres fenêtres lorsque le formulaire est ouvert). Il peut également être contextuel (un formulaire utilisé pour collecter ou afficher des informations qui reste au-dessus des autres fenêtres Access). Vous définissez les propriétés **Modal** et **PopUp** lorsque vous créez le formulaire. Si vous utilisez **Normal** pour l'argument **Mode fenêtre**, le formulaire s'ouvre dans le mode spécifié par les paramètres de ces propriétés. Si vous utilisez **Boîte de dialogue** pour l'argument **Mode fenêtre**, ces propriétés sont définies sur **Oui**. Un formulaire ouvert masqué ou sous forme d'icône retourne au mode spécifié par ses paramètres de propriété lorsque vous l'affichez ou le restaurez.

Lorsque vous ouvrez un formulaire avec l'argument **Mode fenêtre** défini sur **Boîte de dialogue**, Access suspend la macro jusqu'à ce que le formulaire soit fermé ou masqué. Vous pouvez masquer un formulaire en définissant sa propriété **Visible** sur **Non** à l'aide de l'action **DéfinirValeur**.

> [!TIP]
> [!CONSEIL] Vous pouvez sélectionner un formulaire dans le volet de navigation et le faire glisser vers une ligne d'action de macro. Ceci crée automatiquement une action **OuvrirFonction** qui ouvre le formulaire en mode Formulaire.

Le filtre et la condition WHERE que vous appliquez deviennent les paramètres de la propriété **Filter** du formulaire.

## <a name="examples"></a>Exemples

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
<td><p>Accéder au contrôle N° catégorie.</p></td>
</tr>
</tbody>
</table>


La macro suivante ouvre un formulaire de liste de produits dans le coin inférieur droit du formulaire Fournisseurs, affichant les produits du fournisseur actuel. Elle présente l'utilisation des actions **Écho**, **ZoneMessage**, **AtteindreContrôle**, **ArrêtMacro**, **OuvrirFormulaire** et **DéplacerEtDimensionnerFenêtre**. Elle décrit également l'utilisation d'une expression conditionnelle avec les actions **ZoneMessage**, **AtteindreContrôle**, et **ArrêtMacro**. Cette macro doit être associée au bouton Consulter les produits dans le formulaire Fournisseurs.

**Synchroniser des formulaires à l'aide d'une macro**

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condition</p></th>
<th><p>Action</p></th>
<th><p>Arguments : Paramètre</p></th>
<th><p>Commentaire</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Écho sur</strong>: <strong>Non</strong></p></td>
<td><p>Arrêter l’actualisation de l’écran pendant l’exécution de la macro.</p></td>
</tr>
<tr class="even">
<td><p>IsNull([SupplierID])</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: Passez à l'enregistrement du fournisseur dont vous voulez voir les produits, puis cliquez à nouveau sur le bouton Consulter les produits. <strong>Bip</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: sélectionner un fournisseur</p></td>
<td><p>S'il n'existe aucun fournisseur actif dans le formulaire Fournisseurs, afficher un message.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nom du contrôle</strong>: NomSociété</p></td>
<td><p>Déplacer le focus sur le contrôle NomSociété.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>Arrêter la macro.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Nom du formulaire</strong>: Affichage de la liste <strong>des</strong>produits : <strong>Nom DeFiltre</strong>DeFichier : <strong>Condition where</strong>: [SupplierID] = [Forms]! [Fournisseurs]! [SupplierID] <strong>Mode données</strong>: <strong>mode Lecture seule :</strong> <strong>Normal</strong></p></td>
<td><p>Ouvrir le formulaire Liste de produits et afficher les produits du fournisseur actuel.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>MoveAndSizeWindow</strong></p></td>
<td><p><strong>Droite</strong>: 0,7799 &quot; <strong>Bas</strong>: 1,8&quot;</p></td>
<td><p>Positionnez le formulaire Liste de produits dans le coin inférieur droit du formulaire Fournisseurs.</p></td>
</tr>
</tbody>
</table>

