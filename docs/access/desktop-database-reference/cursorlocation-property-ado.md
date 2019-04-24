---
title: CursorLocation, propriété (ADO)
TOCTitle: CursorLocation property (ADO)
ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15)
ms:contentKeyID: 48546182
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25fd81acee3c541c8a3f315f96fa69241272a655
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295219"
---
# <a name="cursorlocation-property-ado"></a>CursorLocation, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique l'emplacement du service de curseur.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de type **Long** qui peut être définie sur l’une des valeurs de [CursorLocationEnum](cursorlocationenum.md).

## <a name="remarks"></a>Remarques

Cette propriété permet de choisir l'une des différentes bibliothèques de curseurs accessibles au fournisseur. En général, vous pouvez choisir une bibliothèque de curseurs côté client ou une bibliothèque située sur le serveur.

Le paramètre de cette propriété n'affecte que les connexions établies après que la définition de la propriété. La modification de la propriété **CursorLocation** n'a aucun effet sur les connexions existantes.

Les curseurs renvoyés par la méthode [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) héritent de ce paramètre. Les objets **Recordset** héritent automatiquement ce paramètre de leurs connexions associées.

Cette propriété est en lecture/écriture dans un objet [Connection](connection-object-ado.md) ou un objet [Recordset](recordset-object-ado.md) fermé, et en lecture seule dans un objet **Recordset** ouvert.

**Utilisation des services de données à distance** Lorsqu'elle est utilisée sur un objet **Recordset** ou **Connection** côté client, la propriété **CursorLocation** peut uniquement être définie sur **adUseClient**.

