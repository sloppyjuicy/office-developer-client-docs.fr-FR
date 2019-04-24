---
title: DataSource, propriété (ADO)
TOCTitle: DataSource property (ADO)
ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15)
ms:contentKeyID: 48545087
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0dec30715d1eb4e31d7490db4cedd015ecf3c040
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294469"
---
# <a name="datasource-property-ado"></a><span data-ttu-id="8d2e1-102">DataSource, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="8d2e1-102">DataSource property (ADO)</span></span>


<span data-ttu-id="8d2e1-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d2e1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8d2e1-104">Indique un objet qui contient des données à représenter sous la forme d’un objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8d2e1-104">Indicates an object that contains data to be represented as a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d2e1-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="8d2e1-105">Remarks</span></span>

<span data-ttu-id="8d2e1-p101">Cette propriété est utilisée pour créer des contrôles liés aux données avec l’environnement de données. L’environnement de données conserve des collections de données (sources de données) contenant des objets nommés (*membres de données*) qui seront représentés en tant qu’objet \**Recordset\*\*\*.*</span><span class="sxs-lookup"><span data-stu-id="8d2e1-p101">This property is used to create data-bound controls with the Data Environment. The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a **Recordset** object *.*</span></span>

<span data-ttu-id="8d2e1-108">Les propriétés [DataMember](datamember-property-ado.md) et **DataSource** doivent être utilisées conjointement.</span><span class="sxs-lookup"><span data-stu-id="8d2e1-108">The [DataMember](datamember-property-ado.md) and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="8d2e1-109">L'objet référencé doit implémenter l'interface **IDataSource** et contenir une interface **IRowset**.</span><span class="sxs-lookup"><span data-stu-id="8d2e1-109">The object referenced must implement the **IDataSource** interface and must contain an **IRowset** interface.</span></span>

<span data-ttu-id="8d2e1-110">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="8d2e1-110">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
