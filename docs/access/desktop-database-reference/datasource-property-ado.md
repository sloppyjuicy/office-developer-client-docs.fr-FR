---
title: DataSource, propriété (ADO)
TOCTitle: DataSource property (ADO)
ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15)
ms:contentKeyID: 48545087
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a6b889deb9ccf713c2313b207387be8f6b1681b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868160"
---
# <a name="datasource-property-ado"></a>DataSource, propriété (ADO)


**S’applique à**: Access 2013, Office 2013

Indique un objet qui contient des données à représenter sous la forme d'un objet [Recordset](recordset-object-ado.md).

## <a name="remarks"></a>Notes

Cette propriété est utilisée pour créer des contrôles liés aux données avec l’environnement de données. L’environnement de données conserve des collections de données (sources de données) contenant des objets nommés (*membres de données*) qui seront représentés en tant qu’objet **Recordset***.*

Les propriétés [DataMember](datamember-property-ado.md) et **DataSource** doivent être utilisées conjointement.

L'objet référencé doit implémenter l'interface **IDataSource** et contenir une interface **IRowset**.

**Utilisation**

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
