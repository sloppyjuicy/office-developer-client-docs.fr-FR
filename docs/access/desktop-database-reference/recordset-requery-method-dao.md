---
title: Méthode Recordset.Requery (DAO)
TOCTitle: Requery Method
ms:assetid: a5d66eb5-499c-4133-f6c3-c7a1619a8a11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821155(v=office.15)
ms:contentKeyID: 48546840
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: bd6f2fdf7d1f8ba9fc47c6223a8f872a655a1e3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307622"
---
# <a name="recordsetrequery-method-dao"></a><span data-ttu-id="90e68-102">Méthode Recordset.Requery (DAO)</span><span class="sxs-lookup"><span data-stu-id="90e68-102">Recordset.Requery Method (DAO)</span></span>

<span data-ttu-id="90e68-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="90e68-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="90e68-104">Met à jour les données dans un objet **[Recordset](recordset-object-dao.md)** en exécutant de nouveau la requête sur laquelle l’objet est basé.</span><span class="sxs-lookup"><span data-stu-id="90e68-104">Updates the data in a **[Recordset](recordset-object-dao.md)** object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="90e68-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90e68-105">Syntax</span></span>

<span data-ttu-id="90e68-106">*expression* .Requery(***NewQueryDef***)</span><span class="sxs-lookup"><span data-stu-id="90e68-106">*expression* .Requery(***NewQueryDef***)</span></span>

<span data-ttu-id="90e68-107">*expression* Variable qui représente un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="90e68-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="90e68-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90e68-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="90e68-109">Nom</span><span class="sxs-lookup"><span data-stu-id="90e68-109">Name</span></span></p></th>
<th><p><span data-ttu-id="90e68-110">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="90e68-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="90e68-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="90e68-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="90e68-112">Description</span><span class="sxs-lookup"><span data-stu-id="90e68-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90e68-113"><em>NewQueryDef</em></span><span class="sxs-lookup"><span data-stu-id="90e68-113"><em>NewQueryDef</em></span></span></p></td>
<td><p><span data-ttu-id="90e68-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="90e68-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="90e68-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="90e68-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="90e68-116">Représente la valeur de la propriété <strong>Name</strong> d’un objet <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="90e68-116">Represents the <strong>Name</strong> property value of a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="90e68-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="90e68-117">Remarks</span></span>

<span data-ttu-id="90e68-118">Utilisez cette méthode pour vous assurer qu’un objet **Recordset** contient les données les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="90e68-118">Use this method to make sure that a **Recordset** contains the most recent data.</span></span> <span data-ttu-id="90e68-119">Cette méthode renseigne à nouveau l’objet **Recordset** actif à partir des paramètres de la requête actuelle ou (dans un espace de travail Microsoft Access) de ceux, nouveaux, fournis par l’argument newquerydef.</span><span class="sxs-lookup"><span data-stu-id="90e68-119">This method re-populates the current **Recordset** by using either the current query parameters or (in a Microsoft Access workspace) the new ones supplied by the  newquerydef argument.</span></span>

<span data-ttu-id="90e68-120">Si vous ne spécifiez pas d’argument newquerydef, l’objet **Recordset** est de nouveau renseigné à partir de la définition et des paramètres de requête déjà utilisés pour renseigner l’objet **Recordset** à l’origine.</span><span class="sxs-lookup"><span data-stu-id="90e68-120">If you don't specify a  newquerydef argument, the **Recordset** is re-populated based on the same query definition and parameters used to originally populate the **Recordset**.</span></span> <span data-ttu-id="90e68-121">Any changes to the underlying data will be reflected during this re-population.</span><span class="sxs-lookup"><span data-stu-id="90e68-121">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="90e68-122">If you didn't use a **QueryDef** to create the **Recordset**, the **Recordset** is re-created from scratch.</span><span class="sxs-lookup"><span data-stu-id="90e68-122">If you didn't use a **QueryDef** to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="90e68-123">Si vous spécifiez l’objet **QueryDef** d’origine dans l’argument newquerydef, **Recordset** fait l’objet d’une nouvelle requête basée sur les paramètres spécifiés par **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="90e68-123">If you specify the original **QueryDef** in the  newquerydef argument, then the **Recordset** is requeried using the parameters specified by the **QueryDef**.</span></span> <span data-ttu-id="90e68-124">Toute modification apportée aux données sous-jacentes sera prise en compte lorsque l’objet sera de nouveau renseigné.</span><span class="sxs-lookup"><span data-stu-id="90e68-124">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="90e68-125">Pour répercuter les modifications effectuées au niveau de la valeur des paramètres de la requête dans l’objet **Recordset**, vous devez fournir l’argument newquerydef.</span><span class="sxs-lookup"><span data-stu-id="90e68-125">To reflect any changes to the query parameter values in the **Recordset**, you must supply the  newquerydef argument.</span></span>

<span data-ttu-id="90e68-126">If you specify a different **QueryDef** than what was originally used to create the **Recordset**, the **Recordset** is re-created from scratch.</span><span class="sxs-lookup"><span data-stu-id="90e68-126">If you specify a different **QueryDef** than what was originally used to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="90e68-127">Lorsque vous utilisez la méthode **Requery**, le premier enregistrement de l'objet **Recordset** devient l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="90e68-127">When you use **Requery**, the first record in the **Recordset** becomes the current record.</span></span>

<span data-ttu-id="90e68-128">Vous ne pouvez pas appliquer la méthode **Requery** aux objets **Recordset** de type feuille de réponse dynamique ou instantané dont la propriété **[Restartable](recordset-restartable-property-dao.md)** a la valeur **False**.</span><span class="sxs-lookup"><span data-stu-id="90e68-128">You can't use the **Requery** method on dynaset- or snapshot-type **Recordset** objects whose **[Restartable](recordset-restartable-property-dao.md)** property is set to **False**.</span></span> <span data-ttu-id="90e68-129">Toutefois, si vous fournissez l’argument facultatif newquerydef, la propriété **Restartable** est ignorée.</span><span class="sxs-lookup"><span data-stu-id="90e68-129">However, if you supply the optional  newquerydef argument, the **Restartable** property is ignored.</span></span>

<span data-ttu-id="90e68-130">Si les propriétés **[BOF](recordset-bof-property-dao.md)** et **[EOF](recordset-eof-property-dao.md)** de l'objet **Recordset** ont toutes deux la valeur **True** après que vous ayez utilisé la méthode **Requery**, la requête ne renvoie aucun enregistrement et l'objet **Recordset** ne contient pas de données.</span><span class="sxs-lookup"><span data-stu-id="90e68-130">If both the **[BOF](recordset-bof-property-dao.md)** and **[EOF](recordset-eof-property-dao.md)** property settings of the **Recordset** object are **True** after you use the **Requery** method, the query didn't return any records and the **Recordset** contains no data.</span></span>

## <a name="example"></a><span data-ttu-id="90e68-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="90e68-131">Example</span></span>

<span data-ttu-id="90e68-132">Cet exemple montre comment la méthode **Requery** peut être utilisée pour actualiser une requête après la modification des données sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="90e68-132">This example shows how the **Requery** method can be used to refresh a query after underlying data has been changed.</span></span>

```vb
    Sub RequeryX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim rstView As Recordset 
     Dim rstChange As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
     "PARAMETERS ViewCountry Text; " & _ 
     "SELECT FirstName, LastName, Country FROM " & _ 
     "Employees WHERE Country = [ViewCountry] " & _ 
     "ORDER BY LastName") 
     
     qdfTemp.Parameters!ViewCountry = "USA" 
     Debug.Print "Data after initial query, " & _ 
     [ViewCountry] = USA" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Change underlying data. 
     Set rstChange = dbsNorthwind.OpenRecordset("Employees") 
     rstChange.AddNew 
     rstChange!FirstName = "Nina" 
     rstChange!LastName = "Roberts" 
     rstChange!Country = "USA" 
     rstChange.Update 
     
     rstView.Requery 
     Debug.Print "Requery after changing underlying data" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Restore original data because this is only a 
     ' demonstration. 
     rstChange.Bookmark = rstChange.LastModified 
     rstChange.Delete 
     rstChange.Close 
     
     rstView.Close 
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="90e68-133">Cet exemple de code montre comment la méthode **Requery** peut être utilisée pour actualiser une requête suite à la modification de ses paramètres.</span><span class="sxs-lookup"><span data-stu-id="90e68-133">This example shows how the **Requery** method can be used to refresh a query after the query parameters have been changed.</span></span>

```vb 
Sub RequeryX2() 
 
 Dim dbsNorthwind As Database 
 Dim qdfTemp As QueryDef 
 Dim prmCountry As Parameter 
 Dim rstView As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
 "PARAMETERS ViewCountry Text; " & _ 
 "SELECT FirstName, LastName, Country FROM " & _ 
 "Employees WHERE Country = [ViewCountry] " & _ 
 "ORDER BY LastName") 
 Set prmCountry = qdfTemp.Parameters!ViewCountry 
 
 qdfTemp.Parameters!ViewCountry = "USA" 
 Debug.Print "Data after initial query, " & _ 
 [ViewCountry] = USA" 
 Set rstView = qdfTemp.OpenRecordset 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 ' Change query parameter. 
 qdfTemp.Parameters!ViewCountry = "UK" 
 ' QueryDef argument must be included so that the 
 ' resulting Recordset reflects the change in the query 
 ' parameter. 
 rstView.Requery qdfTemp 
 Debug.Print "Requery after changing parameter, " & _ 
 "[ViewCountry] = UK" 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 rstView.Close 
 dbsNorthwind.Close 
 
End Sub 
 
```

