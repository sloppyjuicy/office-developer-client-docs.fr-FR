---
title: DataSource, propriété (ADO)
TOCTitle: DataSource property (ADO)
ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15)
ms:contentKeyID: 48545087
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ffb7d6990c19dd0abb0efc572eadb95bdfb7f9c0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558463"
---
# <a name="datasource-property-ado"></a>DataSource, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique un objet qui contient des données à représenter sous la forme d’un objet [Recordset](recordset-object-ado.md).

## <a name="remarks"></a>Remarques

Cette propriété est utilisée pour créer des contrôles liés aux données avec l’environnement de données. L’environnement de données conserve des collections de données (sources de données) contenant des objets nommés (*membres de données*) qui seront représentés en tant qu’objet **Recordset***.*

Les propriétés [DataMember](datamember-property-ado.md) et **DataSource** doivent être utilisées conjointement.

L'objet référencé doit implémenter l'interface **IDataSource** et contenir une interface **IRowset**.

**Utilisation**

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
