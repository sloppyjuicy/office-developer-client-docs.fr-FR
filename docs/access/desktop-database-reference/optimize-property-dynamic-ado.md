---
title: Optimize, propriété dynamique (ADO)
TOCTitle: Optimize dynamic property (ADO)
ms:assetid: 2253b052-2d8a-f6f0-f8b8-f56e79d243de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249001(v=office.15)
ms:contentKeyID: 48543705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4a1fff5911080811bc2556a20667ff2f2391f22e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926779"
---
# <a name="optimize-dynamic-property-ado"></a>Optimize, propriété dynamique (ADO)


**S’applique à**: Access 2013, Office 2013

Indique s'il est nécessaire de créer un index sur un champ.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur **booléenne** indiquant si un index doit être créé.

## <a name="remarks"></a>Remarques

Un index peut améliorer les performances des opérations de recherche ou de tri des valeurs d'un objet [Recordset](recordset-object-ado.md). L'index est interne à ADO : vous ne pouvez pas y accéder explicitement ni l'utiliser dans votre application.

Pour créer un index sur un champ, donnez à la propriété **Optimize** la valeur **True**. Pour supprimer l'index, donnez à cette propriété la valeur **False**.

**Optimize** est une propriété dynamique ajoutée à la collection [Properties](field-object-ado.md) de l'objet [Field](properties-collection-ado.md) lorsque la valeur de la propriété [CursorLocation](cursorlocation-property-ado.md) est **adUseClient**.

**Utilisation**

```vb
    Dim rs As New Recordset
    Dim fld As Field
    rs.CursorLocation = adUseClient      'Enable index creation
    rs.Fields.Append "Field1", adChar, 35, adFldIsNullable
    rs.Open
    Set fld = rs.Fields(0)
    fld.Properties("Optimize") = True    'Create an index
    fld.Properties("Optimize") = False   'Delete an index
```
