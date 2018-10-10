---
title: Comptage des lignes (référence de base de données du bureau Access)
TOCTitle: Counting Rows
ms:assetid: ff684c5e-7f41-0dae-beea-f5c71f79bd84
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250312(v=office.15)
ms:contentKeyID: 48548963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 93a583ef0a8f0ef287835eebdd9d68cf726a19df
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471463"
---
# <a name="counting-rows"></a><span data-ttu-id="78bda-102">Comptage des lignes</span><span class="sxs-lookup"><span data-stu-id="78bda-102">Counting Rows</span></span>


<span data-ttu-id="78bda-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="78bda-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="78bda-p101">La propriété **RecordCount** renvoie une valeur de type **Long** qui indique le nombre d'enregistrements de l'objet **Recordset**. Utilisez la propriété **RecordCount** pour déterminer le nombre d'enregistrements d'un objet **Recordset**. La propriété renvoie -1 quand ADO ne peut pas déterminer le nombre d'enregistrements ou si le fournisseur ou le type de curseur ne prennent pas en charge la propriété **RecordCount**. Toute tentative de lecture de la propriété **RecordCount** sur un objet **Recordset** fermé génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="78bda-p101">The **RecordCount** property returns a **Long** value that indicates the number of records in the **Recordset**. Use the **RecordCount** property to find out how many records are in a **Recordset** object. The property returns -1 when ADO cannot determine the number of records or if the provider or cursor type does not support **RecordCount**. Reading the **RecordCount** property on a closed **Recordset** causes an error.</span></span>

<span data-ttu-id="78bda-p102">La propriété **RecordCount** dépend des fonctionnalités du fournisseur et du type de curseur. La propriété **RecordCount** retourne -1 pour un curseur avant uniquement, le nombre réel pour un curseur statique ou de type jeu de clés et enfin, soit -1, soit le nombre réel pour un curseur dynamique, selon la source de données.</span><span class="sxs-lookup"><span data-stu-id="78bda-p102">The **RecordCount** property depends on the capabilities of the provider and the type of cursor. The **RecordCount** property will return -1 for a forward-only cursor, the actual count for a static or keyset cursor, and either -1 or the actual count for a dynamic cursor, depending on the data source.</span></span>

<span data-ttu-id="78bda-110">L’exemple de **jeu d’enregistrements** est une nouveauté [d’Examen des données](chapter-3-examining-data.md) retourne – 1, car un curseur avant uniquement a été ouvert.</span><span class="sxs-lookup"><span data-stu-id="78bda-110">The sample **Recordset** introduced in [Examining Data](chapter-3-examining-data.md) would return –1 because a forward-only cursor was opened.</span></span> <span data-ttu-id="78bda-111">Pour pouvoir utiliser la propriété **RecordCount**, vous devez ouvrir l'objet **Recordset** avec un curseur plus élaboré (statique ou jeu de clés).</span><span class="sxs-lookup"><span data-stu-id="78bda-111">In order to use the **RecordCount** property, you would need to open the **Recordset** with a more sophisticated cursor (static or keyset).</span></span>

<span data-ttu-id="78bda-p104">Dans certains cas, le fournisseur ou le curseur ne peut fournir la valeur **RecordCount** qu'en procédant au préalable à une extraction de tous les enregistrements à partir de la source de données. Pour forcer ce type d'extraction, il est recommandé d'appeler la méthode **MoveLast** sur l'objet **Recordset** avant d'appeler **RecordCount**.</span><span class="sxs-lookup"><span data-stu-id="78bda-p104">In certain cases, your provider or cursor might be unable to provide the **RecordCount** value without first fetching all records from the data source. To force this type of fetch, call the **Recordset** **MoveLast** method before calling **RecordCount**.</span></span>

<span data-ttu-id="78bda-114">Si vous remplacez la ligne de code qui appelle la méthode **Open** sur l'objet **Recordset** par les éléments suivants,</span><span class="sxs-lookup"><span data-stu-id="78bda-114">If you were to replace the line of code that calls the **Recordset** **Open** method with the following:</span></span>

```vb 
 
oRs.Open sSQL, sCnStr, adOpenStatic, adLockOptimistic, adCmdText 
```

<span data-ttu-id="78bda-p105">vous pouvez utiliser la propriété **RecordCount** dans la mesure où les curseurs statiques et le [fournisseur Microsoft OLE DB pour SQL Server](microsoft-ole-db-provider-for-sql-server.md) prennent en charge la propriété **RecordCount**. À titre d'exemple, le code suivant imprime le nombre d'enregistrements retourné par la commande dans la fenêtre de débogage, en supposant que le curseur prend en charge la propriété **RecordCount**:</span><span class="sxs-lookup"><span data-stu-id="78bda-p105">you would be able to use the **RecordCount** property because static cursors with the [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md) support **RecordCount**. For example, the following code would print out the number of records returned by the command to the debug window, assuming the cursor supports the **RecordCount** property:</span></span>

```vb 
 
Debug.Print oRs.RecordCount ' Output: 4 
```

<span data-ttu-id="78bda-117">À ce stade, il est supposé que des paramètres de curseurs et verrous de ce type sont utilisés. En effet, ils offrent davantage de fonctionnalités même s'ils sont plus coûteux.</span><span class="sxs-lookup"><span data-stu-id="78bda-117">From this point forward, assume that these more capable (but more expensive) cursor and lock type settings are used.</span></span>

