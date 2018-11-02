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
ms.openlocfilehash: 254a54b4b672ba9e40253e3bd95283eec655d3dc
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920507"
---
# <a name="showtoolbar-macro-action"></a>ShowToolbar, action de macro


**S’applique à**: Access 2013, Office 2013

L'action **AfficherBarreOutils** permet d'afficher ou de masquer un groupe de commandes sous l'onglet **Compléments**.


> [!NOTE]
> <P>[!REMARQUE] L'action <STRONG>AfficherBarreOutils</STRONG> n'affecte pas les menus contextuels.</P>




> [!NOTE]
> <P>[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.</P>



## <a name="setting"></a>Valeur

L'action **AfficherBarreOutils** utilise les arguments suivants :

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
<td><p>Le nom du groupe de commandes sous l’onglet <strong>Compléments</strong> que vous souhaitez afficher ou masquer. La zone <strong>Nom de la barre d’outils</strong> dans la section <strong>Arguments de l’Action</strong> du volet Générateur de Macro affiche tous les groupes disponibles qui peuvent être affectées par cette action. Cet argument est obligatoire. Si vous exécutez une macro contenant l’action <strong>AfficherBarreOutils</strong> dans une base de données bibliothèque, Access recherche un groupe portant ce nom, d’abord dans la base de données bibliothèque, puis dans la base de données active.</p></td>
</tr>
<tr class="even">
<td><p><strong>Show</strong></p></td>
<td><p>Spécifie s’il faut afficher ou masquer le groupe et dans les modes d’affichage pour afficher ou masquer. La valeur par défaut est <strong>Oui</strong> (afficher le groupe en permanence). Vous pouvez sélectionner <strong>Oui</strong> pour afficher le groupe à toutes les heures <strong>Où approprié</strong> pour afficher le groupe uniquement lorsque le formulaire adéquat ou l’état est actif, ou <strong>non</strong> pour masquer le groupe en permanence.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Utilisez cette action dans une macro avec des expressions conditionnelles pour afficher ou masquer un groupe sous certaines conditions.

Si vous voulez afficher un groupe spécifique dans un seul formulaire ou état, vous pouvez définir la propriété **SurActivé** de ce formulaire ou état sur le nom d'une macro contenant une action **AfficherBarreOutils** pour afficher le groupe. Définissez ensuite la propriété **SurDésactivé** du formulaire ou de l'état sur le nom d'une macro contenant une action **AfficherBarreOutils** pour masquer le groupe.

Les barres d'outils prédéfinies ne permettent ni d'afficher, ni de masquer des éléments via cette action si vous avez défini la propriété **AllowBuiltInToolbars** sur **False** (0) dans un module Visual Basic pour Applications (VBA), ou si vous avez défini l'option **Afficher les barres d'outils intégrées** sur **False** dans VBA, via la méthode **SetOption**.

Pour exécuter l'action **AfficherBarreOutils** dans un module VBA, utilisez la méthode **ShowToolbar** de l'objet **DoCmd**.

