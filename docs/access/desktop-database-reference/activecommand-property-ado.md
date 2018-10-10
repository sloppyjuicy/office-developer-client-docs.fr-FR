---
title: ActiveCommand, propriété (ADO)
TOCTitle: ActiveCommand Property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f01ae4c821d8beb6c8de84c7ed671a373d7372c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471960"
---
# <a name="activecommand-property-ado"></a>ActiveCommand, propriété (ADO)


**S’applique à**: Access 2013 | Office 2013

Indique l'objet [Command](command-object-ado.md) qui a créé l'objet [Recordset](recordset-object-ado.md) associé.

## <a name="return-value"></a>Valeur de retour

Renvoie une valeur de type **Variant** qui contient un objet **Command**. La valeur par défaut est une référence d'objet Null.

## <a name="remarks"></a>Notes

La propriété **ActiveCommand** est en lecture seule.

Si un objet **Command** n'a pas été utilisé pour créer l'objet **Recordset** actif, une référence d'objet **Null** est renvoyée.

Utilisez cette propriété pour rechercher l'objet **Command** associé lorsque vous ne recevez que l'objet **Recordset** qui en résulte.

