---
title: ShowToolbar, action de macro
TOCTitle: ShowToolbar macro action
ms:assetid: 9e53009b-1e5e-1bee-3bcc-f82dc1b0dc48
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198288(v=office.15)
ms:contentKeyID: 48546649
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm27417
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 01ba59ce0898068788adb9269b3203794d1f31d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306474"
---
# <a name="showtoolbar-macro-action"></a>ShowToolbar, action de macro

**S’applique à** : Access 2013, Office 2013

L'action **AfficherBarreOutils** permet d'afficher ou de masquer un groupe de commandes sous l'onglet **Compléments**.

> [!NOTE]
> - [!REMARQUE] L'action **AfficherBarreOutils** n'affecte pas les menus contextuels.
> - Cette action ne sera pas autorisée si la base de données n’est pas approuvée. 

## <a name="setting"></a>Setting

L’action **AfficherBarreOutils** utilise les arguments suivants :

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
<td><p><strong>Nom de la barre d’outils</strong></p></td>
<td><p>Nom du groupe de commandes de l’onglet <strong>Compléments</strong> que vous souhaitez afficher ou masquer. Le champ <strong>Nom de la barre d’outils</strong> de la section <strong>Arguments de l’action</strong> du Générateur de macro présente tous les groupes disponibles pouvant être affectés par cette action. Cet argument est obligatoire. Si vous exécutez une macro contenant l’action <strong>AfficherBarreOutils</strong> dans une base de données bibliothèque, Access recherche un groupe portant ce nom, d’abord dans la base de données bibliothèque, puis dans la base de données active.</p></td>
</tr>
<tr class="even">
<td><p><strong>Show</strong></p></td>
<td><p>Indique si le groupe doit être affiché ou masqué, et dans quel mode d’affichage. La valeur par défaut <strong>est Oui</strong> (afficher le groupe en permanence). Vous pouvez <strong></strong> sélectionner Oui pour afficher le groupe à tout <strong>moment,</strong> Le cas échéant <strong></strong> pour afficher le groupe uniquement lorsque le formulaire ou l’état approprié est actif, ou Non pour masquer le groupe à tout moment.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Utilisez cette action dans une macro avec des expressions conditionnelles pour afficher ou masquer un groupe sous certaines conditions.

Si vous voulez afficher un groupe spécifique dans un seul formulaire ou état, vous pouvez définir la propriété **SurActivé** de ce formulaire ou état sur le nom d'une macro contenant une action **AfficherBarreOutils** pour afficher le groupe. Définissez ensuite la propriété **SurDésactivé** du formulaire ou de l'état sur le nom d'une macro contenant une action **AfficherBarreOutils** pour masquer le groupe.

Les barres d'outils prédéfinies ne permettent ni d'afficher, ni de masquer des éléments via cette action si vous avez défini la propriété **AllowBuiltInToolbars** sur **False** (0) dans un module Visual Basic pour Applications (VBA), ou si vous avez défini l'option **Afficher les barres d'outils intégrées** sur **False** dans VBA, via la méthode **SetOption**.

Pour exécuter l'action **AfficherBarreOutils** dans un module VBA, utilisez la méthode **ShowToolbar** de l'objet **DoCmd**.

