---
title: TableDef.RecordCount, propriété (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5eb9588927c9e35fea54964f16150735a7374cd5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314286"
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

