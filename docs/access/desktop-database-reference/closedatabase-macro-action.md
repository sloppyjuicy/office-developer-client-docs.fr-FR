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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714436"
---
# <a name="closedatabase-macro-action"></a>CloseDatabase, action de macro


**S’applique à**: Access 2013, Office 2013

Vous pouvez utiliser l'action **FermerBaseDonnées** pour fermer la base de données active.

## <a name="setting"></a>Valeur

L'action **FermerBaseDonnées** ne possède aucun argument.

## <a name="remarks"></a>Remarques

  - Access n'exécute aucune action indiquée à la suite de l'action **FermerBaseDonnées** dans une macro.

  - Cette action a le même effet que l’onglet **fichier** , puis cliquez sur **Fermer de la base de données**. Si la base de données contient des objets qui n'ont pas été enregistrés lorsque vous exécutez l'action **FermerBaseDonnées**, des boîtes de dialogue identiques à celles qui s'affichent lorsque vous cliquez sur **Fermer la base de données** apparaissent.

  - Pour exécuter l'action **FermerBaseDonnées** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **CloseDatabase** de l'objet **DoCmd**.

