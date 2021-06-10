---
title: Container, objet (DAO)
TOCTitle: Container Object
ms:assetid: 22e487cd-e966-fe68-fff3-c680b460cbeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191764(v=office.15)
ms:contentKeyID: 48543720
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c9ebbeae35387f4fd59c39d4c20df6033edb06b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295631"
---
# <a name="container-object-dao"></a><span data-ttu-id="8025b-102">Container, objet (DAO)</span><span class="sxs-lookup"><span data-stu-id="8025b-102">Container object (DAO)</span></span>

<span data-ttu-id="8025b-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8025b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8025b-104">Un objet **Container** regroupe des types d'objets **Document** similaires.</span><span class="sxs-lookup"><span data-stu-id="8025b-104">A **Container** object groups similar types of **Document** objects together.</span></span>

## <a name="remarks"></a><span data-ttu-id="8025b-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="8025b-105">Remarks</span></span>

<span data-ttu-id="8025b-p101">Chaque objet **Database** comporte une collection **Containers** composée d'objets **Container** intégrés. Les applications peuvent définir leurs propres types de document et les conteneurs correspondants (bases de données de moteur de base de données Microsoft Access uniquement). Cependant, il peut arriver que ces objets ne soient pas toujours pris en charge dans DAO.</span><span class="sxs-lookup"><span data-stu-id="8025b-p101">Each **Database** object has a **Containers** collection consisting of built-in **Container** objects. Applications can define their own document types and corresponding containers (Microsoft Access database engine databases only); however, these objects may not always be supported through DAO.</span></span>

<span data-ttu-id="8025b-p102">Certains de ces objets **Container** sont définis par le moteur de base de données Microsoft Access alors que les autres peuvent définis par d'autres applications. Le tableau ci-dessous répertorie le nom de chaque objet **Container** défini par le moteur de base de données Microsoft Access et indique le type d'informations qu'ils contiennent.</span><span class="sxs-lookup"><span data-stu-id="8025b-p102">Some of these **Container** objects are defined by the Microsoft Access database engine while others may be defined by other applications. The following table lists the name of each **Container** object defined by the Microsoft Access database engine and what type of information it contains.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8025b-110">Nom du conteneur</span><span class="sxs-lookup"><span data-stu-id="8025b-110">Container name</span></span></p></th>
<th><p><span data-ttu-id="8025b-111">Contient des informations sur</span><span class="sxs-lookup"><span data-stu-id="8025b-111">Contains information about</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8025b-112">Databases</span><span class="sxs-lookup"><span data-stu-id="8025b-112">Databases</span></span></p></td>
<td><p><span data-ttu-id="8025b-113">Bases de données enregistrées</span><span class="sxs-lookup"><span data-stu-id="8025b-113">Saved databases</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8025b-114">Tables</span><span class="sxs-lookup"><span data-stu-id="8025b-114">Tables</span></span></p></td>
<td><p><span data-ttu-id="8025b-115">Tables et requêtes enregistrées</span><span class="sxs-lookup"><span data-stu-id="8025b-115">Saved tables and queries</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8025b-116">Relations</span><span class="sxs-lookup"><span data-stu-id="8025b-116">Relations</span></span></p></td>
<td><p><span data-ttu-id="8025b-117">Relations enregistrées</span><span class="sxs-lookup"><span data-stu-id="8025b-117">Saved relationships</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="8025b-p103">[!REMARQUE] Ne confondez pas les objets **Container** répertoriés dans le tableau précédent avec les collections du même nom. L'objet **Container** des bases de données renvoie à tous les objets de base de données enregistrés, mais la collection **Databases** renvoie uniquement aux objets de base de données ouverts dans un espace de travail déterminé.</span><span class="sxs-lookup"><span data-stu-id="8025b-p103">Don't confuse the **Container** objects listed in the preceding table with the collections of the same name. The Databases **Container** object refers to all saved database objects, but the **Databases** collection refers only to database objects that are open in a particular workspace.</span></span>

<span data-ttu-id="8025b-p104">Chaque objet **Container** comporte une collection **Documents** qui contient des objets **Document** qui décrivent les instances des objets intégrés du type spécifié par l'objet **Container**. Généralement, vous utilisez un objet **Container** comme liaison intermédiaire vers les informations dans l'objet **Document**. Vous pouvez également utiliser la collection **Containers** pour définir la sécurité de tous les objets **Document** d'un type déterminé.</span><span class="sxs-lookup"><span data-stu-id="8025b-p104">Each **Container** object has a **Documents** collection containing **Document** objects that describe instances of built-in objects of the type specified by the **Container**. You typically use a **Container** object as an intermediate link to the information in the **Document** object. You can also use the **Containers** collection to set security for all **Document** objects of a given type.</span></span>

<span data-ttu-id="8025b-123">Avec un objet **Container** existant, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="8025b-123">With an existing **Container** object, you can:</span></span>

- <span data-ttu-id="8025b-124">Utiliser la propriété **Name** pour renvoyer le nom prédéfini de l'objet **Container**.</span><span class="sxs-lookup"><span data-stu-id="8025b-124">Use the **Name** property to return the predefined name of the **Container** object.</span></span>

- <span data-ttu-id="8025b-p105">Utiliser la propriété **Owner** pour définir ou renvoyer le propriétaire de l'objet **Container**. Pour définir la propriété **Owner**, vous devez disposer de l'autorisation d'écrire pour l'objet **Container**, et vous devez définir la propriété sur le nom d'un objet **User** ou **Group** existant.</span><span class="sxs-lookup"><span data-stu-id="8025b-p105">Use the **Owner** property to set or return the owner of the **Container** object. To set the **Owner** property, you must have write permission for the **Container** object, and you must set the property to the name of an existing **User** or **Group** object.</span></span>

- <span data-ttu-id="8025b-127">Utiliser les propriétés **Permissions** et **UserName** pour définir les autorisations d'accès pour l'objet **Container**. Tout objet **Document** créé dans la collection **Documents** d'un objet **Container** hérite de ces paramètres d'autorisation d'accès.</span><span class="sxs-lookup"><span data-stu-id="8025b-127">Use the **Permissions** and **UserName** properties to set access permissions for the **Container** object; any **Document** object created in the **Documents** collection of a **Container** object inherits these access permission settings.</span></span>

<span data-ttu-id="8025b-128">Comme les objets **Container** sont intégrés, vous ne pouvez pas créer d'objets **Container** ou supprimer des objets Container existants.</span><span class="sxs-lookup"><span data-stu-id="8025b-128">Because **Container** objects are built-in, you can't create new **Container** objects or delete existing ones.</span></span>

<span data-ttu-id="8025b-129">Pour renvoyer à un objet **Container** dans une collection par son numéro ordinal ou par son paramètre de propriété **Name**, utilisez l'une des formes de syntaxe suivantes :</span><span class="sxs-lookup"><span data-stu-id="8025b-129">To refer to a **Container** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="8025b-130">**Conteneurs**(0)</span><span class="sxs-lookup"><span data-stu-id="8025b-130">**Containers**(0)</span></span>

- <span data-ttu-id="8025b-131">**Conteneurs**( »*nom*« )</span><span class="sxs-lookup"><span data-stu-id="8025b-131">**Containers**("*name*")</span></span>

- <span data-ttu-id="8025b-132"> \! Conteneurs \[ *name*\]</span><span class="sxs-lookup"><span data-stu-id="8025b-132">**Containers**\!\[*name*\]</span></span>

## <a name="example"></a><span data-ttu-id="8025b-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="8025b-133">Example</span></span>

<span data-ttu-id="8025b-134">Cet exemple énumère la collection **Containers** de la base de données Northwind et la collection **Properties** de chaque objet **Container** dans la collection.</span><span class="sxs-lookup"><span data-stu-id="8025b-134">This example enumerates the **Containers** collection of the Northwind database and the **Properties** collection of each **Container** object in the collection.</span></span>

```vb
    Sub ContainerObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim ctrLoop As Container 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     
     ' Enumerate Containers collection. 
     For Each ctrLoop In .Containers 
     Debug.Print "Properties of " & ctrLoop.Name _ 
     & " container" 
     
     ' Enumerate Properties collection of each 
     ' Container object. 
     For Each prpLoop In ctrLoop.Properties 
     Debug.Print " " & prpLoop.Name _ 
     & " = " prpLoop 
     Next prpLoop 
     
     Next ctrLoop 
     
     .Close 
     End With 
     
    End Sub
```
