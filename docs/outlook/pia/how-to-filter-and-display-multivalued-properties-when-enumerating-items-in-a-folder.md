---
title: Filtrage et affichage des propriétés à valeurs multiples pendant l’énumération des éléments d’un dossier
TOCTitle: Filter and display multivalued properties when enumerating items in a folder
ms:assetid: 62dd2120-5c85-44b3-89ec-c4ca85aa2964
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184613(v=office.15)
ms:contentKeyID: 55119887
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d6242506bac081ee16d125ea92fbed69939c6abc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542624"
---
# <a name="filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder"></a><span data-ttu-id="98194-102">Filtrage et affichage des propriétés à valeurs multiples pendant l’énumération des éléments d’un dossier</span><span class="sxs-lookup"><span data-stu-id="98194-102">Filter and display multivalued properties when enumerating items in a folder</span></span>

<span data-ttu-id="98194-103">Cet exemple montre comment filtrer et afficher des propriétés à valeurs multiples pendant l’énumération d’éléments dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="98194-103">This example shows how to filter and display multivalued properties while enumerating items in a folder.</span></span>

## <a name="example"></a><span data-ttu-id="98194-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="98194-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="98194-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="98194-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="98194-p101">L'objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) représente un ensemble de données d'éléments issues d'un objet [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) ou [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) . Lorsqu'une propriété binaire, date ou à valeurs multiples est ajoutée en premier lieu à un objet **Table**, la façon de référencer cette propriété affecte son type et son format. Comme les références des noms intégrés retournent parfois une valeur de colonne différente par rapport à une référence à un espace de noms, vous devez déterminer si la propriété est référencée par son nom intégré explicite (s'il existe) ou par un espace de noms (indépendamment de l'existence d'un nom intégré explicite). Le tableau suivant montre la différence dans la représentation de la valeur d'une propriété (en termes de type et de format) selon le type de la propriété d'origine.</span><span class="sxs-lookup"><span data-stu-id="98194-p101">The [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object represents a set of item data from a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) or [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object. When a binary, date, or multivalued property is first added to a **Table** object, the way the property is referenced affects its type and format. Because built-in name references sometimes return a different column value than a namespace reference, you should determine whether the property is referenced by its explicit built-in name (if it has one), or by namespace (regardless of the existence of an explicit built-in name). The following table shows the difference in the property value representation (in terms of type and format) per original property type.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="98194-110">Type</span><span class="sxs-lookup"><span data-stu-id="98194-110">Type</span></span></p></th>
<th><p><span data-ttu-id="98194-111">Type en retour si la propriété spécifiée utilise un nom intégré</span><span class="sxs-lookup"><span data-stu-id="98194-111">Return type if the specified property uses a built-in name</span></span></p></th>
<th><p><span data-ttu-id="98194-112">Type de retour si la propriété spécifiée utilise un espace de noms</span><span class="sxs-lookup"><span data-stu-id="98194-112">Return type if the specified property uses a namespace</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98194-113">Binaire <b>(PT_BINARY)</b></span><span class="sxs-lookup"><span data-stu-id="98194-113">Binary <b>(PT_BINARY)</b></span></span></p></td>
<td><p><span data-ttu-id="98194-114">String</span><span class="sxs-lookup"><span data-stu-id="98194-114">String</span></span></p></td>
<td><p><span data-ttu-id="98194-115">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="98194-115">Byte array</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98194-116">Date <b>(PT_SYSTIME)</b></span><span class="sxs-lookup"><span data-stu-id="98194-116">Date <b>(PT_SYSTIME)</b></span></span></p></td>
<td><p><span data-ttu-id="98194-117">Local <b>DateTime</b></span><span class="sxs-lookup"><span data-stu-id="98194-117">Local <b>DateTime</b></span></span></p></td>
<td><p><span data-ttu-id="98194-118">UTC <b>DateTime</b></span><span class="sxs-lookup"><span data-stu-id="98194-118">UTC <b>DateTime</b></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98194-119">À valeurs multiples (également appelé type mot clé), comme la propriété <b>Categories</b> <b>(PT_MV_STRING8)</b></span><span class="sxs-lookup"><span data-stu-id="98194-119">Multivalued (also known as keyword type) such as <b>Categories</b> property <b>(PT_MV_STRING8)</b></span></span></p></td>
<td><p><span data-ttu-id="98194-120">Chaîne qui contient des valeurs séparées par des virgules</span><span class="sxs-lookup"><span data-stu-id="98194-120">String that contains comma-separated values</span></span></p></td>
<td><p><span data-ttu-id="98194-121">Tableau à une dimension qui contient un élément pour chaque mot clé</span><span class="sxs-lookup"><span data-stu-id="98194-121">One-dimensional array that contains one element for each keyword</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="98194-122">L'exemple de code suivant montre comment ajouter une propriété d'espace de noms de chaîne MAPI à l'objet **Table** et comment les propriétés à valeurs multiples affectent les valeurs retournées dans un objet [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="98194-122">The following code example illustrates how to add a MAPI string namespace property to the **Table** object and how multivalued properties affect the values returned in a [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) object.</span></span> <span data-ttu-id="98194-123">La procédure TableMultiValuedProperties filtre l’objet **Table** pour trouver les lignes où la propriété [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) n’est pas une référence null.</span><span class="sxs-lookup"><span data-stu-id="98194-123">The TableMultiValuedProperties procedure filters the **Table** object for rows where the [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) property is not a null reference.</span></span> <span data-ttu-id="98194-124">La propriété **Categories** est représentée par une propriété qui utilise l’espace de noms de la chaîne MAPI.</span><span class="sxs-lookup"><span data-stu-id="98194-124">The **Categories** property is represented by a property that uses the MAPI string namespace.</span></span> <span data-ttu-id="98194-125">Un filtre DASL est construit pour les éléments ayant des catégories (le filtre réel retourne les catégories n'ayant pas une référence null).</span><span class="sxs-lookup"><span data-stu-id="98194-125">A DAV Searching and Locating (DASL) filter is constructed for items that have categories (the actual filter returns categories that do not have a null reference).</span></span> <span data-ttu-id="98194-126">Une colonne **Categories** est ensuite ajoutée à l’objet **Table** en concaténant le spécificateur de type, 0000001f, avec la constante categoriesProperty.</span><span class="sxs-lookup"><span data-stu-id="98194-126">A **Categories** column is then added to the **Table** object by concatenating the type specifier, 0000001f, with the categoriesProperty constant.</span></span> <span data-ttu-id="98194-127">Enfin, l'objet **Column** qui représente la propriété **Categories** contient un tableau unidimensionnel de chaînes où chaque élément représente une catégorie assignée à l'élément.</span><span class="sxs-lookup"><span data-stu-id="98194-127">Finally, the **Column** object that represents the **Categories** property contains a one-dimensional string array where each element of the array represents a category assigned to the item.</span></span> <span data-ttu-id="98194-128">Les propriétés **Categories** et **Subject** de l’élément sont écrites sur les écouteurs de suivi de la collection [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="98194-128">Both the item’s **Categories** and **Subject** properties are written to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="98194-129">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="98194-129">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="98194-130">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="98194-130">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="98194-131">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="98194-131">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void TableMultiValuedProperties()
{
    const string categoriesProperty =
        "http://schemas.microsoft.com/mapi/string/"
        + "{00020329-0000-0000-C000-000000000046}/Keywords";
    // Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Call GetTable with filter for categories
    string filter = "@SQL="
        + "Not(" + "\"" + categoriesProperty
        + "\"" + " Is Null)";
    Outlook.Table table =
        folder.GetTable(filter,
        Outlook.OlTableContents.olUserItems);
    // Add categories column and append type specifier
    table.Columns.Add(categoriesProperty + "/0000001F");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        string[] categories =
            (string[])nextRow[categoriesProperty + "/0000001F"];
        Debug.WriteLine("Subject: " + nextRow["Subject"]);
        Debug.Write("Categories: ");
        foreach (string category in categories)
        {
            Debug.Write("\t" + category);
        }
        Debug.WriteLine("\n");
    }
}
```

## <a name="see-also"></a><span data-ttu-id="98194-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98194-132">See also</span></span>

- [<span data-ttu-id="98194-133">Rechercher et filtrer</span><span class="sxs-lookup"><span data-stu-id="98194-133">Search and filter</span></span>](search-and-filter.md)

