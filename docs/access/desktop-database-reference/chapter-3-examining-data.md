---
title: 'Chapitre 3 : Examen des données'
TOCTitle: 'Chapter 3: Examining Data'
ms:assetid: 73c69134-3127-3344-d5c3-5ecb9e0e958b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249474(v=office.15)
ms:contentKeyID: 48545648
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 481fbc3bc39f184aeefe6738ac8d2a80fcd1d93f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470724"
---
# <a name="chapter-3-examining-data"></a><span data-ttu-id="36a8d-102">Chapitre 3 : Examen des données</span><span class="sxs-lookup"><span data-stu-id="36a8d-102">Chapter 3: Examining Data</span></span>


<span data-ttu-id="36a8d-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="36a8d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="36a8d-p101">Le chapitre 2 vous a appris à récupérer des données à partir d'une source de données présentée sous la forme d'un objet **Recordset**. Ce chapitre décrit l'objet **Recordset** plus en détail et explique notamment comment naviguer dans un **Recordset** afin d'afficher ses données.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p101">Chapter 2 explained how to retrieve data from a data source as a **Recordset** object. This chapter will discuss the **Recordset** in more detail, including how to navigate through the **Recordset** and view its data.</span></span>

<span data-ttu-id="36a8d-p102">Les objets **Recordset** possèdent des méthodes et des propriétés qui vous permettent de les explorer et d'examiner leur contenu. Selon les fonctionnalités prises en charge par le fournisseur, certaines méthodes et propriétés des objets **Recordset** sont disponibles et d'autres ne le sont pas. Pour continuer à explorer l'objet **Recordset**, imaginez un **jeu d'enregistrements** renvoyé par la base de données exemple Northwind sur Microsoft SQL Server 2000, à l'aide du code suivant :</span><span class="sxs-lookup"><span data-stu-id="36a8d-p102">**Recordsets** have methods and properties designed to make it easy to move through them and examine their contents. Depending on the functionality supported by the provider, some **Recordset** methods or properties might not be available. To continue exploring the **Recordset** object, consider a **Recordset** that would be returned from the Northwind sample database on Microsoft SQL Server 2000, using the following code:</span></span>

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

<span data-ttu-id="36a8d-p103">Cette requête SQL renvoie un **jeu d'enregistrements** constitué de cinq lignes (enregistrements) et de trois colonnes (champs). Les valeurs de chaque ligne sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p103">This SQL query returns a **Recordset** with five rows (records) and three columns (fields). The values for each row are shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="36a8d-111">CHAMP 0</span><span class="sxs-lookup"><span data-stu-id="36a8d-111">FIELD 0</span></span><br />
<span data-ttu-id="36a8d-112">Nom = ProductID</span><span class="sxs-lookup"><span data-stu-id="36a8d-112">Name = ProductID</span></span></p></th>
<th><p><span data-ttu-id="36a8d-113">CHAMP 1</span><span class="sxs-lookup"><span data-stu-id="36a8d-113">FIELD 1</span></span><br />
<span data-ttu-id="36a8d-114">Nom = ProductName</span><span class="sxs-lookup"><span data-stu-id="36a8d-114">Name = ProductName</span></span></p></th>
<th><p><span data-ttu-id="36a8d-115">CHAMP 2</span><span class="sxs-lookup"><span data-stu-id="36a8d-115">FIELD 2</span></span><br />
<span data-ttu-id="36a8d-116">Nom = UnitPrice</span><span class="sxs-lookup"><span data-stu-id="36a8d-116">Name = UnitPrice</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36a8d-117">7</span><span class="sxs-lookup"><span data-stu-id="36a8d-117">7</span></span></p></td>
<td><p><span data-ttu-id="36a8d-118">Pêches séchées bio Oncle Bob</span><span class="sxs-lookup"><span data-stu-id="36a8d-118">Uncle Bob's Organic Dried Pears</span></span></p></td>
<td><p><span data-ttu-id="36a8d-119">30.0000</span><span class="sxs-lookup"><span data-stu-id="36a8d-119">30.0000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36a8d-120">14</span><span class="sxs-lookup"><span data-stu-id="36a8d-120">14</span></span></p></td>
<td><p><span data-ttu-id="36a8d-121">Tofu</span><span class="sxs-lookup"><span data-stu-id="36a8d-121">Tofu</span></span></p></td>
<td><p><span data-ttu-id="36a8d-122">23.2500</span><span class="sxs-lookup"><span data-stu-id="36a8d-122">23.2500</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36a8d-123">28</span><span class="sxs-lookup"><span data-stu-id="36a8d-123">28</span></span></p></td>
<td><p><span data-ttu-id="36a8d-124">Choucroute Frau Kraut</span><span class="sxs-lookup"><span data-stu-id="36a8d-124">Rssle Sauerkraut</span></span></p></td>
<td><p><span data-ttu-id="36a8d-125">45.6000</span><span class="sxs-lookup"><span data-stu-id="36a8d-125">45.6000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36a8d-126">51</span><span class="sxs-lookup"><span data-stu-id="36a8d-126">51</span></span></p></td>
<td><p><span data-ttu-id="36a8d-127">Pommes séchées Manjimup</span><span class="sxs-lookup"><span data-stu-id="36a8d-127">Manjimup Dried Apples</span></span></p></td>
<td><p><span data-ttu-id="36a8d-128">53.0000</span><span class="sxs-lookup"><span data-stu-id="36a8d-128">53.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36a8d-129">74</span><span class="sxs-lookup"><span data-stu-id="36a8d-129">74</span></span></p></td>
<td><p><span data-ttu-id="36a8d-130">Tofu LongVi</span><span class="sxs-lookup"><span data-stu-id="36a8d-130">Longlife Tofu</span></span></p></td>
<td><p><span data-ttu-id="36a8d-131">10.0000</span><span class="sxs-lookup"><span data-stu-id="36a8d-131">10.0000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="36a8d-132">La section suivante explique comment trouver la position actuelle du curseur dans cet exemple de **jeu d'enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="36a8d-132">The next section will explain how to locate the current position of the cursor in this sample **Recordset**.</span></span>

