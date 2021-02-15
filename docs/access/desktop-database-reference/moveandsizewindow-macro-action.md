---
title: MoveAndSizeWindow, action de macro
TOCTitle: MoveAndSizeWindow macro action
ms:assetid: 86bcf45f-90ce-4ca2-a7fb-efbe5347d137
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197001(v=office.15)
ms:contentKeyID: 48546090
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c1b127995a2f9a0af7da80e9df862259b570870e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288805"
---
# <a name="moveandsizewindow-macro-action"></a>MoveAndSizeWindow, action de macro

**S’applique à** : Access 2013, Office 2013

Si vous avez choisi d’utiliser des fenêtres superposées plutôt que des documents à onglets, vous pouvez utiliser l’action **MoveAndSizeWindow** pour déplacer ou resize la fenêtre active. Pour plus d’informations sur la façon de définir les options de fenêtre de document, voir la section Remarques.

## <a name="setting"></a>Setting

**L’action MoveAndSizeWindow a** les arguments suivants.

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
<td><p>Nouvelle position horizontale de l'angle supérieur gauche de la fenêtre mesurée depuis le bord gauche de cette fenêtre. Entrez la position dans la <strong>zone</strong> droite de la section <strong>Arguments de l’action</strong> du volet Générateur de macro.</p></td>
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


Si vous laissez un argument vide, Microsoft Access utilise le paramètre actuel de la fenêtre.

Vous devez entrer une valeur pour au moins un argument.

> [!NOTE]
> Chaque mesure est en pouces ou en centimètres, selon les paramètres régionaux du Panneau de configuration Windows.

## <a name="remarks"></a>Remarques

Pour configurer une application afin qu’elle utilise des fenêtres superposées au lieu de documents à onglets, utilisez la procédure suivante :

1.  Options de **clic**

2.  Cliquez sur **Base de données actuelle.**

3.  Dans la section **Options de l'application**, sous **Options de la fenêtre Document**, cliquez sur **Fenêtres superposées**.

4.  Cliquez **sur OK,** puis fermez et rouvrez la base de données.

Cette action est similaire à celle qui consiste à cliquer sur **Déplacer** ou **Dimensionr** dans le menu Contrôle de **la** fenêtre. Avec les commandes de menu, vous utilisez les touches de direction du clavier pour déplacer ou re resserr la fenêtre. Avec **l’action MoveAndSizeWindow,** vous entrez directement les mesures de position et de taille. Vous pouvez également utiliser la souris pour déplacer et dimensioner des fenêtres.

Vous pouvez utiliser cette action sur n’importe quelle fenêtre, dans n’importe quel affichage.

> [!TIP]
> - Pour déplacer une fenêtre sans la resserriser, entrez  des valeurs pour les **arguments** Droite et Bas, mais laissez les **arguments** Largeur et Hauteur vides. 
> - Pour re tailler une fenêtre sans la déplacer, entrez des  valeurs pour les **arguments** **Largeur** et Hauteur, mais laissez les **arguments** Droite et Bas vides.

Pour exécuter **l’action MoveAndSizeWindow** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **MoveSize** de l’objet **DoCmd.**

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
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Écho sur</strong>: <strong>Non</strong></p></td>
<td><p>Arrêter l’actualisation de l’écran pendant l’exécution de la macro.</p></td>
</tr>
<tr class="even">
<td><p>IsNull([ID fournisseur])</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: Passez à l'enregistrement du fournisseur dont vous voulez voir les produits, puis cliquez à nouveau sur le bouton Consulter les produits. <strong>Bip</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: sélectionner un fournisseur</p></td>
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
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>Arrêter la macro.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Nom du formulaire</strong>: Affichage <strong>de</strong>la liste des produits : Nom <strong>de DatasheetFilter</strong>: <strong>Condition where</strong>: [ID fournisseur] = [Formulaires]! [Fournisseurs]! [SupplierID] <strong>Mode données</strong>: <strong>mode Lecture seule :</strong> <strong>Normal</strong></p></td>
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

