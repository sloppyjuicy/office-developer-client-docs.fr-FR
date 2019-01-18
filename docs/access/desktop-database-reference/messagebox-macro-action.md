---
title: MessageBox, action de macro
TOCTitle: MessageBox macro action
ms:assetid: 326a0e68-38fb-4f81-b319-5a70caa5aec4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192304(v=office.15)
ms:contentKeyID: 48544077
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1175e3903e54fd3420be43dfd9e3652d9990468b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722927"
---
# <a name="messagebox-macro-action"></a>MessageBox, action de macro

**S’applique à**: Access 2013, Office 2013

Vous pouvez utiliser l’action de **contrôle zonemessage** pour afficher une boîte de message contenant un avertissement ou un message d’information. Par exemple, vous pouvez utiliser l’action de **contrôle zonemessage** avec des macros de validation. Lorsqu’un contrôle ou un enregistrement échoue une condition de validation de la macro, une boîte de message peut afficher un message d’erreur et fournissent des instructions sur le type de données qui doivent être saisies.

## <a name="setting"></a>Setting

L’action de **contrôle zonemessage** possède les arguments suivants.

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
<td><p><strong>Message</strong></p></td>
<td><p>Le texte dans la boîte de message. Entrez le texte du message dans la boîte de <strong>Message</strong> dans la section <strong>Arguments de l’Action</strong> du volet Générateur de Macro. Vous pouvez taper jusqu'à 255 caractères ou entrer une expression (précédée d’un signe égal).</p></td>
</tr>
<tr class="even">
<td><p><strong>Beep</strong></p></td>
<td><p>Spécifie si le haut-parleur de votre ordinateur émet un signal sonore lorsque le message s’affiche. Cliquez sur <strong>Oui</strong> (pour émettre un bip sonore) ou <strong>non</strong> (ne pas émettre le signal sonore). La valeur par défaut est <strong>Oui</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Type</strong></p></td>
<td><p>Le type de boîte de message. Chaque type a une autre icône. Cliquez sur <strong>Aucun</strong>, <strong>critique</strong>, <strong>Avertissement ?</strong>, <strong>Avertissement !</strong>, ou les <strong>informations</strong>. La valeur par défaut est <strong>None</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Titre</strong></p></td>
<td><p>Le texte affiché dans la barre de titre de boîte de message. Par exemple, vous pouvez avoir l’affichage de barre de titre &quot;Validation du code client&quot;. Si vous laissez cet argument vide, &quot;Microsoft Access&quot; s’affiche.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous pouvez utiliser l’action de **contrôle zonemessage** pour créer un message d’erreur formaté semblable aux messages d’erreur intégrés affichés par Microsoft Access. L’action de **contrôle zonemessage** vous permet de fournir un message en trois sections pour l’argument Message. Séparez les sections avec le « @ » caractères.

L’exemple suivant affiche un message mis en forme avec un message en plusieurs parties. La première section de texte dans le message s’affiche sous forme de titre en gras. La deuxième section s’affiche sous forme de texte brut sous cet en-tête. La troisième section s’affiche en texte simple sous la seconde section, avec une ligne vide entre eux.

Tapez la chaîne suivante dans l’argument **Message** :

**Mauvais bouton\!@This bouton ne work.@Try une autre.**

Vous ne pouvez pas exécuter l’action de **contrôle zonemessage** dans un module Visual Basic pour Applications (VBA). Utilisez la fonction **MsgBox** .

## <a name="examples"></a>Exemples

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
<td><p>IsNull([N° fournisseur])</p></td>
<td><p><strong>ZoneMessage</strong></p></td>
<td><p><strong>Message</strong>: Passez à l'enregistrement du fournisseur dont vous voulez voir les produits, puis cliquez à nouveau sur le bouton Consulter les produits. <strong>Bip</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: sélectionnez un fournisseur</p></td>
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
<td><p><strong>ArrêtMacro</strong></p></td>
<td><p></p></td>
<td><p>Arrêter la macro.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Nom du formulaire</strong>: produit liste <strong>affichage</strong>: <strong>DatasheetFilter nom</strong>: <strong>Condition Where</strong>: [n° fournisseur] = [Forms] ! [Fournisseurs] ! [N° fournisseur] <strong>Mode données</strong>: <strong>Le Mode lecture OnlyWindow</strong>: <strong>Normal</strong></p></td>
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


**Valider des données à l’aide d’une macro**

La macro de validation suivante vérifie les codes postaux entrés dans un formulaire Fournisseurs. Elle illustre l'utilisation des actions **ArrêtMacro**, **ZoneMessage**, **AnnulerEvénement** et **AtteindreContrôle**. Une expression conditionnelle vérifie le pays/la région et le code postal entrés dans un enregistrement du formulaire. Si le code postal n’est pas dans le format approprié pour le pays/région, la macro affiche une boîte de message et annule l’enregistrement. Elle vous renvoie ensuite au contrôle de code postal, où vous pouvez corriger l’erreur. Cette macro doit être attachée à la propriété **AvantMAJ** du formulaire Fournisseurs.

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
<td><p>IsNull([CountryRegion])</p></td>
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>Si PaysRégion est <strong>Null</strong>, le code postal ne peut pas être validé.</p></td>
</tr>
<tr class="even">
<td><p>[PaysRégion] Dans (&quot;France&quot;,&quot;Italie&quot;,&quot;Espagne&quot;) et Len([PostalCode]) &lt; &gt; 5</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: le code postal doit contenir 5 caractères. <strong>Bip</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erreur de Code Postal</p></td>
<td><p>Si le code postal ne contient pas 5 caractères, affiche un message.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Annule l’événement.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nom du contrôle</strong>: CodePostal</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>[PaysRégion] Dans (&quot;Australie&quot;,&quot;Singapour&quot;) et Len([PostalCode]) &lt; &gt; 4</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: le code postal doit contenir 4 caractères. <strong>Bip</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erreur de Code Postal</p></td>
<td><p>Si le code postal ne contient pas 4 caractères, affiche un message.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Annule l’événement.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nom du contrôle</strong>: CodePostal</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([PaysRégion] = &quot;Canada&quot;) Et ([code postal] pas comme&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: le code postal n’est pas valide. Exemple de code canadien : H1J 1C3 <strong>Bip</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erreur de Code Postal</p></td>
<td><p>Si le code postal n’est pas correct pour le Canada, affiche un message. (Exemple de code postal canadien : H1J 1C3.)</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Annule l’événement.</p></td>
</tr>
</tbody>
</table>

