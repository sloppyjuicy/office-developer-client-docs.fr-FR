---
title: MoveAndSizeWindow, action de macro
TOCTitle: MoveAndSizeWindow macro action
ms:assetid: 86bcf45f-90ce-4ca2-a7fb-efbe5347d137
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197001(v=office.15)
ms:contentKeyID: 48546090
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8737de80c38626b72933eb15a59e08ab0452ce74
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998811"
---
# <a name="moveandsizewindow-macro-action"></a>MoveAndSizeWindow, action de macro

**S’applique à**: Access 2013, Office 2013

Si vous avez défini votre document options de la fenêtre à utiliser des fenêtres superposées au lieu des documents à onglets, vous pouvez utiliser l’action **Déplaceretdimensionnerfenêtre** pour déplacer ou redimensionner la fenêtre active. Pour plus d’informations sur la façon de définir les options de fenêtre de document, voir la section Remarques.

## <a name="setting"></a>Paramètre

L’action **Déplaceretdimensionnerfenêtre** possède les arguments suivants.

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
<td><p><strong>Right</strong></p></td>
<td><p>Nouvelle position horizontale de l'angle supérieur gauche de la fenêtre mesurée depuis le bord gauche de cette fenêtre. Dans la section <strong>Arguments de l’Action</strong> du volet Générateur de Macro, entrez la position dans la zone de <strong>droite</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong>Down</strong></p></td>
<td><p>Nouvelle position verticale de l'angle supérieur gauche de la fenêtre mesurée depuis le haut de cette fenêtre.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Width</strong></p></td>
<td><p>Nouvelle largeur de la fenêtre.</p></td>
</tr>
<tr class="even">
<td><p><strong>Height</strong></p></td>
<td><p>Nouvelle hauteur de la fenêtre.</p></td>
</tr>
</tbody>
</table>


Si vous laissez un argument vierge, Microsoft Access utilise la valeur actuelle de la fenêtre.

Vous devez entrer une valeur pour au moins un argument.

> [!NOTE]
> Chaque mesure est exprimée en pouces ou en centimètres, selon les paramètres régionaux du Panneau de configuration Windows.

## <a name="remarks"></a>Remarques

Pour configurer une application pour utiliser des fenêtres superposées au lieu des documents à onglets, utilisez la procédure suivante :

1.  Cliquez sur **Options**

2.  Cliquez sur **base de données Active**.

3.  Dans la section **Options de l'application**, sous **Options de la fenêtre Document**, cliquez sur **Fenêtres superposées**.

4.  Cliquez sur **OK**, puis fermez et rouvrez la base de données.

Cette action équivaut à cliquer sur **déplacer** ou **taille** sur le **contrôle de** menu fenêtre. Avec les commandes de menu, vous utilisez les touches de direction pour déplacer ou pour redimensionner la fenêtre. Avec l’action **Déplaceretdimensionnerfenêtre** , vous entrez directement les mesures de position et de taille. Vous pouvez également utiliser la souris pour déplacer et dimensionner des fenêtres.

Vous pouvez utiliser cette action sur n’importe quelle fenêtre, dans n’importe quel mode.

> [!TIP]
> - Pour déplacer une fenêtre sans la dimensionner, entrez des valeurs pour la **droite** et **bas** arguments, mais laissez les arguments **largeur** et **hauteur** vide.
> - Pour redimensionner une fenêtre sans la déplacer, entrez des valeurs pour la **largeur** et la **hauteur** arguments, mais laissez les arguments **droite** et **bas** vide.

Pour exécuter l’action **Déplaceretdimensionnerfenêtre** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **MoveSize** de l’objet **DoCmd** .

## <a name="example"></a>Exemple

**Synchroniser des formulaires à l'aide d'une macro**

La macro suivante ouvre un formulaire de liste de produits dans le coin inférieur droit du formulaire Fournisseurs, affichant les produits du fournisseur actuel. Elle présente l'utilisation des actions **Écho**, **ZoneMessage**, **AtteindreContrôle**, **ArrêtMacro**, **OuvrirFormulaire** et **DéplacerEtDimensionnerFenêtre**. Elle décrit également l'utilisation d'une expression conditionnelle avec les actions **ZoneMessage**, **AtteindreContrôle**, et **ArrêtMacro**. Cette macro doit être associée au bouton Consulter les produits dans le formulaire Fournisseurs.

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
<td><p>IsNull ([Réf fournisseur])</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: Passez à l'enregistrement du fournisseur dont vous voulez voir les produits, puis cliquez à nouveau sur le bouton Consulter les produits. <strong>Bip</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: sélectionnez un fournisseur</p></td>
<td><p>S'il n'existe aucun fournisseur actif dans le formulaire Fournisseurs, afficher un message.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nom du contrôle</strong>: NomSociété</p></td>
<td><p>Déplacer le focus sur le contrôle NomSociété.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>ArrêtMacro</strong></p></td>
<td><p></p></td>
<td><p>Arrêter la macro.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OuvrirFormulaire</strong></p></td>
<td><p><strong>Nom du formulaire</strong>: produit liste <strong>affichage</strong>: <strong>DatasheetFilter nom</strong>: <strong>Condition Where</strong>: [Réf fournisseur] = [Forms] ! [Fournisseurs] ! [N° fournisseur] <strong>Mode données</strong>: <strong>Le Mode lecture OnlyWindow</strong>: <strong>Normal</strong></p></td>
<td><p>Ouvrir le formulaire Liste de produits et afficher les produits du fournisseur actuel.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>DéplacerEtDimensionnerFenêtre</strong></p></td>
<td><p><strong>Droite</strong>: 0.7799&quot; <strong>vers le bas</strong>: 1,8&quot;</p></td>
<td><p>Positionnez le formulaire Liste de produits dans le coin inférieur droit du formulaire Fournisseurs.</p></td>
</tr>
</tbody>
</table>

