---
<span data-ttu-id="ba430-101"><<<<<<< Titre tête : TOCTitle tri propriété (ADO) : tri propriété (ADO) === titre : trier, propriété (ADO) TOCTitle : trier, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="ba430-101"><<<<<<< HEAD title: Sort Property (ADO) TOCTitle: Sort Property (ADO) ======= title: Sort property (ADO) TOCTitle: Sort property (ADO)</span></span>
>>>>>>> <span data-ttu-id="ba430-102">Master ms:assetid : f2a39b7f-8b96-cd1a-8248-71f8b867454a ms:mtpsurl : https://msdn.microsoft.com/library/JJ250230(v=office.15) ms:contentKeyID : ms.date 48548652 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="ba430-102">master ms:assetid: f2a39b7f-8b96-cd1a-8248-71f8b867454a ms:mtpsurl: https://msdn.microsoft.com/library/JJ250230(v=office.15) ms:contentKeyID: 48548652 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="ba430-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="ba430-103"><<<<<<< HEAD</span></span>
# <a name="sort-property-ado"></a><span data-ttu-id="ba430-104">Sort, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="ba430-104">Sort Property (ADO)</span></span>
=======
# <a name="sort-property-ado"></a><span data-ttu-id="ba430-105">Sort, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="ba430-105">Sort property (ADO)</span></span>
>>>>>>> <span data-ttu-id="ba430-106">master</span><span class="sxs-lookup"><span data-stu-id="ba430-106">master</span></span>


<span data-ttu-id="ba430-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba430-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ba430-108">Indique un ou plusieurs noms de champs selon lesquels le [Recordset](recordset-object-ado.md) est trié ; indique en outre si les valeurs des champs sont triés en ordre croissant ou décroissant.</span><span class="sxs-lookup"><span data-stu-id="ba430-108">Indicates one or more field names on which the [Recordset](recordset-object-ado.md) is sorted, and whether each field is sorted in ascending or descending order.</span></span>

<span data-ttu-id="ba430-109"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="ba430-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="ba430-110">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="ba430-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="ba430-111">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="ba430-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="ba430-112">master</span><span class="sxs-lookup"><span data-stu-id="ba430-112">master</span></span>

<span data-ttu-id="ba430-p101">Définit ou renvoie une valeur **String** qui indique les noms des champs du **Recorset** selon lesquels le tri est réalisé. Les noms sont séparés par des virgules et éventuellement suivis d'un espace puis du mot clé **ASC** (si les valeurs du champ sont triées en ordre croissant) ou **DESC** (si les valeurs du champ sont triées en ordre décroissant). Si aucun mot clé n'est spécifié, les valeurs du champ sont par défaut triées en ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="ba430-p101">Sets or returns a **String** value that indicates the field names in the **Recordset** on which to sort. Each name is separated by a comma, and is optionally followed by a blank and the keyword, **ASC**, which sorts the field in ascending order, or **DESC**, which sorts the field in descending order. By default, if no keyword is specified, the field is sorted in ascending order.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba430-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="ba430-116">Remarks</span></span>

<span data-ttu-id="ba430-p102">Cette propriété exige que la propriété [CursorLocation](cursorlocation-property-ado.md) ait la valeur **adUseClient**. Un index temporaire est créé pour chaque champ spécifié dans la propriété **Sort** si aucun index n'existe déjà.</span><span class="sxs-lookup"><span data-stu-id="ba430-p102">This property requires the [CursorLocation](cursorlocation-property-ado.md) property to be set to **adUseClient**. A temporary index will be created for each field specified in the **Sort** property if an index does not already exist.</span></span>

<span data-ttu-id="ba430-119">L'opération de tri est d'une grande efficacité parce que les données ne sont pas réorganisées physiquement mais sont simplement lues dans l'ordre spécifié par l'index.</span><span class="sxs-lookup"><span data-stu-id="ba430-119">The sort operation is efficient because data is not physically rearranged, but is simply accessed in the order specified by the index.</span></span>

<span data-ttu-id="ba430-p103">Le fait de donner une chaîne vide comme valeur à la propriété **Sort** réinitialise les lignes dans leur ordre d'origine et supprime les index temporaires. Les index existants ne sont pas supprimés.</span><span class="sxs-lookup"><span data-stu-id="ba430-p103">Setting the **Sort** property to an empty string will reset the rows to their original order and delete temporary indexes. Existing indexes will not be deleted.</span></span>

<span data-ttu-id="ba430-122">Supposons qu’un **objet Recordset** contienne trois champs nommés *firstName*, *middleInitial*et *lastName*.</span><span class="sxs-lookup"><span data-stu-id="ba430-122">Suppose a **Recordset** contains three fields named *firstName*, *middleInitial*, and *lastName*.</span></span> <span data-ttu-id="ba430-123">Définissez la propriété de **tri** pour la chaîne « lastName DESC, firstName ASC », sera ordre dans lequel le **jeu d’enregistrements** par nom de famille en ordre décroissant, puis par prénom par ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="ba430-123">Set the **Sort** property to the string, "lastName DESC, firstName ASC", which will order the **Recordset** by last name in descending order, then by first name in ascending order.</span></span> <span data-ttu-id="ba430-124">Le deuxième prénom (middle initial) est ignoré.</span><span class="sxs-lookup"><span data-stu-id="ba430-124">The middle initial is ignored.</span></span>

<span data-ttu-id="ba430-p105">Les champs ne peuvent pas être nommés « ASC » ou « DESC » car ces noms génèrent des conflits avec les mots-clés **ASC** et **DESC**. Si le nom d'un champ génère un conflit, donnez-lui un alias en utilisant le mot-clé **AS** dans la requête qui renvoie le **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ba430-p105">No field can be named "ASC" or "DESC" because those names conflict with the keywords **ASC** and **DESC**. Give a field with a conflicting name an alias by using the **AS** keyword in the query that returns the **Recordset**.</span></span>

