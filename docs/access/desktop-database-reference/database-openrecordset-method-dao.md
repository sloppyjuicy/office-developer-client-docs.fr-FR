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
ms.openlocfilehash: 0dd33e24914d7e45d8678379df5825a42ef0b6fd
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605834"
---
# <a name="databaseopenrecordset-method-dao"></a><span data-ttu-id="deb05-102">Méthode Database.OpenRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="deb05-102">Database.OpenRecordset Method (DAO)</span></span>

<span data-ttu-id="deb05-103">**S’applique à :** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="deb05-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="deb05-104">Crée un objet **[Recordset](recordset-object-dao.md)** et l'ajoute à la collection **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="deb05-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="deb05-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="deb05-105">Syntax</span></span>

<span data-ttu-id="deb05-106">*expression* . OpenRecordset (_**nom**_, _**Type**_, _**Options**_, _**VerrouillerModification**_)</span><span class="sxs-lookup"><span data-stu-id="deb05-106">*expression* .OpenRecordset(_**Name**_, _**Type**_, _**Options**_, _**LockEdit**_)</span></span>

<span data-ttu-id="deb05-107">*expression* Variable qui représente un objet de **base de données** .</span><span class="sxs-lookup"><span data-stu-id="deb05-107">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="deb05-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="deb05-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="deb05-109">Name</span><span class="sxs-lookup"><span data-stu-id="deb05-109">Name</span></span></p></th>
<th><p><span data-ttu-id="deb05-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="deb05-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="deb05-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="deb05-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="deb05-112">Description</span><span class="sxs-lookup"><span data-stu-id="deb05-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="deb05-113">Name</span><span class="sxs-lookup"><span data-stu-id="deb05-113">Name</span></span></p></td>
<td><p><span data-ttu-id="deb05-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="deb05-114">Required</span></span></p></td>
<td><p><span data-ttu-id="deb05-115"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="deb05-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="deb05-p101">Source des enregistrements du nouveau <strong>Recordset</strong>. La source peut être un nom de table, un nom de requête ou une instruction SQL qui renvoie des enregistrements. Pour les objets <strong>Recordset</strong> de type table dans les bases de données du moteur de base de données Microsoft Access, la source peut uniquement être un nom de table.  </span><span class="sxs-lookup"><span data-stu-id="deb05-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="deb05-119">Type</span><span class="sxs-lookup"><span data-stu-id="deb05-119">Type</span></span></p></td>
<td><p><span data-ttu-id="deb05-120">Facultatif</span><span class="sxs-lookup"><span data-stu-id="deb05-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="deb05-121"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="deb05-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="deb05-122">Constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> qui indique le type de <strong>Recordset</strong> à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="deb05-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p>

> [!NOTE]
> <span data-ttu-id="deb05-p102">Si vous ouvrez un **Recordset** dans un espace de travail Microsoft Access et que vous n’indiquez aucun type, **OpenRecordset** crée un **Recordset** de type table, si possible. Si vous spécifiez une table liée ou une requête, **OpenRecordset** crée un **Recordset** de type feuille de réponse dynamique.</span><span class="sxs-lookup"><span data-stu-id="deb05-p102">If you open a **Recordset** in a Microsoft Access workspace and you don't specify a type, **OpenRecordset** creates a table-type **Recordset**, if possible. If you specify a linked table or query, **OpenRecordset** creates a dynaset-type **Recordset**.</span></span>


</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="deb05-125">Options</span><span class="sxs-lookup"><span data-stu-id="deb05-125">Options</span></span></p></td>
<td><p><span data-ttu-id="deb05-126">Facultatif</span><span class="sxs-lookup"><span data-stu-id="deb05-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="deb05-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="deb05-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="deb05-128">Combinaison de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> qui indiquent les caractéristiques du nouveau <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="deb05-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <span data-ttu-id="deb05-p103">Les constantes **dbConsistent** et **dbInconsistent** s’excluent mutuellement, et l’utilisation de ces deux constantes peut entraîner une erreur. L’indication d’un argument LockEdit lorsqueOptions utilise la constante **dbReadOnly** génère également une erreur.</span><span class="sxs-lookup"><span data-stu-id="deb05-p103">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive, and using both causes an error. Supplying a LockEdit argument when Options uses the **dbReadOnly** constant also causes an error.</span></span>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="deb05-131">VerrouillerModification</span><span class="sxs-lookup"><span data-stu-id="deb05-131">LockEdit</span></span></p></td>
<td><p><span data-ttu-id="deb05-132">Facultatif</span><span class="sxs-lookup"><span data-stu-id="deb05-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="deb05-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="deb05-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="deb05-134">Constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> qui détermine le verrouillage du <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="deb05-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <span data-ttu-id="deb05-p104">Vous pouvez utiliser **dbReadOnly** dans l’argument Options ou l’argument LockedEdit, mais pas dans les deux. Si vous l’utilisez pour les deux arguments, une erreur d’exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="deb05-p104">You can use **dbReadOnly** in either the Options argument or the LockedEdit argument, but not both. If you use it for both arguments, a run-time error occurs.</span></span>


</td>
</tr>
</tbody>
</table>


<span data-ttu-id="deb05-137"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="deb05-137"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="deb05-138">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="deb05-138">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="deb05-139">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="deb05-139">Return value</span></span>
>>>>>>> <span data-ttu-id="deb05-140">master</span><span class="sxs-lookup"><span data-stu-id="deb05-140">master</span></span>

<span data-ttu-id="deb05-141">Recordset</span><span class="sxs-lookup"><span data-stu-id="deb05-141">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="deb05-142">Remarques</span><span class="sxs-lookup"><span data-stu-id="deb05-142">Remarks</span></span>

<span data-ttu-id="deb05-p105">En règle générale, si l'utilisateur obtient cette erreur pendant la mise à jour d'un enregistrement, votre code doit actualiser le contenu des champs et extraire les valeurs nouvellement modifiées. Si l'erreur se produit lors de la suppression d'un enregistrement, votre code doit présenter les nouvelles données de l'enregistrement à l'utilisateur et afficher un message indiquant que les données ont été récemment modifiées. À ce stade, votre code peut demander à l'utilisateur de confirmer sa volonté de supprimer l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="deb05-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="deb05-146">Par ailleurs, il est recommandé d'utiliser la constante **dbSeeChanges** si vous ouvrez un objet **Recordset** dans un espace de travail ODBC connecté au moteur de base de données Microsoft Access pour une table Microsoft SQL Server 6.0 (ou version ultérieure) qui comporte une colonne IDENTITY. À défaut, une erreur risque de se produire.</span><span class="sxs-lookup"><span data-stu-id="deb05-146">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="deb05-p106">L'ouverture de plusieurs objets **Recordset** dans une source de données ODBC peut entraîner un échec car la connexion est occupée par un appel d'objet **OpenRecordset** préalable. Pour contourner ce problème, vous pouvez renseigner totalement l'objet **Recordset** à l'aide de la méthode **MoveLast** dès que l'objet **Recordset** est ouvert.</span><span class="sxs-lookup"><span data-stu-id="deb05-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="deb05-149">Le fait de fermer un objet **Recordset** par le biais de la méthode **[Close](connection-close-method-dao.md)** entraîne sa suppression automatique au niveau de la collection **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="deb05-149">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>


> [!NOTE]
> <span data-ttu-id="deb05-150">Si *la source* fait référence à une instruction SQL composée d’une chaîne concaténée avec une valeur non entière, et les paramètres système spécifient un caractère décimal américain comme une virgule (par exemple, strSQL = « prix &gt; » &amp; lngPrice et lngPrice = 125,50), une erreur se produit lorsque vous essayez d’ouvrir le **jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="deb05-150">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="deb05-151">Cela est dû au fait que pendant la concaténation, le nombre est converti en chaîne en utilisant le caractère décimal par défaut de votre système, et SQL n'accepte que les caractères décimaux usités aux États-Unis.</span><span class="sxs-lookup"><span data-stu-id="deb05-151">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>

<span data-ttu-id="deb05-152">**Lien fourni par** la Communauté [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="deb05-152">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="deb05-153">UtterAccess est le premier forum d'aide et wiki de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="deb05-153">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="deb05-154">Transférer des données d'Access vers Excel</span><span class="sxs-lookup"><span data-stu-id="deb05-154">Transfer data from Access to Excel</span></span>](https://www.utteraccess.com/forum/transfer-data-access-ex-t1672619.html)

## <a name="example"></a><span data-ttu-id="deb05-155">Exemple</span><span class="sxs-lookup"><span data-stu-id="deb05-155">Example</span></span>

<span data-ttu-id="deb05-156">L'exemple suivant montre comment ouvrir un Recordset basé sur une requête avec paramètres.</span><span class="sxs-lookup"><span data-stu-id="deb05-156">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

<span data-ttu-id="deb05-157">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="deb05-157">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

<span data-ttu-id="deb05-158">L'exemple suivant montre comment ouvrir un Recordset basé sur une table ou une requête.</span><span class="sxs-lookup"><span data-stu-id="deb05-158">The following example shows how to open a Recordset based on a table or a query.</span></span>

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

<span data-ttu-id="deb05-159">L'exemple suivant montre comment ouvrir un Recordset basé sur une instruction SQL (Structured Query Language).</span><span class="sxs-lookup"><span data-stu-id="deb05-159">The following example shows how to open a Recordset based on a Structured Query Language (SQL) statement.</span></span>

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

<span data-ttu-id="deb05-160">L'exemple suivant montre comment utiliser la propriété Filter pour déterminer les enregistrements à inclure dans un Recordset ouvert par la suite.</span><span class="sxs-lookup"><span data-stu-id="deb05-160">The following sample shows how to use the Filter property to determine the records to be included in a subsequently opened Recordset.</span></span>

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



