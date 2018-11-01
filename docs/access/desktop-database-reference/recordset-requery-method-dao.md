---
title: Recordset.Requery Method (DAO)
TOCTitle: Requery Method
ms:assetid: a5d66eb5-499c-4133-f6c3-c7a1619a8a11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821155(v=office.15)
ms:contentKeyID: 48546840
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 420ed0f95b283d7d50b4e50ca05c7dfca94a1390
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868475"
---
# <a name="recordsetrequery-method-dao"></a><span data-ttu-id="f04d4-102">Recordset.Requery Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="f04d4-102">Recordset.Requery Method (DAO)</span></span>


<span data-ttu-id="f04d4-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f04d4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f04d4-104">Met à jour les données d'un objet **[Recordset](recordset-object-dao.md)** en réexécutant la requête sur laquelle l'objet est basé.</span><span class="sxs-lookup"><span data-stu-id="f04d4-104">Updates the data in a **[Recordset](recordset-object-dao.md)** object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="f04d4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f04d4-105">Syntax</span></span>

<span data-ttu-id="f04d4-106">*expression* . Requery (***défnouvellerequête***)</span><span class="sxs-lookup"><span data-stu-id="f04d4-106">*expression* .Requery(***NewQueryDef***)</span></span>

<span data-ttu-id="f04d4-107">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="f04d4-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="f04d4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f04d4-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f04d4-109">Name</span><span class="sxs-lookup"><span data-stu-id="f04d4-109">Name</span></span></p></th>
<th><p><span data-ttu-id="f04d4-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="f04d4-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="f04d4-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="f04d4-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="f04d4-112">Description</span><span class="sxs-lookup"><span data-stu-id="f04d4-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f04d4-113">Défnouvellerequête</span><span class="sxs-lookup"><span data-stu-id="f04d4-113">NewQueryDef</span></span></p></td>
<td><p><span data-ttu-id="f04d4-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="f04d4-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="f04d4-115"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="f04d4-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f04d4-116">Représente la valeur de la propriété <strong>Name</strong> d’un objet <strong><a href="querydef-object-dao.md">QueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="f04d4-116">Represents the <strong>Name</strong> property value of a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f04d4-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="f04d4-117">Remarks</span></span>

<span data-ttu-id="f04d4-118">Cette méthode s'avère utile pour s'assurer qu'un objet **Recordset** contient les données les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="f04d4-118">Use this method to make sure that a **Recordset** contains the most recent data.</span></span> <span data-ttu-id="f04d4-119">Cette méthode remplit le **jeu d’enregistrements** actuel en utilisant les paramètres requête en cours ou (dans un espace de travail Microsoft Access) les nouveaux fournis par l’argument défnouvellerequête.</span><span class="sxs-lookup"><span data-stu-id="f04d4-119">This method re-populates the current **Recordset** by using either the current query parameters or (in a Microsoft Access workspace) the new ones supplied by the newquerydef argument.</span></span>

<span data-ttu-id="f04d4-120">Si vous ne spécifiez pas un argument défnouvellerequête, l' **objet Recordset** est rempli en fonction de la définition de la même requête et les paramètres utilisés pour remplir initialement l' **objet Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f04d4-120">If you don't specify a newquerydef argument, the **Recordset** is re-populated based on the same query definition and parameters used to originally populate the **Recordset**.</span></span> <span data-ttu-id="f04d4-121">Toutes les modifications apportées aux données sous-jacentes sont répercutées lors de l'ajout de données.</span><span class="sxs-lookup"><span data-stu-id="f04d4-121">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="f04d4-122">Si vous n'avez pas utilisé **QueryDef** pour créer l'objet **Recordset**, l'objet **Recordset** est entièrement recréé.</span><span class="sxs-lookup"><span data-stu-id="f04d4-122">If you didn't use a **QueryDef** to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="f04d4-123">Si vous spécifiez l' **objet QueryDef** d’origine dans l’argument défnouvellerequête, l' **objet Recordset** est actualisée à l’aide des paramètres spécifiés par l' **objet QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="f04d4-123">If you specify the original **QueryDef** in the newquerydef argument, then the **Recordset** is requeried using the parameters specified by the **QueryDef**.</span></span> <span data-ttu-id="f04d4-124">Les modifications apportées aux données sous-jacentes sont répercutées lors de ce nouveau remplissage.</span><span class="sxs-lookup"><span data-stu-id="f04d4-124">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="f04d4-125">Pour répercuter les modifications apportées aux valeurs de paramètre de requête dans le **jeu d’enregistrements**, vous devez fournir l’argument défnouvellerequête.</span><span class="sxs-lookup"><span data-stu-id="f04d4-125">To reflect any changes to the query parameter values in the **Recordset**, you must supply the newquerydef argument.</span></span>

<span data-ttu-id="f04d4-126">Si vous spécifiez un autre **QueryDef** que celui qui a été utilisé à l'origine pour créer l'objet **Recordset**, l'objet **Recordset** est entièrement recréé.</span><span class="sxs-lookup"><span data-stu-id="f04d4-126">If you specify a different **QueryDef** than what was originally used to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="f04d4-127">Lorsque vous utilisez la méthode **Requery**, le premier enregistrement de l'objet **Recordset** devient l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="f04d4-127">When you use **Requery**, the first record in the **Recordset** becomes the current record.</span></span>

<span data-ttu-id="f04d4-128">Vous ne pouvez pas appliquer la méthode **Requery** aux objets **Recordset** de type feuille de réponse dynamique ou instantané dont la propriété **[Restartable](recordset-restartable-property-dao.md)** a la valeur **False**.</span><span class="sxs-lookup"><span data-stu-id="f04d4-128">You can't use the **Requery** method on dynaset- or snapshot-type **Recordset** objects whose **[Restartable](recordset-restartable-property-dao.md)** property is set to **False**.</span></span> <span data-ttu-id="f04d4-129">Toutefois, si vous indiquez l’argument facultatif défnouvellerequête, la propriété **Restartable** est ignorée.</span><span class="sxs-lookup"><span data-stu-id="f04d4-129">However, if you supply the optional newquerydef argument, the **Restartable** property is ignored.</span></span>

<span data-ttu-id="f04d4-130">Si les propriétés **[BOF](recordset-bof-property-dao.md)** et **[EOF](recordset-eof-property-dao.md)** de l'objet **Recordset** ont toutes deux la valeur **True** après que vous ayez utilisé la méthode **Requery**, la requête ne renvoie aucun enregistrement et l'objet **Recordset** ne contient pas de données.</span><span class="sxs-lookup"><span data-stu-id="f04d4-130">If both the **[BOF](recordset-bof-property-dao.md)** and **[EOF](recordset-eof-property-dao.md)** property settings of the **Recordset** object are **True** after you use the **Requery** method, the query didn't return any records and the **Recordset** contains no data.</span></span>

## <a name="example"></a><span data-ttu-id="f04d4-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="f04d4-131">Example</span></span>

<span data-ttu-id="f04d4-132">Cet exemple de code montre comment la méthode **Requery** peut être utilisée pour actualiser une requête suite à la modification des données sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="f04d4-132">This example shows how the **Requery** method can be used to refresh a query after underlying data has been changed.</span></span>

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

<span data-ttu-id="f04d4-133">Cet exemple de code montre comment la méthode **Requery** peut être utilisée pour actualiser une requête suite à la modification de ses paramètres.</span><span class="sxs-lookup"><span data-stu-id="f04d4-133">This example shows how the **Requery** method can be used to refresh a query after the query parameters have been changed.</span></span>

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

