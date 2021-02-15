---
title: OpenDiagram, action de macro
TOCTitle: OpenDiagram macro action
ms:assetid: 408e7224-02bb-335a-b1b9-cbccbf6e36ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192875(v=office.15)
ms:contentKeyID: 48544427
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm154095
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f4273d6858ad98b723d66ba32fe3b9aa7c902d31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288356"
---
# <a name="opendiagram-macro-action"></a>OpenDiagram, action de macro

**S’applique à** : Access 2013, Office 2013

Dans un projet Access, vous pouvez utiliser l'action **OuvrirSchéma** pour ouvrir un schéma de base de données en mode Création.

> [!NOTE]
> Cette action ne sera pas autorisée si la base de données n’est pas approuvée. 

## <a name="setting"></a>Setting

L’action **OuvrirSchéma** possède l’argument suivant.

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
<td><p><strong>Nom du schéma</strong></p></td>
<td><p>Nom du schéma de base de données à ouvrir. La zone <strong>Nom du schéma</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro affiche tous les schémas de base de données de la base de données active. Cet argument est obligatoire. Si vous exécutez une macro contenant l’action <strong>OuvrirSchéma</strong> dans une base de données bibliothèque, Microsoft Access recherche d’abord le schéma portant ce nom dans la base de données bibliothèque, puis dans la base de données active.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Remarques

Cette action équivaut à double-cliquer sur un schéma de base de données dans le volet de navigation ou à cliquer avec le bouton droit sur le schéma de base de données dans le volet de navigation, puis à cliquer sur **Mode Création**.

> [!TIP]
> [!CONSEIL] Vous pouvez faire glisser un schéma de base de données depuis le volet de navigation vers une ligne d'action de macro. Ceci crée automatiquement une action **OuvrirSchéma** qui ouvre le schéma de base de données en mode Création.

Pour exécuter l'action **OuvrirSchéma** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **OpenDiagram** de l'objet **DoCmd**.

