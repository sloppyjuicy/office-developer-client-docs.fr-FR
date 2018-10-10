---
title: DataMember, propriété (ADO)
TOCTitle: DataMember Property (ADO)
ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15)
ms:contentKeyID: 48548787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a67864ab135c59f146a27f997d4b0df63865a50
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472473"
---
# <a name="datamember-property-ado"></a><span data-ttu-id="2ca08-102">DataMember, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="2ca08-102">DataMember Property (ADO)</span></span>

<span data-ttu-id="2ca08-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2ca08-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2ca08-104">Indique le nom du membre de données qui sera extrait de l'objet référencé par la propriété [DataSource](datasource-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="2ca08-104">Indicates the name of the data member that will be retrieved from the object referenced by the [DataSource](datasource-property-ado.md) property.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="2ca08-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="2ca08-105">Settings and Return Values</span></span>

<span data-ttu-id="2ca08-p101">Définit ou renvoie une valeur de type **String**. Le nom ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="2ca08-p101">Sets or returns a **String** value. The name is not case sensitive.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ca08-108">Notes</span><span class="sxs-lookup"><span data-stu-id="2ca08-108">Remarks</span></span>

<span data-ttu-id="2ca08-p102">Cette propriété est utilisée pour créer des contrôles liés aux données avec l’environnement de données. L’environnement de données conserve des collections de données (sources de données) contenant des objets nommés (*membres de données*) qui seront représentés en tant qu’objet [Recordset](recordset-object-ado.md)*.*</span><span class="sxs-lookup"><span data-stu-id="2ca08-p102">This property is used to create data-bound controls with the Data Environment. The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a [Recordset](recordset-object-ado.md) object *.*</span></span>

<span data-ttu-id="2ca08-111">Les propriétés **DataMember** et **DataSource** doivent être utilisées conjointement.</span><span class="sxs-lookup"><span data-stu-id="2ca08-111">The **DataMember** and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="2ca08-p103">La propriété **DataMember** détermine l'objet spécifié par la propriété **DataSource** à représenter en tant qu'objet **Recordset**. L'objet **Recordset** doit être fermé avant que cette propriété soit définie. Une erreur est générée si la propriété **DataMember** n'est pas définie avant la propriété **DataSource** ou si le nom **DataMember** n'est pas reconnu par l'objet spécifié dans la propriété **DataSource**.</span><span class="sxs-lookup"><span data-stu-id="2ca08-p103">The **DataMember** property determines which object specified by the **DataSource** property will be represented as a **Recordset** object. The **Recordset** object must be closed before this property is set. An error is generated if the **DataMember** property isn't set before the **DataSource** property, or if the **DataMember** name isn't recognized by the object specified in the **DataSource** property.</span></span>

<span data-ttu-id="2ca08-115">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="2ca08-115">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
