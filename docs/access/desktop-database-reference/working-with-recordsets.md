---
title: Utilisation des jeux d'enregistrements
TOCTitle: Working with Recordsets
ms:assetid: 9cd52866-2738-8150-381c-eee0b8a6cd36
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249711(v=office.15)
ms:contentKeyID: 48546608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d57f05905aa0f79c1a72638e70ede8bdabf73b8f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883686"
---
# <a name="working-with-recordsets"></a><span data-ttu-id="0ebe1-102">Utilisation des jeux d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="0ebe1-102">Working with Recordsets</span></span>


<span data-ttu-id="0ebe1-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ebe1-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="0ebe1-p101">L'objet **Recordset** possède des fonctionnalités intégrées permettant de réorganiser l'ordre des données dans le jeu de résultats, ce qui permet, d'une part, de rechercher des enregistrements spécifiques sur base de critères définis et, d'autre part, d'optimiser ces opérations de recherche à l'aide d'index. La disponibilité de ces fonctionnalités dépend du fournisseur et, dans certains cas, notamment celui de la propriété [Index](index-property-ado.md), de la structure même de la source de données.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p101">The **Recordset** object has built-in features that make it possible for you to rearrange the order of the data in the result set, to search for a specific record based on criteria that you supply, and even to optimize those search operations using indexes. Whether these features are available for use depends on the provider and in some cases — such as that of the [Index](index-property-ado.md) property — the structure of the data source itself.</span></span>

## <a name="arranging-data"></a><span data-ttu-id="0ebe1-106">Organisation des données</span><span class="sxs-lookup"><span data-stu-id="0ebe1-106">Arranging Data</span></span>

<span data-ttu-id="0ebe1-p102">En règle générale, le moyen le plus efficace d'organiser les données d'un objet **Recordset** consiste à spécifier une clause ORDER BY dans la commande SQL utilisée pour retourner les résultats dans le jeu d'enregistrements. Gardez néanmoins à l'esprit que vous devrez parfois modifier l'ordre des données dans un objet **Recordset** lorsqu'il a déjà été créé. En définissant la propriété **Sort**, vous êtes en mesure d'établir l'ordre dans lequel les lignes d'un objet **Recordset** seront parcourues. En outre, la propriété **Filter** permet de déterminer les lignes accessibles lors du parcours des lignes.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p102">Often, the most efficient way to order the data in your **Recordset** is by specifying an ORDER BY clause in the SQL command used to return results to it. However, you might need to change the order of the data in a **Recordset** that has already been created. You can use the **Sort** property to establish the order in which rows of a **Recordset** are traversed. Furthermore, the **Filter** property determines which rows are accessible when traversing rows.</span></span>

<span data-ttu-id="0ebe1-p103">La propriété **Sort** définit ou renvoie une valeur de type **String** indiquant les noms des champs de l'objet **Recordset** qui feront l'objet du tri. Chaque nom est séparé par une virgule et peut être suivi d'un espace et du mot clé **ASC** (pour un tri par ordre croissant) ou **DESC** (pour un tri par ordre décroissant). Par défaut, si aucun mot clé n'est spécifié, le champ sera trié par ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p103">The **Sort** property sets or returns a **String** value that indicates the field names in the **Recordset** on which to sort. Each name is separated by a comma and is optionally followed by a space and the keyword **ASC** (which sorts the field in ascending order) or **DESC** (which sorts the field in descending order). By default, if no keyword is specified, the field is sorted in ascending order.</span></span>

<span data-ttu-id="0ebe1-114">L'efficacité de l'opération de tri réside dans le fait que les données ne sont pas triées physiquement, mais simplement accédées dans l'ordre spécifié par un index.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-114">The sort operation is efficient because data is not physically rearranged but is simply accessed in the order specified by an index.</span></span>

<span data-ttu-id="0ebe1-p104">Lorsque vous utilisez la propriété **Sort**, la propriété [CursorLocation](cursorlocation-property-ado.md) doit être définie avec la valeur **adUseClient**. En l'absence d'un index existant, un index temporaire sera créé pour chaque champ spécifié dans la propriété **Sort**.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p104">The **Sort** property requires the [CursorLocation](cursorlocation-property-ado.md) property to be set to **adUseClient**. A temporary index will be created for each field specified in the **Sort** property if an index does not already exist.</span></span>

<span data-ttu-id="0ebe1-p105">Si vous définissez une chaîne vide comme valeur de la propriété **Sort**, les lignes sont rétablies dans leur ordre initial et les index temporaires sont supprimés. En revanche, les index existants seront conservés.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p105">Setting the **Sort** property to an empty string will reset the rows to their original order and delete temporary indexes. Existing indexes will not be deleted.</span></span>

<span data-ttu-id="0ebe1-119">Supposons qu’un **objet Recordset** contienne trois champs nommés *firstName*, *middleInitial*et *lastName*.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-119">Suppose a **Recordset** contains three fields named *firstName*, *middleInitial*, and *lastName*.</span></span> <span data-ttu-id="0ebe1-120">La valeur de la propriété **Sort** la chaîne « », qui sera le **jeu d’enregistrements** par nom de famille en ordre décroissant, puis par prénom par ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-120">Set the **Sort** property to the string "", which will order the **Recordset** by last name in descending order and then by first name in ascending order.</span></span> <span data-ttu-id="0ebe1-121">L'initiale du second prénom sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-121">The middle initial is ignored.</span></span>

<span data-ttu-id="0ebe1-p107">Aucun champ référencé dans une chaîne de critères de tri ne peut être nommé « ASC » ou « DESC », car ces noms provoquent des conflits avec les mots clés **ASC** et **DESC**. Attribuez au nom du champ posant problème un alias à l'aide du mot clé **AS** dans la requête qui retourne l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p107">No field referenced in a sort criteria string can be named "ASC" or "DESC" because those names conflict with the keywords **ASC** and **DESC**. Give a field with a conflicting name an alias by using the **AS** keyword in the query that returns the **Recordset**.</span></span>

<span data-ttu-id="0ebe1-124">Pour plus d'informations sur le filtrage des objets **Recordset**, consultez la section Filtrage des résultats, plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-124">For more details about **Recordset** filtering, see Filtering the Results later in this topic.</span></span>

## <a name="finding-a-specific-record"></a><span data-ttu-id="0ebe1-125">Recherche d'un enregistrement spécifique</span><span class="sxs-lookup"><span data-stu-id="0ebe1-125">Finding a Specific Record</span></span>

<span data-ttu-id="0ebe1-p108">Les méthodes ADO [Find](find-method-ado.md) et [Seek](seek-method-ado.md) permettent de localiser un enregistrement spécifique dans un objet **Recordset**. La méthode **Find** est prise en charge par un grand nombre de fournisseurs, mais est limitée à un seul critère de recherche. La méthode **Seek** permet une recherche basée sur plusieurs critères, mais n'est pas prise en charge par tous les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p108">ADO provides the [Find](find-method-ado.md) and [Seek](seek-method-ado.md) methods for locating a particular record in a **Recordset**. The **Find** method is supported by a variety of providers but is limited to a single search criterion. The **Seek** method supports searching on multiple criteria, but is not supported by many providers.</span></span>

<span data-ttu-id="0ebe1-p109">Des champs indexés permettent d'améliorer considérablement les performances de la méthode **Find** ainsi que des propriétés **Sort** et **Filter** d'un objet **Recordset**. Vous pouvez créer un index interne pour un objet **Field** en définissant sa propriété dynamique [Optimize](optimize-property-dynamic-ado.md). Cette propriété dynamique s'ajoute à la collection **Properties** de l'objet **Field** lorsque vous affectez à la propriété [CursorLocation](cursorlocation-property-ado.md) la valeur **adUseClient**. Gardez à l'esprit qu'il s'agit d'un index interne d'ADO, ce qui signifie que vous ne pouvez y accéder ou l'utiliser à d'autres fins. En outre, sachez que cet index est différent de la propriété **Index** de l'objet [Recordset](index-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p109">Indexes on fields can greatly enhance the performance of the **Recordset** object's **Find** method and **Sort** and **Filter** properties. You can create an internal index for a **Field** object by setting its dynamic [Optimize](optimize-property-dynamic-ado.md) property. This dynamic property is added to the **Field** object's **Properties** collection when you set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**. Remember that this index is internal to ADO — you cannot gain access to it or use it for any other purpose. Also, this index is distinct from the **Recordset** object's [Index](index-property-ado.md) property.</span></span>

<span data-ttu-id="0ebe1-p110">La méthode **Find** permet de localiser rapidement une valeur dans une colonne (champ) d'un objet **Recordset**. Vous pouvez généralement accélérer l'exécution de la méthode **Find** sur une colonne en utilisant la propriété **Optimize** pour y créer un index.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p110">The **Find** method quickly locates a value within a column (field) of a **Recordset**. You can often improve the speed of the **Find** method's operation on a column by using the **Optimize** property to create an index on it.</span></span>

<span data-ttu-id="0ebe1-p111">La méthode **Find** limite votre recherche au contenu d'un seul champ. Quant à la méthode **Seek**, elle requiert la présence d'un index et présente également d'autres limitations. Si vous devez lancer une recherche sur plusieurs champs non indexés ou si votre fournisseur ne prend pas les index en charge, vous pouvez limiter les résultats en utilisant la propriété **Filter** de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p111">The **Find** method limits your search to the contents of one field. The **Seek** method requires that you have an index and has other limitations as well. If you need to search on multiple fields that aren't the basis of an index, or if your provider does not support indexes, you can limit your results using the **Filter** property of the **Recordset** object.</span></span>

## <a name="find"></a><span data-ttu-id="0ebe1-139">Find</span><span class="sxs-lookup"><span data-stu-id="0ebe1-139">Find</span></span>

<span data-ttu-id="0ebe1-p112">La méthode **Find** recherche, dans un objet **Recordset**, une ligne répondant à un critère spécifié. Le cas échéant, il est également possible de définir la direction de la recherche, la ligne de départ et le décalage depuis la ligne de début. Si une ligne correspond au critère défini, la position de la ligne active est définie sur l'enregistrement trouvé. Dans le cas contraire, la position active est définie sur la fin (ou le début) de l'objet **Recordset**, selon la direction de la recherche.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p112">The **Find** method searches a **Recordset** for the row that satisfies a specified criterion. Optionally, the direction of the search, starting row, and offset from the starting row may be specified. If the criterion is met, the current row position is set on the found record; otherwise, the position is set to the end (or start) of the **Recordset**, depending on search direction.</span></span>

<span data-ttu-id="0ebe1-p113">Seul un nom de colonne unique peut être spécifié comme critère. En effet, cette méthode ne prend pas en charge les recherches sur plusieurs colonnes.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p113">Only a single-column name may be specified for the criterion. In other words, this method does not support multi-column searches.</span></span>

<span data-ttu-id="0ebe1-145">L’opérateur de comparaison du critère peut être «**\>**« (supérieur à), »**\<**« (inférieur à), « = » (égal à), »\>= » (supérieur ou égal à), «\<= » (inférieur ou égal à), «\<\>» (différent de), ou « LIKE » (correspondance).</span><span class="sxs-lookup"><span data-stu-id="0ebe1-145">The comparison operator for the criterion may be "**\>**" (greater than), "**\<**" (less than), "=" (equal), "\>=" (greater than or equal), "\<=" (less than or equal), "\<\>" (not equal), or "LIKE" (pattern matching).</span></span>

<span data-ttu-id="0ebe1-146">La valeur du critère doit être une chaîne, un nombre à virgule flottante ou une date.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-146">The criterion value may be a string, floating-point number, or date.</span></span> <span data-ttu-id="0ebe1-147">Valeurs de chaîne sont délimitées par des guillemets simples ou «\#» (signe dièse) marque (par exemple, « état = 'WA' » ou « état = \#WA\#»).</span><span class="sxs-lookup"><span data-stu-id="0ebe1-147">String values are delimited with single quotes or "\#" (number sign) marks (for example, "state = 'WA'" or "state = \#WA\#").</span></span> <span data-ttu-id="0ebe1-148">Valeurs de date sont délimitées par des «\#» (signe dièse) marque (par exemple, « démarrer\_date \> \#7/22/97\#»).</span><span class="sxs-lookup"><span data-stu-id="0ebe1-148">Date values are delimited with "\#" (number sign) marks (for example, "start\_date \> \#7/22/97\#").</span></span>

<span data-ttu-id="0ebe1-p115">Si l'opérateur de comparaison est « like », la valeur de la chaîne peut contenir un astérisque (\*) pour rechercher une ou plusieurs occurrences d'un caractère ou d'une sous-chaîne. Par exemple, « state like 'M\*' » correspond à Maine et Massachusetts. Vous pouvez également utiliser des astérisques au début et à la fin pour rechercher une sous-chaîne dans les valeurs. Par exemple, « state like '\*as\* » correspond à Alaska, Arkansas et Massachusetts.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p115">If the comparison operator is "like", the string value may contain an asterisk (\*) to find one or more occurrences of any character or substring. For example, "state like 'M\*'" matches Maine and Massachusetts. You can also use leading and trailing asterisks to find a substring contained within the values. For example, "state like '\*as\*'" matches Alaska, Arkansas, and Massachusetts.</span></span>

<span data-ttu-id="0ebe1-p116">Les astérisques ne peuvent être utilisés qu'à la fin d'une chaîne de critère ou au début et à la fin d'une chaîne de critère, comme nous l'avons vu dans les exemples précédents. L'utilisation d'un astérisque comme caractère générique de début ('\*str') ou comme caractère générique incorporé ('s\*r') provoque une erreur.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p116">Asterisks can be used only at the end of a criteria string or together at both the beginning and end of a criteria string, as shown above. You cannot use the asterisk as a leading wildcard ('\*str') or embedded wildcard ('s\*r'). This will cause an error.</span></span>

## <a name="seek-and-index"></a><span data-ttu-id="0ebe1-156">Seek et Index</span><span class="sxs-lookup"><span data-stu-id="0ebe1-156">Seek and Index</span></span>

<span data-ttu-id="0ebe1-p117">Il est conseillé d’utiliser conjointement la méthode **Seek** avec la propriété **Index** si le fournisseur sous-jacent prend les index en charge sur l’objet **Recordset**. La méthode [Supports](supports-method-ado.md)**(adSeek)** permet de déterminer si le fournisseur sous-jacent prend **Seek** en charge, et la méthode **Supports(adIndex)** de déterminer si les index sont pris en charge par le fournisseur. (Par exemple, le [fournisseur OLE DB pour Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) prend **Seek** et **Index** en charge.)</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p117">Use the **Seek** method in conjunction with the **Index** property if the underlying provider supports indexes on the **Recordset** object. Use the [Supports](supports-method-ado.md)**(adSeek)** method to determine whether the underlying provider supports **Seek**, and the **Supports(adIndex)** method to determine whether the provider supports indexes. (For example, the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) supports **Seek** and **Index**.)</span></span>

<span data-ttu-id="0ebe1-p118">Si la méthode **Seek** ne trouve pas la ligne recherchée, aucune erreur n'est générée et la ligne est positionnée à la fin du **Recordset**. Veillez à définir la propriété **Index** sur l'index souhaité avant d'exécuter cette méthode.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p118">If **Seek** does not find the desired row, no error occurs, and the row is positioned at the end of the **Recordset**. Set the **Index** property to the desired index before executing this method.</span></span>

<span data-ttu-id="0ebe1-p119">Cette méthode n'est prise en charge qu'avec des curseurs côté serveur. La méthode Seek n'est pas prise en charge lorsque la valeur de la propriété **CursorLocation** de l'objet [Recordset](cursorlocation-property-ado.md) est **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p119">This method is supported only with server-side cursors. Seek is not supported when the **Recordset** object's [CursorLocation](cursorlocation-property-ado.md) property value is **adUseClient**.</span></span>

<span data-ttu-id="0ebe1-164">Cette méthode peut être utilisée dans le seul cas où l'objet **Recordset** a été ouvert avec la valeur [adCmdTableDirect](commandtypeenum.md) de **CommandTypeEnum**.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-164">This method can be used only when the **Recordset** object has been opened with a [CommandTypeEnum](commandtypeenum.md) value of **adCmdTableDirect**.</span></span>

## <a name="filtering-the-results"></a><span data-ttu-id="0ebe1-165">Filtrage des résultats</span><span class="sxs-lookup"><span data-stu-id="0ebe1-165">Filtering the Results</span></span>

<span data-ttu-id="0ebe1-p120">La méthode **Find** limite votre recherche au contenu d'un seul champ. La méthode **Seek** exige la présence d'un index et possède également d'autres limitations.Si vous devez exécuter une recherche sur plusieurs champs non indexés ou si votre fournisseur ne prend pas les index en charge, vous pouvez limiter vos résultats en utilisant la propriété **Filter** de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p120">The **Find** method limits your search to the contents of one field. The **Seek** method requires that you have an index and has other limitations as well. If you need to search on multiple fields that are not the basis of an index or if your provider does not support indexes, you can limit your results using the **Filter** property of the **Recordset** object.</span></span>

<span data-ttu-id="0ebe1-p121">La propriété **Filtre** permet d'effectuer une recherche sélective d'enregistrements dans un objet **Recordset**. L'objet **Recordset** filtré devient le curseur actif. En d'autres termes, les enregistrements qui ne répondent pas aux critères de la propriété **Filter** ne sont pas disponibles dans l'objet **Recordset** tant que la propriété **Filter** n'est pas supprimée. Les autres propriétés qui renvoient des valeurs relatives au curseur actif sont également affectées, par exemple **AbsolutePosition**, **AbsolutePage**, **RecordCount** et **PageCount**. Ceci s'explique par le fait que l'affectation d'une valeur spécifique à la propriété **Filter** déplace la position d'enregistrement actif au niveau du premier enregistrement qui correspond à la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p121">Use the **Filter** property to selectively screen out records in a **Recordset** object. The filtered **Recordset** becomes the current cursor, which means that records that do not satisfy the **Filter** criteria are not available in the **Recordset** until the **Filter** is removed. Other properties that return values based on the current cursor are affected, such as **AbsolutePosition**, **AbsolutePage**, **RecordCount**, and **PageCount**. This is because setting the **Filter** property to a specific value will move the current record to the first record that satisfies the new value.</span></span>

<span data-ttu-id="0ebe1-p122">La propriété **Filter** prend un argument de type Variant. Cette valeur représente l'une des trois méthodes d'utilisation de la propriété **Filter**: une chaîne de critères, une constante **FilterGroupEnum** ou un tableau de signets. Pour plus d'informations, consultez les sections Filtrage à l'aide d'une chaîne de critères, Filtrage avec une constante et Filtrage avec des signets, plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p122">The **Filter** property takes a variant argument. This value represents one of three methods for using the **Filter** property: a criteria string, a **FilterGroupEnum** constant, or an array of bookmarks. For more information, see Filtering with a Criteria String, Filtering with a Constant, and Filtering with Bookmarks later in this topic.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0ebe1-176">[!REMARQUE] Lorsque vous connaissez les données à sélectionner, il est généralement plus efficace d'ouvrir un <STRONG>Recordset</STRONG> avec une instruction SQL capable de filtrer efficacement le jeu de résultats au lieu d'utiliser la propriété <STRONG>Filter</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-176">When you know the data you want to select, it is usually more efficient to open a <STRONG>Recordset</STRONG> with a SQL statement that effectively filters the result set, rather than relying on the <STRONG>Filter</STRONG> property.</span></span></P>



<span data-ttu-id="0ebe1-p123">Pour supprimer un filtre d'un **Recordset**, utilisez la constante **adFilterNone**. En définissant une chaîne vide ("") comme valeur de la propriété **Filter**, vous obtenez le même résultat qu'en utilisant la constante **adFilterNone**.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p123">To remove a filter from a **Recordset**, use the **adFilterNone** constant. Setting the **Filter** property to a zero-length string ("") has the same effect as using the **adFilterNone** constant.</span></span>

## <a name="filtering-with-a-criteria-string"></a><span data-ttu-id="0ebe1-179">Filtrage avec une chaîne de critères</span><span class="sxs-lookup"><span data-stu-id="0ebe1-179">Filtering with a Criteria String</span></span>

<span data-ttu-id="0ebe1-180">La chaîne de critères est composée de clauses de type *NomChamp Opérateur valeur* (par exemple, « LastName = 'Martin' »).</span><span class="sxs-lookup"><span data-stu-id="0ebe1-180">The criteria string is made up of clauses in the form *FieldName Operator Value* (for example, "LastName = 'Smith'").</span></span> <span data-ttu-id="0ebe1-181">Vous pouvez créer des clauses composées en concaténant des clauses avec AND (par exemple, « LastName = 'Martin' AND FirstName = 'John' ») et OR (par exemple,).</span><span class="sxs-lookup"><span data-stu-id="0ebe1-181">You can create compound clauses by concatenating individual clauses with AND (for example, "LastName = 'Smith' AND FirstName = 'John'") and OR (for example, ).</span></span> <span data-ttu-id="0ebe1-182">Vous pouvez créer des clauses composées en concaténant des clauses avec et (par exemple, « LastName = 'Martin' AND FirstName = 'John' ») et ou (par exemple, « LastName = 'Martin' OR LastName = 'Jones' »).</span><span class="sxs-lookup"><span data-stu-id="0ebe1-182">You can create compound clauses by concatenating individual clauses with AND (for example, "LastName = 'Smith' AND FirstName = 'John'") and OR (for example, "LastName = 'Smith' OR LastName = 'Jones'").</span></span> <span data-ttu-id="0ebe1-183">Lorsque vous utilisez des chaînes de critères, gardez les points suivants à l'esprit :</span><span class="sxs-lookup"><span data-stu-id="0ebe1-183">Use the following guidelines for criteria strings:</span></span>

  - <span data-ttu-id="0ebe1-184">*FieldName* doit être un nom de champ valide du **jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-184">*FieldName* must be a valid field name from the **Recordset**.</span></span> <span data-ttu-id="0ebe1-185">Si le nom de champ contient des espaces, vous devez le mettre entre crochets.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-185">If the field name contains spaces, you must enclose the name in square brackets.</span></span>

  - <span data-ttu-id="0ebe1-186">*Opérateur* doit être une des opérations suivantes : \<, \>, \<= \>=, \< \>, = ou LIKE.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-186">*Operator* must be one of the following: \<, \>, \<=, \>=, \<\>, =, or LIKE.</span></span>

  - <span data-ttu-id="0ebe1-187">*Valeur* est la valeur à laquelle vous comparez les valeurs de champ (par exemple, « Smith », \#24/8/95\#, 12.345 ou $50.00).</span><span class="sxs-lookup"><span data-stu-id="0ebe1-187">*Value* is the value with which you will compare the field values (for example, 'Smith', \#8/24/95\#, 12.345, or $50.00).</span></span> <span data-ttu-id="0ebe1-188">Utilisez des guillemets simples (') avec des chaînes et les signes dièse (\#) avec des dates.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-188">Use single quotation marks (') with strings and pound signs (\#) with dates.</span></span> <span data-ttu-id="0ebe1-189">Pour les nombres, vous pouvez utiliser les points décimaux, le signe dollar et les notations scientifiques.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-189">For numbers, you can use decimal points, dollar signs, and scientific notation.</span></span> <span data-ttu-id="0ebe1-190">Si *l’opérateur* est LIKE, *valeur* peut utiliser des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-190">If *Operator* is LIKE, *Value* can use wildcards.</span></span> <span data-ttu-id="0ebe1-191">Uniquement l’astérisque (\*) et le signe de pourcentage (%) des caractères génériques sont autorisés, et ils doivent être le dernier caractère de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-191">Only the asterisk (\*) and percent sign (%) wildcards are allowed, and they must be the last character in the string.</span></span> <span data-ttu-id="0ebe1-192">*Valeur* ne peut pas être null.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-192">*Value* cannot be null.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="0ebe1-193">Pour inclure des guillemets simples (') dans la <EM>valeur</EM>de filtre, utilisez deux guillemets simples pour représenter un.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-193">To include single quotation marks (') in the filter <EM>Value</EM>, use two single quotation marks to represent one.</span></span> <span data-ttu-id="0ebe1-194">Par exemple, pour filtrer sur <EM>Malley</EM>, la chaîne de critères doit être « col1 = ' O'' Malley' ».</span><span class="sxs-lookup"><span data-stu-id="0ebe1-194">For example, to filter on <EM>O'Malley</EM>, the criteria string should be "col1 = 'O''Malley'".</span></span> <span data-ttu-id="0ebe1-195">Pour inclure des guillemets simples au début et à la fin de la valeur du filtre, placez des signes dièse (#) de part et d'autre de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-195">To include single quotation marks at both the beginning and the end of the filter value, enclose the string in pound signs (#).</span></span> <span data-ttu-id="0ebe1-196">Par exemple, pour filtrer sur <EM>'1'</EM>, la chaîne de critères doit être « col1 = #' 1' # ».</span><span class="sxs-lookup"><span data-stu-id="0ebe1-196">For example, to filter on <EM>'1'</EM>, the criteria string should be "col1 = #'1'#".</span></span></P>



<span data-ttu-id="0ebe1-p128">Il n'existe pas de priorité entre AND et OR. Les clauses peuvent être regroupées dans des parenthèses. Notez toutefois que vous ne pouvez pas regrouper des clauses jointes par OR, puis associer le groupe à une autre clause avec AND, comme ceci :</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p128">There is no precedence between AND and OR. Clauses can be grouped within parentheses. However, you cannot group clauses joined by an OR and then join the group to another clause with an AND, like this:</span></span>

```vb 
 
(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John' 
```

<span data-ttu-id="0ebe1-200">Le filtre doit être construit comme suit :</span><span class="sxs-lookup"><span data-stu-id="0ebe1-200">Instead, you would construct this filter as:</span></span>

```vb 
 
(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John') 
```

<span data-ttu-id="0ebe1-201">Dans une clause LIKE, vous pouvez utiliser un caractère générique au début et fin de la chaîne (par exemple, LastName Like '\*mit\*') ou uniquement à la fin de la chaîne (par exemple), ou uniquement à la fin de la chaîne (par exemple, LastName Like ' Smit\*»).</span><span class="sxs-lookup"><span data-stu-id="0ebe1-201">In a LIKE clause, you can use a wildcard at the beginning and end of the pattern (for example, LastName Like '\*mit\*') or only at the end of the pattern (for example, ) or only at the end of the pattern (for example, LastName Like 'Smit\*').</span></span>

## <a name="filtering-with-a-constant"></a><span data-ttu-id="0ebe1-202">Filtrage avec une constante</span><span class="sxs-lookup"><span data-stu-id="0ebe1-202">Filtering with a Constant</span></span>

<span data-ttu-id="0ebe1-203">Les constantes suivantes sont disponibles pour le filtrage des objets **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-203">The following constants are available for filtering **Recordsets**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ebe1-204">Constant</span><span class="sxs-lookup"><span data-stu-id="0ebe1-204">Constant</span></span></p></th>
<th><p><span data-ttu-id="0ebe1-205">Description</span><span class="sxs-lookup"><span data-stu-id="0ebe1-205">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ebe1-206"><strong>adFilterAffectedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="0ebe1-206"><strong>adFilterAffectedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="0ebe1-207">Affiche uniquement les enregistrements concernés par le dernier appel à <strong>Delete</strong>, <strong>Resync</strong>, <strong>UpdateBatch</strong> ou <strong>CancelBatch</strong>.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-207">Filters for viewing only records effected by the last <strong>Delete</strong>, <strong>Resync</strong>, <strong>UpdateBatch</strong>, or <strong>CancelBatch</strong> call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ebe1-208"><strong>adFilterConflictingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="0ebe1-208"><strong>adFilterConflictingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="0ebe1-209">Affiche les enregistrements pour lesquels la dernière mise à jour par lot a échoué.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-209">Filters for viewing the records that failed the last batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ebe1-210"><strong>adFilterFetchedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="0ebe1-210"><strong>adFilterFetchedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="0ebe1-211">Affiche les enregistrements du cache actif , c'est-à-dire les résultats du dernier appel visant à extraire des enregistrements de la base de données.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-211">Filters for viewing the records in the current cache — that is, the results of the last call to retrieve records from the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ebe1-212"><strong>adFilterNone</strong></span><span class="sxs-lookup"><span data-stu-id="0ebe1-212"><strong>adFilterNone</strong></span></span></p></td>
<td><p><span data-ttu-id="0ebe1-213">Supprime le filtre actif et restaure l'affichage de tous les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-213">Removes the current filter and restores all records for viewing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ebe1-214"><strong>adFilterPendingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="0ebe1-214"><strong>adFilterPendingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="0ebe1-p129">Affiche uniquement les enregistrements qui ont été modifiés mais pas encore envoyés au serveur. Applicable uniquement pour le mode de mise à jour par lot.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p129">Filters for viewing only records that have changed but have not yet been sent to the server. Applicable only for batch update mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0ebe1-217">Les constantes de filtre simplifient la résolution des conflits d'enregistrements individuels pendant le mode de mise à jour par lot en vous permettant de n'afficher, par exemple, que les enregistrements affectés par le dernier appel de la méthode **UpdateBatch**, comme illustré dans l'exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="0ebe1-217">The filter constants make it easier to resolve individual record conflicts during batch update mode by allowing you to view, for example, only those records that were effected during the last **UpdateBatch** method call, as shown in the following example:</span></span>

```vb 
 
'BeginDeleteGroup 
    'add some bogus records 
    With objRs1 
        For i = 0 To 8 
            .AddNew 
            .Fields("CompanyName") = "Shipper Number " & i + 1 
            .Fields("Phone") = "(425) 555-000" & (i + 1) 
            .Update 
        Next i 
         
    're-connect & update 
        .ActiveConnection = GetNewConnection 
        .UpdateBatch 
         
    'filter on newly added records 
        .Filter = adFilterAffectedRecords 
        Debug.Print "Deleting the " & .RecordCount & _ 
                    " records you just added." 
         
    'delete the newly added bogus records 
        .Delete adAffectGroup 
        .Filter = adFilterNone 
        Debug.Print .RecordCount & " records remain." 
         
        .Close 
    End With 
'EndDeleteGroup 
```

## <a name="filtering-with-bookmarks"></a><span data-ttu-id="0ebe1-218">Filtrage avec les signets</span><span class="sxs-lookup"><span data-stu-id="0ebe1-218">Filtering with Bookmarks</span></span>

<span data-ttu-id="0ebe1-219">Enfin, vous pouvez transmettre un tableau de signets de type Variant à la propriété **Filter**.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-219">Finally, you can pass a variant array of bookmarks to the **Filter** property.</span></span> <span data-ttu-id="0ebe1-220">Le curseur résultant contiendra uniquement les enregistrements dont le signet a été transmis à la propriété.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-220">The resulting cursor will contain only those records whose bookmark was passed in to the property.</span></span> <span data-ttu-id="0ebe1-221">L’exemple de code suivant crée un tableau de signets à partir des enregistrements dans un **jeu d’enregistrements** qui ont un « B » dans le champ *ProductName* .</span><span class="sxs-lookup"><span data-stu-id="0ebe1-221">The following code example creates an array of bookmarks from the records in a **Recordset** which have a "B" in the *ProductName* field.</span></span> <span data-ttu-id="0ebe1-222">Il passe ensuite le tableau à la propriété **Filter** et affiche les informations de l'objet **Recordset** filtré qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-222">It then passes the array to the **Filter** property and displays information about the resulting filtered **Recordset**.</span></span>

```vb 
 
'BeginFilterBkmk 
    Dim vBkmkArray() As Variant 
    Dim i As Integer 
 
    'Recordset created using "SELECT * FROM Products" as command. 
    'So, we will check to see if ProductName has a capital B, and 
    'if so, add to the array. 
    i = 0 
    Do While Not objRs.EOF 
        If InStr(1, objRs("ProductName"), "B") Then 
            ReDim Preserve vBkmkArray(i) 
            vBkmkArray(i) = objRs.Bookmark 
            i = i + 1 
            Debug.Print objRs("ProductName") 
        End If 
        objRs.MoveNext 
    Loop 
     
    'Filter using the array of bookmarks. 
    objRs.Filter = vBkmkArray 
     
    objRs.MoveFirst 
    Do While Not objRs.EOF 
        Debug.Print objRs("ProductName") 
        objRs.MoveNext 
    Loop 
    'EndFilterBkmk 
```

## <a name="creating-a-clone-of-a-recordset"></a><span data-ttu-id="0ebe1-223">Création d'un clone d'un jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="0ebe1-223">Creating a Clone of a Recordset</span></span>

<span data-ttu-id="0ebe1-p131">Utilisez la méthode **Clone** pour créer plusieurs objets **Recordset** dupliqués, notamment dans le cas où vous souhaitez conserver plusieurs enregistrements actifs dans un jeu d'enregistrements donné. La méthode **Clone** est plus efficace que la technique qui consiste à créer et ouvrir un nouvel objet **Recordset** avec une définition identique à celle de l'original.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p131">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records. Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="0ebe1-p132">L'enregistrement actif d'un clone créé est initialement le premier enregistrement. Le pointeur de l'enregistrement actif dans un objet **Recordset** cloné n'est pas synchronisé avec l'original et vice versa. Vous pouvez naviguer de façon indépendante dans chaque objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p132">The current record of a newly created clone is originally set to the first record. The current record pointer in a cloned **Recordset** is not synchronized with the original or vice versa. You can navigate independently in each **Recordset**.</span></span>

<span data-ttu-id="0ebe1-p133">Les modifications apportées à un objet **Recordset** apparaissent dans tous ses clones, quel que soit le type de curseur utilisé. Toutefois, après l'exécution de la méthode [Requery](requery-method-ado.md) sur l'objet **Recordset** d'origine, les clones ne sont plus synchronisés avec l'original.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p133">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type. However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="0ebe1-231">La fermeture de l'objet **Recordset** d'origine ne ferme pas ses copies pas plus que la fermeture d'une copie ne ferme l'objet d'origine ni aucune autre copie.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-231">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="0ebe1-p134">Vous pouvez cloner un objet **Recordset** uniquement s'il prend en charge les signets. Les valeurs des signets sont interchangeables ; en d'autres termes, une référence de signet d'un objet **Recordset** donné fait référence au même enregistrement dans chacun de ses clones.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-p134">You can clone a **Recordset** object only if it supports bookmarks. Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>

