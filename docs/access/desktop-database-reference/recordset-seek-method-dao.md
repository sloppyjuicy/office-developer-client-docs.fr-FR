---
title: Méthode Recordset.Seek (DAO)
TOCTitle: Seek Method
ms:assetid: ef83d909-c962-b016-7d33-36eacdc25c2c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836416(v=office.15)
ms:contentKeyID: 48548585
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053061
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: db2c90d42feacee58af9eea30a2d99439cb4ddaf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307601"
---
# <a name="recordsetseek-method-dao"></a><span data-ttu-id="571f8-102">Méthode Recordset.Seek (DAO)</span><span class="sxs-lookup"><span data-stu-id="571f8-102">Recordset.Seek Method (DAO)</span></span>

<span data-ttu-id="571f8-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="571f8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="571f8-104">Localise l’enregistrement dans un objet **Recordset** de type table indexé qui correspond aux critères spécifiés pour l’index actuel et fait de cet enregistrement l’enregistrement actif (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="571f8-104">Locates the record in an indexed table-type **Recordset** object that satisfies the specified criteria for the current index and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="571f8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="571f8-105">Syntax</span></span>

<span data-ttu-id="571f8-106">*expression* .Seek(***Comparison***, ***Key1***, ***Key2***, ***Key3***, ***Key4***, ***Key5***, ***Key6***, ***Key7***, ***Key8***, ***Key9***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)</span><span class="sxs-lookup"><span data-stu-id="571f8-106">Seek(\*\*\*\*Comparison\*\*\*\*, \*\*\*\*\*\*Key1\*\*\*\*\*\*, \*\*\*\*\*\*Key2\*\*\*\*\*\*, \*\*\*\*\*\*Key3\*\*\*\*\*\*, \*\*\*\*\*\*Key4\*\*\*\*\*\*, \*\*\*\*\*\*Key5\*\*\*\*\*\*, \*\*\*\*\*\*Key6\*\*\*\*\*\*, ***Key7, Key8, Key9, Key10, Key11, Key12, Key13***)</span></span>

<span data-ttu-id="571f8-107">*expression* Variable qui représente un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="571f8-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="571f8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="571f8-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="571f8-109">Nom</span><span class="sxs-lookup"><span data-stu-id="571f8-109">Name</span></span></p></th>
<th><p><span data-ttu-id="571f8-110">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="571f8-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="571f8-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="571f8-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="571f8-112">Description</span><span class="sxs-lookup"><span data-stu-id="571f8-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="571f8-113"><em>Comparaison</em></span><span class="sxs-lookup"><span data-stu-id="571f8-113"><em>Comparison</em></span></span></p></td>
<td><p><span data-ttu-id="571f8-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="571f8-114">Required</span></span></p></td>
<td><p><span data-ttu-id="571f8-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="571f8-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="571f8-116">L'une des expressions de chaîne suivantes : &lt;, &lt;=, =, &gt;= ou &gt;.</span><span class="sxs-lookup"><span data-stu-id="571f8-116">One of the following string expressions: &lt;, &lt;=, =, &gt;=, or &gt;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="571f8-117"><em>Key1, Key2...Key13</em></span><span class="sxs-lookup"><span data-stu-id="571f8-117"><em>Key1, Key2...Key13</em></span></span></p></td>
<td><p><span data-ttu-id="571f8-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="571f8-118">Required</span></span></p></td>
<td><p><span data-ttu-id="571f8-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="571f8-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="571f8-120">Une ou plusieurs valeurs correspondant aux champs dans l'index actuel de l'objet <strong>Recordset</strong>, comme indiqué par son paramètre de propriété <strong>Index</strong>.</span><span class="sxs-lookup"><span data-stu-id="571f8-120">One or more values corresponding to fields in the <strong>Recordset</strong> object's current index, as specified by its <strong>Index</strong> property setting.</span></span> <span data-ttu-id="571f8-121">Vous pouvez utiliser jusqu'à 13 arguments clés.</span><span class="sxs-lookup"><span data-stu-id="571f8-121">You can use up to 13 key arguments.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="571f8-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="571f8-122">Remarks</span></span>

<span data-ttu-id="571f8-p102">Vous devez définir l’index actuel avec la propriété **Index** avant d’utiliser la méthode **Seek**. Si l’index identifie un champ de clé non unique, la méthode **Seek** localise le premier enregistrement qui correspond aux critères.</span><span class="sxs-lookup"><span data-stu-id="571f8-p102">You must set the current index with the **Index** property before you use **Seek**. If the index identifies a nonunique key field, **Seek** locates the first record that satisfies the criteria.</span></span>

<span data-ttu-id="571f8-125">La méthode **Seek** effectue une recherche dans les champs de clé spécifiés et localise le premier enregistrement qui correspond aux critères spécifiés par comparaison et key1.</span><span class="sxs-lookup"><span data-stu-id="571f8-125">The Seek method searches through the specified key fields and locates the first record that satisfies the criteria specified by comparison and key1.</span></span> <span data-ttu-id="571f8-126">Une fois trouvé, cet enregistrement devient l’enregistrement actif et la propriété **NoMatch** est définie sur **False**.</span><span class="sxs-lookup"><span data-stu-id="571f8-126">Once found, it makes that record current and sets the **NoMatch** property to **False**.</span></span> <span data-ttu-id="571f8-127">Si la méthode **Seek** ne trouve pas de correspondance, la propriété **NoMatch** est définie sur **True**, et l’enregistrement actif n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="571f8-127">If the **Seek** method fails to locate a match, the **NoMatch** property is set to **True**, and the current record is undefined.</span></span>

<span data-ttu-id="571f8-128">Si le paramètre de comparaison est égal (=), supérieur ou égal (\>=) ou supérieur à (\>), la méthode **Seek** commence au début de l’index et effectue une recherche vers l’avant.</span><span class="sxs-lookup"><span data-stu-id="571f8-128">If comparison is equal (=), greater than or equal (>=), or greater than (>), Seek starts at the beginning of the index and searches forward.</span></span>

<span data-ttu-id="571f8-129">Si le paramètre de comparaison est inférieur (\<) ou inférieur ou égal à (\<=), la méthode **Seek** commence à la fin de l’index et effectue une recherche vers l’arrière.</span><span class="sxs-lookup"><span data-stu-id="571f8-129">If comparison is less than (<) or less than or equal (<=), Seek starts at the end of the index and searches backward.</span></span> <span data-ttu-id="571f8-130">Toutefois, s'il existe des doublons à la fin de l'index, la méthode **Seek** démarre arbitrairement à partir de l'un des doublons, puis effectue une recherche vers l'arrière.</span><span class="sxs-lookup"><span data-stu-id="571f8-130">However, if there are duplicate index entries at the end of the index, **Seek** starts at an arbitrary entry among the duplicates and then searches backward.</span></span>

<span data-ttu-id="571f8-131">Vous devez spécifier des valeurs pour tous les champs définis dans l'index.</span><span class="sxs-lookup"><span data-stu-id="571f8-131">You must specify values for all fields defined in the index.</span></span> <span data-ttu-id="571f8-132">Si vous utilisez la méthode **Seek** avec un index à plusieurs colonnes et que vous ne spécifiez pas de valeur de comparaison pour chaque champ de l’index, vous ne pouvez pas utiliser l’opérateur égal (=) dans la comparaison.</span><span class="sxs-lookup"><span data-stu-id="571f8-132">If you use **Seek** with a multiple-column index, and you don't specify a comparison value for every field in the index, then you cannot use the equal (=) operator in the comparison.</span></span> <span data-ttu-id="571f8-133">C’est parce que certains champs de critères (key2, key3 et ainsi de suite) utilisent par défaut Null, ce qui ne correspondra pas.</span><span class="sxs-lookup"><span data-stu-id="571f8-133">That's because some of the criteria fields (key2, key3, and so on) will default to Null, which will probably not match.</span></span> <span data-ttu-id="571f8-134">Par conséquent, pour que l’opérateur d’égalité (=) fonctionne correctement, vous devez avoir un enregistrement entièrement **null** à l’exception de la clé que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="571f8-134">Therefore, the equal operator will work correctly only if you have a record which is all **null** except the key you're looking for.</span></span> <span data-ttu-id="571f8-135">Nous vous recommandons d’utiliser l’opérateur supérieur ou égal (\>=) à la place.</span><span class="sxs-lookup"><span data-stu-id="571f8-135">It's recommended that you use the greater than or equal (>=) operator instead.</span></span>

<span data-ttu-id="571f8-136">L’argument key1 doit être identique à celui du champ de données correspondant dans l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="571f8-136">The key1 argument must be of the same field data type as the corresponding field in the current index.</span></span> <span data-ttu-id="571f8-137">Par exemple, si l’index actuel fait référence à un champ numérique (par exemple, « ID employé »), key1 doit être numérique.</span><span class="sxs-lookup"><span data-stu-id="571f8-137">For example, if the current index refers to a number field (such as Employee ID), key1 must be numeric.</span></span> <span data-ttu-id="571f8-138">De même, si l’index actuel fait référence à un champ de texte (par exemple, « Nom »), key1 doit être une chaîne.</span><span class="sxs-lookup"><span data-stu-id="571f8-138">Similarly, if the current index refers to a Text field (such as Last Name), key1 must be a string.</span></span>

<span data-ttu-id="571f8-139">Il n’est pas obligatoire qu’un enregistrement soit actif lorsque vous utilisez la méthode **Seek**.</span><span class="sxs-lookup"><span data-stu-id="571f8-139">There doesn't have to be a current record when you use **Seek**.</span></span>

<span data-ttu-id="571f8-140">Vous pouvez utiliser la collection d’**[index](indexes-collection-dao.md)** pour énumérer les index existants.</span><span class="sxs-lookup"><span data-stu-id="571f8-140">You can use the **[Indexes](indexes-collection-dao.md)** collection to enumerate the existing indexes.</span></span>

<span data-ttu-id="571f8-p107">Pour localiser un enregistrement dans un **Recordset** de type feuille de réponse dynamique ou capture instantanée qui répond à une condition spécifique non couverte pas les index existants, utilisez les méthodes **[Find](recordset-findfirst-method-dao.md)**. Pour inclure tous les enregistrements, et pas uniquement ceux qui répondent à une condition spécifique, utilisez les méthodes **[Move](recordset-movefirst-method-dao.md)** pour passer d’un enregistrement à un autre.</span><span class="sxs-lookup"><span data-stu-id="571f8-p107">To locate a record in a dynaset- or snapshot-type **Recordset** that satisfies a specific condition that is not covered by existing indexes, use the **[Find](recordset-findfirst-method-dao.md)** methods. To include all records, not just those that satisfy a specific condition, use the **[Move](recordset-movefirst-method-dao.md)** methods to move from record to record.</span></span>

<span data-ttu-id="571f8-p108">Vous ne pouvez pas utiliser la méthode **Seek** sur une table liée, car vous ne pouvez pas ouvrir des tables liées en tant qu’objets **Recordset** de type table. Toutefois, si vous utilisez la méthode **[OpenDatabase](dbengine-opendatabase-method-dao.md)** pour ouvrir directement une base de données ISAM (non ODBC) installable, vous pouvez utiliser **Seek** sur les tables de cette base de données.</span><span class="sxs-lookup"><span data-stu-id="571f8-p108">You can't use the **Seek** method on a linked table because you can't open linked tables as table-type **Recordset** objects. However, if you use the **[OpenDatabase](dbengine-opendatabase-method-dao.md)** method to directly open an installable ISAM (non-ODBC) database, you can use **Seek** on tables in that database.</span></span>

## <a name="example"></a><span data-ttu-id="571f8-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="571f8-145">Example</span></span>

<span data-ttu-id="571f8-146">Cet exemple illustre la méthode **Seek** en autorisant l’utilisateur à rechercher un produit avec un numéro d’identification.</span><span class="sxs-lookup"><span data-stu-id="571f8-146">This example demonstrates the **Seek** method by allowing the user to search for a product based on an ID number.</span></span>

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
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

<span data-ttu-id="571f8-p109">Cet exemple de code montre comment utiliser la propriété **NoMatch** pour déterminer si les opérations **Seek** et **FindFirst** ont abouti. Si ce n'est pas le cas, l'utilisateur en est informé de façon appropriée. Les procédures SeekMatch et FindMatch sont nécessaires à l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="571f8-p109">This example uses the **NoMatch** property to determine whether a **Seek** and a **FindFirst** were successful, and if not, to give appropriate feedback. The SeekMatch and FindMatch procedures are required for this procedure to run.</span></span>

```vb
    Sub NoMatchX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
       Dim rstCustomers As Recordset 
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

<br/>

<span data-ttu-id="571f8-149">L’exemple suivant montre comment utiliser la méthode Seek pour rechercher un enregistrement dans un tableau lié.</span><span class="sxs-lookup"><span data-stu-id="571f8-149">The following example shows how to use the Seek method to find a record in a linked table.</span></span>

<span data-ttu-id="571f8-150">**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="571f8-150">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```
