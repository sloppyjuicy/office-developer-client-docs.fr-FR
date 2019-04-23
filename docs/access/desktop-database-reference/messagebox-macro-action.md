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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289155"
---
# <a name="messagebox-macro-action"></a>MessageBox, action de macro

**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser l'action **MessageBox** pour afficher un message contenant un avertissement ou un message d'information. Par exemple, vous pouvez utiliser l'action **MessageBox** avec des macros de validation. Lorsqu'un contrôle ou un enregistrement ne remplit pas une condition de validation dans la macro, une boîte de message peut afficher un message d'erreur et fournir des instructions sur le type de données à entrer.

## <a name="setting"></a>Setting

L'action **MessageBox** possède les arguments suivants.

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
<td><p>Texte de la zone de message. Entrez le texte du message dans la zone de <strong>message</strong> dans la section arguments de l' <strong>action</strong> du volet générateur de macro. Vous pouvez taper jusqu'à 255 caractères ou entrer une expression (précédée d'un signe égal).</p></td>
</tr>
<tr class="even">
<td><p><strong>Beep</strong></p></td>
<td><p>Indique si le haut-parleur de votre ordinateur émet une tonalité lorsque le message s'affiche. Cliquez sur <strong>Oui</strong> (émettre un signal sonore) ou sur <strong>non</strong> (ne pas émettre de signal sonore). La valeur par défaut est <strong>Oui</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Type</strong></p></td>
<td><p>Type de boîte de message. Chaque type possède une icône différente. Cliquez sur <strong>aucun</strong>, <strong>critique</strong>, <strong>Avertissement?</strong>, <strong>Avertissement!</strong>ou <strong>informations</strong>. La valeur par défaut est <strong>aucun</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Titre</strong></p></td>
<td><p>Texte affiché dans la barre de titre de la zone de message. Par exemple, vous pouvez faire en sorte que la &quot;barre de titre&quot;affiche la validation de l'ID client. Si vous laissez cet argument vide, &quot;Microsoft Access&quot; s'affiche.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous pouvez utiliser l'action **MessageBox** pour créer un message d'erreur mis en forme de la même manière que les messages d'erreur intégrés affichés par Microsoft Access. L'action **MessageBox** vous permet de fournir un message dans trois sections pour l'argument message. Vous séparez les sections avec le caractère «@».

L'exemple suivant affiche une boîte de message mise en forme avec un message de section. La première section du texte du message est affichée sous la forme d'un en-tête en gras. La deuxième section est affichée sous forme de texte brut sous cet en-tête. La troisième section est affichée sous forme de texte brut sous la deuxième section, avec une ligne vide entre elles.

Tapez la chaîne suivante dans l'argument **message** :

**Bouton\!incorrect @This bouton ne fonctionne pas. @Try un autre.**

Vous ne pouvez pas exécuter l'action **MessageBox** dans un module Visual Basic pour applications (VBA). Utilisez la fonction **MsgBox** à la place.

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
<td><p>IsNull ([n ° fournisseur])</p></td>
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
<td><p><strong>Nom du formulaire</strong>: liste des produits <strong>affichage</strong>: <strong>nom donnéesnom du filtre</strong>: <strong>condition WHERE</strong>: [n ° fournisseur] = [Forms]! [Fournisseurs]! Fournisseur <strong>Mode données</strong>: <strong>mode lecture seulemode fenêtre</strong>: <strong>normal</strong></p></td>
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


**Valider des données à l’aide d’une macro**

La macro de validation suivante vérifie les codes postaux entrés dans un formulaire Fournisseurs. Elle illustre l’utilisation des actions **ArrêtMacro**, **ZoneMessage**, **AnnulerEvénement** et **AtteindreContrôle**. Une expression conditionnelle vérifie le pays/la région et le code postal entrés dans un enregistrement du formulaire. Si le code postal n'est pas au format approprié pour le pays/la région, la macro affiche une zone de message et annule l'enregistrement de l'enregistrement. Elle vous renvoie ensuite au contrôle CodePostal, dans lequel vous pouvez corriger l'erreur. Cette macro doit être attachée à la propriété **AvantMAJ** du formulaire Fournisseurs.

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
<td><p>IsNull ([PaysRégion])</p></td>
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>Si PaysRégion a la <strong>valeur null</strong>, le code postal ne peut pas être validé.</p></td>
</tr>
<tr class="even">
<td><p>Région In (&quot;France&quot;,&quot;Italie&quot;,&quot;Espagne&quot;) et Len ([CodePostal]) &lt; &gt; 5</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: le code postal doit comporter 5 caractères. <strong>Bip</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erreur de code postal</p></td>
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
<td><p><strong>Nom du contrôle</strong>: PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Région En (&quot;Australie&quot;,&quot;Singapour&quot;) et NBCAR ([CodePostal]) &lt; &gt; 4</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: le code postal doit contenir 4 caractères. <strong>Bip</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erreur de code postal</p></td>
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
<td><p><strong>Nom du contrôle</strong>: PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([PaysRégion] = &quot;Canada&quot;) Et ([CodePostal] non comme&quot;[A-z] [0-9] [A-z] [0-9] [A-z] [0-9]&quot;</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: le code postal n'est pas valide. Exemple de code canadien: H1J 1C3 <strong>bip</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erreur de code postal</p></td>
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

