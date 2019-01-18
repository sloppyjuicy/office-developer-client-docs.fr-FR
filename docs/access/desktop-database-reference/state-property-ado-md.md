---
title: State, propriété (ADO MD)
TOCTitle: State property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 051a9f0cc50ae3a60edb033f6807f72fc0688976
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702445"
---
# <a name="state-property-ado-md"></a>State, propriété (ADO MD)


**S’applique à**: Access 2013, Office 2013

Indique l'état actuel de l'ensemble de cellules.

## <a name="return-values"></a>Valeurs de retour

Retourne un entier de type **Long** qui indique la condition actuelle de l'objet [Cellset](cellset-object-ado-md.md) et est en lecture seule. Les valeurs suivantes sont valides : **adStateClosed** (0) et **adStateOpen** (1).

## <a name="remarks"></a>Notes

Pour utiliser les noms des constantes [ObjectStateEnum](objectstateenum.md) la bibliothèque de types ADO doit être référencée dans votre projet. Pour plus d'informations, consultez [Utilisation d'ADO avec ADO MD](using-ado-with-ado-md.md).

