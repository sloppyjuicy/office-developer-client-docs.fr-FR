---
title: CancelEvent, action de macro
TOCTitle: CancelEvent macro action
ms:assetid: d9d3ea99-c9fb-2524-c570-e3ee6d20af98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835110(v=office.15)
ms:contentKeyID: 48548066
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm78430
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: a1f5882119a52c0c3f73d4d4da96e4e8ec8f8377
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558596"
---
# <a name="cancelevent-macro-action"></a>CancelEvent, action de macro

**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser **l’action AnnulerEvent** pour annuler l’événement qui a entraîné l’utilisation de la macro contenant cette action par Access. Le nom de la macro est le paramètre d’une propriété de type événement comme **AvantMAJ**, **SurOuverture**, **SurLibération** ou **SurImpression**.

## <a name="setting"></a>Paramètre

L’action **AnnulerEvénement** ne possède aucun argument.

## <a name="remarks"></a>Remarques

Dans un formulaire, l’action **AnnulerEvénement** est généralement utilisée dans une macro de validation avec la propriété de type événement **AvantMAJ**. Lorsqu’un utilisateur entre des données dans un contrôle ou un enregistrement, Access exécute la macro avant d’ajouter les données dans la base de données. Si ces données ne répondent pas aux conditions de validation de la macro, l’action **AnnulerÉvénement** annule le processus de mise à jour avant même qu’il ne débute.

Cette action est souvent utilisée avec l'action **ZoneMessage** pour indiquer que les données n'ont pas rempli les conditions de validation et pour fournir des informations utiles sur le genre de données qui doit être entré.

Les événements suivants peuvent être annulés par l’action **AnnulerEvénement**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Dirty</strong></p></td>
<td><p><strong>MouseDown</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>BeforeDelConfirm</strong></p></td>
<td><p><strong>Exit</strong></p></td>
<td><p><strong>NoData</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>BeforeInsert</strong></p></td>
<td><p><strong>Filtre</strong></p></td>
<td><p><strong>Ouvert</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>BeforeUpdate</strong></p></td>
<td><p><strong>Format</strong></p></td>
<td><p><strong>Print</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>DblClick</strong></p></td>
<td><p><strong>KeyPress</strong></p></td>
<td><p><strong>Unload</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Supprimer</strong></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Vous pouvez utiliser l’action **AnnulerEvénement** avec l’événement **SourisAppuyée** uniquement pour annuler l’événement qui est déclenché lorsque vous cliquez avec le bouton droit sur un objet.

Si le paramètre de la propriété de type événement **SurDoubleClic** d’un contrôle spécifie une macro contenant l’action **AnnulerEvénement**, l’action annule l’événement **DoubleClic**.

Le comportement par défaut des événements pouvant être annulés (à savoir, le comportement d'Access lorsque l'événement est déclenché) a lieu une fois la macro événementielle exécutée. Ceci vous permet d'annuler le comportement par défaut. Par exemple, lorsque vous double-cliquez sur un mot sur lequel se trouve le point d'insertion dans une zone de texte, Access sélectionne normalement ce mot. Vous pouvez, cependant, annuler ce comportement par défaut dans la macro événementielle **DoubleClic** et exécuter une autre action comme l'ouverture d'un formulaire contenant des informations sur le contenu de la zone de texte. Le comportement par défaut des événements ne pouvant pas être annulés a lieu avant l'exécution de la macro.

> [!NOTE]
> [!REMARQUE] Si la propriété de type événement **SurLibération** d'un formulaire spécifie une macro qui exécute une action **AnnulerEvénement**, vous ne pourrez pas fermer le formulaire. Vous devez soit corriger la condition à l'origine de l'exécution de l'action **AnnulerEvénement**, soit ouvrir la macro et supprimer l'action **AnnulerEvénement**. Si le formulaire est un formulaire modal, vous ne pourrez pas ouvrir la macro.

Pour exécuter l’action **AnnulerEvénement** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **CancelEvent** de l’objet **DoCmd**.

## <a name="example"></a>Exemple

Valider des données à l’aide d’une macro

La macro de validation suivante vérifie les codes postaux entrés dans un formulaire Fournisseurs. Elle illustre l’utilisation des actions **ArrêtMacro**, **ZoneMessage**, **AnnulerEvénement** et **AtteindreContrôle**. Une expression conditionnelle vérifie le pays/la région et le code postal entrés dans un enregistrement du formulaire. Si le code postal n’est pas dans le format correct pour le pays/la région, la macro affiche une zone de message et annule la sauvegarde de l’enregistrement. Elle vous renvoie ensuite au contrôle Code postal où vous pouvez corriger l’erreur. Cette macro doit être attachée à la propriété **AvantMAJ** du formulaire Fournisseurs.

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
<td><p>StopMacro</p></td>
<td><p></p></td>
<td><p>Si PaysRégion est <strong>Null</strong>, le code postal ne peut pas être validé.</p></td>
</tr>
<tr class="even">
<td><p>[CountryRegion] In ( &quot; France , Italie , Espagne ) et &quot; &quot; &quot; &quot; &quot; Len([Code postal]) &lt; &gt; 5</p></td>
<td><p>MessageBox</p></td>
<td><p>Message : Le code postal doit contenir 5 caractères. Beep : <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</p></td>
<td><p>Si le code postal ne contient pas 5 caractères, affiche un message.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p>CancelEvent</p></td>
<td><p></p></td>
<td><p>Annule l’événement.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>GoToControl</p></td>
<td><p>Nom du contrôle : CodePostal</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>[CountryRegion] In ( &quot; Australie , Singapour ) et &quot; &quot; &quot; Len([Code postal]) &lt; &gt; 4</p></td>
<td><p>MessageBox</p></td>
<td><p>Message : Le code postal doit contenir 4 caractères. Beep : <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</p></td>
<td><p>Si le code postal ne contient pas 4 caractères, affiche un message.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p>CancelEvent</p></td>
<td><p></p></td>
<td><p>Annule l’événement.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>GoToControl</p></td>
<td><p>Nom du contrôle : CodePostal</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([CountryRegion] = &quot; Canada &quot; ) And ([Postal Code] Not Like &quot; [A-Z][0-9][A-Z] [0-9][A-Z][0-9] &quot; )</p></td>
<td><p>MessageBox</p></td>
<td><p>Message : Le code postal n’est pas valide. Exemple de code canadien : Signal sonore H1J 1C3 : Oui <strong>Type</strong> : Titre de <strong>l’information</strong> : Erreur de code postal</p></td>
<td><p>Si le code postal n’est pas correct pour le Canada, affiche un message. (Exemple de code postal canadien : H1J 1C3.)</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p>CancelEvent</p></td>
<td><p></p></td>
<td><p>Annule l’événement.</p></td>
</tr>
</tbody>
</table>

