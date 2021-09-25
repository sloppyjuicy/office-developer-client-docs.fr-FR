---
title: ActiveCommand, propriété (ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ab0bee62d55b11ce9a35e08cecf814cb4d75d5a4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586319"
---
# <a name="activecommand-property-ado"></a>ActiveCommand, propriété (ADO)

**S’applique à** : Access 2013, Office 2013

Indique l'objet [Command](command-object-ado.md) qui a créé l'objet [Recordset](recordset-object-ado.md) associé.

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur de type **Variant** qui contient un objet **Command**. La valeur par défaut est une référence d'objet Null.

## <a name="remarks"></a>Remarques

La propriété  **ActiveCommand** est en lecture seule.

Si un **objet Command** n’a pas été utilisé pour créer l’objet **Recordset** actuel, une référence d’objet **Null** est renvoyée.

Utilisez cette propriété pour rechercher l'objet **Command** associé lorsque vous ne recevez que l'objet **Recordset** qui en résulte.

