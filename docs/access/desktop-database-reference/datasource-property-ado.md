---
<span data-ttu-id="dd4dc-101"><<<<<<< Titre tête : TOCTitle DataSource propriété (ADO) : DataSource propriété (ADO) === titre : DataSource, propriété (ADO) TOCTitle : DataSource, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="dd4dc-101"><<<<<<< HEAD title: DataSource Property (ADO) TOCTitle: DataSource Property (ADO) ======= title: DataSource property (ADO) TOCTitle: DataSource property (ADO)</span></span>
>>>>>>> <span data-ttu-id="dd4dc-102">Master ms:assetid : 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e ms:mtpsurl : https://msdn.microsoft.com/library/JJ249325(v=office.15) ms:contentKeyID : ms.date 48545087 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="dd4dc-102">master ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15) ms:contentKeyID: 48545087 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="dd4dc-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="dd4dc-103"><<<<<<< HEAD</span></span>
# <a name="datasource-property-ado"></a><span data-ttu-id="dd4dc-104">DataSource, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="dd4dc-104">DataSource Property (ADO)</span></span>
=======
# <a name="datasource-property-ado"></a><span data-ttu-id="dd4dc-105">DataSource, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="dd4dc-105">DataSource property (ADO)</span></span>
>>>>>>> <span data-ttu-id="dd4dc-106">master</span><span class="sxs-lookup"><span data-stu-id="dd4dc-106">master</span></span>


<span data-ttu-id="dd4dc-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="dd4dc-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dd4dc-108">Indique un objet qui contient des données à représenter sous la forme d'un objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="dd4dc-108">Indicates an object that contains data to be represented as a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd4dc-109">Notes</span><span class="sxs-lookup"><span data-stu-id="dd4dc-109">Remarks</span></span>

<span data-ttu-id="dd4dc-p101">Cette propriété est utilisée pour créer des contrôles liés aux données avec l’environnement de données. L’environnement de données conserve des collections de données (sources de données) contenant des objets nommés (*membres de données*) qui seront représentés en tant qu’objet \**Recordset\*\*\*.*</span><span class="sxs-lookup"><span data-stu-id="dd4dc-p101">This property is used to create data-bound controls with the Data Environment. The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a **Recordset** object *.*</span></span>

<span data-ttu-id="dd4dc-112">Les propriétés [DataMember](datamember-property-ado.md) et **DataSource** doivent être utilisées conjointement.</span><span class="sxs-lookup"><span data-stu-id="dd4dc-112">The [DataMember](datamember-property-ado.md) and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="dd4dc-113">L'objet référencé doit implémenter l'interface **IDataSource** et contenir une interface **IRowset**.</span><span class="sxs-lookup"><span data-stu-id="dd4dc-113">The object referenced must implement the **IDataSource** interface and must contain an **IRowset** interface.</span></span>

<span data-ttu-id="dd4dc-114">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="dd4dc-114">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
