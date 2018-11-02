---
title: Méthode Recordset2.Seek (DAO)
TOCTitle: Seek Method
ms:assetid: 9871619b-a303-c97d-54c0-defc8d9b87f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197940(v=office.15)
ms:contentKeyID: 48546489
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6dacfb1b46899397647c928c2b8032a97417fbf5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927416"
---
# <a name="recordset2seek-method-dao"></a><span data-ttu-id="ee6d0-102">Méthode Recordset2.Seek (DAO)</span><span class="sxs-lookup"><span data-stu-id="ee6d0-102">Recordset2.Seek method (DAO)</span></span>


<span data-ttu-id="ee6d0-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee6d0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ee6d0-104">Localise l'enregistrement dans un objet **Recordset** de type table indexée en fonction des critères spécifiés pour l'index actuel et en fait l'enregistrement actif (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="ee6d0-104">Locates the record in an indexed table-type **Recordset** object that satisfies the specified criteria for the current index and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="ee6d0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee6d0-105">Syntax</span></span>

<span data-ttu-id="ee6d0-106">*expression* . Seek (***comparaison***, ***touche1***, ***Key2***, ***Key3***, ***Touche4***, ***Touche5***, ***Touche6***, ***Touche7***, ***Touche8***, ***Touche9***, ***Touche10***, ***Touche11***, ***Touche12***, ***Touche13***)</span><span class="sxs-lookup"><span data-stu-id="ee6d0-106">*expression* .Seek(***Comparison***, ***Key1***, ***Key2***, ***Key3***, ***Key4***, ***Key5***, ***Key6***, ***Key7***, ***Key8***, ***Key9***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)</span></span>

<span data-ttu-id="ee6d0-107">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="ee6d0-107">*expression* A variable that represents a **Recordset2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="ee6d0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee6d0-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee6d0-109">Name</span><span class="sxs-lookup"><span data-stu-id="ee6d0-109">Name</span></span></p></th>
<th><p><span data-ttu-id="ee6d0-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="ee6d0-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="ee6d0-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="ee6d0-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="ee6d0-112">Description</span><span class="sxs-lookup"><span data-stu-id="ee6d0-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee6d0-113">Comparison</span><span class="sxs-lookup"><span data-stu-id="ee6d0-113">Comparison</span></span></p></td>
<td><p><span data-ttu-id="ee6d0-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ee6d0-114">Required</span></span></p></td>
<td><p><span data-ttu-id="ee6d0-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="ee6d0-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="ee6d0-116">L'une des expressions de chaîne suivantes : &lt;, &lt;=, =, &gt;= ou &gt;.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-116">One of the following string expressions: &lt;, &lt;=, =, &gt;=, or &gt;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee6d0-117">Key1, Key2...Key13</span><span class="sxs-lookup"><span data-stu-id="ee6d0-117">Key1, Key2...Key13</span></span></p></td>
<td><p><span data-ttu-id="ee6d0-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ee6d0-118">Required</span></span></p></td>
<td><p><span data-ttu-id="ee6d0-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ee6d0-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ee6d0-120">Une ou plusieurs valeurs correspondant aux champs dans l'index actuel de l'objet <strong>Recordset</strong>, comme indiqué par son paramètre de propriété <strong>Index</strong>.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-120">One or more values corresponding to fields in the <strong>Recordset</strong> object's current index, as specified by its <strong>Index</strong> property setting.</span></span> <span data-ttu-id="ee6d0-121">Vous pouvez utiliser les arguments clés jusqu'à 13.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-121">You can use up to 13 key arguments.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ee6d0-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="ee6d0-122">Remarks</span></span>

<span data-ttu-id="ee6d0-p102">Vous devez définir l'index actuel via la propriété **Index** avant d'utiliser la méthode **Seek**. Si l'index identifie un champ de clé non unique, **Seek** localise le premier enregistrement correspondant aux critères.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-p102">You must set the current index with the **Index** property before you use **Seek**. If the index identifies a nonunique key field, **Seek** locates the first record that satisfies the criteria.</span></span>

<span data-ttu-id="ee6d0-125">La méthode **Seek** recherche dans les champs de clé spécifiées et recherche le premier enregistrement qui répond aux critères spécifiés par comparaison et touche1.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-125">The **Seek** method searches through the specified key fields and locates the first record that satisfies the criteria specified by comparison and key1.</span></span> <span data-ttu-id="ee6d0-126">Une fois l'enregistrement trouvé, il devient actif et la propriété **NoMatch** reçoit la valeur **False**.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-126">Once found, it makes that record current and sets the **NoMatch** property to **False**.</span></span> <span data-ttu-id="ee6d0-127">Si la méthode **Seek** ne parvient pas à trouver de correspondance, la propriété **NoMatch** est affectée de la valeur **True**, et l'enregistrement actif n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-127">If the **Seek** method fails to locate a match, the **NoMatch** property is set to **True**, and the current record is undefined.</span></span>

<span data-ttu-id="ee6d0-128">Si la comparaison est égal (=), supérieur ou égal (\>=), supérieur ou (\>), **Seek** commence au début de l’index et de transférer des recherches.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-128">If comparison is equal (=), greater than or equal (\>=), or greater than (\>), **Seek** starts at the beginning of the index and searches forward.</span></span>

<span data-ttu-id="ee6d0-129">Si la comparaison est inférieure à (\<) ou inférieur ou égal (\<=), **Seek** commence à la fin de l’index et de recherche vers l’arrière.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-129">If comparison is less than (\<) or less than or equal (\<=), **Seek** starts at the end of the index and searches backward.</span></span> <span data-ttu-id="ee6d0-130">Toutefois, s'il existe des doublons à la fin de l'index, la méthode **Seek** démarre arbitrairement à partir de l'un des doublons, puis effectue une recherche vers l'arrière.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-130">However, if there are duplicate index entries at the end of the index, **Seek** starts at an arbitrary entry among the duplicates and then searches backward.</span></span>

<span data-ttu-id="ee6d0-131">Vous devez spécifier des valeurs pour tous les champs définis dans l'index.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-131">You must specify values for all fields defined in the index.</span></span> <span data-ttu-id="ee6d0-132">Si vous utilisez **Seek** avec un index à plusieurs colonnes, et que vous ne spécifiez pas de valeur de comparaison pour chaque champ de l'index, vous ne pouvez pas utiliser l'opérateur égal (=) dans la comparaison.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-132">If you use **Seek** with a multiple-column index, and you don't specify a comparison value for every field in the index, then you cannot use the equal (=) operator in the comparison.</span></span> <span data-ttu-id="ee6d0-133">C’est parce que certains des champs de critères (key2 key3 et ainsi de suite) par défaut Null, ce qui correspondra probablement pas.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-133">That's because some of the criteria fields (key2, key3, and so on) will default to Null, which will probably not match.</span></span> <span data-ttu-id="ee6d0-134">Par conséquent, l'opérateur égal ne fonctionnera correctement que s'il existe un enregistrement dont les valeurs sont toutes **null** hormis la clé que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-134">Therefore, the equal operator will work correctly only if you have a record which is all **null** except the key you're looking for.</span></span> <span data-ttu-id="ee6d0-135">Il est recommandé d’utiliser supérieur ou égal (\>=) opérateur à la place.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-135">It's recommended that you use the greater than or equal (\>=) operator instead.</span></span>

<span data-ttu-id="ee6d0-136">L’argument touche1 doit être du même type de données de champ que le champ correspondant dans l’index en cours.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-136">The key1 argument must be of the same field data type as the corresponding field in the current index.</span></span> <span data-ttu-id="ee6d0-137">Par exemple, si l’index actuel fait référence à un champ numérique (par exemple, ID d’employé), l’argument touche1 doit être numérique.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-137">For example, if the current index refers to a number field (such as Employee ID), key1 must be numeric.</span></span> <span data-ttu-id="ee6d0-138">De même, si l’index actuel fait référence à un champ de texte (tel que le nom de famille), touche1 doit être une chaîne.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-138">Similarly, if the current index refers to a Text field (such as Last Name), key1 must be a string.</span></span>

<span data-ttu-id="ee6d0-139">Il n'est pas nécessaire d'avoir un enregistrement actif pour utiliser **Seek**.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-139">There doesn't have to be a current record when you use **Seek**.</span></span>

<span data-ttu-id="ee6d0-140">Vous pouvez utiliser la collection **[Indexes](indexes-collection-dao.md)** pour énumérer les index existants.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-140">You can use the **[Indexes](indexes-collection-dao.md)** collection to enumerate the existing indexes.</span></span>

<span data-ttu-id="ee6d0-p107">Pour rechercher un enregistrement dans un objet **Recordset** de type feuille de réponse dynamique ou instantané qui satisfasse à une condition spécifique non représentée par les index existants, utilisez la méthode **[Find](recordset2-findfirst-method-dao.md)**. Pour inclure tous les enregistrements, et pas seulement ceux qui répondent à une condition spécifique, utilisez la méthode **[Move](recordset-movefirst-method-dao.md)** pour passer d'un enregistrement à un autre.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-p107">To locate a record in a dynaset- or snapshot-type **Recordset** that satisfies a specific condition that is not covered by existing indexes, use the **[Find](recordset2-findfirst-method-dao.md)** methods. To include all records, not just those that satisfy a specific condition, use the **[Move](recordset-movefirst-method-dao.md)** methods to move from record to record.</span></span>

<span data-ttu-id="ee6d0-p108">Vous ne pouvez pas appliquer la méthode **Seek** à une table liée, car les tables liées ne peuvent pas être ouvertes en tant qu'objets **Recordset** de type table. Cependant, si vous vous servez de la méthode **[OpenDatabase](dbengine-opendatabase-method-dao.md)** pour ouvrir directement une base de données ISAM installable (non ODBC), vous pouvez appliquer la méthode **Seek** aux tables de cette base de données.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-p108">You can't use the **Seek** method on a linked table because you can't open linked tables as table-type **Recordset** objects. However, if you use the **[OpenDatabase](dbengine-opendatabase-method-dao.md)** method to directly open an installable ISAM (non-ODBC) database, you can use **Seek** on tables in that database.</span></span>

## <a name="example"></a><span data-ttu-id="ee6d0-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="ee6d0-145">Example</span></span>

<span data-ttu-id="ee6d0-146">Cet exemple démontre la méthode **Seek** en permettant à l'utilisateur de rechercher un produit en fonction d'un numéro d'identification.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-146">This example demonstrates the **Seek** method by allowing the user to search for a product based on an ID number.</span></span>

```vb
    Sub SeekX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim intFirst As Integer 
     Dim intLast As Integer 
     Dim strMessage As String 
     Dim strSeek As String 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' You must open a table-type Recordset to use an index, 
     ' and hence the Seek method. 
     Set rstProducts = _ 
     dbsNorthwind.OpenRecordset("Products", dbOpenTable) 
     
     With rstProducts 
     ' Set the index. 
     .Index = "PrimaryKey" 
     
     ' Get the lowest and highest product IDs. 
     .MoveLast 
     intLast = !ProductID 
     .MoveFirst 
     intFirst = !ProductID 
     
     Do While True 
     ' Display current record information and ask user 
     ' for ID number. 
     strMessage = "Product ID: " & !ProductID & vbCr & _ 
     "Name: " & !ProductName & vbCr & vbCr & _ 
     "Enter a product ID between " & intFirst & _ 
     " and " & intLast & "." 
     strSeek = InputBox(strMessage) 
     
     If strSeek = "" Then Exit Do 
     
     ' Store current bookmark in case the Seek fails. 
     varBookmark = .Bookmark 
     
     .Seek "=", Val(strSeek) 
     
     ' Return to the current record if the Seek fails. 
     If .NoMatch Then 
     MsgBox "ID not found!" 
     .Bookmark = varBookmark 
     End If 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="ee6d0-p109">Cet exemple de code montre comment utiliser la propriété **NoMatch** pour déterminer si les opérations **Seek** et **FindFirst** ont abouti. Si ce n'est pas le cas, l'utilisateur en est informé de façon appropriée. Les procédures SeekMatch et FindMatch sont nécessaires à l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="ee6d0-p109">This example uses the **NoMatch** property to determine whether a **Seek** and a **FindFirst** were successful, and if not, to give appropriate feedback. The SeekMatch and FindMatch procedures are required for this procedure to run.</span></span>

```vb
    Sub NoMatchX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim rstCustomers As Recordset2 
     Dim strMessage As String 
     Dim strSeek As String 
     Dim strCountry As String 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Default is dbOpenTable; required if Index property will 
     ' be used. 
     Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
     With rstProducts 
     .Index = "PrimaryKey" 
     
     Do While True 
     ' Show current record information; ask user for 
     ' input. 
     strMessage = "NoMatch with Seek method" & vbCr & _ 
     "Product ID: " & !ProductID & vbCr & _ 
     "Product Name: " & !ProductName & vbCr & _ 
     "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
     "Enter a product ID." 
     strSeek = InputBox(strMessage) 
     If strSeek = "" Then Exit Do 
     
     ' Call procedure that seeks for a record based on 
     ' the ID number supplied by the user. 
     SeekMatch rstProducts, Val(strSeek) 
     Loop 
     
     .Close 
     End With 
     
     Set rstCustomers = dbsNorthwind.OpenRecordset( _ 
     "SELECT CompanyName, Country FROM Customers " & _ 
     "ORDER BY CompanyName", dbOpenSnapshot) 
     
     With rstCustomers 
     
     Do While True 
     ' Show current record information; ask user for 
     ' input. 
     strMessage = "NoMatch with FindFirst method" & _ 
     vbCr & "Customer Name: " & !CompanyName & _ 
     vbCr & "Country: " & !Country & vbCr & _ 
     "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
     "Enter country on which to search." 
     strCountry = Trim(InputBox(strMessage)) 
     If strCountry = "" Then Exit Do 
     
     ' Call procedure that finds a record based on 
     ' the country name supplied by the user. 
     FindMatch rstCustomers, _ 
     "Country = '" & strCountry & "'" 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub SeekMatch(rstTemp As Recordset, _ 
     intSeek As Integer) 
     
     Dim varBookmark As Variant 
     Dim strMessage As String 
     
     With rstTemp 
     ' Store current record location. 
     varBookmark = .Bookmark 
     .Seek "=", intSeek 
     
     ' If Seek method fails, notify user and return to the 
     ' last current record. 
     If .NoMatch Then 
     strMessage = _ 
     "Not found! Returning to current record." & _ 
     vbCr & vbCr & "NoMatch = " & .NoMatch 
     MsgBox strMessage 
     .Bookmark = varBookmark 
     End If 
     
     End With 
     
    End Sub 
     
    Sub FindMatch(rstTemp As Recordset, _ 
     strFind As String) 
     
     Dim varBookmark As Variant 
     Dim strMessage As String 
     
     With rstTemp 
     ' Store current record location. 
     varBookmark = .Bookmark 
     .FindFirst strFind 
     
     ' If Find method fails, notify user and return to the 
     ' last current record. 
     If .NoMatch Then 
     strMessage = _ 
     "Not found! Returning to current record." & _ 
     vbCr & vbCr & "NoMatch = " & .NoMatch 
     MsgBox strMessage 
     .Bookmark = varBookmark 
     End If 
     
     End With 
     
    End Sub
```
