---
title: CloseDatabase, action de macro
TOCTitle: CloseDatabase macro action
ms:assetid: c4b4278d-932c-99f6-da2d-8953109b44b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823085(v=office.15)
ms:contentKeyID: 48547598
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ac29cbdae8c162a992f2763530514150ca0240ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296296"
---
# <a name="closedatabase-macro-action"></a>CloseDatabase, action de macro


**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser l’action **FermerBaseDonnées** pour fermer la base de données active.

## <a name="setting"></a>Setting

L’action **FermerBaseDonnées** ne possède aucun argument.

## <a name="remarks"></a>Remarques

  - Access n’exécute aucune action indiquée à la suite de l’action **FermerBaseDonnées** dans une macro.

  - Cette action équivaut à cliquer sur l'onglet **fichier** , puis à cliquer sur **Fermer la base de données**. Si la base de données contient des objets qui n'ont pas été enregistrés lorsque vous exécutez l'action **FermerBaseDonnées**, des boîtes de dialogue identiques à celles qui s'affichent lorsque vous cliquez sur **Fermer la base de données** apparaissent.

  - Pour exécuter l'action **FermerBaseDonnées** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **CloseDatabase** de l'objet **DoCmd**.

