---
title: Recordset2. Seek, méthode (DAO)
TOCTitle: Seek Method
ms:assetid: 9871619b-a303-c97d-54c0-defc8d9b87f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197940(v=office.15)
ms:contentKeyID: 48546489
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9510faab9035f2b2cbcccae0a8ddefa484a95cb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307188"
---
# <a name="recordset2seek-method-dao"></a><span data-ttu-id="1839c-102">Recordset2. Seek, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="1839c-102">Recordset2.Seek method (DAO)</span></span>

<span data-ttu-id="1839c-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1839c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1839c-104">Localise l’enregistrement dans un objet **Recordset** de type table indexé qui correspond aux critères spécifiés pour l’index actuel et fait de cet enregistrement l’enregistrement actif (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="1839c-104">Locates the record in an indexed table-type **Recordset** object that satisfies the specified criteria for the current index and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="1839c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1839c-105">Syntax</span></span>

<span data-ttu-id="1839c-106">*expression* . Seek (***Comparison***, ***key1***, ***touche2***, ***Key3***, ***Key4***, ***Key5***, ***Key6***, ***Key7***, ***Key8***, ***Key9***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)</span><span class="sxs-lookup"><span data-stu-id="1839c-106">*expression* .Seek(***Comparison***, ***Key1***, ***Key2***, ***Key3***, ***Key4***, ***Key5***, ***Key6***, ***Key7***, ***Key8***, ***Key9***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)</span></span>

<span data-ttu-id="1839c-107">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="1839c-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="1839c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1839c-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1839c-109">Nom</span><span class="sxs-lookup"><span data-stu-id="1839c-109">Name</span></span></p></th>
<th><p><span data-ttu-id="1839c-110">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="1839c-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="1839c-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="1839c-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="1839c-112">Description</span><span class="sxs-lookup"><span data-stu-id="1839c-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1839c-113"><em>Comparison</em></span><span class="sxs-lookup"><span data-stu-id="1839c-113"><em>Comparison</em></span></span></p></td>
<td><p><span data-ttu-id="1839c-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1839c-114">Required</span></span></p></td>
<td><p><span data-ttu-id="1839c-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="1839c-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="1839c-116">L'une des expressions de chaîne suivantes : &lt;, &lt;=, =, &gt;= ou &gt;.</span><span class="sxs-lookup"><span data-stu-id="1839c-116">One of the following string expressions: &lt;, &lt;=, =, &gt;=, or &gt;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1839c-117"><em>Key1, Key2...Key13</em></span><span class="sxs-lookup"><span data-stu-id="1839c-117"><em>Key1, Key2...Key13</em></span></span></p></td>
<td><p><span data-ttu-id="1839c-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1839c-118">Required</span></span></p></td>
<td><p><span data-ttu-id="1839c-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1839c-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1839c-120">Une ou plusieurs valeurs correspondant aux champs dans l'index actuel de l'objet <strong>Recordset</strong>, comme indiqué par son paramètre de propriété <strong>Index</strong>.</span><span class="sxs-lookup"><span data-stu-id="1839c-120">One or more values corresponding to fields in the <strong>Recordset</strong> object's current index, as specified by its <strong>Index</strong> property setting.</span></span> <span data-ttu-id="1839c-121">Vous pouvez utiliser jusqu’à 13 arguments key.</span><span class="sxs-lookup"><span data-stu-id="1839c-121">You can use up to 13 key arguments.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1839c-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="1839c-122">Remarks</span></span>

<span data-ttu-id="1839c-p102">Vous devez définir l’index actuel avec la propriété **Index** avant d’utiliser la méthode **Seek**. Si l’index identifie un champ de clé non unique, la méthode **Seek** localise le premier enregistrement qui correspond aux critères.</span><span class="sxs-lookup"><span data-stu-id="1839c-p102">You must set the current index with the **Index** property before you use **Seek**. If the index identifies a nonunique key field, **Seek** locates the first record that satisfies the criteria.</span></span>

<span data-ttu-id="1839c-125">La méthode **Seek** recherche dans les champs de clé spécifiés et localise le premier enregistrement qui correspond aux critères spécifiés par Comparison et key1.</span><span class="sxs-lookup"><span data-stu-id="1839c-125">The **Seek** method searches through the specified key fields and locates the first record that satisfies the criteria specified by comparison and key1.</span></span> <span data-ttu-id="1839c-126">Une fois trouvé, cet enregistrement devient l’enregistrement actif et la propriété **NoMatch** est définie sur **False**.</span><span class="sxs-lookup"><span data-stu-id="1839c-126">Once found, it makes that record current and sets the **NoMatch** property to **False**.</span></span> <span data-ttu-id="1839c-127">Si la méthode **Seek** ne trouve pas de correspondance, la propriété **NoMatch** est définie sur **True**, et l’enregistrement actif n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="1839c-127">If the **Seek** method fails to locate a match, the **NoMatch** property is set to **True**, and the current record is undefined.</span></span>

<span data-ttu-id="1839c-128">Si comparaison est égal (=), supérieur ou égal (\>=) ou supérieur à (\>), la méthode **Seek** commence au début de l'index et effectue une recherche vers l'avant.</span><span class="sxs-lookup"><span data-stu-id="1839c-128">If comparison is equal (=), greater than or equal (\>=), or greater than (\>), **Seek** starts at the beginning of the index and searches forward.</span></span>

<span data-ttu-id="1839c-129">Si comparaison est inférieur à (\<) ou inférieur ou égal (\<=), la méthode **Seek** commence à la fin de l'index et effectue une recherche vers l'arrière.</span><span class="sxs-lookup"><span data-stu-id="1839c-129">If comparison is less than (\<) or less than or equal (\<=), **Seek** starts at the end of the index and searches backward.</span></span> <span data-ttu-id="1839c-130">Toutefois, s'il existe des doublons à la fin de l'index, la méthode **Seek** démarre arbitrairement à partir de l'un des doublons, puis effectue une recherche vers l'arrière.</span><span class="sxs-lookup"><span data-stu-id="1839c-130">However, if there are duplicate index entries at the end of the index, **Seek** starts at an arbitrary entry among the duplicates and then searches backward.</span></span>

<span data-ttu-id="1839c-131">Vous devez spécifier des valeurs pour tous les champs définis dans l'index.</span><span class="sxs-lookup"><span data-stu-id="1839c-131">You must specify values for all fields defined in the index.</span></span> <span data-ttu-id="1839c-132">Si vous utilisez la méthode **Seek** avec un index à plusieurs colonnes et que vous ne spécifiez pas de valeur de comparaison pour chaque champ de l’index, vous ne pouvez pas utiliser l’opérateur égal (=) dans la comparaison.</span><span class="sxs-lookup"><span data-stu-id="1839c-132">If you use **Seek** with a multiple-column index, and you don't specify a comparison value for every field in the index, then you cannot use the equal (=) operator in the comparison.</span></span> <span data-ttu-id="1839c-133">Ceci est dû au fait que certains champs de critères (key2, key3, etc.) seront définis par défaut sur Null, et ne correspondront probablement pas.</span><span class="sxs-lookup"><span data-stu-id="1839c-133">That's because some of the criteria fields (key2, key3, and so on) will default to Null, which will probably not match.</span></span> <span data-ttu-id="1839c-134">Par conséquent, l’opérateur égal ne fonctionnera correctement que si vous disposez d’un enregistrement entièrement **null**, à l’exception de la clé que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="1839c-134">Therefore, the equal operator will work correctly only if you have a record which is all **null** except the key you're looking for.</span></span> <span data-ttu-id="1839c-135">Il est recommandé d'utiliser à la place l'opérateur supérieur ou\>égal (=).</span><span class="sxs-lookup"><span data-stu-id="1839c-135">It's recommended that you use the greater than or equal (\>=) operator instead.</span></span>

<span data-ttu-id="1839c-136">L’argument key1 doit être du même type de champ que le champ correspondant dans l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="1839c-136">The key1 argument must be of the same field data type as the corresponding field in the current index.</span></span> <span data-ttu-id="1839c-137">Par exemple, si l’index actuel fait référence à un champ numérique (comme Employee ID), key1 doit être numérique.</span><span class="sxs-lookup"><span data-stu-id="1839c-137">For example, if the current index refers to a number field (such as Employee ID), key1 must be numeric.</span></span> <span data-ttu-id="1839c-138">De même, si l’index actuel fait référence à un champ de texte (comme Last Name), key1 doit être une chaîne.</span><span class="sxs-lookup"><span data-stu-id="1839c-138">Similarly, if the current index refers to a Text field (such as Last Name), key1 must be a string.</span></span>

<span data-ttu-id="1839c-139">Il n'est pas nécessaire d'avoir un enregistrement actif pour utiliser **Seek**.</span><span class="sxs-lookup"><span data-stu-id="1839c-139">There doesn't have to be a current record when you use **Seek**.</span></span>

<span data-ttu-id="1839c-140">Vous pouvez utiliser la collection **[Indexes](indexes-collection-dao.md)** pour énumérer les index existants.</span><span class="sxs-lookup"><span data-stu-id="1839c-140">You can use the **[Indexes](indexes-collection-dao.md)** collection to enumerate the existing indexes.</span></span>

<span data-ttu-id="1839c-p107">Pour rechercher un enregistrement dans un objet **Recordset** de type feuille de réponse dynamique ou instantané qui satisfasse à une condition spécifique non représentée par les index existants, utilisez la méthode **[Find](recordset2-findfirst-method-dao.md)**. Pour inclure tous les enregistrements, et pas seulement ceux qui répondent à une condition spécifique, utilisez la méthode **[Move](recordset-movefirst-method-dao.md)** pour passer d'un enregistrement à un autre.</span><span class="sxs-lookup"><span data-stu-id="1839c-p107">To locate a record in a dynaset- or snapshot-type **Recordset** that satisfies a specific condition that is not covered by existing indexes, use the **[Find](recordset2-findfirst-method-dao.md)** methods. To include all records, not just those that satisfy a specific condition, use the **[Move](recordset-movefirst-method-dao.md)** methods to move from record to record.</span></span>

<span data-ttu-id="1839c-p108">Vous ne pouvez pas appliquer la méthode **Seek** à une table liée, car les tables liées ne peuvent pas être ouvertes en tant qu'objets **Recordset** de type table. Cependant, si vous vous servez de la méthode **[OpenDatabase](dbengine-opendatabase-method-dao.md)** pour ouvrir directement une base de données ISAM installable (non ODBC), vous pouvez appliquer la méthode **Seek** aux tables de cette base de données.</span><span class="sxs-lookup"><span data-stu-id="1839c-p108">You can't use the **Seek** method on a linked table because you can't open linked tables as table-type **Recordset** objects. However, if you use the **[OpenDatabase](dbengine-opendatabase-method-dao.md)** method to directly open an installable ISAM (non-ODBC) database, you can use **Seek** on tables in that database.</span></span>

## <a name="example"></a><span data-ttu-id="1839c-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="1839c-145">Example</span></span>

<span data-ttu-id="1839c-146">Cet exemple illustre la méthode **Seek** en autorisant l’utilisateur à rechercher un produit avec un numéro d’identification.</span><span class="sxs-lookup"><span data-stu-id="1839c-146">This example demonstrates the **Seek** method by allowing the user to search for a product based on an ID number.</span></span>

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

<span data-ttu-id="1839c-p109">Cet exemple de code montre comment utiliser la propriété **NoMatch** pour déterminer si les opérations **Seek** et **FindFirst** ont abouti. Si ce n'est pas le cas, l'utilisateur en est informé de façon appropriée. Les procédures SeekMatch et FindMatch sont nécessaires à l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="1839c-p109">This example uses the **NoMatch** property to determine whether a **Seek** and a **FindFirst** were successful, and if not, to give appropriate feedback. The SeekMatch and FindMatch procedures are required for this procedure to run.</span></span>

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
