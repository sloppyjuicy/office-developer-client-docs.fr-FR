---
title: Fields, collection
TOCTitle: The Fields Collection
ms:assetid: 3bda8e5d-eceb-9605-c4d7-c1f4cc00ce6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249154(v=office.15)
ms:contentKeyID: 48544297
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ce08ac5952151471ce74afd9a8a49600d8e8f633
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705581"
---
# <a name="fields-collection"></a><span data-ttu-id="197ca-102">Fields, collection</span><span class="sxs-lookup"><span data-stu-id="197ca-102">Fields collection</span></span>


<span data-ttu-id="197ca-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="197ca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="197ca-p101">La collection **Fields** est une des collections intrinsèques d'ADO. Une collection est un ensemble hiérarchique d'éléments qui peuvent être référencés en tant qu'unité.</span><span class="sxs-lookup"><span data-stu-id="197ca-p101">The **Fields** collection is one of ADO's intrinsic collections. A collection is an ordered set of items that can be referred to as a unit.</span></span>

<span data-ttu-id="197ca-p102">La collection **Fields** contient un objet **Field** pour chaque champ (colonne) de l'objet **Recordset**. Comme toutes les collections ADO, elle possède les propriétés **Count** et **Item**, ainsi que les méthodes **Append** et **Refresh**. Notons également la présence des méthodes **CancelUpdate**, **Delete**, **Resync** et **Update**, non disponibles pour les autres collections ADO.</span><span class="sxs-lookup"><span data-stu-id="197ca-p102">The **Fields** collection contains a **Field** object for every field (column) in the **Recordset**. Like all ADO collections, it has **Count** and **Item** properties, as well as **Append** and **Refresh** methods. It also has **CancelUpdate**, **Delete**, **Resync**, and **Update** methods, which are not available to other ADO collections.</span></span>

## <a name="examining-the-fields-collection"></a><span data-ttu-id="197ca-109">Présentation de la collection Fields</span><span class="sxs-lookup"><span data-stu-id="197ca-109">Examining the Fields Collection</span></span>

<span data-ttu-id="197ca-110">Prendre en compte la collection **Fields** de l’exemple de **que jeu d’enregistrements** présenté dans ce chapitre.</span><span class="sxs-lookup"><span data-stu-id="197ca-110">Consider the **Fields** collection of the sample **Recordset** introduced in this chapter.</span></span> <span data-ttu-id="197ca-111">L’exemple de **que jeu d’enregistrements** a été dérivé de l’instruction SQL</span><span class="sxs-lookup"><span data-stu-id="197ca-111">The sample **Recordset** was derived from the SQL statement</span></span>

```sql 
 
SELECT ProductID, ProductName, UnitPrice FROM Products WHERE CategoryID = 7 
```

<span data-ttu-id="197ca-112">Nous constatons donc que la collection **Fields** de l'objet **Recordset** contient trois champs.</span><span class="sxs-lookup"><span data-stu-id="197ca-112">Thus, you should find that the **Recordset** **Fields** collection contains three fields.</span></span>

```vb 
 
'BeginWalkFields 
 Dim objFields As ADODB.Fields 
 
 objRs.Open strSQL, strConnStr, adOpenForwardOnly, adLockReadOnly, adCmdText 
 
 Set objFields = objRs.Fields 
 
 For intLoop = 0 To (objFields.Count - 1) 
 Debug.Print objFields.Item(intLoop).Name 
 Next 
'EndWalkFields 
```

<span data-ttu-id="197ca-p104">Ce code détermine simplement le nombre d'objets **Field** de la collection **Fields**, par l'intermédiaire de la propriété **Count**. Il parcourt la collection et renvoie la valeur de la propriété **Name** de chaque objet **Field**. Il existe bien d'autres propriétés **Field** qui permettent d'obtenir des informations concernant un champ. Pour plus d'informations sur les requêtes qu'il est possible d'exécuter sur un objet **Field**, consultez la rubrique [Field, objet](the-field-object.md).</span><span class="sxs-lookup"><span data-stu-id="197ca-p104">This code simply determines the number of **Field** objects in the **Fields** collection using the **Count** property and loops through the collection, returning the value of the **Name** property for each **Field** object. You can use many more **Field** properties to get information about a field. For more information about querying a **Field**, see [The Field Object](the-field-object.md).</span></span>

## <a name="counting-columns"></a><span data-ttu-id="197ca-116">Comptage des colonnes</span><span class="sxs-lookup"><span data-stu-id="197ca-116">Counting Columns</span></span>

<span data-ttu-id="197ca-p105">Assez logiquement, la propriété **Count** retourne le nombre réel d'objets **Field** compris dans la collection **Fields**. La numérotation des membres d'une collection commençant à zéro, vous devez toujours coder les boucles en commençant par le membre zéro et en terminant par la valeur de la propriété **Count** moins 1. Si vous utilisez Microsoft Visual Basic et souhaitez parcourir les éléments d'une collection sans vérifier la valeur de la propriété **Count**, utilisez la commande **For** **Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="197ca-p105">As you might expect, the **Count** property returns the actual number of **Field** objects in the **Fields** collection. Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the **Count** property minus 1. If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the **Count** property, use the **For** **Each...Next** command.</span></span>

<span data-ttu-id="197ca-120">Si la propriété **Count** a pour valeur zéro, cela signifie que la collection ne contient aucun objet.</span><span class="sxs-lookup"><span data-stu-id="197ca-120">If the **Count** property is zero, there are no objects in the collection.</span></span>

## <a name="getting-to-the-field"></a><span data-ttu-id="197ca-121">Accès à l'objet Field</span><span class="sxs-lookup"><span data-stu-id="197ca-121">Getting to the Field</span></span>

<span data-ttu-id="197ca-p106">Comme dans toute collection ADO, la propriété **Item** constitue la propriété par défaut de la collection. Elle retourne l'objet **Field** spécifié par le nom ou l'index qui lui est passé. Par conséquent, les instructions suivantes sont équivalentes pour l'exemple d'objet **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="197ca-p106">As with any ADO collection, the **Item** property is the default property of the collection. It returns the individual **Field** object specified by the name or index passed to it. Therefore, the following statements are equivalent for the sample **Recordset**:</span></span>

```vb 
 
objField = objRecordset.Fields.Item("ProductID") 
objField = objRecordset.Fields("ProductID") 
objField = objRecordset.Fields.Item(0) 
objField = objRecordset.Fields(0) 
```

<span data-ttu-id="197ca-p107">Si ces méthodes sont équivalentes, vous vous demandez laquelle choisir. Cela dépend. Le recours à un index pour extraire un objet **Field** d'une collection est plus rapide car cela permet d'accéder directement directement à l'objet **Field**, sans devoir effectuer une recherche de chaîne. En revanche, le nombre d'objets **Fields** de la collection doit être connu et, si l'ordre est modifié, la référence à l'index de l'objet **Field** doit être modifiée en conséquence. Bien que cette méthode soit plus lente, l'utilisation du nom de l'objet **Field** offre davantage de souplesse car elle ne dépend pas de l'ordre des objets **Fields** dans la collection.</span><span class="sxs-lookup"><span data-stu-id="197ca-p107">If these methods are equivalent, which is best? It depends. Using an index to retrieve a **Field** from the collection is faster because it accesses the **Field** directly without having to perform a string lookup. On the other hand, the order of **Fields** within the collection must be known, and if the order changes, the reference to the **Field's** index will have to be changed wherever it occurs. Although slightly slower, using the name of the **Field** is more flexible because it doesn't depend on the order of the **Fields** in the collection.</span></span>

## <a name="using-the-refresh-method"></a><span data-ttu-id="197ca-130">Utilisation de la méthode Refresh</span><span class="sxs-lookup"><span data-stu-id="197ca-130">Using the Refresh Method</span></span>

<span data-ttu-id="197ca-p108">Contrairement à ce qui se passe pour d'autres collections ADO, l'utilisation de la méthode **Refresh** de la collection **Fields** n'a pas d'effet visible. Pour récupérer les modifications de la structure de base de données sous-jacente, vous devez utiliser la méthode **Requery** ou, si l'objet **Recordset** ne prend pas en charge les signets, la méthode **MoveFirst**, qui provoquera une nouvelle exécution de la commande auprès du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="197ca-p108">Unlike some other ADO collections, using the **Refresh** method on the **Fields** collection has no visible effect. To retrieve changes from the underlying database structure, you must use either the **Requery** method, or if the **Recordset** object does not support bookmarks, the **MoveFirst** method, which will cause the command to be executed against the provider again.</span></span>

## <a name="adding-fields-to-a-recordset"></a><span data-ttu-id="197ca-133">Ajout de champs à un jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="197ca-133">Adding Fields to a Recordset</span></span>

<span data-ttu-id="197ca-134">La méthode **Append** permet d'ajouter des champs à un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="197ca-134">The **Append** method is used to add fields to a **Recordset**.</span></span>

<span data-ttu-id="197ca-p109">Vous pouvez utiliser la méthode **Append** pour créer un objet **Recordset** par programme, sans ouvrir de connexion à une source de données. Une erreur d'exécution se produit si la méthode **Append** est appelée sur la collection **Fields** d'un objet **Recordset** ouvert ou sur un objet **Recordset** dans lequel la propriété **ActiveConnection** est définie. Vous pouvez ajouter des champs à un objet **Recordset** uniquement lorsque celui-ci n'est pas ouvert et n'a pas encore été connecté à une source de données. Notez toutefois que, pour spécifier les valeurs de la collection **Fields** récemment ajoutée, l'objet **Recordset** doit être ouvert.</span><span class="sxs-lookup"><span data-stu-id="197ca-p109">You can use the **Append** method to fabricate a **Recordset** programmatically without opening a connection to a data source. A run-time error will occur if the **Append** method is called on the **Fields** collection of an open **Recordset** or on a **Recordset** where the **ActiveConnection** property has been set. You can append fields only to a **Recordset** that is not open and has not yet been connected to a data source. However, to specify values for the newly appended **Fields**, the **Recordset** must first be opened.</span></span>

<span data-ttu-id="197ca-p110">Les développeurs ont parfois besoin d'un emplacement de stockage temporaire pour certaines données, ou souhaitent que certaines données se comportent comme si elles provenaient d'un serveur, pour participer à la liaison des données dans une interface utilisateur. ADO (en association avec le [Service de curseur Microsoft pour OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md)) permet de construire un objet **Recordset** vide en spécifiant les informations de colonnes et en appelant la méthode **Open**. Dans l'exemple suivant, trois nouveaux champs sont ajoutés à un nouvel objet **Recordset**. Par la suite, l'objet **Recordset** est ouvert, deux nouveaux enregistrements sont ajoutés et l'objet **Recordset** est stocké de façon persistante dans un fichier. Pour plus d'informations sur la persistance des objets **Recordset**, consultez le [chapitre 5 : Mise à jour et persistance des données](chapter-5-updating-and-persisting-data.md).)</span><span class="sxs-lookup"><span data-stu-id="197ca-p110">Developers often need a place to temporarily store some data, or want some data to act as if it came from a server so it can participate in data binding in a user interface. ADO (in conjunction with the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md)) enables the developer to build an empty **Recordset** object by specifying column information and calling **Open**. In the following example, three new fields are appended to a new **Recordset** object. Then the **Recordset** is opened, two new records are added, and the **Recordset** is persisted to a file. (For more information about **Recordset** persistence, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).)</span></span>

```vb 
 
 'BeginFabricate 
 Dim objRs As New ADODB.Recordset 
 
 With objRs.Fields 
 .Append "StudentID", adChar, 11, adFldUpdatable 
 .Append "FullName", adVarChar, 50, adFldUpdatable 
 .Append "PhoneNmbr", adVarChar, 20, adFldUpdatable 
 End With 
 
 With objRs 
 .Open 
 
 .AddNew 
 .Fields(0) = "123-45-6789" 
 .Fields(1) = "John Doe" 
 .Fields(2) = "(425) 555-5555" 
 .Update 
 
 .AddNew 
 .Fields(0) = "123-45-6780" 
 .Fields(1) = "Jane Doe" 
 .Fields(2) = "(615) 555-1212" 
 .Update 
 End With 
 
 objRs.Save App.Path & "\FabriTest.adtg", adPersistADTG 
 
 objRs.Close 
 'EndFabricate 
```

<span data-ttu-id="197ca-p111">L'utilisation de la méthode **Append** de la collection **Fields** diffère selon qu'elle concerne un objet **Recordset** ou un objet **Record**. Pour plus d'informations sur les objets **Record**, consultez le [chapitre 10 : Enregistrements et flux](chapter-10-records-and-streams.md).</span><span class="sxs-lookup"><span data-stu-id="197ca-p111">The usage of the **Fields** **Append** method differs between the **Recordset** object and the **Record** object. For more information about the **Record** object, see [Chapter 10: Records and Streams](chapter-10-records-and-streams.md).</span></span>

