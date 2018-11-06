---
title: RepaintObject, action de macro
TOCTitle: RepaintObject macro action
ms:assetid: e8fa7d0b-578c-5071-2bd5-b772b48637a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836055(v=office.15)
ms:contentKeyID: 48548431
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm195788
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 69429aa0c623be06eae93a5e62fa06f1f0687007
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996460"
---
# <a name="repaintobject-macro-action"></a>RepaintObject, action de macro

**S’applique à**: Access 2013, Office 2013

Vous pouvez utiliser l'action **RedessinerObjet** pour effectuer les mises à jour d'écran en attente pour l'objet de base de données spécifié ou pour celui actif si aucun objet n'est spécifié. Ces mises à jour englobent les nouveaux calculs en attente des contrôles de l'objet.

## <a name="setting"></a>Valeur

L'action **RedessinerObjet** accepte les arguments suivants.

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
<td><p><strong>Type d'objet</strong></p></td>
<td><p>Type d’objet à redessiner. Cliquez sur <strong>Table</strong>, <strong>Requête</strong>, <strong>Formulaire</strong>, <strong>État</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Page d’accès aux données</strong>, <strong>Vue serveur</strong>, <strong>Schéma</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong> dans la zone <strong>Type d’objet</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Laissez cet argument vide pour sélectionner l’objet actif.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nom de l'objet</strong></p></td>
<td><p>Nom de l’objet à redessiner. La zone <strong>Nom de l’objet</strong> affiche tous les objets dans la base de données dont le type correspond à celui sélectionné par l’argument <strong>Type d’objet</strong>. Si vous laissez l’argument <strong>Type d’objet</strong> vide, laissez cet argument également vide.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

Pour achever des mises à jour d'écran en attente, Microsoft Office Access attend d'avoir terminé d'autres tâches en attente. Avec cette action, vous pouvez faire en sorte que tous les contrôles de l'objet spécifié soient immédiatement redessinés. Vous pouvez utiliser cette action dans les cas suivants :

- Lorsque vous utilisez l'action **DéfinirValeur** pour modifier des valeurs dans une série de contrôles. Access n'affiche pas toujours immédiatement les modifications, surtout si d'autres contrôles (tels que des contrôles calculés) dépendent des valeurs des contrôles modifiés.

- Lorsque vous voulez être certain que le formulaire affiché montre les données de tous ses contrôles. Par exemple, des contrôles contenant des objets OLE n'affichent pas immédiatement leurs données après que vous avez ouvert un formulaire.

> [!NOTE]
> - Dans la mesure où cette action n'entraîne pas de réactualisation de la base de données, elle n'affiche pas les enregistrements nouveaux et modifiés pas plus qu'elle ne supprime les enregistrements supprimés de la table ou requête sous-jacente de l'objet. Utilisez l'action **Actualiser** pour actualiser la source de l'objet ou l'un de ses contrôles. Utilisez l'action **AfficherTousEnreg** pour afficher les enregistrements les plus récents et supprimer tous les filtres.
> - L'action **RedessinerObjet** n'a pas le même effet que l'option **Actualiser** dans le groupe **Enregistrements** de l'onglet **Accueil**, laquelle affiche toutes les modifications que vous ou d'autres utilisateurs avez apportées aux enregistrements actuellement affichés dans des formulaires et des feuilles de données.

Pour exécuter l'action **RedessinerObjet** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **RepaintObject** de l'objet **DoCmd**.

