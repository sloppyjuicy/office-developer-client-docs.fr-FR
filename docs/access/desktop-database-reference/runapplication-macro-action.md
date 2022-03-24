---
title: RunApplication, action de macro
TOCTitle: RunApplication macro action
ms:assetid: 29967e6e-c441-b115-3ee6-2299b8a3bc25
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192038(v=office.15)
ms:contentKeyID: 48543885
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm93359
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: b459c9027b407bb3bdf33f88d66db42c40b517e6
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63717375"
---
# <a name="runapplication-macro-action"></a>RunApplication, action de macro

**S’applique à** : Access 2013, Office 2013

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Note de sécurité" alt="Security note" /><strong>Note de sécurité</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Soyez prudent lors de l’exécution de fichiers ou de code exécutables dans les macros ou les applications. Les fichiers ou le code exécutables peuvent être utilisés pour effectuer des actions pouvant compromettre la sécurité de votre ordinateur et de vos données.</td>
</tr>
</tbody>
</table>

Vous pouvez utiliser l'action **ExécuterApplication** pour exécuter une application Microsoft Windows ou MS-DOS telle que Microsoft Office Excel, Microsoft Office Word ou Microsoft Office PowerPoint dans Microsoft Office Access. Vous pouvez, par exemple, souhaiter coller des données d'une feuille de calcul Excel dans votre base de données Access.

> [!NOTE]
> Cette action ne sera pas autorisée si la base de données n’est pas approuvée. 

## <a name="setting"></a>Setting

L’action **ExécuterApplication** utilise l’argument suivant :

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument de l’action</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Ligne de commande</strong></p></td>
<td><p>Ligne de commande est utilisé pour démarrer l’application (y compris le chemin d’accès et tous les paramètres nécessaires, tels que les commutateurs qui exécutent l’application dans un mode particulier). Tapez la ligne de commande dans la zone <strong>Ligne commande</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Cet argument est obligatoire.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

L'application sélectionnée avec cette action est chargée et s'exécute en avant-plan. La macro comprenant cette action continue de s'exécuter après avoir démarré l'application.

Vous pouvez transférer les données entre l'autre application et Access à l'aide de la fonctionnalité d'échange dynamique de données (DDE) Microsoft Windows ou le Presse-papiers. Vous pouvez utiliser l'action **EnvoiTouches** pour envoyer une séquence de touches à l'autre application (bien que l'échange dynamique de données soit plus efficace pour le transfert de données). Vous pouvez également partager des données entre applications à l'aide de l'automation.

Les applications MS-DOS sont exécutées dans une fenêtre MS-DOS au sein de l'environnement Windows.

Dans les systèmes d'exploitation Windows, il existe plusieurs façons d'exécuter une application, notamment en démarrant le programme à partir de l'Explorateur Windows, en utilisant la commande **Exécuter** du menu **Démarrer** ou en double-cliquant sur l'icône d'un programme dans le Bureau Windows.

Vous ne pouvez pas exécuter l'action **ExécuterApplication** dans un module Visual Basic pour Applications (VBA). Utilisez à la place la fonction **Shell** VBA.

