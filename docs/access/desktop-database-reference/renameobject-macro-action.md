---
title: RenameObject, action de macro
TOCTitle: RenameObject macro action
ms:assetid: fee04eb0-23c0-5d57-b903-e1ae54f2d25e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837293(v=office.15)
ms:contentKeyID: 48548948
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165893
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ce16b86ea06e041d490d0c68917daf18bd80dbb6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698385"
---
# <a name="renameobject-macro-action"></a>RenameObject, action de macro

**S’applique à**: Access 2013, Office 2013

Vous pouvez utiliser l'action **RenommerObjet** pour renommer un objet de base de données spécifique.

> [!NOTE]
> [!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée.

## <a name="setting"></a>Valeur

L'action **RenommerObjet** utilise les arguments suivants :

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
<td><p><strong>Nouveau nom</strong></p></td>
<td><p>Nouveau nom pour l’objet de base de données. Entrez le nom de l’objet dans la zone <strong>Nouveau nom</strong> de la section <strong>Arguments de l’action</strong> dans le volet Générateur de macro. Cet argument est obligatoire.</p></td>
</tr>
<tr class="even">
<td><p><strong>Type d'objet</strong></p></td>
<td><p>Type d’objet que vous voulez renommer. Cliquez sur <strong>Table</strong>, <strong>Requête</strong>, <strong>Formulaire</strong>, <strong>État</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Page d’accès aux données</strong>, <strong>Vue serveur</strong>, <strong>Schéma</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong>. Pour renommer l’objet sélectionné dans le volet de navigation, laissez cet argument vide.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Ancien nom</strong></p></td>
<td><p>Nom de l’objet à renommer. La zone <strong>Ancien nom</strong> affiche tous les objets dans la base de données dont le type correspond à celui sélectionné par l’argument <strong>Type d’objet</strong>. Si vous laissez l’argument <strong>Type d’objet</strong> vide, laissez cet argument également vide. 

</p><p><strong>Remarque</strong>: Si vous exécutez une macro contenant l’action <STRONG>Renommer</STRONG> dans une base de données bibliothèque, Microsoft Access recherche d’abord l’objet portant ce nom dans la base de données bibliothèque, puis dans la base de données en cours.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

Le nouveau nom de l'objet de base de données doit respecter les conventions d'appellation standard pour les objets Access.

Vous ne pouvez pas renommer un objet ouvert.

Si vous laissez les arguments **Type d'objet** et **Ancien nom** vides, Access renomme l'objet sélectionné dans le volet de navigation. Pour sélectionner un objet dans le volet de navigation, vous pouvez utiliser l'action **SélectionnerObjet** en attribuant la valeur **Oui** à l'argument **Dans le volet de navigation**.

Vous pouvez également renommer un objet en cliquant avec le bouton droit sur celui-ci dans le volet de navigation, en cliquant sur **RenommerObjet** et en indiquant un nouveau nom. Avec l'action **Renommer**, vous ne devez pas d'abord sélectionner l'objet dans le volet de navigation ni arrêter la macro pour entrer le nouveau nom.

Cette action diffère de l'action **CopierObjet** qui crée une copie de l'objet sous un nouveau nom.

Pour exécuter l'action **RenommerObjet** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Rename** de l'objet **DoCmd**.

