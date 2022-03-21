---
title: Écho, action de macro (référence de base de données de bureau Access)
TOCTitle: Echo macro action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 85e1bd5a5def9ab9701f250d053f138369380f57
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63632916"
---
# <a name="echo-macro-action"></a>Echo, action de macro

**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser l’action **Écho** pour spécifier si l’écho est allumé. Par exemple, vous pouvez utiliser cette action pour masquer ou afficher les résultats d’une macro pendant qu’elle s’exécute.

## <a name="setting"></a>Paramètres

> [!NOTE]
> Cette action ne sera pas autorisée si la base de données n’est pas approuvée.

**L’action Écho** a les arguments suivants.

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
<td><p><strong>Écho sur</strong></p></td>
<td><p>Cliquez <strong>sur Oui</strong> (activer l’écho) ou <strong>Non (désactiver</strong> l’écho<strong></strong>) dans la zone Écho sur dans la section <strong>Arguments de l’action</strong> du volet Générateur de macro. La valeur par défaut est <strong>Oui</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Texte de la barre d’état</strong></p></td>
<td><p>Texte à afficher dans la barre d’état lorsque l’écho est désactivé. Par exemple, lorsque l’écho est désactivé, la barre d’état peut afficher &quot;la macro en cours d’exécution.&quot;</p></td>
</tr>
</tbody>
</table>


Lorsqu’une macro s’exécute, la mise à jour de l’écran affiche souvent des informations qui ne sont pas essentielles au fonctionnement de la macro. Lorsque vous définissez **l’argument Écho sur** **non**, la macro s’exécute sans mettre à jour l’écran. À la fin de la macro, Access réessaie automatiquement l’écho et réessaie la fenêtre. Le **paramètre Non** de l’argument **Écho sur** n’affecte pas la fonctionnalité de la macro ou ses résultats.

**L’action Écho** ne supprime pas l’affichage des boîtes de dialogue modales, telles que les messages d’erreur, ou les formulaires de fenêtre publicitaire, tels que les feuilles de propriétés. Vous pouvez utiliser des boîtes de dialogue et des formulaires pop-up pour collecter ou afficher des informations, même si l’écho est désactivé. Pour supprimer tous les messages ou boîtes de dialogue, à l’exception des boîtes de dialogue et des boîtes de dialogue d’erreur qui exigent que l’utilisateur entre des informations, utilisez l’action **DéfinirWarnings** .

Vous pouvez exécuter l’action **Écho** plusieurs fois dans une macro. Cela vous permet de modifier le texte de la barre d’état pendant l’exécutement de la macro.

Si vous éteinez l’écho, vous pouvez utiliser l’action **DisplayHourglassPointer** pour transformer le pointeur de la souris en icône de sablier (ou n’importe quelle icône de pointeur de souris que vous avez définie pour « Occupé ») afin de fournir une indication visuelle de l’exécution de la macro.

Pour exécuter l’action **Écho** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Echo** de **l’objet DoCmd**.

## <a name="examples"></a>Exemples

### <a name="set-the-value-of-a-control-by-using-a-macro"></a>Définissez la valeur d’un contrôle en utilisant une macro

La macro suivante ouvre le formulaire Ajouter des produits à partir d’un bouton dans le formulaire Fournisseurs. Elle présente l’utilisation des actions **Écho**, **FermerFenêtre**, **OuvrirFormulaire**, **DéfinirValeur** et **AtteindreContrôle**. L’action **DéfinirValeur** définit le contrôle N° fournisseur dans le formulaire Produits sur le fournisseur actif dans le formulaire Fournisseurs. L’action **AtteindreContrôle** déplace ensuite le focus vers le champ N° catégorie, où vous pouvez commencer à entrer des données pour le nouveau produit. Cette macro doit être associée au bouton Ajouter des produits dans le formulaire Fournisseurs.

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
<td><p>Accéder au contrôle N° catégorie.</p></td>
</tr>
</tbody>
</table>


### <a name="synchronize-forms-by-using-a-macro"></a>Synchroniser des formulaires à l’aide d’une macro

La macro suivante ouvre le formulaire Liste de produits dans le coin inférieur droit du formulaire Fournisseurs, affichant les produits du fournisseur actuel. Elle présente l'utilisation des actions **Écho**, **ZoneMessage**, **AtteindreContrôle**, **ArrêtMacro**, **OuvrirFormulaire** et **DéplacerEtDimensionnerFenêtre**. Elle décrit également l'utilisation d'une expression conditionnelle avec les actions **ZoneMessage**, **AtteindreContrôle**, et **ArrêtMacro**. Cette macro doit être associée au bouton Consulter les produits dans le formulaire Fournisseurs.

<table>
<colgroup>
<col />
<col />
<col />
<col />
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
<td><p>IsNull([ID fournisseur])</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: Passez à l'enregistrement du fournisseur dont vous voulez voir les produits, puis cliquez à nouveau sur le bouton Consulter les produits. <strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</p></td>
<td><p>S'il n'existe aucun fournisseur actif dans le formulaire Fournisseurs, afficher un message.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>AtteindreContrôle</strong></p></td>
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
<td><p><strong>OuvrirFormulaire</strong></p></td>
<td><p><strong>Nom du formulaire</strong> : <strong>Affichage de la</strong> liste des produits <strong>: Nom de DatasheetFilter</strong> : <strong>Condition Where</strong> : [ID fournisseur] = [Formulaires]! [Fournisseurs]! [SupplierID] <strong>Mode données</strong> : <strong>mode Lecture seule :</strong> <strong>Normal</strong></p></td>
<td><p>Ouvrir le formulaire Liste de produits et afficher les produits du fournisseur actuel.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>MoveAndSizeWindow</strong></p></td>
<td><p><strong>Droite</strong> : 0,7799 <strong>:</strong>&quot; 1,8&quot;</p></td>
<td><p>Positionnez le formulaire Liste de produits dans le coin inférieur droit du formulaire Fournisseurs.</p></td>
</tr>
</tbody>
</table>

