---
title: Action de Macro écho (référence de base de données du bureau Access)
TOCTitle: Echo Macro Action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39471ea4bab2ec1bbeb8cd22ecb00aa5df3bc411
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863968"
---
# <a name="echo-macro-action"></a>Action de Macro écho


**S’applique à**: Access 2013 | Office 2013

Vous pouvez utiliser l’action **écho** pour spécifier si l’écho est activé. Par exemple, vous pouvez utiliser cette action pour masquer ou afficher les résultats d’une macro pendant son exécution.

## <a name="setting"></a>Paramètre


> [!NOTE]
> [!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.



L’action **écho** possède les arguments suivants.

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
<td><p><strong>Écho</strong></p></td>
<td><p>Cliquez sur <strong>Oui</strong> (pour activer l’écho) ou <strong>non</strong> (pour désactiver l’écho) dans la zone <strong>Écho</strong> dans la section <strong>Arguments de l’Action</strong> du volet Générateur de Macro. La valeur par défaut est <strong>Oui</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Texte de la barre d’état</strong></p></td>
<td><p>Le texte à afficher dans la barre lorsque l’écho est désactivé. Par exemple, lorsque l’écho est désactivé, la barre d’état peut afficher &quot;la macro est en cours d’exécution.&quot;</p></td>
</tr>
</tbody>
</table>


S’exécute une macro, la mise à jour souvent affiche des informations pas indispensable au fonctionnement de la macro. Lorsque vous définissez l’argument **Écho actif** sur **non**, la macro s’exécute sans mise à jour de l’écran. Une fois la macro terminée, Access automatiquement activer l’écho et redessine la fenêtre. Le paramètre **non** de l’argument **Écho actif** n’affecte pas la fonctionnalité de la macro ni ses résultats.

L’action **écho** ne supprime pas l’affichage des boîtes de dialogue modales, telles que des formulaires indépendants, tels que des feuilles de propriétés ou des messages d’erreur. Vous pouvez utiliser les boîtes de dialogue et formulaires indépendants pour rassembler ou afficher plus d’informations, même si l’écho est désactivé. Pour supprimer toutes les boîtes de message ou, à l’exception des boîtes de dialogue qui exigent que l’utilisateur à entrer des informations et des boîtes de message d’erreur, utilisez l’action **avertissements** .

Vous pouvez exécuter l’action **écho** plusieurs fois dans une macro. Cela vous permet de modifier le texte de barre d’état pendant l’exécution de la macro.

Si vous désactivez l’écho, vous pouvez utiliser l’action **Afficherpointeursablier** pour transformer le pointeur de souris en icône de sablier (ou celle que vous avez définie pour « Occupé ») pour fournir une indication visuelle de la macro est en cours d’exécution.

Pour exécuter l’action **écho** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Echo** de l’objet **DoCmd** .

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
<td><p><strong>Élément</strong>: [Forms]![Produits]![N° fournisseur] <strong>Expression</strong>: N° fournisseur</p></td>
<td><p>Définissez le contrôle N° fournisseur sur le fournisseur actuel dans le formulaire Fournisseurs.</p></td>
</tr>
<tr class="odd">
<td><p><strong>AtteindreContrôle</strong></p></td>
<td><p><strong>Nom du contrôle</strong>: N° catégorie</p></td>
<td><p>Accéder au contrôle N° catégorie.</p></td>
</tr>
</tbody>
</table>


**Synchroniser des formulaires à l'aide d'une macro**

La macro suivante ouvre le formulaire liste des produits dans le coin inférieur droit du formulaire fournisseurs, affichant les produits du fournisseur actif. Elle présente l'utilisation des actions **Écho**, **ZoneMessage**, **AtteindreContrôle**, **ArrêtMacro**, **OuvrirFormulaire** et **DéplacerEtDimensionnerFenêtre**. Elle décrit également l'utilisation d'une expression conditionnelle avec les actions **ZoneMessage**, **AtteindreContrôle**, et **ArrêtMacro**. Cette macro doit être associée au bouton Consulter les produits dans le formulaire Fournisseurs.

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
<td><p>...</p></td>
<td><p><strong>AtteindreContrôle</strong></p></td>
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

