---
title: RunCode, action de macro
TOCTitle: RunCode macro action
ms:assetid: cb0625be-4b5d-4927-9b0e-59a6e411b5bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834373(v=office.15)
ms:contentKeyID: 48547706
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98700
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 646c1393cc798c1f827e6ceaebf46bfe7c87bcbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306831"
---
# <a name="runcode-macro-action"></a>RunCode, action de macro

**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser l’action **ExécuterCode** pour appeler une procédure Function Visual Basic pour Applications (VBA).

## <a name="setting"></a>Paramètre

L’action **ExécuterCode** accepte l’argument suivant.

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
<td><p><strong>Nom de la fonction</strong></p></td>
<td><p>Nom de la procédure Function VBA à appeler. Placez tous les arguments de la fonction entre parenthèses. Entrez le nom de la fonction dans la zone <strong>Nom fonction</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Cet argument est obligatoire.</p><p><strong>REMARQUE</strong>: dans une base de données Access (.mdb ou .accdb), cliquez sur le bouton Créer pour utiliser le Générateur d’expression afin de sélectionner une fonction pour cet argument. <strong></strong> Cliquez sur la fonction de votre choix dans la liste proposée par le Générateur d’expression.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Les procédures Function définies par l'utilisateur sont stockées dans des modules Microsoft Access.

Vous devez inclure des parenthèses, même si la procédure Function ne prend aucun argument, comme dans l'exemple suivant :

`TestFunction()`

Contrairement aux noms de fonction définis par l’utilisateur  utilisés pour les paramètres de propriété d’événement, le nom de la fonction dans l’argument Nom de la fonction ne commence pas par un signe égal ( **=** ).

Access ignore la valeur renvoyée par la fonction.

> [!NOTE]
> [!REMARQUE] Vous ne pouvez pas appeler une procédure Function à partir d'une macro si le nom de la fonction est identique à celui du module.

> [!TIP]
> [!CONSEIL] Pour exécuter une procédure Sub ou une procédure événementielle rédigée en Visual Basic, créez une procédure Function qui appelle la procédure Sub ou la procédure événementielle. Ensuite, utilisez l'action **ExécuterCode** pour exécuter la procédure Function.

Si vous utilisez l'action **ExécuterCode** pour appeler une fonction, Access recherche la fonction correspondant au nom spécifié par l'argument **Nom fonction** dans les modules standard de la base de données. Toutefois, lorsque cette action est exécutée en réponse à un clic d'une commande de menu dans un formulaire ou un état ou en réponse à un événement d'un formulaire ou d'un état, Access recherche d'abord la fonction dans le module de classe du formulaire ou de l'état, puis dans les modules standard. Access n'effectue pas de recherche dans les modules de classe affichés dans la zone **Modules** du volet de navigation pour la fonction spécifiée par l'argument **Nom fonction**.

Cette action n'est pas disponible dans un module VBA. À la place, exécutez la procédure Function requise directement dans VBA.

