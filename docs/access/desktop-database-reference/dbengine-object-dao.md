---
title: Objet DBEngine (DAO)
TOCTitle: DBEngine Object
ms:assetid: ceaeb505-615e-37ba-4633-27240ef8c5de
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834506(v=office.15)
ms:contentKeyID: 48547792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0d0ebafc885e02d0098c67bb55e56a1744557973
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923601"
---
# <a name="dbengine-object-dao"></a><span data-ttu-id="281ec-102">Objet DBEngine (DAO)</span><span class="sxs-lookup"><span data-stu-id="281ec-102">DBEngine object (DAO)</span></span>

<span data-ttu-id="281ec-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="281ec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="281ec-104">L'objet **DBEngine** est l'objet de niveau supérieur dans le modèle objet DAO.</span><span class="sxs-lookup"><span data-stu-id="281ec-104">The **DBEngine** object is the top level object in the DAO object model.</span></span>

## <a name="remarks"></a><span data-ttu-id="281ec-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="281ec-105">Remarks</span></span>

<span data-ttu-id="281ec-p101">L'objet **DBEngine** contient et contrôle tous les autres objets dans la hiérarchie des objets DAO. Vous ne pouvez pas créer d'autres objets **DBEngine** et l'objet **DBEngine** n'est pas un élément d'une collection.</span><span class="sxs-lookup"><span data-stu-id="281ec-p101">The **DBEngine** object contains and controls all other objects in the hierarchy of DAO objects. You can't create additional **DBEngine** objects, and the **DBEngine** object isn't an element of any collection.</span></span>

<span data-ttu-id="281ec-108">Avec tous les types de base de données ou de connexion, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="281ec-108">With any type of database or connection, you can:</span></span>

  - <span data-ttu-id="281ec-109">Utiliser la propriété **Version** pour obtenir le numéro de version DAO.</span><span class="sxs-lookup"><span data-stu-id="281ec-109">Use the **Version** property to obtain the DAO version number.</span></span>

  - <span data-ttu-id="281ec-110">Utiliser la propriété **LoginTimeout** pour obtenir ou définir le temps d'expiration de la connexion ODBC et la méthode **RegisterDatabase** pour fournir des informations ODBC au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="281ec-110">Use the **LoginTimeout** property to obtain or set the ODBC login timeout, and the **RegisterDatabase** method to provide ODBC information to the Microsoft Access database engine.</span></span>

  - <span data-ttu-id="281ec-111">Utiliser les propriétés **DefaultPassword** et **DefaultUser** pour définir l'identification et le mot de passe utilisateur pour l'objet **Workspace** par défaut.</span><span class="sxs-lookup"><span data-stu-id="281ec-111">Use the **DefaultPassword** and **DefaultUser** properties to set the user identification and password for the default **Workspace** object.</span></span>

  - <span data-ttu-id="281ec-p102">Utiliser la méthode **CreateWorkspace** pour créer un objet **Workspace**. Vous pouvez utiliser des arguments facultatifs pour remplacer les paramètres des propriétés **DefaultType**, **DefaultPassword** et **DefaultUser**.</span><span class="sxs-lookup"><span data-stu-id="281ec-p102">Use the **CreateWorkspace** method to create a new **Workspace** object. You can use optional arguments to override the settings of the **DefaultType**, **DefaultPassword**, and **DefaultUser** properties.</span></span>

  - <span data-ttu-id="281ec-114">Utiliser la méthode **OpenDatabase** pour ouvrir une base de données dans l'objet **Workspace** par défaut, et utiliser les méthodes **BeginTrans**, **Commit** et **Rollback** pour contrôler les transactions dans l'objet **Workspace** par défaut.</span><span class="sxs-lookup"><span data-stu-id="281ec-114">Use the **OpenDatabase** method to open a database in the default **Workspace**, and use the **BeginTrans**, **Commit**, and **Rollback** methods to control transactions on the default **Workspace**.</span></span>

  - <span data-ttu-id="281ec-115">Utiliser la collection **Workspaces** pour référencer des objets **Workspace** spécifiques.</span><span class="sxs-lookup"><span data-stu-id="281ec-115">Use the **Workspaces** collection to reference specific **Workspace** objects.</span></span>

  - <span data-ttu-id="281ec-116">Utiliser la collection **Errors** pour examiner les détails des erreurs d'accès aux données.</span><span class="sxs-lookup"><span data-stu-id="281ec-116">Use the **Errors** collection to examine data access error details.</span></span>

<span data-ttu-id="281ec-p103">D'autres propriétés et méthodes sont disponibles lorsque vous utilisez DAO avec le moteur de base de données Microsoft Access. Vous pouvez les utiliser pour contrôler le moteur de base de données Microsoft Access, manipuler ses propriétés, et effectuer des tâches sur des objets temporaires qui ne sont pas des éléments de collections. Par exemple, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="281ec-p103">Other properties and methods are only available when you use DAO with the Microsoft Access database engine. You can use them to control the Microsoft Access database engine, manipulate its properties, and perform tasks on temporary objects that aren't elements of collections. For example, you can:</span></span>

  - <span data-ttu-id="281ec-120">Utiliser la méthode **CreateDatabase** pour créer un objet **Database** de moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="281ec-120">Use the **CreateDatabase** method to create a new Microsoft Access database engine **Database** object.</span></span>

  - <span data-ttu-id="281ec-121">Utiliser la méthode **Idle** pour permettre au moteur de base de données Microsoft Access de terminer des tâches en attente.</span><span class="sxs-lookup"><span data-stu-id="281ec-121">Use the **Idle** method to enable the Microsoft Access database engine to complete any pending tasks.</span></span>

  - <span data-ttu-id="281ec-122">Utiliser les méthodes **CompactDatabase** et **RepairDatabase** pour effectuer la maintenance des fichiers de base de données.</span><span class="sxs-lookup"><span data-stu-id="281ec-122">Use the **CompactDatabase** and **RepairDatabase** methods to maintain database files.</span></span>

  - <span data-ttu-id="281ec-p104">Utiliser les propriétés **IniPath** et **SystemDB** pour spécifier respectivement l'emplacement des informations de registre Windows du moteur de base de données Microsoft Access et celui du fichier d'informations de groupe de travail Microsoft Access. La méthode **SetOption** permet de remplacer les paramètres du registre Windows pour le moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="281ec-p104">Use the **IniPath** and **SystemDB** properties to specify the location of Microsoft Access database engine Windows Registry information and the Microsoft Access workgroup information file, respectively. The **SetOption** method allows you override windows registry settings for the Microsoft Access database engine.</span></span>

<span data-ttu-id="281ec-125">Une fois que vous modifiez les paramètres des propriétés **DefaultType** et **IniPath**, seuls les objets **Workspace** suivants reflètent ces modifications.</span><span class="sxs-lookup"><span data-stu-id="281ec-125">After you change the **DefaultType** and **IniPath** property settings, only subsequent **Workspace** objects will reflect these changes.</span></span>

<span data-ttu-id="281ec-126">Pour renvoyer à une collection qui appartient à l'objet **DBEngine**, ou pour renvoyer à une méthode ou à une propriété qui s'applique à cet objet, utilisez cette syntaxe :</span><span class="sxs-lookup"><span data-stu-id="281ec-126">To refer to a collection that belongs to the **DBEngine** object, or to refer to a method or property that applies to this object, use this syntax:</span></span>

<span data-ttu-id="281ec-127">\[**DBEngine**. \] \[collection | méthode | propriété\]</span><span class="sxs-lookup"><span data-stu-id="281ec-127">\[**DBEngine**.\]\[collection | method | property\]</span></span>

## <a name="example"></a><span data-ttu-id="281ec-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="281ec-128">Example</span></span>

<span data-ttu-id="281ec-129">Cet exemple énumère les collections de l'objet **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="281ec-129">This example enumerates the collections of the **DBEngine** object.</span></span>

```vb
    Sub DBEngineX() 
     
     Dim wrkLoop As Workspace 
     Dim prpLoop As Property 
     
     With DBEngine 
     Debug.Print "DBEngine Properties" 
     
     ' Enumerate Properties collection of DBEngine, 
     ' trapping for properties whose values are 
     ' invalid in this context. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " = " _ 
     & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     Debug.Print "Workspaces collection of DBEngine" 
     
     ' Enumerate Workspaces collection of DBEngine. 
     For Each wrkLoop In .Workspaces 
     Debug.Print " " & wrkLoop.Name 
     
     ' Enumerate Properties collection of each 
     ' Workspace object, trapping for properties 
     ' whose values are invalid in this context. 
     For Each prpLoop In wrkLoop.Properties 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & _ 
     " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     Next wrkLoop 
     
     End With 
     
    End Sub
```
