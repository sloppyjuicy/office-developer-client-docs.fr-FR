---
title: Recordset2. Requery, méthode (DAO)
TOCTitle: Requery Method
ms:assetid: d063c1e0-2fb7-b5cf-4d98-6f77a5a13cec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834712(v=office.15)
ms:contentKeyID: 48547837
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052940
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 44f573d179c26677fc801dac82e0deecc3874fb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307209"
---
# <a name="recordset2requery-method-dao"></a><span data-ttu-id="91a5a-102">Recordset2. Requery, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="91a5a-102">Recordset2.Requery method (DAO)</span></span>

<span data-ttu-id="91a5a-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="91a5a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="91a5a-104">Met à jour les données d'un objet **[Recordset](recordset-object-dao.md)** en réexécutant la requête sur laquelle l'objet est basé.</span><span class="sxs-lookup"><span data-stu-id="91a5a-104">Updates the data in a **[Recordset](recordset-object-dao.md)** object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="91a5a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91a5a-105">Syntax</span></span>

<span data-ttu-id="91a5a-106">*expression* . Requery (***défnouvellerequête***)</span><span class="sxs-lookup"><span data-stu-id="91a5a-106">*expression* .Requery(***NewQueryDef***)</span></span>

<span data-ttu-id="91a5a-107">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="91a5a-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="91a5a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91a5a-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="91a5a-109">Nom</span><span class="sxs-lookup"><span data-stu-id="91a5a-109">Name</span></span></p></th>
<th><p><span data-ttu-id="91a5a-110">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="91a5a-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="91a5a-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="91a5a-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="91a5a-112">Description</span><span class="sxs-lookup"><span data-stu-id="91a5a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91a5a-113"><em>Défnouvellerequête</em></span><span class="sxs-lookup"><span data-stu-id="91a5a-113"><em>NewQueryDef</em></span></span></p></td>
<td><p><span data-ttu-id="91a5a-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="91a5a-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="91a5a-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="91a5a-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="91a5a-116">Représente la valeur de la propriété <strong>Name</strong> d’un objet <strong><a href="querydef-object-dao.md">QueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="91a5a-116">Represents the <strong>Name</strong> property value of a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="91a5a-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="91a5a-117">Remarks</span></span>

<span data-ttu-id="91a5a-118">Cette méthode s'avère utile pour s'assurer qu'un objet **Recordset** contient les données les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="91a5a-118">Use this method to make sure that a **Recordset** contains the most recent data.</span></span> <span data-ttu-id="91a5a-119">Cette méthode remplit à nouveau l' **objet Recordset** actif à l'aide des paramètres de requête actuels ou (dans un espace de travail Microsoft Access) des nouveaux paramètres fournis par l'argument défnouvellerequête.</span><span class="sxs-lookup"><span data-stu-id="91a5a-119">This method re-populates the current **Recordset** by using either the current query parameters or (in a Microsoft Access workspace) the new ones supplied by the newquerydef argument.</span></span>

<span data-ttu-id="91a5a-120">Si vous ne spécifiez pas d'argument défnouvellerequête, l' **objet Recordset** est rempli en fonction de la définition de requête et des paramètres utilisés pour remplir initialement l' **objet Recordset**.</span><span class="sxs-lookup"><span data-stu-id="91a5a-120">If you don't specify a newquerydef argument, the **Recordset** is re-populated based on the same query definition and parameters used to originally populate the **Recordset**.</span></span> <span data-ttu-id="91a5a-121">Any changes to the underlying data will be reflected during this re-population.</span><span class="sxs-lookup"><span data-stu-id="91a5a-121">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="91a5a-122">If you didn't use a **QueryDef** to create the **Recordset**, the **Recordset** is re-created from scratch.</span><span class="sxs-lookup"><span data-stu-id="91a5a-122">If you didn't use a **QueryDef** to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="91a5a-123">Si vous spécifiez l' **objet querydef** d'origine dans l'argument défnouvellerequête, l' **objet Recordset** est reinterrogé à l'aide des paramètres spécifiés par l' **objet querydef**.</span><span class="sxs-lookup"><span data-stu-id="91a5a-123">If you specify the original **QueryDef** in the newquerydef argument, then the **Recordset** is requeried using the parameters specified by the **QueryDef**.</span></span> <span data-ttu-id="91a5a-124">Les modifications apportées aux données sous-jacentes sont répercutées lors de ce nouveau remplissage.</span><span class="sxs-lookup"><span data-stu-id="91a5a-124">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="91a5a-125">Pour répercuter les modifications apportées aux valeurs des paramètres de requête dans l' **objet Recordset**, vous devez spécifier l'argument défnouvellerequête.</span><span class="sxs-lookup"><span data-stu-id="91a5a-125">To reflect any changes to the query parameter values in the **Recordset**, you must supply the newquerydef argument.</span></span>

<span data-ttu-id="91a5a-126">If you specify a different **QueryDef** than what was originally used to create the **Recordset**, the **Recordset** is re-created from scratch.</span><span class="sxs-lookup"><span data-stu-id="91a5a-126">If you specify a different **QueryDef** than what was originally used to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="91a5a-127">Lorsque vous utilisez la méthode **Requery**, le premier enregistrement de l'objet **Recordset** devient l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="91a5a-127">When you use **Requery**, the first record in the **Recordset** becomes the current record.</span></span>

<span data-ttu-id="91a5a-128">Vous ne pouvez pas appliquer la méthode **Requery** aux objets **Recordset** de type feuille de réponse dynamique ou instantané dont la propriété **[Restartable](recordset2-restartable-property-dao.md)** a la valeur **False**.</span><span class="sxs-lookup"><span data-stu-id="91a5a-128">You can't use the **Requery** method on dynaset- or snapshot-type **Recordset** objects whose **[Restartable](recordset2-restartable-property-dao.md)** property is set to **False**.</span></span> <span data-ttu-id="91a5a-129">Toutefois, si vous fournissez l'argument facultatif défnouvellerequête, \*\*\*\* la propriété Restartable est ignorée.</span><span class="sxs-lookup"><span data-stu-id="91a5a-129">However, if you supply the optional newquerydef argument, the **Restartable** property is ignored.</span></span>

<span data-ttu-id="91a5a-130">Si les propriétés **[BOF](recordset2-bof-property-dao.md)** et **[EOF](recordset2-eof-property-dao.md)** de l'objet **Recordset** ont toutes deux la valeur **True** après que vous ayez utilisé la méthode **Requery**, la requête ne renvoie aucun enregistrement et l'objet **Recordset** ne contient pas de données.</span><span class="sxs-lookup"><span data-stu-id="91a5a-130">If both the **[BOF](recordset2-bof-property-dao.md)** and **[EOF](recordset2-eof-property-dao.md)** property settings of the **Recordset** object are **True** after you use the **Requery** method, the query didn't return any records and the **Recordset** contains no data.</span></span>

## <a name="example"></a><span data-ttu-id="91a5a-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="91a5a-131">Example</span></span>

<span data-ttu-id="91a5a-132">Cet exemple de code montre comment la méthode **Requery** peut être utilisée pour actualiser une requête suite à la modification des données sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="91a5a-132">This example shows how the **Requery** method can be used to refresh a query after underlying data has been changed.</span></span>

```vb
    Sub RequeryX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim rstView As Recordset2 
     Dim rstChange As Recordset2 
     
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

<span data-ttu-id="91a5a-133">Cet exemple de code montre comment la méthode **Requery** peut être utilisée pour actualiser une requête suite à la modification de ses paramètres.</span><span class="sxs-lookup"><span data-stu-id="91a5a-133">This example shows how the **Requery** method can be used to refresh a query after the query parameters have been changed.</span></span>

```vb
Sub RequeryX2() 
 
 Dim dbsNorthwind As Database 
 Dim qdfTemp As QueryDef 
 Dim prmCountry As Parameter 
 Dim rstView As Recordset2 
 
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

