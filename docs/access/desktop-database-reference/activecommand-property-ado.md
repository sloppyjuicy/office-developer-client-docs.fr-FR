---
title: ActiveCommand, propriété (ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 18fa38176f7174f27b46604c6182dfbdaa422f06
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705294"
---
# <a name="activecommand-property-ado"></a>ActiveCommand, propriété (ADO)

**S’applique à**: Access 2013, Office 2013

Indique l'objet [Command](command-object-ado.md) qui a créé l'objet [Recordset](recordset-object-ado.md) associé.

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur de type **Variant** qui contient un objet **Command**. La valeur par défaut est une référence d'objet Null.

## <a name="remarks"></a>Notes

La propriété **ActiveCommand** est en lecture seule.

Si un objet **Command** n’était utilisé pour créer l' **objet Recordset**actif, une référence d’objet **Null** est renvoyée.

Utilisez cette propriété pour rechercher l'objet **Command** associé lorsque vous ne recevez que l'objet **Recordset** qui en résulte.

