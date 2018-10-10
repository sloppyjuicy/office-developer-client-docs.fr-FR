---
title: CursorLocation, propriété (ADO)
TOCTitle: CursorLocation Property (ADO)
ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15)
ms:contentKeyID: 48546182
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9805b032a0e1a203d2a4057fb74757826a2a47b4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470885"
---
# <a name="cursorlocation-property-ado"></a>CursorLocation, propriété (ADO)


**S’applique à**: Access 2013 | Office 2013

Indique l'emplacement du service de curseur.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de type **Long** qui peut être définie sur l'une des valeurs de [CursorLocationEnum](cursorlocationenum.md).

## <a name="remarks"></a>Notes

Cette propriété permet de choisir l'une des différentes bibliothèques de curseurs accessibles au fournisseur. En général, vous pouvez choisir une bibliothèque de curseurs côté client ou une bibliothèque située sur le serveur.

Le paramètre de cette propriété n'affecte que les connexions établies après que la définition de la propriété. La modification de la propriété **CursorLocation** n'a aucun effet sur les connexions existantes.

Les curseurs renvoyés par la méthode [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) héritent de ce paramètre. Les objets **Recordset** héritent automatiquement ce paramètre de leurs connexions associées.

Cette propriété est en lecture/écriture dans un objet [Connection](connection-object-ado.md) ou un objet [Recordset](recordset-object-ado.md) fermé, et en lecture seule dans un objet **Recordset** ouvert.

**L’utilisation du Service de données à distance** Lorsqu’elle est utilisée sur un côté client **Recordset** ou un objet **Connection** , la propriété **CursorLocation** peut uniquement être définie **adUseClient**.

