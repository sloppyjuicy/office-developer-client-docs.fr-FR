---
title: Properties Collection (DAO)
TOCTitle: Properties Collection
ms:assetid: cd07184a-a261-29c9-542f-bc2eff6f4af6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834455(v=office.15)
ms:contentKeyID: 48547753
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 45c36e12ab5d646e225690711d035ba8d36f4cc1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469733"
---
# <a name="properties-collection-dao"></a><span data-ttu-id="29bac-102">Properties Collection (DAO)</span><span class="sxs-lookup"><span data-stu-id="29bac-102">Properties Collection (DAO)</span></span>


<span data-ttu-id="29bac-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="29bac-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="29bac-104">Une collection **Properties** contient tous les objets **[Property](property-object-dao.md)** d'une instance spécifique d'un objet.</span><span class="sxs-lookup"><span data-stu-id="29bac-104">A **Properties** collection contains all the **[Property](property-object-dao.md)** objects for a specific instance of an object.</span></span>

## <a name="remarks"></a><span data-ttu-id="29bac-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="29bac-105">Remarks</span></span>

<span data-ttu-id="29bac-p101">Tous les objets DAO, à l'exception des objets **Connection** et **Error**, contiennent une collection **Properties**, laquelle est dotée d'un certain nombre d'objets **Property** intégrés. Ces objets **Property** (souvent appelés simplement propriétés) caractérisent de manière unique cette instance de l'objet.</span><span class="sxs-lookup"><span data-stu-id="29bac-p101">Every DAO object except the **Connection** and **Error** objects contains a **Properties** collection, which has certain built-in **Property** objects. These **Property** objects (which are often just called properties) uniquely characterize that instance of the object.</span></span>

<span data-ttu-id="29bac-p102">Outre les propriétés intégrées, vous pouvez également créer et ajouter vos propres propriétés. Pour ajouter une propriété personnalisée à une instance existante d'un objet, il convient d'abord d'en définir les caractéristiques à l'aide de la méthode **CreateProperty**, puis de l'ajouter à la collection à l'aide de la méthode **Append**. Le référencement d'un objet **Property** défini par l'utilisateur qui n'a pas encore été ajouté à une collection **Properties** entraîne une erreur. Tout comme l'ajout d'un objet **Property** défini par l'utilisateur à une collection **Properties** comptant déjà un objet **Property** avec le même nom.</span><span class="sxs-lookup"><span data-stu-id="29bac-p102">In addition to the built-in properties, you can also create and add your own user-defined properties. To add a user-defined property to an existing instance of an object, first define its characteristics with the **CreateProperty** method, then add it to the collection with the **Append** method. Referencing a user-defined **Property** object that has not yet been appended to a **Properties** collection will cause an error, as will appending a user-defined **Property** object to a **Properties** collection containing a **Property** object of the same name.</span></span>

<span data-ttu-id="29bac-111">Vous pouvez utiliser la méthode **Delete** pour supprimer des propriétés personnalisées de la collection **Properties** mais vous ne pouvez pas supprimer les propriétés intégrées.</span><span class="sxs-lookup"><span data-stu-id="29bac-111">You can use the **Delete** method to remove user-defined properties from the **Properties** collection, but you can't remove built-in properties.</span></span>


> [!NOTE]
> <P><span data-ttu-id="29bac-p103">[!REMARQUE] Un objet <STRONG>Property</STRONG> défini par l'utilisateur est associé uniquement à l'instance spécifique d'un objet. La propriété n'est pas définie pour toutes les instances d'objets du type sélectionné.</span><span class="sxs-lookup"><span data-stu-id="29bac-p103">A user-defined <STRONG>Property</STRONG> object is associated only with the specific instance of an object. The property isn't defined for all instances of objects of the selected type.</span></span></P>



<span data-ttu-id="29bac-114">Pour faire référence à un objet **Property** intégré d'une collection par son numéro ordinal ou par son paramètre de propriété **Name**, utilisez l'une des syntaxes suivantes :</span><span class="sxs-lookup"><span data-stu-id="29bac-114">To refer to a built-in **Property** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="29bac-115">objet. **Propriétés** (0)</span><span class="sxs-lookup"><span data-stu-id="29bac-115">object.**Properties**(0)</span></span>

<span data-ttu-id="29bac-116">objet. **Propriétés** (« nom »)</span><span class="sxs-lookup"><span data-stu-id="29bac-116">object.**Properties**("name")</span></span>

<span data-ttu-id="29bac-117">objet. **Propriétés** \! \[nom\]</span><span class="sxs-lookup"><span data-stu-id="29bac-117">object.**Properties**\!\[name\]</span></span>

<span data-ttu-id="29bac-118">Pour une propriété intégrée, vous pouvez également utiliser la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="29bac-118">For a built-in property, you can also use this syntax:</span></span>

<span data-ttu-id="29bac-119">objet.Name</span><span class="sxs-lookup"><span data-stu-id="29bac-119">object.name</span></span>


> [!NOTE]
> <P><span data-ttu-id="29bac-120">Pour une propriété définie par l’utilisateur, vous devez utiliser l’objet complet. <STRONG>Propriétés</STRONG> syntaxe (« nom »).</span><span class="sxs-lookup"><span data-stu-id="29bac-120">For a user-defined property, you must use the full object.<STRONG>Properties</STRONG>("name") syntax.</span></span></P>



<span data-ttu-id="29bac-p104">Avec les mêmes formes de syntaxe, vous pouvez également faire référence à la propriété **Value** d'un objet **Property**. Le contexte de la référence déterminera si vous faites référence à l'objet **Property** lui-même ou à la propriété **Value** de l'objet **Property**.</span><span class="sxs-lookup"><span data-stu-id="29bac-p104">With the same syntax forms, you can also refer to the **Value** property of a **Property** object. The context of the reference will determine whether you are referring to the **Property** object itself or the **Value** property of the **Property** object.</span></span>

## <a name="example"></a><span data-ttu-id="29bac-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="29bac-123">Example</span></span>

<span data-ttu-id="29bac-p105">Cet exemple crée une propriété définie par l'utilisateur pour la base de données active, définit ses propriétés **Type** et **Value** et l'ajoute à la collection **Properties** de la base de données. Il énumère ensuite toutes les propriétés de la base de données.</span><span class="sxs-lookup"><span data-stu-id="29bac-p105">This example creates a user-defined property for the current database, sets its **Type** and **Value** properties, and appends it to the **Properties** collection of the database. Then the example enumerates all properties in the database.</span></span>

```vb
    Sub PropertyX() 
     
     Dim dbsNorthwind As Database 
     Dim prpNew As Property 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Create and append user-defined property. 
     Set prpNew = .CreateProperty() 
     prpNew.Name = "UserDefined" 
     prpNew.Type = dbText 
     prpNew.Value = "This is a user-defined property." 
     .Properties.Append prpNew 
     
     ' Enumerate all properties of current database. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     With prpLoop 
     Debug.Print " " & .Name 
     Debug.Print " Type: " & .Type 
     Debug.Print " Value: " & .Value 
     Debug.Print " Inherited: " & _ 
     .Inherited 
     End With 
     Next prpLoop 
     
     ' Delete new property because this is a 
     ' demonstration. 
     .Properties.Delete "UserDefined" 
     End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="29bac-p106">Cet exemple tente de définir la valeur d'une propriété définie par l'utilisateur. Si la propriété n'existe pas, il utilise la méthode **CreateProperty** pour créer la nouvelle propriété et en définir la valeur. La procédure SetProperty est requise pour exécuter cette opération.</span><span class="sxs-lookup"><span data-stu-id="29bac-p106">This example tries to set the value of a user-defined property. If the property doesn't exist, it uses the **CreateProperty** method to create and set the value of the new property. The SetProperty procedure is required for this procedure to run.</span></span>

```vb
    Sub CreatePropertyX() 
     
     Dim dbsNorthwind As Database 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Set the Archive property to True. 
     SetProperty dbsNorthwind, "Archive", True 
     
     With dbsNorthwind 
     Debug.Print "Properties of " & .Name 
     
     ' Enumerate Properties collection of the Northwind 
     ' database. 
     For Each prpLoop In .Properties 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     Next prpLoop 
     
     ' Delete the new property since this is a 
     ' demonstration. 
     .Properties.Delete "Archive" 
     
     .Close 
     End With 
     
    End Sub 
     
    Sub SetProperty(dbsTemp As Database, strName As String, _ 
     booTemp As Boolean) 
     
     Dim prpNew As Property 
     Dim errLoop As Error 
     
     ' Attempt to set the specified property. 
     On Error GoTo Err_Property 
     dbsTemp.Properties("strName") = booTemp 
     On Error GoTo 0 
     
     Exit Sub 
     
    Err_Property: 
     
     ' Error 3270 means that the property was not found. 
     If DBEngine.Errors(0).Number = 3270 Then 
     ' Create property, set its value, and append it to the 
     ' Properties collection. 
     Set prpNew = dbsTemp.CreateProperty(strName, _ 
     dbBoolean, booTemp) 
     dbsTemp.Properties.Append prpNew 
     Resume Next 
     Else 
     ' If different error has occurred, display message. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & vbCr & _ 
     errLoop.Description 
     Next errLoop 
     End 
     End If 
     
    End Sub
```
