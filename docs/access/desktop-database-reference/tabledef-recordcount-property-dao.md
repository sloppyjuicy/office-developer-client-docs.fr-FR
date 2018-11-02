---
title: Propriété TableDef.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4b24aaa5aec9b17adc169c67733a19a9077a4930
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920920"
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

