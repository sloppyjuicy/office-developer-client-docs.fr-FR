---
title: Database.OpenRecordset, méthode (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: a243bc79-cac4-fe12-768d-d3d017954e78
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820966(v=office.15)
ms:contentKeyID: 48546753
ms.date: 06/04/2019
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052939
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: b13abd7f3f2c856a0f1a1288717d6f8affb81252
ms.sourcegitcommit: 4a570873914c58dd4cdbe97b5d9ec41866dc797c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2019
ms.locfileid: "34675742"
---
# <a name="databaseopenrecordset-method-dao"></a><span data-ttu-id="e5fbc-102">Database.OpenRecordset, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="e5fbc-102">Database.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="e5fbc-103">**S’applique à** : Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e5fbc-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="e5fbc-104">Crée un objet **[Recordset](recordset-object-dao.md)** et l’ajoute à la collection **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="e5fbc-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5fbc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5fbc-105">Syntax</span></span>

<span data-ttu-id="e5fbc-106">*expression*.**OpenRecordset** (_Name_, _Type_, _Options_, _LockEdit_)</span><span class="sxs-lookup"><span data-stu-id="e5fbc-106">*expression*.**OpenRecordset** (_Name_, _Type_, _Options_, _LockEdit_)</span></span>

<span data-ttu-id="e5fbc-107">*expression* Variable qui représente un objet **Database**.</span><span class="sxs-lookup"><span data-stu-id="e5fbc-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="e5fbc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5fbc-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e5fbc-109">Nom</span><span class="sxs-lookup"><span data-stu-id="e5fbc-109">Name</span></span></p></th>
<th><p><span data-ttu-id="e5fbc-110">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="e5fbc-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="e5fbc-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="e5fbc-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="e5fbc-112">Description</span><span class="sxs-lookup"><span data-stu-id="e5fbc-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e5fbc-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="e5fbc-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="e5fbc-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e5fbc-114">Required</span></span></p></td>
<td><p><span data-ttu-id="e5fbc-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="e5fbc-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="e5fbc-p101">Source des enregistrements du nouveau <strong>Recordset</strong>. La source peut être un nom de table, un nom de requête ou une instruction SQL qui renvoie des enregistrements. Pour les objets <strong>Recordset</strong> de type table dans les bases de données du moteur de base de données Microsoft Access, la source peut uniquement être un nom de table.</span><span class="sxs-lookup"><span data-stu-id="e5fbc-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5fbc-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="e5fbc-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="e5fbc-120">Facultatif</span><span class="sxs-lookup"><span data-stu-id="e5fbc-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="e5fbc-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e5fbc-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e5fbc-122">Constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> qui indique le type de <strong>Recordset</strong> à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="e5fbc-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="e5fbc-123"><strong>REMARQUE</strong> : si vous ouvrez un objet <strong>Recordset</strong> dans un espace de travail Microsoft Access et que vous n’indiquez aucun type, <strong>OpenRecordset</strong> crée un objet <strong>Recordset</strong> de type table, si possible.</span><span class="sxs-lookup"><span data-stu-id="e5fbc-123"><strong>NOTE</strong>: If you open a <strong>Recordset</strong> in a Microsoft Access workspace and you don't specify a type, <strong>OpenRecordset</strong> creates a table-type <strong>Recordset</strong>, if possible.</span></span> <span data-ttu-id="e5fbc-124">If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="e5fbc-124">If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5fbc-125"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="e5fbc-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="e5fbc-126">Facultatif</span><span class="sxs-lookup"><span data-stu-id="e5fbc-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="e5fbc-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e5fbc-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e5fbc-128">Combinaison de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> qui indiquent les caractéristiques du nouveau <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="e5fbc-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="e5fbc-129"><strong>REMARQUE</strong> : <strong>dbConsistent</strong> et <strong>dbInconsistent</strong> s’excluent mutuellement, et l’utilisation de ces deux constantes peut entraîner une erreur.</span><span class="sxs-lookup"><span data-stu-id="e5fbc-129"><strong>NOTE</strong>: The constants <strong>dbConsistent</strong> and <strong>dbInconsistent</strong> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="e5fbc-130">Fournir un argument LockEdit lorsque Options utilise la constante <strong>dbReadOnly</strong> génère également une erreur.</span><span class="sxs-lookup"><span data-stu-id="e5fbc-130">Supplying a LockEdit argument when Options uses the <strong>dbReadOnly</strong> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5fbc-131"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="e5fbc-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="e5fbc-132">Facultatif</span><span class="sxs-lookup"><span data-stu-id="e5fbc-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="e5fbc-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e5fbc-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e5fbc-134">Constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> qui détermine le verrouillage du <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="e5fbc-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="e5fbc-135"><strong>REMARQUE</strong> : vous pouvez utiliser <strong>dbReadOnly</strong> dans l’argument Options ou l’argument LockedEdit, mais pas dans les deux.</span><span class="sxs-lookup"><span data-stu-id="e5fbc-135"><strong>NOTE</strong>: You can use <strong>dbReadOnly</strong> in either the Options argument or the LockedEdit argument, but not both.</span></span> <span data-ttu-id="e5fbc-136">Si vous l’utilisez dans les deux arguments, une erreur d’exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="e5fbc-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="e5fbc-137">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e5fbc-137">Return value</span></span>

<span data-ttu-id="e5fbc-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="e5fbc-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="e5fbc-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="e5fbc-139">Remarks</span></span>

<span data-ttu-id="e5fbc-p105">En règle générale, si l’utilisateur obtient cette erreur lors de la mise à jour d’un enregistrement, votre code doit actualiser le contenu des champs et récupérer les valeurs nouvellement modifiées. Si une erreur survient lors de la suppression d’un enregistrement, votre code peut afficher les données du nouvel enregistrement à l’utilisateur, ainsi qu’un message indiquant que les données ont récemment été modifiées. À ce stade, votre code peut demander une confirmation pour s’assurer que l’utilisateur souhaite toujours supprimer l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e5fbc-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="e5fbc-143">Vous pouvez également utiliser la constante **dbSeeChanges** si vous ouvrez un **Recordset** dans un espace de travail ODBC connecté au moteur de base de données Microsoft Access par rapport à une table Microsoft SQL Server 6.0 (ou version ultérieure) qui comporte une colonne IDENTITY, sinon une erreur peut survenir.</span><span class="sxs-lookup"><span data-stu-id="e5fbc-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="e5fbc-p106">L’ouverture de plusieurs objets **Recordset** sur une source de données ODBC peut échouer car la connexion est occupée par un appel **OpenRecordset** précédent. Pour éviter cela, vous pouvez remplir complètement l’objet **Recordset** à l’aide de la méthode **MoveLast** dès l’ouverture du **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="e5fbc-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="e5fbc-146">La fermeture d’un **Recordset** avec la méthode **[Close](connection-close-method-dao.md)** le supprime automatiquement de la collection **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="e5fbc-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>


> [!NOTE]
> <span data-ttu-id="e5fbc-147">Si l’argument *source* fait référence à une instruction SQL composée d’une chaîne concaténée avec une valeur non entière, et que les paramètres système spécifient un caractère décimal d’un format différent de celui des États-Unis, tel qu’une virgule (par exemple, strSQL = "PRICE &gt; " &amp; lngPrice, et lngPrice = 125,50), une erreur se produit lorsque vous essayez d’ouvrir l’objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="e5fbc-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="e5fbc-148">Cela s'explique par le fait que lors de la concaténation, le nombre est converti en chaîne à l'aide du caractère décimal par défaut du système et le langage SQL n'accepte que les caractères décimaux de la notation américaine.</span><span class="sxs-lookup"><span data-stu-id="e5fbc-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>

<span data-ttu-id="e5fbc-149">**Lien fourni par** la communauté [UtterAccess](https://www.utteraccess.com).</span><span class="sxs-lookup"><span data-stu-id="e5fbc-149">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="e5fbc-150">UtterAccess est un forum d’aide et wiki de Microsoft Access réputé.</span><span class="sxs-lookup"><span data-stu-id="e5fbc-150">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="e5fbc-151">Transfert de données entre Access et Excel</span><span class="sxs-lookup"><span data-stu-id="e5fbc-151">Transfer data from Access to Excel</span></span>](https://www.utteraccess.com/forum/transfer-data-access-ex-t1672619.html)

## <a name="example"></a><span data-ttu-id="e5fbc-152">Exemple</span><span class="sxs-lookup"><span data-stu-id="e5fbc-152">Example</span></span>

<span data-ttu-id="e5fbc-153">L’exemple suivant montre comment ouvrir un objet Recordset basé sur une requête avec paramètres.</span><span class="sxs-lookup"><span data-stu-id="e5fbc-153">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

<span data-ttu-id="e5fbc-154">**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="e5fbc-154">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qfd = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```

<br/>

<span data-ttu-id="e5fbc-155">L’exemple suivant montre comment ouvrir un Recordset basé sur un tableau ou une requête.</span><span class="sxs-lookup"><span data-stu-id="e5fbc-155">The following example shows how to open a Recordset based on a table or a query.</span></span>

```vb 
    Dim dbs As DAO.Database
    Dim rsTable As DAO.Recordset
    Dim rsQuery As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Open a table-type Recordset
    Set rsTable = dbs.OpenRecordset("Table1", dbOpenTable)
    
    'Open a dynaset-type Recordset using a saved query
    Set rsQuery = dbs.OpenRecordset("qryMyQuery", dbOpenDynaset)
```

<br/>

<span data-ttu-id="e5fbc-156">L’exemple suivant montre comment ouvrir un Recordset basé sur une instruction SQL (Structured Query Language).</span><span class="sxs-lookup"><span data-stu-id="e5fbc-156">The following example shows how to open a Recordset based on a Structured Query Language (SQL) statement.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rsSQL As DAO.Recordset
    Dim strSQL As String
    
    Set dbs = CurrentDb
    
    'Open a snapshot-type Recordset based on an SQL statement
    strSQL = "SELECT * FROM Table1 WHERE Field2 = 33"
    Set rsSQL = dbs.OpenRecordset(strSQL, dbOpenSnapshot)
```

<br/>

<span data-ttu-id="e5fbc-157">L’exemple suivant montre comment utiliser la propriété Filter pour déterminer les enregistrements à inclure dans un Recordset ouvert par la suite.</span><span class="sxs-lookup"><span data-stu-id="e5fbc-157">The following sample shows how to use the Filter property to determine the records to be included in a subsequently opened Recordset.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rst = dbs.OpenRecordset(_ 
        "SELECT * FROM Customers WHERE LastVisitDate BETWEEN Date()-60 " & _
        "AND Date()-30 ORDER BY LastVisitDate DESC")
    
    'Begin row processing
    Do While Not rst.EOF
        
        'Retrieve the name of the first city in the selected rows
        strCity = rst!City
    
        'Now filter the Recordset to return only the customers from that city
        rst.Filter = "City = '" & strCity & "'"
        Set rstFiltered = rst.OpenRecordset
    
        'Process the rows
        Do While Not rstFiltered.EOF
            rstFiltered.Edit
            rstFiltered!ToBeVisited = True
            rstFiltered.Update
            rstFiltered.MoveNext
        Loop
    
        'We've done what was needed. Now exit
        Exit Do
        rst.MoveNext
       
    Loop
    
    'Cleanup
    rstFiltered.Close
    rst.Close
    
    Set rstFiltered = Nothing
    Set rst = Nothing
```



