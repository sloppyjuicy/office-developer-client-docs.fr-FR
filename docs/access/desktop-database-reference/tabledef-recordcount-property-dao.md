---
title: TableDef.RecordCount, propriété (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d73d4ce60757b7c9ca4758a6957dd9f176666757
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585178"
---
# <a name="tabledefrecordcount-property-dao"></a>TableDef.RecordCount, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Renvoie le nombre total d'enregistrements dans un objet **[TableDef](tabledef-object-dao.md)**. Type de données **Long** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* .RecordCount

*expression* Variable représentant un objet **TableDef**.

## <a name="remarks"></a>Remarques

A **jeu d’enregistrements** ou **TableDef** de l’objet sans enregistrement contient un **RecordCount** paramètre de la propriété de 0.

Lorsque vous travaillez avec des objets **TableDef** liés, la valeur de la propriété **RecordCount** est toujours égale à –1.

