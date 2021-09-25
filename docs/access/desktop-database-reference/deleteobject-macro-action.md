---
title: DeleteObject, action de macro
TOCTitle: DeleteObject macro action
ms:assetid: a8deb2a7-4e73-8696-b8c1-3a3939d813f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821415(v=office.15)
ms:contentKeyID: 48546912
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152112
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 32fcab6018adcdb40af56788a036154ce99a8ca6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553122"
---
# <a name="deleteobject-macro-action"></a>DeleteObject, action de macro

**S’applique à** : Access 2013, Office 2013

Utilisez l'action **SupprimerObjet** pour supprimer un objet de base de données spécifique.

> [!NOTE]
> Cette action ne sera pas autorisée si la base de données n’est pas approuvée. 

## <a name="setting"></a>Paramètre

L’action **SupprimerObjet** possède les arguments suivants.

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
<td><p>Type d’objet à supprimer. Cliquez sur <strong>Table</strong>, <strong>Requête</strong>, <strong>Formulaire</strong>, <strong>État</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Page d’accès aux données</strong>, <strong>Vue serveur</strong>, <strong>Schéma</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong> dans la zone <strong>Type d’objet</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Pour supprimer l’objet sélectionné dans le volet de navigation, laissez cet argument vide.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nom de l’objet</strong></p></td>
<td><p>Nom de l’objet à supprimer. La zone <strong>Nom de l’objet</strong> affiche tous les objets de la base de données correspondant au type sélectionné par l’argument <strong>Type d’objet</strong>. Si vous laissez la zone <strong>Type d’objet</strong> vide, laissez également celle-ci vide. Si vous exécutez une macro contenant l’action <strong>SupprimerObjet</strong> dans une base de données bibliothèque, Microsoft Office Access 2007 commence par rechercher un objet portant ce nom dans la base de données bibliothèque, puis dans la base de données active.</p></td>
</tr>
</tbody>
</table>

> [!WARNING]
> [!ATTENTION] Si vous laissez les zones **Type d'objet** et **Nom de l'objet** vides, Access supprime l'objet sélectionné dans le volet de navigation sans afficher de message d'avertissement lorsqu'il rencontre l'action **SupprimerObjet**.

## <a name="remarks"></a>Remarques

Vous pouvez utiliser l'action **SupprimerObjet** pour supprimer des objets temporaires créés pendant l'exécution de la macro. Par exemple, vous pouvez être amené à utiliser l'action **OuvrirRequête** pour exécuter une requête Création de table qui crée une table temporaire. Lorsque vous avez terminé d'utiliser la table temporaire, vous pouvez utiliser l'action **SupprimerObjet** pour la supprimer.

Cette action équivaut à sélectionner un objet dans le volet de navigation, puis à appuyer sur la touche Suppr ou encore, à cliquer avec le bouton droit sur l'objet dans le volet de navigation, puis à cliquer sur **Supprimer**.

Pour exécuter l'action **SupprimerObjet** dans un module Visual Basic pour Applications, vous pouvez utiliser la méthode **DeleteObject** de l'objet **DoCmd**.

