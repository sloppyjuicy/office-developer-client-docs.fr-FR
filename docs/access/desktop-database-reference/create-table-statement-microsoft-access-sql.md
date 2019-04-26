---
title: Instruction CREATE TABLE (Microsoft Access SQL)
TOCTitle: CREATE TABLE statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 296e1405245d6204d136888e78b6a3846b468a1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295358"
---
# <a name="create-table-statement-microsoft-access-sql"></a><span data-ttu-id="9a2b0-102">Instruction CREATE TABLE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="9a2b0-102">CREATE TABLE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="9a2b0-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a2b0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9a2b0-104">Crée une table.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-104">Creates a new table.</span></span>

> [!NOTE]
> <span data-ttu-id="9a2b0-105">Le moteur de base de données Access ne prend pas en charge l’utilisation de l’instruction CREATE TABLE ou de toute instruction DDL avec des bases de données d’un moteur de base de données autre que Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-105">The Microsoft Access database engine does not support the use of CREATE TABLE, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="9a2b0-106">Utilisez plutôt les méthodes **Create** de DAO.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-106">Use the DAO Create methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a2b0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a2b0-107">Syntax</span></span>

<span data-ttu-id="9a2b0-108">CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])</span><span class="sxs-lookup"><span data-stu-id="9a2b0-108">CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])</span></span>

<span data-ttu-id="9a2b0-109">L’instruction CREATE TABLE comprend les parties suivantes :</span><span class="sxs-lookup"><span data-stu-id="9a2b0-109">The CREATE TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a2b0-110">Quitter</span><span class="sxs-lookup"><span data-stu-id="9a2b0-110">Part</span></span></p></th>
<th><p><span data-ttu-id="9a2b0-111">Description</span><span class="sxs-lookup"><span data-stu-id="9a2b0-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a2b0-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="9a2b0-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="9a2b0-113">Nom de la table à créer.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-113">The name of the table to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a2b0-114"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="9a2b0-114"><em>field1</em>  ,  <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="9a2b0-p102">Nom du ou des champs à créer dans la nouvelle table. Vous devez créer au moins un champ.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-p102">The name of field or fields to be created in the new table. You must create at least one field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a2b0-117"><em>type</em></span><span class="sxs-lookup"><span data-stu-id="9a2b0-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="9a2b0-118">Type de données de <em>field</em> dans la nouvelle table.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-118">The data type of <em>field</em> in the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a2b0-119"><em>size</em></span><span class="sxs-lookup"><span data-stu-id="9a2b0-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="9a2b0-120">Taille du champ en nombre de caractères (champs texte et binaires seulement).</span><span class="sxs-lookup"><span data-stu-id="9a2b0-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a2b0-121"><em>index1</em>, <em>index2</em></span><span class="sxs-lookup"><span data-stu-id="9a2b0-121"><em>index1</em>  ,  <em>index2</em></span></span></p></td>
<td><p><span data-ttu-id="9a2b0-122">Clause CONSTRAINT définissant un index de champ unique.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-122">A CONSTRAINT clause defining a single-field index.</span></span> <span data-ttu-id="9a2b0-123">Pour plus d'informations sur la création de cet index, voir <a href="constraint-clause-microsoft-access-sql.md">Clause CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-123">For more information on how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT Clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a2b0-124"><em>multifieldindex</em></span><span class="sxs-lookup"><span data-stu-id="9a2b0-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="9a2b0-125">Clause CONSTRAINT définissant un index multi-champ.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-125">A CONSTRAINT clause defining a multiple-field index.</span></span> <span data-ttu-id="9a2b0-126">Pour plus d'informations sur la création de cet index, voir <a href="constraint-clause-microsoft-access-sql.md">Clause CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-126">For more information on how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT Clause</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9a2b0-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="9a2b0-127">Remarks</span></span>

<span data-ttu-id="9a2b0-128">L’instruction CREATE TABLE permet de définir une nouvelle table, ses champs et ses contraintes de champ.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-128">Use the CREATE TABLE statement to define a new table and its fields and field constraints.</span></span> <span data-ttu-id="9a2b0-129">Si NOT NULL est spécifié pour un champ, les nouveaux enregistrements doivent contenir des données valides dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-129">If NOT NULL is specified for a field, then new records are required to have valid data in that field.</span></span>

<span data-ttu-id="9a2b0-p106">Une clause CONSTRAINT établit diverses restrictions sur un champ et peut être utilisée pour établir la clé primaire. Vous pouvez également utiliser l'instruction [CREATE INDEX](create-index-statement-microsoft-access-sql.md) pour créer une clé primaire ou des index supplémentaires sur les tables existantes.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-p106">A CONSTRAINT clause establishes various restrictions on a field, and can be used to establish the primary key. You can also use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to create a primary key or additional indexes on existing tables.</span></span>

<span data-ttu-id="9a2b0-p107">Vous pouvez utiliser l’instruction NON NULL sur un champ unique ou à l’intérieur d’une clause CONSTRAINT nommée qui s’applique à une instruction CONSTRAINT nommée portant sur un ou plusieurs champs. Toutefois, vous ne pouvez appliquer la restriction NON NULL qu’une seule fois à un champ. Une tentative d’appliquer cette restriction plusieurs fois génère une erreur d’exécution.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-p107">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT. However, you can apply the NOT NULL restriction only once to a field. Attempting to apply this restriction more than once results in a run-time error.</span></span>

<span data-ttu-id="9a2b0-135">Lors de la création d'une table temporaire, celle-ci n'est visible que dans la session dans laquelle elle a été créée.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-135">When a TEMPORARY table is created it is visible only within the session in which it was created.</span></span> <span data-ttu-id="9a2b0-136">Elle est supprimée automatiquement à la fin de la session.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-136">It is automatically deleted when the session is terminated.</span></span> <span data-ttu-id="9a2b0-137">Les tables temporaires sont accessible par plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-137">Temporary tables can be accessed by more than one user.</span></span>

<span data-ttu-id="9a2b0-138">L’attribut WITH COMPRESSION peut être utilisé uniquement avec les types de données CARACTÈRE et MÉMO (également appelé TEXTE) et leurs synonymes.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-138">The WITH COMPRESSION attribute can be used only with the CHARACTER and MEMO (also known as TEXT) data types and their synonyms.</span></span>

<span data-ttu-id="9a2b0-139">L’attribut WITH COMPRESSION a été ajouté pour les colonnes de type CARACTÈRE en raison de la modification du format de représentation de caractère Unicode.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-139">The WITH COMPRESSION attribute was added for CHARACTER columns because of the change to the Unicode character representation format.</span></span> <span data-ttu-id="9a2b0-140">Les caractères Unicode nécessitent uniformément deux octets par caractère.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-140">Unicode characters uniformly require two bytes for each character.</span></span> <span data-ttu-id="9a2b0-141">Pour les bases de données Microsoft Jet qui contiennent principalement des données caractères, cela pourrait signifier que le fichier de base de données doublerait de taille lors de la conversion au format du moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-141">For existing Microsoft® Jet databases that contain predominately character data, this could mean that the database file would nearly double in size when converted to the Microsoft Access database engine format.</span></span> <span data-ttu-id="9a2b0-142">Cependant, la représentation Unicode de nombreux jeux de caractères, anciennement appelés jeux de caractères codés sur un octet (SBCS), peut facilement être compressée à un seul octet.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-142">However, Unicode representation of many character sets, those formerly denoted as Single-Byte Character Sets (SBCS) can easily be compressed to a single byte.</span></span> <span data-ttu-id="9a2b0-143">Si vous définissez une colonne de type CARACTÈRE avec cet attribut, les données sont automatiquement compressées pour le stockage, et décompressées lors de leur extraction de la colonne.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-143">If you define a CHARACTER column with this attribute, data will automatically be compressed as it is stored and uncompressed when retrieved from the column.</span></span>

<span data-ttu-id="9a2b0-p110">Des colonnes de type MÉMO peuvent également être définies pour stocker des données dans un format compressé. Il existe cependant une limitation. Seules les instances de colonnes de type MÉMO qui, une fois compressées, ne dépassent pas 4 096 octets, sont compressées. Les autres instances des colonnes de type MÉMO ne sont pas compressées. Cela signifie que, dans un tableau donné, pour une colonne de type MÉMO donnée, certaines données peuvent être compressées et d’autres pas.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-p110">MEMO columns can also be defined to store data in a compressed format. However, there is a limitation. Only instances of MEMO columns that, when compressed, will fit within 4096 bytes or less, will be compressed. All other instances of MEMO columns will remain uncompressed. This means that within a given table, for a given MEMO column, some data may be compressed and some data may not be compressed.</span></span>

## <a name="example"></a><span data-ttu-id="9a2b0-149">Exemple</span><span class="sxs-lookup"><span data-stu-id="9a2b0-149">Example</span></span>

<span data-ttu-id="9a2b0-150">Cet exemple crée une nouvelle table appelée ThisTable qui comporte deux champs de texte.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-150">This example creates a new table called ThisTable with two text fields.</span></span>

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

<span data-ttu-id="9a2b0-151">Cet exemple crée une nouvelle table appelée MyTable avec deux champs de texte, un champ Date/Heure et un index unique composé de ces trois champs.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-151">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

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

<span data-ttu-id="9a2b0-p111">Cet exemple crée une nouvelle table avec deux champs de texte et un champ **Entier**. Le champ SSN correspond à la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="9a2b0-p111">This example creates a new table with two text fields and an **Integer** field. The SSN field is the primary key.</span></span>

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
