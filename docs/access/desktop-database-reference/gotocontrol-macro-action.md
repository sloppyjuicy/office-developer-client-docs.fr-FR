---
title: GoToControl, action de macro
TOCTitle: GoToControl macro action
ms:assetid: caff76dc-7ca8-4f87-8144-89445ed4600d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834370(v=office.15)
ms:contentKeyID: 48547705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3e0fc7c44449caa39ecbde9d0516ef63187a77d4
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63633441"
---
# <a name="gotocontrol-macro-action"></a>GoToControl, action de macro

**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser l’action **GoToControl** pour déplacer le focus sur le champ ou le contrôle spécifié dans l’enregistrement actuel du formulaire ouvert, de la feuille de données du formulaire, de la feuille de données de table ou de la feuille de données de requête. Vous pouvez utiliser cette action lorsque vous souhaitez mettre le focus sur un champ ou un contrôle particulier. Ce champ ou le contrôle puis utilisable pour des comparaisons ou des actions **TrouverEnregistrement**. Vous pouvez également utiliser cette action pour naviguer dans un formulaire sous certaines conditions. Par exemple, si l'utilisateur saisit non dans un contrôle conjoint sur un formulaire d'assurance maladie, le focus peut automatiquement passer le contrôle nom du conjoint/partenaire et déplacer vers le contrôle suivant.

## <a name="setting"></a>Paramètres

> [!NOTE]
> Cette action n’est pas disponible pour une utilisation avec des pages d’accès aux données.

L’action **AtteindreContrôle** possède l’argument suivant.

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
<td><p><strong>Nom du contrôle</strong></p></td>
<td><p>Nom du champ ou du contrôle dans lequel vous souhaitez déplacer le focus. Entrez le nom du champ ou du contrôle dans la zone <strong>Nom</strong> du contrôle dans la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Cet argument est obligatoire.</p>
<p><strong>REMARQUE</strong> : entrez uniquement le nom du champ ou du contrôle dans <strong>l’argument Nom</strong> du contrôle, et non l’identificateur complet, tel que Forms ! Produits ! [ID de produit].</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous ne pouvez pas utiliser **l’action GoToControl** pour déplacer le focus sur un contrôle sur un formulaire masqué.

> [!TIP]
> Vous pouvez utiliser **l’action GoToControl** pour vous déplacer vers un sous-form, qui est un type de contrôle. Vous pouvez ensuite utiliser **l’action MettreEnregistrement** pour passer à un enregistrement particulier dans le sous-form. Vous pouvez également vous déplacer vers un contrôle d’un sous-form à l’aide de l’action **GoToControl** pour passer d’abord au sous-form, puis au contrôle sur le sous-form.

Pour exécuter **l’action GoToControl** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **GoToControl** de l’objet **DoCmd**. Vous pouvez également utiliser la méthode **SetFocus** pour placer le focus sur un contrôle dans un formulaire ou un de ses sous-formulaires, ou à un champ dans une table ouverte, une requête ou une feuille de données de formulaire.

## <a name="examples"></a>Exemples

**Définissez la valeur d'un contrôle en utilisant une macro**

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
<td><p>Formulaire Fermer la liste des produits.</p></td>
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


**Valider des données à l’aide d’une macro**

La macro de validation suivante vérifie les codes postaux entrés dans un formulaire Fournisseurs. Elle illustre l’utilisation des actions **ArrêtMacro**, **ZoneMessage**, **AnnulerEvénement** et **AtteindreContrôle**. Une expression conditionnelle vérifie le pays/la région et le code postal entrés dans un enregistrement du formulaire. Si le code postal n’est pas dans le format correct pour le pays/la région, la macro affiche une zone de message et annule la sauvegarde de l’enregistrement. La macro vous renvoie ensuite au contrôle Code postal, où vous pouvez corriger l’erreur. Cette macro doit être attachée à la propriété **AvantMAJ** du formulaire Fournisseurs.

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
<td><p>IsNull([CountryRegion])</p></td>
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>Si CountryRegion a la valeur <strong>Null</strong>, le code postal ne peut pas être validé.</p></td>
</tr>
<tr class="even">
<td><p>[CountryRegion] In (&quot;France,Italie,Espagne&quot;&quot;&quot;&quot;&quot;) et Len([Code postal]) 5 &lt;&gt;</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong> : le code postal doit être de 5 caractères. <strong>Beep</strong> : <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</p></td>
<td><p>Si le code postal ne compte pas 5 caractères, affiche un message.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Annule l’événement.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>AtteindreContrôle</strong></p></td>
<td><p><strong>Nom du contrôle</strong> : PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>[CountryRegion] In (&quot;Australie,Singapour&quot;&quot;&quot;) et Len([Code postal]) &lt;&gt; 4</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p>Message : Le code postal doit contenir 4 caractères. <strong>Beep</strong> : <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</p></td>
<td><p>Si le code postal ne compte pas 4 caractères, affiche un message.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Annule l’événement.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>AtteindreContrôle</strong></p></td>
<td><p><strong>Nom du contrôle</strong> : PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([CountryRegion] = &quot; Canada&quot;) And ([Postal Code] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message :</strong> le code postal n’est pas valide. Exemple de code canadien : Bip H1J 1C3 <strong>:</strong> <strong>YesType</strong> : <strong>InformationTitle</strong> : Erreur de code postal</p></td>
<td><p>Si le code postal n’est pas correct pour le Canada, affichez un message. (Exemple de code postal canadien : H1J 1C3.)</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Annule l’événement.</p></td>
</tr>
</tbody>
</table>

