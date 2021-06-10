---
title: 'Chapitre 3 : Examen de données'
TOCTitle: 'Chapter 3: Examining data'
ms:assetid: 73c69134-3127-3344-d5c3-5ecb9e0e958b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249474(v=office.15)
ms:contentKeyID: 48545648
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fcf837a02c40d11fecfa56b8aa34ac80a848411
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296457"
---
# <a name="chapter-3-examining-data"></a><span data-ttu-id="048d0-102">Chapitre 3 : Examen de données</span><span class="sxs-lookup"><span data-stu-id="048d0-102">Chapter 3: Examining data</span></span>

<span data-ttu-id="048d0-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="048d0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="048d0-p101">Le chapitre 2 vous a appris à récupérer des données à partir d'une source de données présentée sous la forme d'un objet **Recordset**. Ce chapitre décrit l'objet **Recordset** plus en détail et explique notamment comment naviguer dans un **Recordset** afin d'afficher ses données.</span><span class="sxs-lookup"><span data-stu-id="048d0-p101">Chapter 2 explained how to retrieve data from a data source as a **Recordset** object. This chapter will discuss the **Recordset** in more detail, including how to navigate through the **Recordset** and view its data.</span></span>

<span data-ttu-id="048d0-p102">Les objets **Recordset** possèdent des méthodes et des propriétés qui vous permettent de les explorer et d'examiner leur contenu. Selon les fonctionnalités prises en charge par le fournisseur, certaines méthodes et propriétés des objets **Recordset** sont disponibles et d'autres ne le sont pas. Pour continuer à explorer l'objet **Recordset**, imaginez un **jeu d'enregistrements** renvoyé par la base de données exemple Northwind sur Microsoft SQL Server 2000, à l'aide du code suivant :</span><span class="sxs-lookup"><span data-stu-id="048d0-p102">**Recordsets** have methods and properties designed to make it easy to move through them and examine their contents. Depending on the functionality supported by the provider, some **Recordset** methods or properties might not be available. To continue exploring the **Recordset** object, consider a **Recordset** that would be returned from the Northwind sample database on Microsoft SQL Server 2000, using the following code:</span></span>

```vb 
 
'BeginRsTour 
Public Sub RecordsetTour() 
 On Error GoTo ErrHandler: 
 
 Dim objRs As New ADODB.Recordset 
 Dim strSQL As String 
 
 strSQL = "SELECT ProductID, ProductName, UnitPrice FROM Products " & _ 
 "WHERE CategoryID = 7" '7 = Produce 
 
 objRs.Open strSQL, strConnStr, adOpenForwardOnly, _ 
 adLockReadOnly, adCmdText 
 
 'Clean up 
 objRs.Close 
 Set objRs = Nothing 
 Exit Sub 
 
ErrHandler: 
 If Not objRs Is Nothing Then 
 If objRs.State = adStateOpen Then objRs.Close 
 Set objRs = Nothing 
 End If 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndRsTour 
```

<br/>

<span data-ttu-id="048d0-p103">Cette requête SQL renvoie un **jeu d'enregistrements** constitué de cinq lignes (enregistrements) et de trois colonnes (champs). Les valeurs de chaque ligne sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="048d0-p103">This SQL query returns a **Recordset** with five rows (records) and three columns (fields). The values for each row are shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="048d0-111">CHAMP 0</span><span class="sxs-lookup"><span data-stu-id="048d0-111">FIELD 0</span></span><br />
<span data-ttu-id="048d0-112">Name = ProductID</span><span class="sxs-lookup"><span data-stu-id="048d0-112">Name = ProductID</span></span></p></th>
<th><p><span data-ttu-id="048d0-113">CHAMP 1</span><span class="sxs-lookup"><span data-stu-id="048d0-113">FIELD 1</span></span><br />
<span data-ttu-id="048d0-114">Name = ProductName</span><span class="sxs-lookup"><span data-stu-id="048d0-114">Name = ProductName</span></span></p></th>
<th><p><span data-ttu-id="048d0-115">CHAMP 2</span><span class="sxs-lookup"><span data-stu-id="048d0-115">FIELD 2</span></span><br />
<span data-ttu-id="048d0-116">Name = UnitPrice</span><span class="sxs-lookup"><span data-stu-id="048d0-116">Name = UnitPrice</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="048d0-117">7 </span><span class="sxs-lookup"><span data-stu-id="048d0-117">7</span></span></p></td>
<td><p><span data-ttu-id="048d0-118">Pêches séchées bio Oncle Bob</span><span class="sxs-lookup"><span data-stu-id="048d0-118">Uncle Bob's Organic Dried Pears</span></span></p></td>
<td><p><span data-ttu-id="048d0-119">30.0000</span><span class="sxs-lookup"><span data-stu-id="048d0-119">30.0000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="048d0-120">14 </span><span class="sxs-lookup"><span data-stu-id="048d0-120">14</span></span></p></td>
<td><p><span data-ttu-id="048d0-121">Tofu</span><span class="sxs-lookup"><span data-stu-id="048d0-121">Tofu</span></span></p></td>
<td><p><span data-ttu-id="048d0-122">23.2500</span><span class="sxs-lookup"><span data-stu-id="048d0-122">23.2500</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="048d0-123">28</span><span class="sxs-lookup"><span data-stu-id="048d0-123">28</span></span></p></td>
<td><p><span data-ttu-id="048d0-124">Choucroute Frau Kraut</span><span class="sxs-lookup"><span data-stu-id="048d0-124">Rssle Sauerkraut</span></span></p></td>
<td><p><span data-ttu-id="048d0-125">45.6000</span><span class="sxs-lookup"><span data-stu-id="048d0-125">45.6000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="048d0-126">51</span><span class="sxs-lookup"><span data-stu-id="048d0-126">51</span></span></p></td>
<td><p><span data-ttu-id="048d0-127">Pommes séchées Manjimup</span><span class="sxs-lookup"><span data-stu-id="048d0-127">Manjimup Dried Apples</span></span></p></td>
<td><p><span data-ttu-id="048d0-128">53.0000</span><span class="sxs-lookup"><span data-stu-id="048d0-128">53.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="048d0-129">74</span><span class="sxs-lookup"><span data-stu-id="048d0-129">74</span></span></p></td>
<td><p><span data-ttu-id="048d0-130">Tofu LongVi</span><span class="sxs-lookup"><span data-stu-id="048d0-130">Longlife Tofu</span></span></p></td>
<td><p><span data-ttu-id="048d0-131">10.0000</span><span class="sxs-lookup"><span data-stu-id="048d0-131">10.0000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="048d0-132">La section suivante explique comment localiser la position actuelle du curseur dans cet exemple **de jeu d’enregistrements.**</span><span class="sxs-lookup"><span data-stu-id="048d0-132">The next section explains how to locate the current position of the cursor in this sample **Recordset**.</span></span>

<span data-ttu-id="048d0-133">Ce chapitre présente les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="048d0-133">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="048d0-134">Recherche de l’enregistrement actuel (ADO)</span><span class="sxs-lookup"><span data-stu-id="048d0-134">Locating the current record (ADO)</span></span>](locating-the-current-record.md)
- [<span data-ttu-id="048d0-135">Navigation dans les données (ADO)</span><span class="sxs-lookup"><span data-stu-id="048d0-135">Navigating through the data (ADO)</span></span>](navigating-through-the-data.md)
- [<span data-ttu-id="048d0-136">Understanding Recordset structure (ADO)</span><span class="sxs-lookup"><span data-stu-id="048d0-136">Understanding Recordset structure (ADO)</span></span>](understanding-recordset-structure.md)
