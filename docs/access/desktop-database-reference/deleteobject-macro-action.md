---
title: SupprimerObjet, action de macro
TOCTitle: DeleteObject Macro Action
ms:assetid: a8deb2a7-4e73-8696-b8c1-3a3939d813f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821415(v=office.15)
ms:contentKeyID: 48546912
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152112
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f9ac791ffd0f11c11358298570db833f8d561d11
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860937"
---
# <a name="deleteobject-macro-action"></a>SupprimerObjet, action de macro


**S’applique à**: Access 2013 | Office 2013

Utilisez l'action **SupprimerObjet** pour supprimer un objet de base de données spécifique.


> [!NOTE]
> [!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.

## <a name="setting"></a>Valeur

L'action **SupprimerObjet** possède les arguments suivants.

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
<td><p>Type d’objet à supprimer. Cliquez sur <strong>Table</strong>, <strong>Requête</strong>, <strong>Formulaire</strong>, <strong>État</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Page d’accès aux données</strong>, <strong>Vue serveur</strong>, <strong>Schéma</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong> dans la zone <strong>Type d’objet</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Pour supprimer l’objet sélectionné dans le volet de navigation, laissez cet argument vide.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nom de l'objet</strong></p></td>
<td><p>Nom de l’objet à supprimer. La zone <strong>Nom de l'objet</strong> regroupe tous les objets de la base de données ayant le type sélectionné par l'argument <strong>Type d'objet</strong>. Si vous laissez la zone <strong>Type d’objet</strong> vide, laissez cette zone vide également. Si vous exécutez une macro contenant l’action <strong>SupprimerObjet</strong> dans une base de données bibliothèque, Microsoft Office Access 2007 commence par rechercher un objet portant ce nom dans la base de données bibliothèque, puis dans la base de données active.</p></td>
</tr>
</tbody>
</table>



> [!WARNING]
> [!ATTENTION] Si vous laissez les zones **Type d'objet** et **Nom de l'objet** vides, Access supprime l'objet sélectionné dans le volet de navigation sans afficher de message d'avertissement lorsqu'il rencontre l'action **SupprimerObjet**.



## <a name="remarks"></a>Remarques

Vous pouvez utiliser l'action **SupprimerObjet** pour supprimer des objets temporaires créés pendant l'exécution de la macro. Par exemple, vous pouvez être amené à utiliser l'action **OuvrirRequête** pour exécuter une requête Création de table qui crée une table temporaire. Lorsque vous avez terminé d'utiliser la table temporaire, vous pouvez utiliser l'action **SupprimerObjet** pour la supprimer.

Cette action équivaut à sélectionner un objet dans le volet de navigation, puis à appuyer sur la touche Suppr ou encore, à cliquer avec le bouton droit sur l'objet dans le volet de navigation, puis à cliquer sur **Supprimer**.

Pour exécuter l'action **SupprimerObjet** dans un module Visual Basic pour Applications, vous pouvez utiliser la méthode **DeleteObject** de l'objet **DoCmd**.

