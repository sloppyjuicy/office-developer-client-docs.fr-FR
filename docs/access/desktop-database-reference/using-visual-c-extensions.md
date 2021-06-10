---
title: Utilisation des extensions Visual C++
TOCTitle: Using Visual C++ Extensions
ms:assetid: 0fb1014c-7ab6-6add-d09f-e5e48b2b32cb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248866(v=office.15)
ms:contentKeyID: 48543270
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8bf2234e5935c2a1a13871e7e45c980fb9f33109
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312060"
---
# <a name="using-visual-c-extensions"></a><span data-ttu-id="67461-102">Utilisation d’extensions Visual C++</span><span class="sxs-lookup"><span data-stu-id="67461-102">Using Visual C++ Extensions</span></span>


<span data-ttu-id="67461-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="67461-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="the-iadorecordbinding-interface"></a><span data-ttu-id="67461-104">Interface IADORecordBinding</span><span class="sxs-lookup"><span data-stu-id="67461-104">The IADORecordBinding Interface</span></span>

<span data-ttu-id="67461-p101">Les extensions Microsoft Visual C++ pour ADO associent, ou lient, des champs d'un objet [Recordset](recordset-object-ado.md) à des variables C/C++. Chaque fois que la ligne active de l'objet **Recordset** lié est modifiée, tous les champs liés de l'objet **Recordset** sont copiés dans les variables C/C++. Si nécessaire, les données copiées sont converties dans le type de données déclaré de la variable C/C++.</span><span class="sxs-lookup"><span data-stu-id="67461-p101">The Microsoft Visual C++ Extensions for ADO associate, or bind, fields of a [Recordset](recordset-object-ado.md) object to C/C++ variables. Whenever the current row of the bound **Recordset** changes, all the bound fields in the **Recordset** are copied to the C/C++ variables. If necessary, the copied data is converted to the declared data type of the C/C++ variable.</span></span>

<span data-ttu-id="67461-p102">La méthode **BindToRecordset** de l'interface **IADORecordBinding** lie les champs à des variables C/C++. La méthode **AddNew** ajoute une nouvelle ligne à l'objet **Recordset** lié. La méthode **Update** remplit des champs dans des nouvelles lignes de l'objet **Recordset** ou met à jour des champs de lignes existantes, avec la valeur des variables C/C++.</span><span class="sxs-lookup"><span data-stu-id="67461-p102">The **BindToRecordset** method of the **IADORecordBinding** interface binds fields to C/C++ variables. The **AddNew** method adds a new row to the bound **Recordset**. The **Update** method populates fields in new rows of the **Recordset**, or updates fields in existing rows, with the value of the C/C++ variables.</span></span>

<span data-ttu-id="67461-p103">L'interface **IADORecordBinding** est implémentée par l'objet **Recordset**. Vous n'avez pas à coder l'implémentation vous-même.</span><span class="sxs-lookup"><span data-stu-id="67461-p103">The **IADORecordBinding** interface is implemented by the **Recordset** object. You do not code the implementation yourself.</span></span>

## <a name="binding-entries"></a><span data-ttu-id="67461-113">Entrées de liaison</span><span class="sxs-lookup"><span data-stu-id="67461-113">Binding Entries</span></span>

<span data-ttu-id="67461-p104">Les extensions Visual C++ pour ADO mappent les champs d’un objet [Recordset](recordset-object-ado.md) à des variables C/C++. La définition du mappage entre un champ et une variable s’appelle *entrée de liaison*. Les macros fournissent des entrées de liaison pour les données numériques ainsi que les données de longueur fixe et variable. Les entrées de liaison et les variables C/C++ sont déclarées dans une classe dérivée de la classe des extensions Visual C++, **CADORecordBinding**. La classe **CADORecordBinding** est définie en interne par les macros des entrées de liaison.</span><span class="sxs-lookup"><span data-stu-id="67461-p104">The Visual C++ Extensions for ADO map fields of a [Recordset](recordset-object-ado.md) object to C/C++ variables. The definition of a mapping between a field and a variable is called a *binding entry*. Macros provide binding entries for numeric, fixed-length, and variable-length data. The binding entries and C/C++ variables are declared in a class derived from the Visual C++ Extensions class, **CADORecordBinding**. The **CADORecordBinding** class is defined internally by the binding entry macros.</span></span>

<span data-ttu-id="67461-p105">En interne, ADO mappe les paramètres de ces macros à une structure **DBBINDING** OLE DB et crée un objet **accesseur** OLE DB permettant de gérer le mouvement et la conversion des données entre les champs et les variables. Pour OLE DB, les données se composent de trois parties : une *mémoire tampon* dans laquelle les données sont stockées, un *état* qui indique si un champ a été correctement stocké dans la mémoire tampon ou comment la variable doit être restaurée dans le champ et la *longueur* des données. Pour plus d'informations, consultez le manuel *OLE DB Programmer's Reference*, Chapter 6: Getting and Setting Data (en anglais).</span><span class="sxs-lookup"><span data-stu-id="67461-p105">ADO internally maps the parameters in these macros to an OLE DB **DBBINDING** structure and creates an OLE DB **Accessor** object to manage the movement and conversion of data between fields and variables. OLE DB defines data as consisting of three parts: A *buffer* where the data is stored; a *status* that indicates whether a field was successfully stored in the buffer, or how the variable should be restored to the field; and the *length* of the data. (See the *OLE DB Programmer's Reference*, Chapter 6: Getting and Setting Data for more information.)</span></span>

## <a name="header-file"></a><span data-ttu-id="67461-122">Fichier d'en-tête</span><span class="sxs-lookup"><span data-stu-id="67461-122">Header File</span></span>

<span data-ttu-id="67461-123">Incluez le fichier suivant dans votre application pour pouvoir utiliser les extensions Visual C++ pour ADO :</span><span class="sxs-lookup"><span data-stu-id="67461-123">Include the following file in your application in order to use the Visual C++ Extensions for ADO:</span></span>

```cpp 
 
#include <icrsint.h> 
```

## <a name="binding-recordset-fields"></a><span data-ttu-id="67461-124">Liaison des champs d'un objet Recordset</span><span class="sxs-lookup"><span data-stu-id="67461-124">Binding Recordset Fields</span></span>

<span data-ttu-id="67461-125">**Pour lier les champs d'un objet Recordset à des variables C/C++**</span><span class="sxs-lookup"><span data-stu-id="67461-125">**To Bind Recordset Fields to C/C++ Variables**</span></span>

1.  <span data-ttu-id="67461-126">Créez une classe dérivée de la classe **CADORecordBinding**.</span><span class="sxs-lookup"><span data-stu-id="67461-126">Create a class derived from the **CADORecordBinding** class.</span></span>

2.  <span data-ttu-id="67461-127">Spécifiez les entrées de liaison et les variables C/C++ correspondantes dans la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="67461-127">Specify binding entries and corresponding C/C++ variables in the derived class.</span></span> <span data-ttu-id="67461-128">Mettre entre crochets les entrées de liaison entre les macros **BEGIN \_ ADO \_ BINDING** et **END \_ ADO \_ BINDING.**</span><span class="sxs-lookup"><span data-stu-id="67461-128">Bracket the binding entries between **BEGIN\_ADO\_BINDING** and **END\_ADO\_BINDING** macros.</span></span> <span data-ttu-id="67461-129">Les macros ne doivent pas se terminer par des virgules ou des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="67461-129">Do not terminate the macros with commas or semicolons.</span></span> <span data-ttu-id="67461-130">Les délimiteurs appropriés sont spécifiés automatiquement par chaque macro.</span><span class="sxs-lookup"><span data-stu-id="67461-130">Appropriate delimiters are specified automatically by each macro.</span></span> <span data-ttu-id="67461-131">Spécifiez une entrée de liaison pour chaque champ à mapper à une variable C/C++.</span><span class="sxs-lookup"><span data-stu-id="67461-131">Specify one binding entry for each field to be mapped to a C/C++ variable.</span></span> <span data-ttu-id="67461-132">Utilisez un membre approprié de la famille de macros ENTRÉE LONGUEUR FIXE **ADO, \_ \_ \_** ENTRÉE NUMÉRIQUE **ADO \_ \_** ou **LONGUEUR \_ VARIABLE \_ \_ ADO.**</span><span class="sxs-lookup"><span data-stu-id="67461-132">Use an appropriate member from the **ADO\_FIXED\_LENGTH\_ENTRY**, **ADO\_NUMERIC\_ENTRY**, or **ADO\_VARIABLE\_LENGTH\_ENTRY** family of macros.</span></span>

3.  <span data-ttu-id="67461-p107">Dans votre application, créez une instance de la classe dérivée de **CADORecordBinding**. Obtenez l'interface **IADORecordBinding** de l'objet **Recordset**, puis appelez la méthode **BindToRecordset** pour lier les champs de l'objet **Recordset** aux variables C/C++.</span><span class="sxs-lookup"><span data-stu-id="67461-p107">In your application, create an instance of the class derived from **CADORecordBinding**. Get the **IADORecordBinding** interface from the **Recordset**. Then call the **BindToRecordset** method to bind the **Recordset** fields to the C/C++ variables.</span></span>

<span data-ttu-id="67461-136">Pour plus d’informations, voir [Exemple d’extensions Visual C++](visual-c-extensions-example.md).</span><span class="sxs-lookup"><span data-stu-id="67461-136">See the [Visual C++ Extensions Example](visual-c-extensions-example.md) for more information.</span></span>

## <a name="interface-methods"></a><span data-ttu-id="67461-137">Méthodes d'interface</span><span class="sxs-lookup"><span data-stu-id="67461-137">Interface Methods</span></span>

<span data-ttu-id="67461-p108">L'interface **IADORecordBinding** comporte trois méthodes : **BindToRecordset**, **AddNew** et **Update**. Le seul argument de chaque méthode est un pointeur vers une instance de la classe dérivée de **CADORecordBinding**. En conséquence, les méthodes **AddNew** et **Update** ne peuvent spécifier aucun des paramètres des méthodes ADO du même nom.</span><span class="sxs-lookup"><span data-stu-id="67461-p108">The **IADORecordBinding** interface has three methods: **BindToRecordset**, **AddNew**, and **Update**. The sole argument to each method is a pointer to an instance of the class derived from **CADORecordBinding**. Therefore, the **AddNew** and **Update** methods cannot specify any of the parameters of their ADO method namesakes.</span></span>

<span data-ttu-id="67461-141">**Syntaxe**</span><span class="sxs-lookup"><span data-stu-id="67461-141">**Syntax**</span></span>

<span data-ttu-id="67461-142">La méthode **BindToRecordset** associe les champs d'un objet **Recordset** à des variables C/C++.</span><span class="sxs-lookup"><span data-stu-id="67461-142">The **BindToRecordset** method associates the **Recordset** fields with C/C++ variables.</span></span>

`BindToRecordset(CADORecordBinding *binding)` 

<span data-ttu-id="67461-143">La méthode **AddNew** appelle la méthode ADO éponyme, à savoir la méthode [AddNew](addnew-method-ado.md) ADO, pour ajouter une nouvelle ligne à l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="67461-143">The **AddNew** method invokes its namesake, the ADO [AddNew](addnew-method-ado.md) method, to add a new row to the **Recordset**.</span></span>

`AddNew(CADORecordBinding *binding)` 

<span data-ttu-id="67461-144">La méthode **Update** appelle la méthode ADO éponyme, à savoir la méthode [Update](update-method-ado.md) ADO, pour mettre à jour l’objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="67461-144">The **Update** method invokes its namesake, the ADO [Update](update-method-ado.md) method, to update the **Recordset**.</span></span>

`Update(CADORecordBinding *binding)` 

## <a name="binding-entry-macros"></a><span data-ttu-id="67461-145">Macros d'entrées de liaison</span><span class="sxs-lookup"><span data-stu-id="67461-145">Binding Entry Macros</span></span>

<span data-ttu-id="67461-p109">Les macros d'entrées de liaison définissent l'association entre un champ d'un objet **Recordset** et une variable. Des macros de début et de fin délimitent le jeu d'entrées de liaison.</span><span class="sxs-lookup"><span data-stu-id="67461-p109">Binding entry macros define the association of a **Recordset** field and a variable. A beginning and ending macro delimits the set of binding entries.</span></span>

<span data-ttu-id="67461-p110">Des familles de macros sont fournies pour les données de longueur fixe, telles que **adDate** ou **adBoolean**, les donnés numériques, telles que **adTinyInt**, **adInteger** ou **adDouble** et les données de longueur variable, telles que **adChar**, **adVarChar** ou **adVarBinary**. Tous les types numériques, à l'exception de **adVarNumeric**, sont également des données de longueur fixe. Chaque famille possède des jeux de paramètres différents, ce qui vous permet d'exclure des informations de liaison superflues.</span><span class="sxs-lookup"><span data-stu-id="67461-p110">Families of macros are provided for fixed-length data, such as **adDate** or **adBoolean**; numeric data, such as **adTinyInt**, **adInteger**, or **adDouble**; and variable-length data, such as **adChar**, **adVarChar** or **adVarBinary**. All numeric types, except for **adVarNumeric**, are also fixed-length types. Each family has differing sets of parameters so that you can exclude binding information that is of no interest.</span></span>

<span data-ttu-id="67461-151">Pour plus d'informations, consultez le manuel *OLE DB Programmer's Reference*, Appendix A: Data Types (en anglais).</span><span class="sxs-lookup"><span data-stu-id="67461-151">See the *OLE DB Programmer's Reference,* Appendix A: Data Types for additional information.</span></span>

<span data-ttu-id="67461-152">_**Début des entrées de liaison**_</span><span class="sxs-lookup"><span data-stu-id="67461-152">_**Begin Binding Entries**_</span></span>

<span data-ttu-id="67461-153">**BEGIN \_ ADO \_ BINDING**(*Class*)</span><span class="sxs-lookup"><span data-stu-id="67461-153">**BEGIN\_ADO\_BINDING**(*Class*)</span></span>

<span data-ttu-id="67461-154">_**Données de longueur fixe**_</span><span class="sxs-lookup"><span data-stu-id="67461-154">_**Fixed-Length Data**_</span></span>

<span data-ttu-id="67461-155">**ADO \_ FIXED \_ LENGTH \_ ENTRY**(*Ordinal, DataType, Buffer, Status, Modify*)</span><span class="sxs-lookup"><span data-stu-id="67461-155">**ADO\_FIXED\_LENGTH\_ENTRY**(*Ordinal, DataType, Buffer, Status, Modify*)</span></span>  
<span data-ttu-id="67461-156">**ADO \_ FIXED \_ LENGTH \_ ENTRY2**(*Ordinal, DataType, Buffer, Modify*)</span><span class="sxs-lookup"><span data-stu-id="67461-156">**ADO\_FIXED\_LENGTH\_ENTRY2**(*Ordinal, DataType, Buffer, Modify*)</span></span>

<span data-ttu-id="67461-157">_**Données numériques**_</span><span class="sxs-lookup"><span data-stu-id="67461-157">_**Numeric Data**_</span></span>

<span data-ttu-id="67461-158">**ADO \_ NUMERIC \_ ENTRY**(*Ordinal, DataType, Buffer, Precision, Scale, Status, Modify*)</span><span class="sxs-lookup"><span data-stu-id="67461-158">**ADO\_NUMERIC\_ENTRY**(*Ordinal, DataType, Buffer, Precision, Scale, Status, Modify*)</span></span>  
<span data-ttu-id="67461-159">**ADO \_ NUMERIC \_ ENTRY2**(*Ordinal, DataType, Buffer, Precision, Scale, Modify*)</span><span class="sxs-lookup"><span data-stu-id="67461-159">**ADO\_NUMERIC\_ENTRY2**(*Ordinal, DataType, Buffer, Precision, Scale, Modify*)</span></span>

<span data-ttu-id="67461-160">_**Données de longueur variable**_</span><span class="sxs-lookup"><span data-stu-id="67461-160">_**Variable-Length Data**_</span></span>

<span data-ttu-id="67461-161">**ADO \_ ENTRÉE \_ DE LONGUEUR \_ VARIABLE**(*Ordinal, Type de données, Mémoire tampon, Taille, État, Longueur, Modifier*)</span><span class="sxs-lookup"><span data-stu-id="67461-161">**ADO\_VARIABLE\_LENGTH\_ENTRY**(*Ordinal, DataType, Buffer, Size, Status, Length, Modify*)</span></span>  
<span data-ttu-id="67461-162">**ADO \_ VARIABLE \_ LENGTH \_ ENTRY2**(*Ordinal, DataType, Buffer, Size, Status, Modify*)</span><span class="sxs-lookup"><span data-stu-id="67461-162">**ADO\_VARIABLE\_LENGTH\_ENTRY2**(*Ordinal, DataType, Buffer, Size, Status, Modify*)</span></span>  
<span data-ttu-id="67461-163">**ADO \_ VARIABLE \_ LENGTH \_ ENTRY3**(*Ordinal, DataType, Buffer, Size, Length, Modify*)</span><span class="sxs-lookup"><span data-stu-id="67461-163">**ADO\_VARIABLE\_LENGTH\_ENTRY3**(*Ordinal, DataType, Buffer, Size, Length, Modify*)</span></span>  
<span data-ttu-id="67461-164">**ADO \_ VARIABLE \_ LENGTH \_ ENTRY4**(*Ordinal, DataType, Buffer, Size, Modify*)</span><span class="sxs-lookup"><span data-stu-id="67461-164">**ADO\_VARIABLE\_LENGTH\_ENTRY4**(*Ordinal, DataType, Buffer, Size, Modify*)</span></span>

<span data-ttu-id="67461-165">_**Entrées de liaison de fin**_</span><span class="sxs-lookup"><span data-stu-id="67461-165">_**End Binding Entries**_</span></span>

<span data-ttu-id="67461-166">**END \_ LIAISON \_ ADO**()</span><span class="sxs-lookup"><span data-stu-id="67461-166">**END\_ADO\_BINDING**()</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="67461-167">Parameter</span><span class="sxs-lookup"><span data-stu-id="67461-167">Parameter</span></span></p></th>
<th><p><span data-ttu-id="67461-168">Description</span><span class="sxs-lookup"><span data-stu-id="67461-168">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67461-169"><em>Classe</em></span><span class="sxs-lookup"><span data-stu-id="67461-169"><em>Class</em></span></span></p></td>
<td><p><span data-ttu-id="67461-170">Classe dans laquelle sont définies les entrées de liaison et les variables C/C++.</span><span class="sxs-lookup"><span data-stu-id="67461-170">Class in which the binding entries and C/C++ variables are defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67461-171"><em>Ordinal</em></span><span class="sxs-lookup"><span data-stu-id="67461-171"><em>Ordinal</em></span></span></p></td>
<td><p><span data-ttu-id="67461-172">Nombre ordinal, à partir de un, du champ de l'objet <strong>Recordset</strong> correspondant à la variable C/C++.</span><span class="sxs-lookup"><span data-stu-id="67461-172">Ordinal number, counting from one, of the <strong>Recordset</strong> field corresponding to your C/C++ variable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67461-173"><em>DataType</em></span><span class="sxs-lookup"><span data-stu-id="67461-173"><em>DataType</em></span></span></p></td>
<td><p><span data-ttu-id="67461-p111">Type de données ADO équivalent de la variable C/C++ (les types de données valides sont répertoriés à la rubrique <a href="datatypeenum.md">DataTypeEnum</a>). La valeur du champ de l’objet <strong>Recordset</strong> sera convertie dans ce type de données, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="67461-p111">Equivalent ADO data type of the C/C++ variable (see <a href="datatypeenum.md">DataTypeEnum</a> for a list of valid data types). The value of the <strong>Recordset</strong> field will be converted to this data type if necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67461-176"><em>Buffer</em></span><span class="sxs-lookup"><span data-stu-id="67461-176"><em>Buffer</em></span></span></p></td>
<td><p><span data-ttu-id="67461-177">Nom de la variable C/C++ dans laquelle le champ de l'objet <strong>Recordset</strong> va être stocké.</span><span class="sxs-lookup"><span data-stu-id="67461-177">Name of the C/C++ variable where the <strong>Recordset</strong> field will be stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67461-178"><em>Taille</em></span><span class="sxs-lookup"><span data-stu-id="67461-178"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="67461-p112">Taille maximale, en octets, du paramètre <em>Mémoire tampon</em>. Si le paramètre <em>Mémoire tampon</em> contient une chaîne de longueur variable, prévoyez de l'espace pour un zéro de fin.</span><span class="sxs-lookup"><span data-stu-id="67461-p112">Maximum size in bytes of <em>Buffer</em>. If <em>Buffer</em> will contain a variable-length string, allow room for a terminating zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67461-181"><em>État</em></span><span class="sxs-lookup"><span data-stu-id="67461-181"><em>Status</em></span></span></p></td>
<td><p><span data-ttu-id="67461-182">Nom d'une variable qui indique si le contenu du paramètre <em>Mémoire tampon</em> est valide et si la conversion du champ en <em>Type de données</em> s'est correctement déroulée.</span><span class="sxs-lookup"><span data-stu-id="67461-182">Name of a variable that will indicate whether the contents of <em>Buffer</em> are valid, and whether the conversion of the field to <em>DataType</em> was successful.</span></span> <span data-ttu-id="67461-183">Les deux valeurs les plus importantes de cette variable sont <strong>adFldOK</strong>, qui indique que la conversion s'est correctement déroulée, et <strong>adFldNull</strong>, qui indique que la valeur du champ est un VARIANT de type VT_NULL et que ce champ n'est pas simplement vide.</span><span class="sxs-lookup"><span data-stu-id="67461-183">The two most important values for this variable are <strong>adFldOK</strong>, which means the conversion was successful; and <strong>adFldNull</strong>, which means the value of the field would be a VARIANT of type VT_NULL and not merely empty.</span></span> <span data-ttu-id="67461-184">Les valeurs possibles <em>pour l’état</em> sont répertoriées dans le tableau suivant, &quot; Valeurs d’état.&quot;</span><span class="sxs-lookup"><span data-stu-id="67461-184">Possible values for <em>Status</em> are listed in the next table, &quot;Status Values.&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67461-185"><em>Modify</em></span><span class="sxs-lookup"><span data-stu-id="67461-185"><em>Modify</em></span></span></p></td>
<td><p><span data-ttu-id="67461-186">Indicateur booléen. S'il a la valeur TRUE, il indique qu'ADO est autorisé à mettre à jour l'objet <strong>Recordset</strong> correspondant avec la valeur contenue dans le paramètre <em>Mémoire tampon</em>.
</span><span class="sxs-lookup"><span data-stu-id="67461-186">Boolean flag; if TRUE, indicates ADO is allowed to update the corresponding <strong>Recordset</strong> field with the value contained in <em>Buffer</em>.</span></span> <span data-ttu-id="67461-187">Affectez la valeur TRUE au paramètre <em>modifier</em> booléen pour permettre à ADO de mettre à jour le champ lié et la valeur FALSE si vous voulez examiner le champ sans le modifier.</span><span class="sxs-lookup"><span data-stu-id="67461-187">Set the Boolean <em>modify</em> parameter to TRUE to enable ADO to update the bound field, and FALSE if you want to examine the field but not change it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67461-188"><em>Précision</em></span><span class="sxs-lookup"><span data-stu-id="67461-188"><em>Precision</em></span></span></p></td>
<td><p><span data-ttu-id="67461-189">Nombre de chiffres pouvant être représenté dans une variable numérique.</span><span class="sxs-lookup"><span data-stu-id="67461-189">Number of digits that can be represented in a numeric variable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67461-190"><em>Scale</em></span><span class="sxs-lookup"><span data-stu-id="67461-190"><em>Scale</em></span></span></p></td>
<td><p><span data-ttu-id="67461-191">Nombre de décimales dans une variable numérique.</span><span class="sxs-lookup"><span data-stu-id="67461-191">Number of decimal places in a numeric variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67461-192"><em>Length</em></span><span class="sxs-lookup"><span data-stu-id="67461-192"><em>Length</em></span></span></p></td>
<td><p><span data-ttu-id="67461-193">Nom d'une variable à quatre octets qui doit contenir la longueur réelle des données dans <em>Mémoire tampon</em>.</span><span class="sxs-lookup"><span data-stu-id="67461-193">Name of a four-byte variable that will contain the actual length of the data in <em>Buffer</em>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="status-values"></a><span data-ttu-id="67461-194">Valeurs du paramètre État</span><span class="sxs-lookup"><span data-stu-id="67461-194">Status Values</span></span>

<span data-ttu-id="67461-195">La valeur de la variable *État* indique si un champ a été correctement copié dans une variable.</span><span class="sxs-lookup"><span data-stu-id="67461-195">The value of the *Status* variable indicates whether a field was successfully copied to a variable.</span></span>

<span data-ttu-id="67461-196">Lorsque vous définissez les données, vous pouvez affecter à *État* la valeur **adFldNull** pour indiquer que le champ de l'objet **Recordset** doit avoir une valeur null.</span><span class="sxs-lookup"><span data-stu-id="67461-196">When setting data, *Status* may be set to **adFldNull** to indicate the **Recordset** field should be set to null.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="67461-197">Constante</span><span class="sxs-lookup"><span data-stu-id="67461-197">Constant</span></span></p></th>
<th><p><span data-ttu-id="67461-198">Valeur</span><span class="sxs-lookup"><span data-stu-id="67461-198">Value</span></span></p></th>
<th><p><span data-ttu-id="67461-199">Description</span><span class="sxs-lookup"><span data-stu-id="67461-199">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67461-200"><strong>adFldOK</strong></span><span class="sxs-lookup"><span data-stu-id="67461-200"><strong>adFldOK</strong></span></span></p></td>
<td><p><span data-ttu-id="67461-201">0</span><span class="sxs-lookup"><span data-stu-id="67461-201">0</span></span></p></td>
<td><p><span data-ttu-id="67461-202">Une valeur de champ non null a été retournée.</span><span class="sxs-lookup"><span data-stu-id="67461-202">A non-null field value was returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67461-203"><strong>adFldBadAccessor</strong></span><span class="sxs-lookup"><span data-stu-id="67461-203"><strong>adFldBadAccessor</strong></span></span></p></td>
<td><p><span data-ttu-id="67461-204">1</span><span class="sxs-lookup"><span data-stu-id="67461-204">1</span></span></p></td>
<td><p><span data-ttu-id="67461-205">Liaison non valide.</span><span class="sxs-lookup"><span data-stu-id="67461-205">Binding was invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67461-206"><strong>adFldCantConvertValue</strong></span><span class="sxs-lookup"><span data-stu-id="67461-206"><strong>adFldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="67461-207">2</span><span class="sxs-lookup"><span data-stu-id="67461-207">2</span></span></p></td>
<td><p><span data-ttu-id="67461-208">La valeur n'a pas pu être convertie pour une raison autre qu'une non correspondance de signes ou un dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="67461-208">Value couldn't be converted for reasons other than sign mismatch or data overflow.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67461-209"><strong>adFldNull</strong></span><span class="sxs-lookup"><span data-stu-id="67461-209"><strong>adFldNull</strong></span></span></p></td>
<td><p><span data-ttu-id="67461-210">3</span><span class="sxs-lookup"><span data-stu-id="67461-210">3</span></span></p></td>
<td><p><span data-ttu-id="67461-211">Lors de l'obtention d'un champ, indique qu'une valeur null a été retournée.</span><span class="sxs-lookup"><span data-stu-id="67461-211">When getting a field, indicates a null value was returned.</span></span> <span data-ttu-id="67461-212">Lors de la définition d'un champ, indique que le champ doit être affecté de la valeur <strong>NULL</strong> lorsqu'il ne peut pas coder lui-même la valeur <strong>NULL</strong> (par exemple, un tableau de caractères ou un nombre entier).</span><span class="sxs-lookup"><span data-stu-id="67461-212">When setting a field, indicates the field should be set to <strong>NULL</strong> when the field cannot encode <strong>NULL</strong> itself (for example, a character array or an integer).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67461-213"><strong>adFldTruncated</strong></span><span class="sxs-lookup"><span data-stu-id="67461-213"><strong>adFldTruncated</strong></span></span></p></td>
<td><p><span data-ttu-id="67461-214">4 </span><span class="sxs-lookup"><span data-stu-id="67461-214">4</span></span></p></td>
<td><p><span data-ttu-id="67461-215">Des données de longueur variable ou des chiffres ont été tronqués.</span><span class="sxs-lookup"><span data-stu-id="67461-215">Variable-length data or numeric digits were truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67461-216"><strong>adFldSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="67461-216"><strong>adFldSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="67461-217">5 </span><span class="sxs-lookup"><span data-stu-id="67461-217">5</span></span></p></td>
<td><p><span data-ttu-id="67461-218">La valeur est signée et le type de données de la variable ne l'est pas.</span><span class="sxs-lookup"><span data-stu-id="67461-218">Value is signed and variable data type is unsigned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67461-219"><strong>adFldDataOverFlow</strong></span><span class="sxs-lookup"><span data-stu-id="67461-219"><strong>adFldDataOverFlow</strong></span></span></p></td>
<td><p><span data-ttu-id="67461-220">6 </span><span class="sxs-lookup"><span data-stu-id="67461-220">6</span></span></p></td>
<td><p><span data-ttu-id="67461-221">La valeur est supérieure à la capacité de stockage du type de données de la variable.</span><span class="sxs-lookup"><span data-stu-id="67461-221">Value is larger than could be stored in the variable data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67461-222"><strong>adFldCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="67461-222"><strong>adFldCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="67461-223">7 </span><span class="sxs-lookup"><span data-stu-id="67461-223">7</span></span></p></td>
<td><p><span data-ttu-id="67461-224">Type de colonne inconnu et champ déjà ouvert.</span><span class="sxs-lookup"><span data-stu-id="67461-224">Unknown column type and field already open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67461-225"><strong>adFldUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="67461-225"><strong>adFldUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="67461-226">8 </span><span class="sxs-lookup"><span data-stu-id="67461-226">8</span></span></p></td>
<td><p><span data-ttu-id="67461-227">La valeur du champ n'a pas pu être déterminée, par exemple, sur un nouveau champ non assigné et ne comportant aucune valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="67461-227">Field value could not be determined — for example, on a new, unassigned field with no default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67461-228"><strong>adFldPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="67461-228"><strong>adFldPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="67461-229">9 </span><span class="sxs-lookup"><span data-stu-id="67461-229">9</span></span></p></td>
<td><p><span data-ttu-id="67461-230">Lors d'une mise à jour, absence d'autorisation d'écriture des données.</span><span class="sxs-lookup"><span data-stu-id="67461-230">When updating, no permission to write data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67461-231"><strong>adFldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="67461-231"><strong>adFldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="67461-232">10</span><span class="sxs-lookup"><span data-stu-id="67461-232">10</span></span></p></td>
<td><p><span data-ttu-id="67461-233">Lors d'une mise à jour, la valeur du champ enfreint l'intégrité de la colonne.</span><span class="sxs-lookup"><span data-stu-id="67461-233">When updating, field value would violate column integrity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67461-234"><strong>adFldSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="67461-234"><strong>adFldSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="67461-235">11</span><span class="sxs-lookup"><span data-stu-id="67461-235">11</span></span></p></td>
<td><p><span data-ttu-id="67461-236">Lors d'une mise à jour, la valeur du champ ne respecte pas le schéma de colonne.</span><span class="sxs-lookup"><span data-stu-id="67461-236">When updating, field value would violate column schema.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67461-237"><strong>adFldBadStatus</strong></span><span class="sxs-lookup"><span data-stu-id="67461-237"><strong>adFldBadStatus</strong></span></span></p></td>
<td><p><span data-ttu-id="67461-238">12 </span><span class="sxs-lookup"><span data-stu-id="67461-238">12</span></span></p></td>
<td><p><span data-ttu-id="67461-239">Lors d'une mise à jour, paramètre d'état incorrect.</span><span class="sxs-lookup"><span data-stu-id="67461-239">When updating, invalid status parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67461-240"><strong>adFldDefault</strong></span><span class="sxs-lookup"><span data-stu-id="67461-240"><strong>adFldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="67461-241">13</span><span class="sxs-lookup"><span data-stu-id="67461-241">13</span></span></p></td>
<td><p><span data-ttu-id="67461-242">Lors d'une mise à jour, une valeur par défaut a été utilisée.</span><span class="sxs-lookup"><span data-stu-id="67461-242">When updating, a default value was used.</span></span></p></td>
</tr>
</tbody>
</table>

