---
title: Document Object (DAO)
TOCTitle: Document Object
ms:assetid: b51d4545-b157-4c7c-fdbe-16a25afffdb3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822082(v=office.15)
ms:contentKeyID: 48547247
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 27caa87aa250b0604c163b347bb5202e1c9b994b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880774"
---
# <a name="document-object-dao"></a><span data-ttu-id="4e062-102">Document Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="4e062-102">Document Object (DAO)</span></span>


<span data-ttu-id="4e062-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4e062-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4e062-p101">Un objet **Document** inclut des informations sur une instance d'un objet. L'objet peut être une base de données, une table enregistrée, une requête ou une relation (bases de données de moteur de base de données Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="4e062-p101">A **Document** object includes information about one instance of an object. The object can be a database, saved table, query, or relationship (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="4e062-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="4e062-106">Remarks</span></span>

<span data-ttu-id="4e062-p102">Chaque objet **Container** comporte une collection **Documents** qui contient des objets **Document** qui décrivent des instances d'objets intégrés du type spécifié par l'objet **Container**. Le tableau ci-dessous répertorie le type d'objet que chaque objet **Document** décrit, le nom de son objet **Container** et le type d'informations contenues dans l'objet **Document**.</span><span class="sxs-lookup"><span data-stu-id="4e062-p102">Each **Container** object has a **Documents** collection containing **Document** objects that describe instances of built-in objects of the type specified by the **Container**. The following table lists the type of object each **Document** describes, the name of its **Container** object, and what type of information **Document** contains.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4e062-109">Document</span><span class="sxs-lookup"><span data-stu-id="4e062-109">Document</span></span></p></th>
<th><p><span data-ttu-id="4e062-110">Conteneur</span><span class="sxs-lookup"><span data-stu-id="4e062-110">Container</span></span></p></th>
<th><p><span data-ttu-id="4e062-111">Contient des informations sur</span><span class="sxs-lookup"><span data-stu-id="4e062-111">Contains information about</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e062-112">Base de données</span><span class="sxs-lookup"><span data-stu-id="4e062-112">Database</span></span></p></td>
<td><p><span data-ttu-id="4e062-113">Bases de données</span><span class="sxs-lookup"><span data-stu-id="4e062-113">Databases</span></span></p></td>
<td><p><span data-ttu-id="4e062-114">Base de données enregistrée</span><span class="sxs-lookup"><span data-stu-id="4e062-114">Saved database</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e062-115">Table ou requête</span><span class="sxs-lookup"><span data-stu-id="4e062-115">Table or query</span></span></p></td>
<td><p><span data-ttu-id="4e062-116">Tables</span><span class="sxs-lookup"><span data-stu-id="4e062-116">Tables</span></span></p></td>
<td><p><span data-ttu-id="4e062-117">Table ou requête enregistrée</span><span class="sxs-lookup"><span data-stu-id="4e062-117">Saved table or query</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e062-118">Relation</span><span class="sxs-lookup"><span data-stu-id="4e062-118">Relationship</span></span></p></td>
<td><p><span data-ttu-id="4e062-119">Relations</span><span class="sxs-lookup"><span data-stu-id="4e062-119">Relations</span></span></p></td>
<td><p><span data-ttu-id="4e062-120">Relation enregistrée</span><span class="sxs-lookup"><span data-stu-id="4e062-120">Saved relationship</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="4e062-p103">[!REMARQUE] Ne confondez pas les objets **Container** répertoriés dans le tableau précédent avec les collections du même nom. L'objet **Container** des bases de données renvoie à tous les objets de base de données enregistrés, mais la collection **Databases** renvoie uniquement aux objets de base de données ouverts dans un espace de travail déterminé.</span><span class="sxs-lookup"><span data-stu-id="4e062-p103">Don't confuse the **Container** objects listed in the preceding table with the collections of the same name. The Databases **Container** object refers to all saved database objects, but the **Databases** collection refers only to database objects that are open in a particular workspace.</span></span>



<span data-ttu-id="4e062-123">Avec un objet **Document**, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="4e062-123">With a **Document** object, you can:</span></span>

  - <span data-ttu-id="4e062-124">Utiliser la propriété **Name** pour renvoyer le nom qu'un utilisateur ou le moteur de base de données Microsoft Access a donné à l'objet lorsqu'il a été créé.</span><span class="sxs-lookup"><span data-stu-id="4e062-124">Use the **Name** property to return the name that a user or the Microsoft Access database engine gave to the object when it was created.</span></span>

  - <span data-ttu-id="4e062-125">Utiliser la propriété **Container** pour renvoyer le nom de l'objet **Container** qui contient l'objet **Document**.</span><span class="sxs-lookup"><span data-stu-id="4e062-125">Use the **Container** property to return the name of the **Container** object that contains the **Document** object.</span></span>

  - <span data-ttu-id="4e062-p104">Utiliser la propriété **Owner** pour définir ou renvoyer le propriétaire de l'objet. Pour définir la propriété **Owner**, vous devez disposer de l'autorisation d'écrire pour l'objet **Document**, et vous devez définir la propriété sur le nom d'un objet **User** ou **Group** existant.</span><span class="sxs-lookup"><span data-stu-id="4e062-p104">Use the **Owner** property to set or return the owner of the object. To set the **Owner** property, you must have write permission for the **Document** object, and you must set the property to the name of an existing **User** or **Group** object.</span></span>

  - <span data-ttu-id="4e062-p105">Utiliser les propriétés **UserName** ou **Permissions** pour définir ou renvoyer les autorisations d'accès d'un utilisateur ou d'un groupe pour l'objet. Pour définir ces propriétés, vous devez disposer de l'autorisation d'écrire pour l'objet **Document**, et vous devez définir la propriété **UserName** sur le nom d'un objet **User** ou **Group** existant.</span><span class="sxs-lookup"><span data-stu-id="4e062-p105">Use the **UserName** or **Permissions** properties to set or return the access permissions of a user or group for the object. To set these properties, you must have write permission for the **Document** object, and you must set the **UserName** property to the name of an existing **User** or **Group** object.</span></span>

  - <span data-ttu-id="4e062-130">Utiliser les propriétés **DateCreated** et **LastUpdated** pour renvoyer la date et l'heure auxquelles l'objet **Document** a été créé et modifié pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="4e062-130">Use the **DateCreated** and **LastUpdated** properties to return the date and time when the **Document** object was created and last modified.</span></span>

<span data-ttu-id="4e062-p106">Dans la mesure où un objet **Document** correspond à un objet existant, vous ne pouvez pas créer d'objet **Document** ou supprimer des objets existants. Pour faire référence à un objet **Document** dans une collection par son numéro ordinal ou par son paramètre de propriété **Name**Name, utilisez l'une formes de syntaxe suivantes :</span><span class="sxs-lookup"><span data-stu-id="4e062-p106">Because a **Document** object corresponds to an existing object, you can't create new **Document** objects or delete existing ones. To refer to a **Document** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

  - <span data-ttu-id="4e062-133">**Documents**(0)</span><span class="sxs-lookup"><span data-stu-id="4e062-133">**Documents**(0)</span></span>

  - <span data-ttu-id="4e062-134">**Documents** («*nom*»)</span><span class="sxs-lookup"><span data-stu-id="4e062-134">**Documents**("*name*")</span></span>

  - <span data-ttu-id="4e062-135">**Documents**\!\[*nom*\]</span><span class="sxs-lookup"><span data-stu-id="4e062-135">**Documents**\!\[*name*\]</span></span>

## <a name="example"></a><span data-ttu-id="4e062-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="4e062-136">Example</span></span>

<span data-ttu-id="4e062-137">Cet exemple énumère la collection **Documents** du conteneur Tables, puis la collection **Properties** du premier objet **Document** de la collection.</span><span class="sxs-lookup"><span data-stu-id="4e062-137">This example enumerates the **Documents** collection of the Tables container, and then enumerates the **Properties** collection of the first **Document** object in the collection.</span></span>

```vb 
Sub DocumentX() 
 
 Dim dbsNorthwind As Database 
 Dim docLoop As Document 
 Dim prpLoop As Property 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind.Containers!Tables 
 Debug.Print "Documents in " & .Name & " container" 
 ' Enumerate the Documents collection of the Tables 
 ' container. 
 For Each docLoop In .Documents 
 Debug.Print " " & docLoop.Name 
 Next docLoop 
 With .Documents(0) 
 ' Enumerate the Properties collection of the first. 
 ' Document object of the Tables container. 
 Debug.Print "Properties of " & .Name & " document" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 End With 
 
 dbsNorthwind.Close 
 
End Sub 
 
```

<span data-ttu-id="4e062-138">Cet exemple utilise les propriétés **Owner** et **SystemDB** pour afficher les propriétaires de différents objets **Document**.</span><span class="sxs-lookup"><span data-stu-id="4e062-138">This example uses the **Owner** and **SystemDB** properties to show the owners of a variety of **Document** objects.</span></span>

```vb 
Sub OwnerX() 
 
 ' Ensure that the Microsoft Access workgroup file is 
 ' available. 
 DBEngine.SystemDB = "system.mdw" 
 
 Dim dbsNorthwind As Database 
 Dim ctrLoop As Container 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 Debug.Print "Document owners:" 
 ' Enumerate Containers collection and show the owner 
 ' of the first Document in each container's Documents 
 ' collection. 
 For Each ctrLoop In .Containers 
 With ctrLoop 
 Debug.Print " [" & .Documents(0).Name & _ 
 "] in [" & .Name & _ 
 "] container owned by [" & _ 
 .Documents(0).Owner & "]" 
 End With 
 Next ctrLoop 
 
 .Close 
 End With 
 
End Sub 
 
```

