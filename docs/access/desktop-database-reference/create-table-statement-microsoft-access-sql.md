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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710936"
---
# <a name="create-table-statement-microsoft-access-sql"></a><span data-ttu-id="52ede-102">Instruction CREATE TABLE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="52ede-102">CREATE TABLE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="52ede-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="52ede-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="52ede-104">Crée une table.</span><span class="sxs-lookup"><span data-stu-id="52ede-104">Creates a new table.</span></span>

> [!NOTE]
> <span data-ttu-id="52ede-105">[!REMARQUE] Le moteur de base de données Microsoft Access ne prend pas en charge l'utilisation de l'instruction CREATE TABLE, ni d'aucune instruction DDL, avec des bases de données autres que celles du moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="52ede-105">The Microsoft Access database engine does not support the use of CREATE TABLE, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="52ede-106">Utilisez les méthodes DAO **créer** à la place.</span><span class="sxs-lookup"><span data-stu-id="52ede-106">Use the DAO **Create** methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="52ede-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52ede-107">Syntax</span></span>

<span data-ttu-id="52ede-108">CRÉER \[temporaire\] TABLE *table* (*type champ1* \[(*taille*)\] \[non NULL\] \[WITH COMPRESSION | AVEC COMP\] \[ *index1* \] \[, *champ2* *type* \[(*taille*)\] \[non NULL\] \[ *index2* \] \[,... \] \] \[, CONSTRAINT *index de plusieurs champs* \[,... \]\])</span><span class="sxs-lookup"><span data-stu-id="52ede-108">CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])</span></span>

<span data-ttu-id="52ede-109">L’instruction CREATE TABLE comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="52ede-109">The CREATE TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52ede-110">Élément</span><span class="sxs-lookup"><span data-stu-id="52ede-110">Part</span></span></p></th>
<th><p><span data-ttu-id="52ede-111">Description</span><span class="sxs-lookup"><span data-stu-id="52ede-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52ede-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="52ede-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="52ede-113">Nom de la table à créer.</span><span class="sxs-lookup"><span data-stu-id="52ede-113">The name of the table to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52ede-114"><em>champ1</em>, <em>champ2</em></span><span class="sxs-lookup"><span data-stu-id="52ede-114"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="52ede-p102">Nom du ou des champs à créer dans la nouvelle table. Vous devez créer au moins un champ.</span><span class="sxs-lookup"><span data-stu-id="52ede-p102">The name of field or fields to be created in the new table. You must create at least one field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52ede-117"><em>type</em></span><span class="sxs-lookup"><span data-stu-id="52ede-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="52ede-118">Le type de données du <em>champ</em> dans la nouvelle table.</span><span class="sxs-lookup"><span data-stu-id="52ede-118">The data type of <em>field</em> in the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52ede-119"><em>taille</em></span><span class="sxs-lookup"><span data-stu-id="52ede-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="52ede-120">Taille du champ en nombre de caractères (champs texte et binaires seulement).</span><span class="sxs-lookup"><span data-stu-id="52ede-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52ede-121"><em>index1</em>, <em>index2</em></span><span class="sxs-lookup"><span data-stu-id="52ede-121"><em>index1</em>, <em>index2</em></span></span></p></td>
<td><p><span data-ttu-id="52ede-122">Clause CONSTRAINT définissant un index de champ unique.</span><span class="sxs-lookup"><span data-stu-id="52ede-122">A CONSTRAINT clause defining a single-field index.</span></span> <span data-ttu-id="52ede-123">Pour plus d’informations sur la création de cet index, voir la <a href="constraint-clause-microsoft-access-sql.md">clause CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="52ede-123">For more information about how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52ede-124"><em>indexmultichamp</em></span><span class="sxs-lookup"><span data-stu-id="52ede-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="52ede-125">Clause CONSTRAINT définissant un index multichamp.</span><span class="sxs-lookup"><span data-stu-id="52ede-125">A CONSTRAINT clause defining a multiple-field index.</span></span> <span data-ttu-id="52ede-126">Pour plus d’informations sur la création de cet index, voir la <a href="constraint-clause-microsoft-access-sql.md">clause CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="52ede-126">For more information about how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="52ede-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="52ede-127">Remarks</span></span>

<span data-ttu-id="52ede-128">Utilisez l'instruction CREATE TABLE pour définir une nouvelle table, ses champs et ses contraintes de champ.</span><span class="sxs-lookup"><span data-stu-id="52ede-128">Use the CREATE TABLE statement to define a new table and its fields and field constraints.</span></span> <span data-ttu-id="52ede-129">Si ce n’est pas NULL est spécifiée pour un champ, de nouveaux enregistrements sont requis pour contenir des données valides dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="52ede-129">If NOT NULL is specified for a field, new records are required to have valid data in that field.</span></span>

<span data-ttu-id="52ede-p106">Une clause CONSTRAINT établit diverses restrictions sur un champ et peut être utilisée pour établir la clé primaire. Vous pouvez également utiliser l'instruction [CREATE INDEX](create-index-statement-microsoft-access-sql.md) pour créer une clé primaire ou des index supplémentaires sur les tables existantes.</span><span class="sxs-lookup"><span data-stu-id="52ede-p106">A CONSTRAINT clause establishes various restrictions on a field, and can be used to establish the primary key. You can also use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to create a primary key or additional indexes on existing tables.</span></span>

<span data-ttu-id="52ede-p107">Vous ne pouvez pas utiliser NOT NULL sur un champ unique ou dans une clause nommée CONSTRAINT qui s'applique à une clause CONSTRAINT nommée de champ unique ou multichamp. Cependant, vous ne pouvez appliquer la restriction NOT NULL qu'une seule fois à un champ. Toute tentative d'application de cette restriction plus d'une fois entraîne une erreur d'exécution.</span><span class="sxs-lookup"><span data-stu-id="52ede-p107">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT. However, you can apply the NOT NULL restriction only once to a field. Attempting to apply this restriction more than once results in a run-time error.</span></span>

<span data-ttu-id="52ede-135">Lorsqu’une table temporaire est créée, il est visible uniquement dans la session dans laquelle il a été créé.</span><span class="sxs-lookup"><span data-stu-id="52ede-135">When a TEMPORARY table is created, it is visible only within the session in which it was created.</span></span> <span data-ttu-id="52ede-136">Elle est automatiquement supprimée lorsque la session est terminée.</span><span class="sxs-lookup"><span data-stu-id="52ede-136">It is automatically deleted when the session is terminated.</span></span> <span data-ttu-id="52ede-137">Les tables temporaires sont accessibles par plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="52ede-137">Temporary tables can be accessed by more than one user.</span></span>

<span data-ttu-id="52ede-138">L'attribut WITH COMPRESSION peut être utilisé uniquement avec les types de données CARACTÈRES et MÉMO (également connus sous le nom de données TEXTE) et leurs synonymes.</span><span class="sxs-lookup"><span data-stu-id="52ede-138">The WITH COMPRESSION attribute can be used only with the CHARACTER and MEMO (also known as TEXT) data types and their synonyms.</span></span>

<span data-ttu-id="52ede-139">L'attribut WITH COMPRESSION a été ajouté pour les colonnes CARACTÈRES en raison du changement de format de représentation des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="52ede-139">The WITH COMPRESSION attribute was added for CHARACTER columns because of the change to the Unicode character representation format.</span></span> <span data-ttu-id="52ede-140">Les caractères Unicode nécessitent uniformément deux octets pour chaque caractère.</span><span class="sxs-lookup"><span data-stu-id="52ede-140">Unicode characters uniformly require two bytes for each character.</span></span> <span data-ttu-id="52ede-141">Pour Microsoft Jet bases de données existantes qui contiennent principalement des caractères, cela signifie que le fichier de base de données risque de doubler taille lors de la conversion au format de moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="52ede-141">For existing Microsoft Jet databases that contain predominately character data, this could mean that the database file would nearly double in size when converted to the Microsoft Access database engine format.</span></span> <span data-ttu-id="52ede-142">Toutefois, représentation Unicode de plusieurs jeux de caractères, ceux précédemment indiqués comme un octet caractère définit (SBCS), peut facilement être compressée en un octet unique.</span><span class="sxs-lookup"><span data-stu-id="52ede-142">However, Unicode representation of many character sets, those formerly denoted as Single-Byte Character Sets (SBCS), can easily be compressed to a single byte.</span></span> <span data-ttu-id="52ede-143">Si vous définissez une colonne de caractères avec cet attribut, les données seront automatiquement compressées au moment du stockage, et décompressées lors de leur récupération à partir de la colonne.</span><span class="sxs-lookup"><span data-stu-id="52ede-143">If you define a CHARACTER column with this attribute, data will automatically be compressed as it is stored and uncompressed when retrieved from the column.</span></span>

<span data-ttu-id="52ede-p110">Les colonnes MÉMO peuvent également être définies pour stocker des données dans un format compressé. Toutefois, il existe une limite. Seules les instances des colonnes MÉMO qui, une fois compressées, représentent 4 096 octets ou moins, seront compressées. Toutes les autres instances des colonnes MÉMO resteront non compressées. Cela signifie que dans une table donnée, pour une colonne MÉMO donnée, certaines données peuvent être compressées et d'autres non.</span><span class="sxs-lookup"><span data-stu-id="52ede-p110">MEMO columns can also be defined to store data in a compressed format. However, there is a limitation. Only instances of MEMO columns that, when compressed, will fit within 4096 bytes or less, will be compressed. All other instances of MEMO columns will remain uncompressed. This means that within a given table, for a given MEMO column, some data may be compressed and some data may not be compressed.</span></span>

## <a name="example"></a><span data-ttu-id="52ede-149">Exemple</span><span class="sxs-lookup"><span data-stu-id="52ede-149">Example</span></span>

<span data-ttu-id="52ede-150">Cet exemple crée une nouvelle table appelée ThisTable qui comporte deux champs de texte.</span><span class="sxs-lookup"><span data-stu-id="52ede-150">This example creates a new table called ThisTable with two text fields.</span></span>

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

<span data-ttu-id="52ede-151">Cet exemple crée une nouvelle table appelée MyTable avec deux champs de texte, un champ Date/Heure et un index unique composé de ces trois champs.</span><span class="sxs-lookup"><span data-stu-id="52ede-151">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

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

<span data-ttu-id="52ede-p111">Cet exemple crée une nouvelle table avec deux champs de texte et un champ **Entier**. Le champ SSN correspond à la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="52ede-p111">This example creates a new table with two text fields and an **Integer** field. The SSN field is the primary key.</span></span>

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
