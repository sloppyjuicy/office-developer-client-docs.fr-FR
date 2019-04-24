---
title: ECHO, action de macro (référence de base de données de bureau Access)
TOCTitle: Echo macro action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d536ed47c780b7f9f1675a9879e86aeff80b67f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293622"
---
# <a name="echo-macro-action"></a>Echo, action de macro

**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser l'action **echo** pour spécifier si l'écho est activé. Par exemple, vous pouvez utiliser cette action pour masquer ou afficher les résultats d'une macro pendant son exécution.

## <a name="setting"></a>Setting

> [!NOTE]
> Cette action ne sera pas autorisée si la base de données n’est pas approuvée.

L'action **echo** possède les arguments suivants.

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
<td><p><strong>Écho activé</strong></p></td>
<td><p>Cliquez sur <strong>Oui</strong> (activer l'écho) ou <strong>non</strong> (désactiver l'écho) dans la zone <strong>écho actif</strong> de la section arguments de l' <strong>action</strong> du volet générateur de macro. La valeur par défaut est <strong>Oui</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Texte de la barre d’état</strong></p></td>
<td><p>Texte à afficher dans la barre d'État lorsque l'écho est désactivé. Par exemple, lorsque l'écho est désactivé, la barre d'État peut &quot;afficher la macro est en cours d'exécution.&quot;</p></td>
</tr>
</tbody>
</table>


Lors de l'exécution d'une macro, la mise à jour de l'écran affiche souvent des informations qui ne sont pas essentielles au fonctionnement de la macro. Lorsque vous définissez l'argument **écho actif** sur **non**, la macro s'exécute sans mettre à jour l'écran. À la fin de l'exécution de la macro, Access réactive automatiquement l'écho et redessine la fenêtre. Le paramètre aucun de l'argument **écho actif** n'a **aucune** incidence sur la fonctionnalité de la macro ou de ses résultats.

L'action **écho** ne supprime pas l'affichage des boîtes de dialogue modales, telles que les messages d'erreur ou les formulaires indépendants, tels que les feuilles de propriétés. Vous pouvez utiliser des boîtes de dialogue et des formulaires contextuels pour collecter ou afficher des informations, même si l'écho est désactivé. Pour supprimer toutes les boîtes de dialogue ou de message, à l'exception des boîtes de message d'erreur et des boîtes de dialogue qui demandent à l'utilisateur d'entrer des informations, utilisez l'action **avertissements** .

Vous pouvez exécuter l'action **echo** plusieurs fois dans une macro. Cela vous permet de modifier le texte de la barre d'État pendant l'exécution de la macro.

Si vous désactivez l'écho, vous pouvez utiliser l'action **afficherpointeursablier** pour transformer le pointeur de la souris en icône de sablier (ou quelle icône de pointeur de souris vous avez définie pour «occupé») pour fournir une indication visuelle de l'exécution de la macro.

Pour exécuter l'action **echo** dans un module Visual Basic pour applications (VBA), utilisez la méthode **echo** de l'objet **DoCmd** .

## <a name="examples"></a>Exemples

### <a name="set-the-value-of-a-control-by-using-a-macro"></a>Définissez la valeur d’un contrôle en utilisant une macro

La macro suivante ouvre le formulaire Ajouter des produits à partir d’un bouton dans le formulaire Fournisseurs. Elle présente l’utilisation des actions **Écho**, **FermerFenêtre**, **OuvrirFormulaire**, **DéfinirValeur** et **AtteindreContrôle**. L’action **DéfinirValeur** définit le contrôle N° fournisseur dans le formulaire Produits sur le fournisseur actif dans le formulaire Fournisseurs. L’action **AtteindreContrôle** déplace ensuite le focus vers le champ N° catégorie, où vous pouvez commencer à entrer des données pour le nouveau produit. Cette macro doit être associée au bouton Ajouter des produits dans le formulaire Fournisseurs.

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
<td><p><strong>Fermerfenêtre</strong></p></td>
<td><p><strong>Type d'objet</strong>: <strong>Formulairenom nom</strong>: liste des produits <strong>Enregistrer</strong>: <strong>non</strong></p></td>
<td><p>Fermer le formulaire Liste des produits.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Nom du formulaire</strong>: <strong>produits affichage</strong>: <strong>formulairemode mode</strong> <strong>ajoutermode fenêtre</strong>: <strong>normal</strong></p></td>
<td><p>Ouvrir le formulaire Produits.</p></td>
</tr>
<tr class="even">
<td><p><strong>SetValue</strong></p></td>
<td><p><strong>Élément</strong>: [Forms]![Produits]![N° fournisseur] <strong>Expression</strong>: N° fournisseur</p></td>
<td><p>Définissez le contrôle N° fournisseur sur le fournisseur actuel dans le formulaire Fournisseurs.</p></td>
</tr>
<tr class="odd">
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nom du contrôle</strong>: N° catégorie</p></td>
<td><p>Accéder au contrôle N° catégorie.</p></td>
</tr>
</tbody>
</table>


### <a name="synchronize-forms-by-using-a-macro"></a>Synchroniser des formulaires à l’aide d’une macro

La macro suivante ouvre le formulaire liste des produits dans le coin inférieur droit du formulaire fournisseurs, en affichant les produits du fournisseur actuel. Elle présente l'utilisation des actions **Écho**, **ZoneMessage**, **AtteindreContrôle**, **ArrêtMacro**, **OuvrirFormulaire** et **DéplacerEtDimensionnerFenêtre**. Elle décrit également l'utilisation d'une expression conditionnelle avec les actions **ZoneMessage**, **AtteindreContrôle**, et **ArrêtMacro**. Cette macro doit être associée au bouton Consulter les produits dans le formulaire Fournisseurs.

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
<td><p><strong>Écho</strong></p></td>
<td><p><strong>Écho sur</strong>: <strong>Non</strong></p></td>
<td><p>Arrêter l'actualisation de l'écran pendant l'exécution de la macro.</p></td>
</tr>
<tr class="even">
<td><p>IsNull ([ID fournisseur])</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: Passez à l'enregistrement du fournisseur dont vous voulez voir les produits, puis cliquez à nouveau sur le bouton Consulter les produits. <strong>Bip</strong>: <strong>YesType</strong>: <strong>aucuntitre</strong>: sélectionnez un fournisseur</p></td>
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
<td><p><strong>Nom du formulaire</strong>: liste des produits <strong>affichage</strong>: <strong>nom donnéesnom du filtre</strong>: <strong>condition WHERE</strong>: [Réf fournisseur] = [Forms]! [Fournisseurs]! Fournisseur <strong>Mode données</strong>: <strong>mode lecture seulemode fenêtre</strong>: <strong>normal</strong></p></td>
<td><p>Ouvrir le formulaire Liste de produits et afficher les produits du fournisseur actuel.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>Déplaceretdimensionnerfenêtre</strong></p></td>
<td><p><strong>droite</strong>: 0,7799&quot; <strong>bas</strong>: 1,8&quot;</p></td>
<td><p>Positionnez le formulaire Liste de produits dans le coin inférieur droit du formulaire Fournisseurs.</p></td>
</tr>
</tbody>
</table>

