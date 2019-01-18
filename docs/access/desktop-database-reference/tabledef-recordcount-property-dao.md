---
title: Propriété TableDef.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5eb9588927c9e35fea54964f16150735a7374cd5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722864"
---
# <a name="tabledefrecordcount-property-dao"></a>Propriété TableDef.RecordCount (DAO)


**S’applique à**: Access 2013, Office 2013

Renvoie le nombre total d'enregistrements dans un objet **[TableDef](tabledef-object-dao.md)**. Type de données **Long** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . RecordCount

*expression* Variable qui représente un objet **TableDef** .

## <a name="remarks"></a>Remarques

Un objet **Recordset** ou **TableDef** sans enregistrements a une valeur de propriété **RecordCount** égale à 0.

Lorsque vous travaillez avec des objets **TableDef** liés, la valeur de la propriété **RecordCount** est toujours égale à –1.

