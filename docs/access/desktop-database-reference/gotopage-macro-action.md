---
title: GoToPage, action de macro
TOCTitle: GoToPage macro action
ms:assetid: 611aadff-83b7-e74d-4093-93fb5ce6e3ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194858(v=office.15)
ms:contentKeyID: 48545199
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm129285
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 9e4d7acd7c0f07f4d18a0a997c999cb877dbcb45
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626497"
---
# <a name="gotopage-macro-action"></a>GoToPage, action de macro

**S’applique à** : Access 2013, Office 2013

Utilisez l'action **AtteindrePage** pour placer le focus dans le formulaire actif sur le premier contrôle d'une page spécifique. Vous pouvez utiliser cette action si vous avez créé un formulaire contenant différents groupes d'informations connexes séparés par des sauts de page. Par exemple, un formulaire Employés peut contenir des informations personnelles sur une page, des informations professionnelles sur une autre page et des informations sur les ventes sur une troisième page. Vous pouvez utiliser l'action **AtteindrePage** pour vous placer sur la page de votre choix. Vous pouvez également présenter plusieurs pages d'informations sur un même formulaire en utilisant des contrôles Onglet.

## <a name="setting"></a>Paramètre

L’action **AtteindrePage** possède les arguments suivants.

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
<td><p><strong>Numéro de page</strong></p></td>
<td><p>Numéro de la page sur laquelle placer le focus. Entrez le numéro de la page dans la zone <strong>Numéro de page</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Si vous laissez cet argument vide, le focus reste sur la page active. Vous pouvez utiliser les arguments <strong>Droite</strong> et <strong>Bas</strong> pour afficher la partie de la page qui vous intéresse.</p></td>
</tr>
<tr class="even">
<td><p><strong>Right</strong></p></td>
<td><p>Position horizontale de la partie de la page, mesurée à partir du bord gauche de la fenêtre principale, qui doit apparaître sur le bord gauche de la fenêtre. Cet argument est obligatoire si l’argument <strong>Bas</strong> est spécifié.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Down</strong></p></td>
<td><p>Position verticale de la partie de la page, mesurée à partir du bord supérieur de la fenêtre principale, qui doit apparaître sur le bord supérieur de la fenêtre. Cet argument est obligatoire si l’argument <strong>Haut</strong> est spécifié.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Les arguments **Droite** et **Bas** sont mesurés en pouces ou en centimètres, selon les paramètres régionaux définis dans le Panneau de configuration de Windows.

## <a name="remarks"></a>Remarques

Vous pouvez utiliser cette action pour sélectionner le premier contrôle (comme défini par l’ordre de tabulation du formulaire) sur la page spécifiée. Utilisez l’action **AtteindreContrôle** pour vous placer dans un contrôle particulier sur le formulaire.

Vous pouvez utiliser les **arguments** **Droit** et Bas pour les formulaires dont les pages sont plus grandes que la fenêtre Access. Utilisez l'argument **Numéro de page** pour vous placer sur la page de votre choix, puis utilisez les arguments **Droite** et **Bas** pour afficher la partie de la page de votre choix. Access affiche la partie de la page dont l'angle supérieur gauche est décalé de la distance spécifiée de l'angle supérieur gauche de la page.

Vous pouvez utiliser l'action **AtteindrePage** dans les cas suivants :

- pour placer le focus sur une page dans un formulaire masqué ;

- pour placer le focus sur une autre page dans le contrôle Onglet.

Pour exécuter l'action **AtteindrePage** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **GoToPage** de l'objet **DoCmd**.

