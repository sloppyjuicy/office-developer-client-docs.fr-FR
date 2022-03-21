---
title: CloseWindow, action de macro
TOCTitle: CloseWindow macro action
ms:assetid: ba96bc26-7f3f-fd3d-8d3a-e18bfe90cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822510(v=office.15)
ms:contentKeyID: 48547377
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm64319
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: f5fe216231b404ca84564b274fbfca86fddd3e91
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63631644"
---
# <a name="closewindow-macro-action"></a>CloseWindow, action de macro


**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser l’action **FermerWindow** pour fermer un onglet de document Access spécifié ou l’onglet de document actif si aucun onglet n’est spécifié.

## <a name="setting"></a>Paramètres

L’action **FermerFenêtre** utilise les arguments suivants :

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
<td><p><strong>Type d’objet</strong></p></td>
<td><p>Type d’objet dont vous voulez fermer l’onglet de document. Cliquez sur <strong>Table</strong>, <strong>Requête</strong>, <strong>Formulaire</strong>, <strong>État</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Page d’accès aux données</strong>, <strong>Vue serveur</strong>, <strong>Schéma</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong> dans la zone <strong>Type d’objet</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Pour sélectionner l’onglet de document actif, laissez cet argument vide. 

</p>

> [!NOTE]
> Si vous fermez un module dans Visual Basic Editor, vous devez utiliser **Module** dans l’argument **Type d’objet**.


<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Nom de l’objet</strong></p></td>
<td><p>Nom de l’objet à fermer. La zone <strong>Nom de l’objet</strong> affiche tous les objets de la base de données correspondant au type sélectionné par l’argument <strong>Type d’objet</strong>. Cliquez sur l’objet pour le fermer. Si vous laissez l’argument <strong>Type d’objet</strong> vide, laissez également celui-ci vide.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Save</strong></p></td>
<td><p>Indique si les modifications apportées à l’objet doivent être enregistrées à la fermeture. Cliquez sur <strong>Oui</strong> (enregistrer l’objet), sur <strong>Non</strong> (fermer l’objet sans enregistrer) ou sur <strong>Avec confirmation</strong> (demander à l’utilisateur d’enregistrer ou non l’objet). La valeur par défaut est <strong>Avec confirmation</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

L'action **FermerFenêtre** fonctionne sur tous les objets de base de données que l'utilisateur peut ouvrir ou fermer explicitement. Cette action équivaut à sélectionner un objet, puis à le fermer en cliquant avec le bouton droit sur l'onglet de document de l'objet, puis en cliquant sur le bouton **Fermer** dans le menu contextuel ou en cliquant sur le bouton **Fermer** de l'objet.

Si l'argument **Enregistrer** est défini sur **Avec confirmation** et que l'objet n'a pas encore été enregistré au moment de l'exécution de l'action **FermerFenêtre**, une boîte de dialogue demande à l'utilisateur d'enregistrer l'objet avant que la macro ne le ferme. Si vous avez défini l'argument **Avertissements actifs** de l'action **Avertissements** sur **Non**, la boîte de dialogue n'est pas affichée et l'objet est automatiquement enregistré.

Pour exécuter l'action **FermerFenêtre** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Close** de l'objet **DoCmd**.

