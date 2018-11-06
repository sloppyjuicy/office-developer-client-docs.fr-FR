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
ms.openlocfilehash: b04870a416874e2136e21b40c62d8e64a6182efe
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998545"
---
# <a name="opendiagram-macro-action"></a>OpenDiagram, action de macro

**S’applique à**: Access 2013, Office 2013

Dans un projet Access, vous pouvez utiliser l'action **OuvrirSchéma** pour ouvrir un schéma de base de données en mode Création.

> [!NOTE]
> [!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. 

## <a name="setting"></a>Paramètre

L'action **OuvrirSchéma** possède l'argument suivant.

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
<td><p>Le nom du schéma de base de données à ouvrir. La zone <strong>Nom du schéma</strong> dans la section <strong>Arguments de l’Action</strong> du volet Générateur de Macro affiche tous les schémas de base de données dans la base de données en cours. Cet argument est obligatoire. Si vous exécutez une macro contenant l’action <strong>OuvrirSchéma</strong> dans une base de données bibliothèque, Microsoft Access recherche d’abord le schéma portant ce nom dans la base de données bibliothèque, puis dans la base de données active.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Notes

Cette action équivaut à double-cliquer sur un schéma de base de données dans le volet de navigation ou à cliquer avec le bouton droit sur le schéma de base de données dans le volet de navigation, puis à cliquer sur **Mode Création**.

> [!TIP]
> [!CONSEIL] Vous pouvez faire glisser un schéma de base de données depuis le volet de navigation vers une ligne d'action de macro. Ceci crée automatiquement une action **OuvrirSchéma** qui ouvre le schéma de base de données en mode Création.

Pour exécuter l'action **OuvrirSchéma** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **OpenDiagram** de l'objet **DoCmd**.

