---
title: Méthode Database.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: a243bc79-cac4-fe12-768d-d3d017954e78
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820966(v=office.15)
ms:contentKeyID: 48546753
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052939
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 73bb48db5b47ff1824e962ac44324a17ae0636ad
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707681"
---
# <a name="databaseopenrecordset-method-dao"></a><span data-ttu-id="2f08b-102">Méthode Database.OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="2f08b-102">Database.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="2f08b-103">**S’applique à :** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f08b-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="2f08b-104">Crée un objet **[Recordset](recordset-object-dao.md)** et l'ajoute à la collection **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="2f08b-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f08b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f08b-105">Syntax</span></span>

<span data-ttu-id="2f08b-106">*expression* . OpenRecordset (_**nom**_, _**Type**_, _**Options**_, _**VerrouillerModification**_)</span><span class="sxs-lookup"><span data-stu-id="2f08b-106">*expression* .OpenRecordset(_**Name**_, _**Type**_, _**Options**_, _**LockEdit**_)</span></span>

<span data-ttu-id="2f08b-107">*expression* Variable qui représente un objet de **base de données** .</span><span class="sxs-lookup"><span data-stu-id="2f08b-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f08b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f08b-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f08b-109">Nom</span><span class="sxs-lookup"><span data-stu-id="2f08b-109">Name</span></span></p></th>
<th><p><span data-ttu-id="2f08b-110">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="2f08b-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="2f08b-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="2f08b-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="2f08b-112">Description</span><span class="sxs-lookup"><span data-stu-id="2f08b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f08b-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="2f08b-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="2f08b-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2f08b-114">Required</span></span></p></td>
<td><p><span data-ttu-id="2f08b-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="2f08b-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="2f08b-p101">Source des enregistrements du nouveau <strong>Recordset</strong>. La source peut être un nom de table, un nom de requête ou une instruction SQL qui renvoie des enregistrements. Pour les objets <strong>Recordset</strong> de type table dans les bases de données du moteur de base de données Microsoft Access, la source peut uniquement être un nom de table.  </span><span class="sxs-lookup"><span data-stu-id="2f08b-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f08b-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="2f08b-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="2f08b-120">Facultatif</span><span class="sxs-lookup"><span data-stu-id="2f08b-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="2f08b-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="2f08b-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2f08b-122">Constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> qui indique le type de <strong>Recordset</strong> à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="2f08b-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="2f08b-123"><strong>Remarque</strong>: Si vous ouvrez un <strong>objet Recordset</strong> dans un espace de travail Microsoft Access et que vous ne spécifiez pas un type, <strong>OpenRecordset</strong> crée un <strong>objet Recordset</strong>de type table, si possible.</span><span class="sxs-lookup"><span data-stu-id="2f08b-123"><strong>NOTE</strong>: If you open a <strong>Recordset</strong> in a Microsoft Access workspace and you don't specify a type, <strong>OpenRecordset</strong> creates a table-type <strong>Recordset</strong>, if possible.</span></span> <span data-ttu-id="2f08b-124">Si vous spécifiez une table liée ou une requête, <strong>OpenRecordset</strong> crée un <strong>jeu d’enregistrements</strong>de type feuille de réponse dynamique.</span><span class="sxs-lookup"><span data-stu-id="2f08b-124">If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f08b-125"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="2f08b-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="2f08b-126">Facultatif</span><span class="sxs-lookup"><span data-stu-id="2f08b-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="2f08b-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="2f08b-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2f08b-128">Combinaison de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> qui indiquent les caractéristiques du nouveau <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="2f08b-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="2f08b-129"><strong>Remarque</strong>: l’une des constantes <strong>dbConsistent</strong> et <strong>dbInconsistent</strong> s’excluent mutuellement, et les deux entraîne une erreur.</span><span class="sxs-lookup"><span data-stu-id="2f08b-129"><strong>NOTE</strong>: The constants <strong>dbConsistent</strong> and <strong>dbInconsistent</strong> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="2f08b-130">Fournir un argument VerrouillerModification lorsque Options utilise la constante <strong>peut entraîner</strong> génère également une erreur.</span><span class="sxs-lookup"><span data-stu-id="2f08b-130">Supplying a LockEdit argument when Options uses the <strong>dbReadOnly</strong> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f08b-131"><em>VerrouillerModification</em></span><span class="sxs-lookup"><span data-stu-id="2f08b-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="2f08b-132">Facultatif</span><span class="sxs-lookup"><span data-stu-id="2f08b-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="2f08b-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="2f08b-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2f08b-134">Constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> qui détermine le verrouillage du <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="2f08b-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="2f08b-135"><strong>Remarque</strong>: vous pouvez utiliser <strong>peut entraîner</strong> dans l’argument Options ou l’argument LockedEdit, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="2f08b-135"><strong>NOTE</strong>: You can use <strong>dbReadOnly</strong> in either the Options argument or the LockedEdit argument, but not both.</span></span> <span data-ttu-id="2f08b-136">Si vous l’utilisez pour les deux arguments, une erreur d’exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="2f08b-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="2f08b-137">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2f08b-137">Return value</span></span>

<span data-ttu-id="2f08b-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="2f08b-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="2f08b-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="2f08b-139">Remarks</span></span>

<span data-ttu-id="2f08b-p105">En règle générale, si l'utilisateur obtient cette erreur pendant la mise à jour d'un enregistrement, votre code doit actualiser le contenu des champs et extraire les valeurs nouvellement modifiées. Si l'erreur se produit lors de la suppression d'un enregistrement, votre code doit présenter les nouvelles données de l'enregistrement à l'utilisateur et afficher un message indiquant que les données ont été récemment modifiées. À ce stade, votre code peut demander à l'utilisateur de confirmer sa volonté de supprimer l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2f08b-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="2f08b-143">Par ailleurs, il est recommandé d'utiliser la constante **dbSeeChanges** si vous ouvrez un objet **Recordset** dans un espace de travail ODBC connecté au moteur de base de données Microsoft Access pour une table Microsoft SQL Server 6.0 (ou version ultérieure) qui comporte une colonne IDENTITY. À défaut, une erreur risque de se produire.</span><span class="sxs-lookup"><span data-stu-id="2f08b-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="2f08b-p106">L'ouverture de plusieurs objets **Recordset** dans une source de données ODBC peut entraîner un échec car la connexion est occupée par un appel d'objet **OpenRecordset** préalable. Pour contourner ce problème, vous pouvez renseigner totalement l'objet **Recordset** à l'aide de la méthode **MoveLast** dès que l'objet **Recordset** est ouvert.</span><span class="sxs-lookup"><span data-stu-id="2f08b-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="2f08b-146">Le fait de fermer un objet **Recordset** par le biais de la méthode **[Close](connection-close-method-dao.md)** entraîne sa suppression automatique au niveau de la collection **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="2f08b-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>


> [!NOTE]
> <span data-ttu-id="2f08b-147">Si *la source* fait référence à une instruction SQL composée d’une chaîne concaténée avec une valeur non entière, et les paramètres système spécifient un caractère décimal américain comme une virgule (par exemple, strSQL = « prix &gt; » &amp; lngPrice et lngPrice = 125,50), une erreur se produit lorsque vous essayez d’ouvrir le **jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="2f08b-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="2f08b-148">Cela est dû au fait que pendant la concaténation, le nombre est converti en chaîne en utilisant le caractère décimal par défaut de votre système, et SQL n'accepte que les caractères décimaux usités aux États-Unis.</span><span class="sxs-lookup"><span data-stu-id="2f08b-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>

<span data-ttu-id="2f08b-149">**Lien fourni par** la Communauté [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="2f08b-149">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="2f08b-150">UtterAccess est un forum d’aide et wiki de Microsoft Access réputé.</span><span class="sxs-lookup"><span data-stu-id="2f08b-150">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="2f08b-151">Transférer des données d'Access vers Excel</span><span class="sxs-lookup"><span data-stu-id="2f08b-151">Transfer data from Access to Excel</span></span>](https://www.utteraccess.com/forum/transfer-data-access-ex-t1672619.html)

## <a name="example"></a><span data-ttu-id="2f08b-152">Exemple</span><span class="sxs-lookup"><span data-stu-id="2f08b-152">Example</span></span>

<span data-ttu-id="2f08b-153">L'exemple suivant montre comment ouvrir un Recordset basé sur une requête avec paramètres.</span><span class="sxs-lookup"><span data-stu-id="2f08b-153">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

<span data-ttu-id="2f08b-154">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="2f08b-154">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

<span data-ttu-id="2f08b-155">L'exemple suivant montre comment ouvrir un Recordset basé sur une table ou une requête.</span><span class="sxs-lookup"><span data-stu-id="2f08b-155">The following example shows how to open a Recordset based on a table or a query.</span></span>

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

<span data-ttu-id="2f08b-156">L'exemple suivant montre comment ouvrir un Recordset basé sur une instruction SQL (Structured Query Language).</span><span class="sxs-lookup"><span data-stu-id="2f08b-156">The following example shows how to open a Recordset based on a Structured Query Language (SQL) statement.</span></span>

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

<span data-ttu-id="2f08b-157">L'exemple suivant montre comment utiliser la propriété Filter pour déterminer les enregistrements à inclure dans un Recordset ouvert par la suite.</span><span class="sxs-lookup"><span data-stu-id="2f08b-157">The following sample shows how to use the Filter property to determine the records to be included in a subsequently opened Recordset.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rest = dbs.OpenRecordset(_ 
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



