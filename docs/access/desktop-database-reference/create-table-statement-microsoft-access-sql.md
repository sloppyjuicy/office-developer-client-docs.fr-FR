---
title: Instruction CREATE TABLE (Microsoft Access SQL)
TOCTitle: CREATE TABLE statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 09/03/2019
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: dfcbbd55f2d20589849f63f260d40b507c8639f1
ms.sourcegitcommit: b27eedbc4538f78ee15134bf19abbc319605c3bc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2019
ms.locfileid: "36706172"
---
# <a name="create-table-statement-microsoft-access-sql"></a><span data-ttu-id="e0c20-102">Instruction CREATE TABLE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="e0c20-102">CREATE TABLE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="e0c20-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e0c20-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e0c20-104">Crée une table.</span><span class="sxs-lookup"><span data-stu-id="e0c20-104">Creates a new table.</span></span>

> [!NOTE]
> <span data-ttu-id="e0c20-105">Le moteur de base de données Access ne prend pas en charge l’utilisation de l’instruction CREATE TABLE ou de toute instruction DDL avec des bases de données d’un moteur de base de données autre que Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="e0c20-105">The Microsoft Access database engine does not support the use of CREATE TABLE, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="e0c20-106">Utilisez plutôt les méthodes **Create** de DAO.</span><span class="sxs-lookup"><span data-stu-id="e0c20-106">Use the DAO **Create** methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0c20-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0c20-107">Syntax</span></span>

<span data-ttu-id="e0c20-108">CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])</span><span class="sxs-lookup"><span data-stu-id="e0c20-108">CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])</span></span>

<span data-ttu-id="e0c20-109">L’instruction CREATE TABLE comprend les parties suivantes :</span><span class="sxs-lookup"><span data-stu-id="e0c20-109">The CREATE TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0c20-110">Quitter</span><span class="sxs-lookup"><span data-stu-id="e0c20-110">Part</span></span></p></th>
<th><p><span data-ttu-id="e0c20-111">Description</span><span class="sxs-lookup"><span data-stu-id="e0c20-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0c20-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="e0c20-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="e0c20-113">Nom de la table à créer.</span><span class="sxs-lookup"><span data-stu-id="e0c20-113">The name of the table to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0c20-114"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="e0c20-114"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="e0c20-p102">Nom du ou des champs à créer dans la nouvelle table. Vous devez créer au moins un champ.</span><span class="sxs-lookup"><span data-stu-id="e0c20-p102">The name of field or fields to be created in the new table. You must create at least one field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0c20-117"><em>type</em></span><span class="sxs-lookup"><span data-stu-id="e0c20-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="e0c20-118">Type de données de <em>field</em> dans la nouvelle table.</span><span class="sxs-lookup"><span data-stu-id="e0c20-118">The data type of <em>field</em> in the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0c20-119"><em>size</em></span><span class="sxs-lookup"><span data-stu-id="e0c20-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="e0c20-120">Taille du champ en nombre de caractères (champs texte et binaires seulement).</span><span class="sxs-lookup"><span data-stu-id="e0c20-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0c20-121"><em>index1</em>, <em>index2</em></span><span class="sxs-lookup"><span data-stu-id="e0c20-121"><em>index1</em>, <em>index2</em></span></span></p></td>
<td><p><span data-ttu-id="e0c20-122">Clause CONSTRAINT définissant un index de champ unique.</span><span class="sxs-lookup"><span data-stu-id="e0c20-122">A CONSTRAINT clause defining a single-field index.</span></span> <span data-ttu-id="e0c20-123">Pour plus d'informations sur la création de cet index, voir <a href="constraint-clause-microsoft-access-sql.md">Clause CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="e0c20-123">For more information about how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0c20-124"><em>multifieldindex</em></span><span class="sxs-lookup"><span data-stu-id="e0c20-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="e0c20-125">Clause CONSTRAINT définissant un index multi-champ.</span><span class="sxs-lookup"><span data-stu-id="e0c20-125">A CONSTRAINT clause defining a multiple-field index.</span></span> <span data-ttu-id="e0c20-126">Pour plus d'informations sur la création de cet index, voir <a href="constraint-clause-microsoft-access-sql.md">Clause CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="e0c20-126">For more information about how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e0c20-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="e0c20-127">Remarks</span></span>

<span data-ttu-id="e0c20-128">L’instruction CREATE TABLE permet de définir une nouvelle table, ses champs et ses contraintes de champ.</span><span class="sxs-lookup"><span data-stu-id="e0c20-128">Use the CREATE TABLE statement to define a new table and its fields and field constraints.</span></span> <span data-ttu-id="e0c20-129">Si NOT NULL est spécifié pour un champ, les nouveaux enregistrements doivent contenir des données valides dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="e0c20-129">If NOT NULL is specified for a field, new records are required to have valid data in that field.</span></span>

<span data-ttu-id="e0c20-p106">Une clause CONSTRAINT établit diverses restrictions sur un champ et peut être utilisée pour établir la clé primaire. Vous pouvez également utiliser l'instruction [CREATE INDEX](create-index-statement-microsoft-access-sql.md) pour créer une clé primaire ou des index supplémentaires sur les tables existantes.</span><span class="sxs-lookup"><span data-stu-id="e0c20-p106">A CONSTRAINT clause establishes various restrictions on a field, and can be used to establish the primary key. You can also use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to create a primary key or additional indexes on existing tables.</span></span>

<span data-ttu-id="e0c20-p107">Vous pouvez utiliser l’instruction NON NULL sur un champ unique ou à l’intérieur d’une clause CONSTRAINT nommée qui s’applique à une instruction CONSTRAINT nommée portant sur un ou plusieurs champs. Toutefois, vous ne pouvez appliquer la restriction NON NULL qu’une seule fois à un champ. Une tentative d’appliquer cette restriction plusieurs fois génère une erreur d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e0c20-p107">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT. However, you can apply the NOT NULL restriction only once to a field. Attempting to apply this restriction more than once results in a run-time error.</span></span>

<span data-ttu-id="e0c20-135">Lors de la création d'une table temporaire, celle-ci n'est visible que dans la session dans laquelle elle a été créée.</span><span class="sxs-lookup"><span data-stu-id="e0c20-135">When a TEMPORARY table is created, it is visible only within the session in which it was created.</span></span> <span data-ttu-id="e0c20-136">Elle est supprimée automatiquement à la fin de la session.</span><span class="sxs-lookup"><span data-stu-id="e0c20-136">It is automatically deleted when the session is terminated.</span></span> <span data-ttu-id="e0c20-137">Les tables temporaires sont accessible par plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e0c20-137">Temporary tables can be accessed by more than one user.</span></span>

<span data-ttu-id="e0c20-138">L’attribut WITH COMPRESSION peut être utilisé uniquement avec les types de données CARACTÈRE et MÉMO (également appelé TEXTE) et leurs synonymes.</span><span class="sxs-lookup"><span data-stu-id="e0c20-138">The WITH COMPRESSION attribute can be used only with the CHARACTER and MEMO (also known as TEXT) data types and their synonyms.</span></span>

<span data-ttu-id="e0c20-139">L’attribut WITH COMPRESSION a été ajouté pour les colonnes de type CARACTÈRE en raison de la modification du format de représentation de caractère Unicode.</span><span class="sxs-lookup"><span data-stu-id="e0c20-139">The WITH COMPRESSION attribute was added for CHARACTER columns because of the change to the Unicode character representation format.</span></span> <span data-ttu-id="e0c20-140">Les caractères Unicode nécessitent uniformément deux octets par caractère.</span><span class="sxs-lookup"><span data-stu-id="e0c20-140">Unicode characters uniformly require two bytes for each character.</span></span> <span data-ttu-id="e0c20-141">Pour les bases de données Microsoft Jet qui contiennent principalement des données caractères, cela pourrait signifier que le fichier de base de données doublerait de taille lors de la conversion au format du moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="e0c20-141">For existing Microsoft Jet databases that contain predominately character data, this could mean that the database file would nearly double in size when converted to the Microsoft Access database engine format.</span></span> <span data-ttu-id="e0c20-142">Cependant, la représentation Unicode de nombreux jeux de caractères, anciennement appelés jeux de caractères codés sur un octet (SBCS), peut facilement être compressée à un seul octet.</span><span class="sxs-lookup"><span data-stu-id="e0c20-142">However, Unicode representation of many character sets, those formerly denoted as Single-Byte Character Sets (SBCS), can easily be compressed to a single byte.</span></span> <span data-ttu-id="e0c20-143">Si vous définissez une colonne de type CARACTÈRE avec cet attribut, les données sont automatiquement compressées pour le stockage, et décompressées lors de leur extraction de la colonne.</span><span class="sxs-lookup"><span data-stu-id="e0c20-143">If you define a CHARACTER column with this attribute, data will automatically be compressed as it is stored and uncompressed when retrieved from the column.</span></span>

<span data-ttu-id="e0c20-p110">Des colonnes de type MÉMO peuvent également être définies pour stocker des données dans un format compressé. Il existe cependant une limitation. Seules les instances de colonnes de type MÉMO qui, une fois compressées, ne dépassent pas 4 096 octets, sont compressées. Les autres instances des colonnes de type MÉMO ne sont pas compressées. Cela signifie que, dans un tableau donné, pour une colonne de type MÉMO donnée, certaines données peuvent être compressées et d’autres pas.</span><span class="sxs-lookup"><span data-stu-id="e0c20-p110">MEMO columns can also be defined to store data in a compressed format. However, there is a limitation. Only instances of MEMO columns that, when compressed, will fit within 4096 bytes or less, will be compressed. All other instances of MEMO columns will remain uncompressed. This means that within a given table, for a given MEMO column, some data may be compressed and some data may not be compressed.</span></span>

## <a name="example"></a><span data-ttu-id="e0c20-149">Exemple</span><span class="sxs-lookup"><span data-stu-id="e0c20-149">Example</span></span>

<span data-ttu-id="e0c20-150">Cet exemple crée une nouvelle table appelée ThisTable qui comporte deux champs de texte.</span><span class="sxs-lookup"><span data-stu-id="e0c20-150">This example creates a new table called ThisTable with two text fields.</span></span>

```vb
    Sub CreateTableX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with two text fields. 
        dbs.Execute "CREATE TABLE ThisTable " _ 
            & "(FirstName CHAR, LastName CHAR);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="e0c20-151">Cet exemple crée une nouvelle table appelée MyTable avec deux champs de texte, un champ Date/Heure et un index unique composé de ces trois champs.</span><span class="sxs-lookup"><span data-stu-id="e0c20-151">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

```vb
    Sub CreateTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
     
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a unique 
        ' index made up of all three fields. 
        dbs.Execute "CREATE TABLE MyTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "DateOfBirth DATETIME, " _ 
            & "CONSTRAINT MyTableConstraint UNIQUE " _ 
            & "(FirstName, LastName, DateOfBirth));" 
     
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="e0c20-p111">Cet exemple crée une nouvelle table avec deux champs de texte et un champ **Entier**. Le champ SSN correspond à la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="e0c20-p111">This example creates a new table with two text fields and an **Integer** field. The SSN field is the primary key.</span></span>

```vb
    Sub CreateTableX3() 
     
         Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a primary 
        ' key. 
        dbs.Execute "CREATE TABLE NewTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "SSN INTEGER CONSTRAINT MyFieldConstraint " _ 
            & "PRIMARY KEY);" 
     
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="e0c20-154">Cet exemple crée une table appelée `~~Kitsch'n Sync` qui illustre tous les différents types de champ et d’index.</span><span class="sxs-lookup"><span data-stu-id="e0c20-154">This example creates a new table called `~~Kitsch'n Sync` that demonstrates all the different field and index types.</span></span> <span data-ttu-id="e0c20-155">Le champ AutoNumber correspond à la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="e0c20-155">The SSN field is the primary key.</span></span>

```vb
    Sub CreateTableX6()
        On Error Resume Next
        Application.CurrentDb.Execute "Drop Table [~~Kitsch'n Sync];"
        On Error GoTo 0
        
        'This example uses ADODB instead of the DAO shown in the previous
        'ones because DAO does not support the DECIMAL and GUID data types
        Dim con As ADODB.Connection
        Set con = CurrentProject.Connection
        con.Execute "" _
            & "CREATE TABLE [~~Kitsch'n Sync](" _
                & " [Auto]                  COUNTER" _
                & ",[Byte]                  BYTE" _
                & ",[Integer]               SMALLINT" _
                & ",[Long]                  INTEGER" _
                & ",[Single]                REAL" _
                & ",[Double]                FLOAT" _
                & ",[Decimal]               DECIMAL(18,5)" _
                & ",[Currency]              MONEY" _
                & ",[ShortText]             CHAR" _
                & ",[LongText]              MEMO" _
                & ",[PlaceHolder1]          MEMO" _
                & ",[DateTime]              DATETIME" _
                & ",[YesNo]                 BIT" _
                & ",[OleObject]             IMAGE" _
                & ",[ReplicationID]         UNIQUEIDENTIFIER" _
                & ",[Required]              INTEGER NOT NULL" _
                & ",[Unicode Compression]   MEMO WITH COMP" _
                & ",[Indexed]               INTEGER" _
                & ",CONSTRAINT [PrimaryKey] PRIMARY KEY ([Auto])" _
                & ",CONSTRAINT [Unique Index] UNIQUE ([Byte],[Integer],[Long])" _
            & ");"
        con.Execute "CREATE INDEX [Single-Field Index] ON [~~Kitsch'n Sync]([Indexed]);"
        con.Execute "CREATE INDEX [Multi-Field Index] ON [~~Kitsch'n Sync]([Auto],[Required]);"
        con.Execute "CREATE INDEX [IgnoreNulls Index] ON [~~Kitsch'n Sync]([Single],[Double]) WITH IGNORE NULL;"
        con.Execute "CREATE UNIQUE INDEX [Combined Index] ON [~~Kitsch'n Sync]([ShortText],[LongText]) WITH IGNORE NULL;"
        Set con = Nothing
    
        'Add a Hyperlink Field
        Dim AllDefs As DAO.TableDefs, TblDef As DAO.TableDef, Fld As DAO.Field
        Set AllDefs = Application.CurrentDb.TableDefs
        Set TblDef = AllDefs("~~Kitsch'n Sync")
        Set Fld = TblDef.CreateField("Hyperlink", dbMemo)
        Fld.Attributes = dbHyperlinkField + dbVariableField
        Fld.OrdinalPosition = 10
        TblDef.Fields.Append Fld
        
        DoCmd.RunSQL "ALTER TABLE [~~Kitsch'n Sync] DROP COLUMN [PlaceHolder1];"
    End Sub
```
