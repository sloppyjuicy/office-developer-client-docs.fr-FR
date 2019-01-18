---
title: Sort, propriété (ADO)
TOCTitle: Sort property (ADO)
ms:assetid: f2a39b7f-8b96-cd1a-8248-71f8b867454a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250230(v=office.15)
ms:contentKeyID: 48548652
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 62ac60b1c7575f0b0d3e003dc58a11fe4d86c131
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711412"
---
# <a name="sort-property-ado"></a><span data-ttu-id="f2ee2-102">Sort, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="f2ee2-102">Sort property (ADO)</span></span>


<span data-ttu-id="f2ee2-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2ee2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f2ee2-104">Indique un ou plusieurs noms de champs selon lesquels le [Recordset](recordset-object-ado.md) est trié ; indique en outre si les valeurs des champs sont triés en ordre croissant ou décroissant.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-104">Indicates one or more field names on which the [Recordset](recordset-object-ado.md) is sorted, and whether each field is sorted in ascending or descending order.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="f2ee2-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="f2ee2-105">Settings and return values</span></span>

<span data-ttu-id="f2ee2-p101">Définit ou renvoie une valeur **String** qui indique les noms des champs du **Recorset** selon lesquels le tri est réalisé. Les noms sont séparés par des virgules et éventuellement suivis d'un espace puis du mot clé **ASC** (si les valeurs du champ sont triées en ordre croissant) ou **DESC** (si les valeurs du champ sont triées en ordre décroissant). Si aucun mot clé n'est spécifié, les valeurs du champ sont par défaut triées en ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-p101">Sets or returns a **String** value that indicates the field names in the **Recordset** on which to sort. Each name is separated by a comma, and is optionally followed by a blank and the keyword, **ASC**, which sorts the field in ascending order, or **DESC**, which sorts the field in descending order. By default, if no keyword is specified, the field is sorted in ascending order.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2ee2-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="f2ee2-109">Remarks</span></span>

<span data-ttu-id="f2ee2-p102">Cette propriété exige que la propriété [CursorLocation](cursorlocation-property-ado.md) ait la valeur **adUseClient**. Un index temporaire est créé pour chaque champ spécifié dans la propriété **Sort** si aucun index n'existe déjà.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-p102">This property requires the [CursorLocation](cursorlocation-property-ado.md) property to be set to **adUseClient**. A temporary index will be created for each field specified in the **Sort** property if an index does not already exist.</span></span>

<span data-ttu-id="f2ee2-112">L'opération de tri est d'une grande efficacité parce que les données ne sont pas réorganisées physiquement mais sont simplement lues dans l'ordre spécifié par l'index.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-112">The sort operation is efficient because data is not physically rearranged, but is simply accessed in the order specified by the index.</span></span>

<span data-ttu-id="f2ee2-p103">Le fait de donner une chaîne vide comme valeur à la propriété **Sort** réinitialise les lignes dans leur ordre d'origine et supprime les index temporaires. Les index existants ne sont pas supprimés.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-p103">Setting the **Sort** property to an empty string will reset the rows to their original order and delete temporary indexes. Existing indexes will not be deleted.</span></span>

<span data-ttu-id="f2ee2-115">Supposons qu’un **objet Recordset** contienne trois champs nommés *firstName*, *middleInitial*et *lastName*.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-115">Suppose a **Recordset** contains three fields named *firstName*, *middleInitial*, and *lastName*.</span></span> <span data-ttu-id="f2ee2-116">Définissez la propriété de **tri** pour la chaîne « lastName DESC, firstName ASC », sera ordre dans lequel le **jeu d’enregistrements** par nom de famille en ordre décroissant, puis par prénom par ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-116">Set the **Sort** property to the string, "lastName DESC, firstName ASC", which will order the **Recordset** by last name in descending order, then by first name in ascending order.</span></span> <span data-ttu-id="f2ee2-117">Le deuxième prénom (middle initial) est ignoré.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-117">The middle initial is ignored.</span></span>

<span data-ttu-id="f2ee2-p105">Les champs ne peuvent pas être nommés « ASC » ou « DESC » car ces noms génèrent des conflits avec les mots-clés **ASC** et **DESC**. Si le nom d'un champ génère un conflit, donnez-lui un alias en utilisant le mot-clé **AS** dans la requête qui renvoie le **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f2ee2-p105">No field can be named "ASC" or "DESC" because those names conflict with the keywords **ASC** and **DESC**. Give a field with a conflicting name an alias by using the **AS** keyword in the query that returns the **Recordset**.</span></span>

