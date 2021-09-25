---
title: SaveObject, action de macro
TOCTitle: SaveObject macro action
ms:assetid: 85716dfc-f76f-ca47-cc40-f8f88162f85a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196789(v=office.15)
ms:contentKeyID: 48546060
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm116962
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: eb5ec32eadaf99732758860976aa59c4a29ef6c2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593641"
---
# <a name="saveobject-macro-action"></a>SaveObject, action de macro

**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser l'action **EnregistrerObjet** pour enregistrer un objet Access spécifié ou l'objet actif si aucun n'est spécifié. Vous pouvez également enregistrer l'objet actif sous un nouveau nom dans certains cas (cela équivaut à utiliser la commande **Enregistrer sous** dans la **barre d'outils Accès rapide**).

> [!NOTE]
> Cette action ne sera pas autorisée si la base de données n’est pas approuvée. 

## <a name="setting"></a>Paramètre

L’action **EnregistrerObjet** utilise les arguments suivants :

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
<td><p><strong>Type d’objet</strong></p></td>
<td><p>Type d’objet à enregistrer. Cliquez sur <strong>Table</strong>, <strong>Requête</strong>, <strong>Formulaire</strong>, <strong>État</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Page d’accès aux données</strong>, <strong>Vue serveur</strong>, <strong>Schéma</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong> dans la zone <strong>Type d’objet</strong> de la section <strong>Arguments de l’action</strong> dans le volet Générateur de macro. Pour sélectionner l’objet actif, laissez cet argument vide. Si vous sélectionnez un type d’objet, vous devez sélectionner un nom d’objet existant dans l’argument <strong>Nom de l’objet</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nom de l’objet</strong></p></td>
<td><p>Nom de l’objet à enregistrer. La zone <strong>Nom de l’objet</strong> montre tous les objets de la base de données du type sélectionné par l’argument <strong>Type d’objet</strong>. Si vous ne spécifiez rien dans l’argument <strong>Type d’objet</strong>, vous pouvez laisser cet argument vide pour enregistrer l’objet actif ou, dans certains cas, entrer un nouveau nom dans cet argument pour enregistrer l’objet actif sous ce nom. Si vous entrez un nouveau nom, ce dernier doit respecter les conventions d’appellation des objets Microsoft Office Access.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

L'action **EnregistrerObjet** s'applique à tous les objets de base de données que l'utilisateur peut explicitement ouvrir et enregistrer. L'objet spécifié doit être ouvert pour que l'action **EnregistrerObjet** puisse être appliquée à celui-ci. Cette action équivaut à sélectionner un objet puis à l'enregistrer en cliquant sur **Enregistrer** dans la **barre d'outils Accès rapide**. 

En laissant l'argument **Type d'objet** vide et en spécifiant un nouveau nom dans l'argument **Nom de l'objet**, vous obtenez le même résultat qu'en cliquant sur **Enregistrer sous** dans la **barre d'outils Accès rapide** et en indiquant un nouveau nom pour l'objet actif. L'utilisation de l'action **EnregistrerObjet** vous permet de spécifier un objet à enregistrer et d'exécuter une commande **Enregistrer sous** à partir d'une macro.

> [!NOTE]
> [!REMARQUE] Vous ne pouvez pas utiliser l'action **EnregistrerObjet** pour enregistrer un des éléments suivants sous un nouveau nom :
> - Formulaire en mode Formulaire ou en mode Feuille de données
> - Un rapport en mode Aperçu avant impression
> - Un module
> - Affichage serveur en mode Feuille de données ou Aperçu avant impression
> - Page d’accès aux données en affichage Page
> - Un tableau en mode Feuille de données ou Aperçu avant impression
> - Requête en mode Feuille de données ou Aperçu avant impression
> - Procédure stockée en mode Feuille de données ou Aperçu avant impression

L'action **EnregistrerObjet** enregistre toujours l'objet spécifié ou l'objet actif dans la base de données qui a servi à créer l'objet, que cette action soit effectuée dans une macro exécutée dans la base de données active ou une base de données bibliothèque.

Si vous enregistrez l'objet actif sous un nouveau nom mais si ce nom est identique à celui d'un objet existant du même type, une boîte de dialogue vous demande si vous souhaitez remplacer l'objet existant. Si vous avez sélectionné la valeur **Non** pour l'argument **Avertissements actifs** de l'action **Avertissements**, la boîte de dialogue n'est pas affichée et l'ancien objet est automatiquement remplacé.

Pour exécuter l'action **EnregistrerObjet** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Save** de l'objet **DoCmd**.

