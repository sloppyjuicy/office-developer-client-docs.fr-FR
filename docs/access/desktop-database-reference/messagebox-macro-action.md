---
title: MessageBox, action de macro
TOCTitle: MessageBox macro action
ms:assetid: 326a0e68-38fb-4f81-b319-5a70caa5aec4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192304(v=office.15)
ms:contentKeyID: 48544077
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7b90cf3437e2baa0865ebb851e36b94de917955b
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63634764"
---
# <a name="messagebox-macro-action"></a>MessageBox, action de macro

**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser l’action **MessageBox** pour afficher une boîte de message contenant un avertissement ou un message d’information. Par exemple, vous pouvez utiliser l’action **MessageBox** avec des macros de validation. Lorsqu’un contrôle ou un enregistrement échoue à une condition de validation dans la macro, une boîte de message peut afficher un message d’erreur et fournir des instructions sur le type de données à entrer.

## <a name="setting"></a>Paramètres

**L’action MessageBox** possède les arguments suivants.

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
<td><p><strong>Message</strong></p></td>
<td><p>Texte dans la zone de message. Entrez le texte du message dans la <strong>zone Message</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Vous pouvez taper jusqu’à 255 caractères ou entrer une expression (précédée d’un signe égal).</p></td>
</tr>
<tr class="even">
<td><p><strong>Beep</strong></p></td>
<td><p>Indique si le haut-parleur de votre ordinateur sonne un signal sonore lorsque le message s’affiche. Cliquez <strong>sur Oui</strong> (sonner le signal sonore) ou <strong>non</strong> (ne pas sonner le signal sonore). La valeur par défaut est <strong>Oui</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Type</strong></p></td>
<td><p>Type de boîte de message. Chaque type possède une icône différente. Cliquez <strong>sur Aucun</strong>, <strong>Critique</strong>, <strong>Avertissement ?</strong>, <strong>Avertissement !</strong>, ou <strong>Informations</strong>. La valeur par défaut est <strong>Aucun</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Titre</strong></p></td>
<td><p>Texte affiché dans la barre de titre de la boîte de message. Par exemple, la barre de titre peut afficher la &quot;validation de l’ID client&quot;. Si vous laissez cet argument vide, &quot;Microsoft Access&quot; s’affiche.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous pouvez utiliser l’action **MessageBox** pour créer un message d’erreur mis en forme semblable aux messages d’erreur intégrés affichés par Microsoft Access. **L’action MessageBox** vous permet de fournir un message en trois sections pour l’argument Message. Vous séparez les sections par le caractère « @ ».

L’exemple suivant affiche une boîte de message mise en forme avec un message en sections. La première section de texte du message s’affiche en gras. La deuxième section s’affiche en texte simple sous ce titre. La troisième section s’affiche sous la deuxième section sous un texte simple, avec une ligne vide entre elles.

Tapez la chaîne suivante dans **l’argument** Message :

**Un bouton @This\! n’est pas work.@Try autre.**

Vous ne pouvez pas exécuter l’action **MessageBox** dans un module Visual Basic pour Applications (VBA). Utilisez plutôt **la fonction MsgBox** .

## <a name="examples"></a>Exemples

**Synchroniser des formulaires à l'aide d'une macro**

La macro suivante ouvre un formulaire de liste de produits dans le coin inférieur droit du formulaire Fournisseurs, affichant les produits du fournisseur actuel. Elle présente l'utilisation des actions **Écho**, **ZoneMessage**, **AtteindreContrôle**, **ArrêtMacro**, **OuvrirFormulaire** et **DéplacerEtDimensionnerFenêtre**. Elle décrit également l'utilisation d'une expression conditionnelle avec les actions **ZoneMessage**, **AtteindreContrôle**, et **ArrêtMacro**. Cette macro doit être associée au bouton Consulter les produits dans le formulaire Fournisseurs.

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
<td><p>IsNull([SupplierID])</p></td>
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
<td><p><strong>Nom du formulaire</strong> : Affichage de liste <strong>de</strong> produits <strong>: Nom de DatasheetFilter</strong> : <strong>Condition where</strong>: [SupplierID] = [Forms]! [Fournisseurs]! [SupplierID] <strong>Mode données</strong> : <strong>mode Lecture seule :</strong> <strong>Normal</strong></p></td>
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


**Valider des données à l’aide d’une macro**

La macro de validation suivante vérifie les codes postaux entrés dans un formulaire Fournisseurs. Elle illustre l’utilisation des actions **ArrêtMacro**, **ZoneMessage**, **AnnulerEvénement** et **AtteindreContrôle**. Une expression conditionnelle vérifie le pays/la région et le code postal entrés dans un enregistrement du formulaire. Si le code postal n’est pas dans le bon format pour le pays/la région, la macro affiche une boîte de message et annule l’enregistrement. Il vous renvoie ensuite au contrôle PostalCode, où vous pouvez corriger l’erreur. Cette macro doit être attachée à la propriété **AvantMAJ** du formulaire Fournisseurs.

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
<td><p>[CountryRegion] In (&quot;France,Italie,Espagne&quot;&quot;&quot;&quot;&quot;) et Len([PostalCode]) 5 &lt;&gt;</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong> : le code postal doit être de 5 caractères. <strong>Beep</strong> : <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</p></td>
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
<td><p><strong>AtteindreContrôle</strong></p></td>
<td><p><strong>Nom du contrôle</strong> : PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>[CountryRegion] In (&quot;Australie,Singapour&quot;&quot;&quot;) et Len([PostalCode]) &lt;&gt; 4</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong> : le code postal doit être de 4 caractères. <strong>Beep</strong> : <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</p></td>
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
<td><p><strong>AtteindreContrôle</strong></p></td>
<td><p><strong>Nom du contrôle</strong> : PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([CountryRegion] = &quot; Canada&quot;) And ([PostalCode] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message :</strong> le code postal n’est pas valide. Exemple de code canadien : Bip H1J 1C3 <strong>:</strong> <strong>YesType</strong> : <strong>InformationTitle</strong> : Erreur de code postal</p></td>
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

