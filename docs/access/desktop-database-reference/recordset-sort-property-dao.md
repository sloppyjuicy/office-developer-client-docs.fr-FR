---
title: Propriété Recordset.Sort (DAO)
TOCTitle: Sort Property
ms:assetid: 9be9bf62-f713-537e-4df0-3a54d485a523
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198077(v=office.15)
ms:contentKeyID: 48546582
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053063
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 18547162e7a0d64cc0ac7b0cdb2f0afa79185985
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926261"
---
# <a name="recordsetsort-property-dao"></a><span data-ttu-id="6d9b8-102">Propriété Recordset.Sort (DAO)</span><span class="sxs-lookup"><span data-stu-id="6d9b8-102">Recordset.Sort property (DAO)</span></span>


<span data-ttu-id="6d9b8-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d9b8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d9b8-104">Définit ou renvoie l'ordre de tri des enregistrements d'un objet **[Recordset](recordset-object-dao.md)** (espace de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="6d9b8-104">Sets or returns the sort order for records in a **[Recordset](recordset-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="6d9b8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d9b8-105">Syntax</span></span>

<span data-ttu-id="6d9b8-106">*expression* . Tri</span><span class="sxs-lookup"><span data-stu-id="6d9b8-106">*expression* .Sort</span></span>

<span data-ttu-id="6d9b8-107">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="6d9b8-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d9b8-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="6d9b8-108">Remarks</span></span>

<span data-ttu-id="6d9b8-109">Vous pouvez utiliser la propriété **Sort** avec feuille de réponse dynamique et instantané – objets **Recordset** de type.</span><span class="sxs-lookup"><span data-stu-id="6d9b8-109">You can use the **Sort** property with dynaset– and snapshot–type **Recordset** objects.</span></span>

<span data-ttu-id="6d9b8-p101">Lorsque vous définissez cette propriété pour un objet, le tri est exécuté lorsqu'un autre objet **Recordset** est créé par la suite à partir de cet objet. Le paramètre de la propriété **Sort** remplace l'ordre de tri défini pour un objet **[QueryDef](querydef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="6d9b8-p101">When you set this property for an object, sorting occurs when a subsequent **Recordset** object is created from that object. The **Sort** property setting overrides any sort order specified for a **[QueryDef](querydef-object-dao.md)** object.</span></span>

<span data-ttu-id="6d9b8-112">Par défaut, l'ordre de tri est croissant (A à Z ou 0 à 100).</span><span class="sxs-lookup"><span data-stu-id="6d9b8-112">The default sort order is ascending (A to Z or 0 to 100).</span></span>

<span data-ttu-id="6d9b8-113">La propriété **Sort** ne s’applique aux objets **Recordset** de type table ou avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="6d9b8-113">The **Sort** property doesn't apply to table– or forward–only–type **Recordset** objects.</span></span> <span data-ttu-id="6d9b8-114">Pour trier un objet **Recordset** de type table, utilisez la propriété **[Index](recordset-index-property-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="6d9b8-114">To sort a table–type **Recordset** object, use the **[Index](recordset-index-property-dao.md)** property.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6d9b8-115">[!REMARQUE] Dans la plupart des cas, il est plus rapide d'ouvrir un nouvel objet <STRONG>Recordset</STRONG> à l'aide d'une instruction SQL qui comprend les critères de tri.</span><span class="sxs-lookup"><span data-stu-id="6d9b8-115">In many cases, it's faster to open a new <STRONG>Recordset</STRONG> object by using an SQL statement that includes the sorting criteria.</span></span></P>



## <a name="example"></a><span data-ttu-id="6d9b8-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="6d9b8-116">Example</span></span>

<span data-ttu-id="6d9b8-p103">Cet exemple illustre la propriété **Sort** en modifiant sa valeur et en créant un nouvel objet **Recordset**. La fonction SortOutput est nécessaire à l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="6d9b8-p103">This example demonstrates the **Sort** property by changing its value and creating a new **Recordset**. The SortOutput function is required for this procedure to run.</span></span>

```vb
    Sub SortX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim rstSortEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     SortOutput "Original Recordset:", rstEmployees 
     .Sort = "LastName, FirstName" 
     ' Print report showing Sort property and record order. 
     SortOutput _ 
     "Recordset after changing Sort property:", _ 
     rstEmployees 
     ' Open new Recordset from current one. 
     Set rstSortEmployees = .OpenRecordset 
     ' Print report showing Sort property and record order. 
     SortOutput "New Recordset:", rstSortEmployees 
     rstSortEmployees.Close 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function SortOutput(strTemp As String, _ 
     rstTemp As Recordset) 
     
     With rstTemp 
     Debug.Print strTemp 
     Debug.Print " Sort = " & _ 
     IIf(.Sort <> "", .Sort, "[Empty]") 
     .MoveFirst 
     
     ' Enumerate Recordset. 
     Do While Not .EOF 
     Debug.Print " " & !LastName & _ 
     ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Function 
```

<br/>

<span data-ttu-id="6d9b8-p104">Lorsque vous savez quelles données sélectionner, il est généralement plus efficace de créer un objet **Recordset** avec une instruction SQL. Cet exemple montre comment créer un seul objet **Recordset** et obtenir les mêmes résultats que dans l'exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="6d9b8-p104">When you know the data you want to select, it's usually more efficient to create a **Recordset** with an SQL statement. This example shows how you can create just one **Recordset** and obtain the same results as in the preceding example.</span></span>

```vb
    Sub SortX2() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Open a Recordset from an SQL statement that specifies a 
     ' sort order. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("SELECT * " & _ 
     "FROM Employees ORDER BY LastName, FirstName", _ 
     dbOpenDynaset) 
     
     dbsNorthwind.Close 
     
    End Sub
```
