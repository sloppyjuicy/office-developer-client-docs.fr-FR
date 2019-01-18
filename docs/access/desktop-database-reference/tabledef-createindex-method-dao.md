---
title: Méthode TableDef.CreateIndex (DAO)
TOCTitle: CreateIndex Method
ms:assetid: 857b25c1-01fa-b926-0c74-7105e71b7505
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196791(v=office.15)
ms:contentKeyID: 48546062
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052970
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: baa82b659cc2260d4a003c644b2d03d6c897fd21
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706233"
---
# <a name="tabledefcreateindex-method-dao"></a><span data-ttu-id="ba778-102">Méthode TableDef.CreateIndex (DAO)</span><span class="sxs-lookup"><span data-stu-id="ba778-102">TableDef.CreateIndex method (DAO)</span></span>

<span data-ttu-id="ba778-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba778-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="ba778-p101">Crée un nouvel objet **[Index](index-object-dao.md)** (Espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="ba778-p101">Creates a new **[Index](index-object-dao.md)** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="ba778-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba778-106">Syntax</span></span>

<span data-ttu-id="ba778-107">*expression* . CreateIndex (***nom***)</span><span class="sxs-lookup"><span data-stu-id="ba778-107">*expression* .CreateIndex(***Name***)</span></span>

<span data-ttu-id="ba778-108">*expression* Variable qui représente un objet **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="ba778-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="ba778-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba778-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ba778-110">Nom</span><span class="sxs-lookup"><span data-stu-id="ba778-110">Name</span></span></p></th>
<th><p><span data-ttu-id="ba778-111">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="ba778-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="ba778-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="ba778-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="ba778-113">Description</span><span class="sxs-lookup"><span data-stu-id="ba778-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba778-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="ba778-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="ba778-115">Facultatif</span><span class="sxs-lookup"><span data-stu-id="ba778-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="ba778-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ba778-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ba778-p102">Type <strong>String</strong> qui identifie de façon unique le nouvel objet <strong>Index</strong>. Consultez la propriété <strong>Name</strong> pour plus d'informations sur les noms d'objets <strong>Index</strong> valides.</span><span class="sxs-lookup"><span data-stu-id="ba778-p102">A <strong>String</strong> that uniquely names the new <strong>Index</strong> object. See the <strong>Name</strong> property for details on valid <strong>Index</strong> names.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="ba778-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ba778-119">Return value</span></span>

<span data-ttu-id="ba778-120">Index</span><span class="sxs-lookup"><span data-stu-id="ba778-120">Index</span></span>

## <a name="remarks"></a><span data-ttu-id="ba778-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="ba778-121">Remarks</span></span>

<span data-ttu-id="ba778-122">Vous pouvez utiliser la méthode **CreateIndex** afin de créer un un objet **Index** pour un objet **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="ba778-122">You can use the **CreateIndex** method to create a new **Index** object for a **TableDef** object.</span></span> <span data-ttu-id="ba778-123">Si vous ne spécifiez pas le nom facultatif **CreateIndex**, vous pouvez utiliser une instruction d’affectation appropriée pour définir ou redéfinir la propriété **Name** avant d’ajouter le nouvel objet à une collection.</span><span class="sxs-lookup"><span data-stu-id="ba778-123">If you omit the optional name part when you use **CreateIndex**, you can use an appropriate assignment statement to set or reset the **Name** property before you append the new object to a collection.</span></span> <span data-ttu-id="ba778-124">Après l'ajout de l'objet, il n'est pas toujours possible de définir sa propriété **Name**, selon le type d'objet qui contient la collection **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="ba778-124">After you append the object, you may or may not be able to set its **Name** property, depending on the type of object that contains the **Indexes** collection.</span></span> <span data-ttu-id="ba778-125">Pour plus d'informations, consultez la rubrique de la propriété **Name**.</span><span class="sxs-lookup"><span data-stu-id="ba778-125">See the **Name** property topic for more details.</span></span>

<span data-ttu-id="ba778-126">Si le nom fait référence à un objet qui est déjà membre de la collection, une erreur d’exécution se produit lorsque vous utilisez la méthode **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="ba778-126">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="ba778-127">Pour supprimer un objet **Index** d'une collection, appelez la méthode **[Delete](fields-delete-method-dao.md)** sur la collection.</span><span class="sxs-lookup"><span data-stu-id="ba778-127">To remove an **Index** object from a collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="ba778-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="ba778-128">Example</span></span>

<span data-ttu-id="ba778-p104">Cet exemple utilise la méthode **CreateIndex** pour créer deux nouveaux objets **Index** et les ajouter à la collection **Indexes** de l'objet **TableDef** Employees. Il énumère ensuite la collection Indexes de l'objet **TableDef**, la collection **Fields** des nouveaux objets **Index**, et la collection Properties des nouveaux objets **Index**. La fonction CreateIndexOutput est requise pour exécuter cette opération.</span><span class="sxs-lookup"><span data-stu-id="ba778-p104">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object. It then enumerates the Indexes collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects. The CreateIndexOutput function is required for this procedure to run.</span></span>

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```
