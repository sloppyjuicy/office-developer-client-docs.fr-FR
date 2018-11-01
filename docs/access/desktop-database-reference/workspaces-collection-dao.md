---
title: Workspaces Collection (DAO)
TOCTitle: Workspaces Collection
ms:assetid: 88b851ce-4180-964f-582e-bc9571bf554c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197057(v=office.15)
ms:contentKeyID: 48546142
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4108be7d6c1b2ee66ec5cddf4d26599796bf844c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870267"
---
# <a name="workspaces-collection-dao"></a><span data-ttu-id="5c508-102">Workspaces Collection (DAO)</span><span class="sxs-lookup"><span data-stu-id="5c508-102">Workspaces Collection (DAO)</span></span>


<span data-ttu-id="5c508-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5c508-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5c508-p101">Une collection **Workspaces** contient tous les objets **Workspace** actifs et non masqués de l'objet **DBEngine**. (Les objets **Workspace** masqués ne sont ni ajoutés à la collection ni référencés par la variable à laquelle ils sont affectés.)</span><span class="sxs-lookup"><span data-stu-id="5c508-p101">A **Workspaces** collection contains all active, unhidden **Workspace** objects of the **DBEngine** object. (Hidden **Workspace** objects are not appended to the collection and referenced by the variable to which they are assigned.)</span></span>

## <a name="remarks"></a><span data-ttu-id="5c508-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="5c508-106">Remarks</span></span>

<span data-ttu-id="5c508-107">L'objet **Workspace** permet de gérer la session active ou de démarrer une session supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="5c508-107">Use the **Workspace** object to manage the current session or to start an additional session.</span></span>

<span data-ttu-id="5c508-108">Lorsque vous consultez ou utilisez un objet **Workspace** , vous créez automatiquement l’espace de travail par défaut, DBEngine.Workspaces(0).</span><span class="sxs-lookup"><span data-stu-id="5c508-108">When you first refer to or use a **Workspace** object, you automatically create the default workspace, DBEngine.Workspaces(0).</span></span> <span data-ttu-id="5c508-109">Les paramètres des propriétés **Name** et **UserName** de l’espace de travail par défaut sont «\#espace de travail par défaut\#» et « Admin », respectivement.</span><span class="sxs-lookup"><span data-stu-id="5c508-109">The settings of the **Name** and **UserName** properties of the default workspace are "\#Default Workspace\#" and "Admin," respectively.</span></span> <span data-ttu-id="5c508-110">Si la sécurité est activée, le paramètre de propriété **UserName** correspond au nom de l'utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="5c508-110">If security is enabled, the **UserName** property setting is the name of the user who logged on.</span></span>

<span data-ttu-id="5c508-p103">Vous pouvez créer de nouveaux objets **Workspace** à l'aide de la méthode **[CreateWorkspace](dbengine-createworkspace-method-dao.md)**. Une fois le nouvel objet **Workspace** créé, vous devez l'ajouter à la collection **Workspaces** si vous devez vous y référer à partir de la collection. **Workspaces** Toutefois, vous pouvez utiliser un objet **Workspace** nouvellement créé sans l'ajouter à la collection **Workspaces**.</span><span class="sxs-lookup"><span data-stu-id="5c508-p103">You can create new **Workspace** objects with the **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** method. After you create a new **Workspace** object, you must append it to the **Workspaces** collection if you need to refer to it from the **Workspaces** collection. You can, however, use a newly created **Workspace** object without appending it to the **Workspaces** collection.</span></span>

<span data-ttu-id="5c508-114">Pour faire référence à un objet **Workspace** d'une collection par son numéro ordinal ou par son paramètre de propriété **Name**, utilisez l'une des syntaxes suivantes :</span><span class="sxs-lookup"><span data-stu-id="5c508-114">To refer to a **Workspace** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="5c508-115">**DBEngine**. **Espaces de travail** (0)</span><span class="sxs-lookup"><span data-stu-id="5c508-115">**DBEngine**.**Workspaces**(0)</span></span>

<span data-ttu-id="5c508-116">**DBEngine**. **Espaces de travail** (« nom »)</span><span class="sxs-lookup"><span data-stu-id="5c508-116">**DBEngine**.**Workspaces**("name")</span></span>

<span data-ttu-id="5c508-117">**DBEngine**. **Espaces de travail** \! \[nom\]</span><span class="sxs-lookup"><span data-stu-id="5c508-117">**DBEngine**.**Workspaces**\!\[name\]</span></span>


> [!NOTE]
> <span data-ttu-id="5c508-p104">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5c508-p104">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>



## <a name="example"></a><span data-ttu-id="5c508-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="5c508-120">Example</span></span>

<span data-ttu-id="5c508-p105">Cet exemple crée un nouvel objet Microsoft Access et l'ajoute aux collections **Workspaces**. Il énumère ensuite les collections **Workspaces** et la collection **Properties** de chaque objet **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="5c508-p105">This example creates a new Microsoft Access Workspace object and appends it to the **Workspaces** collection. It then enumerates the **Workspaces** collections and the **Properties** collection of the **Workspace** object.</span></span>

```vb 
Sub WorkspaceX() 
 
 Dim wrkNewAcc As Workspace 
 Dim wrkLoop As Workspace 
 Dim prpLoop As Property 
 
 ' Create a new Microsoft Access workspace. 
 Set wrkNewAcc = CreateWorkspace("NewAccessWorkspace", _ 
 "admin", "", dbUseJet) 
 Workspaces.Append wrkNewAcc 
 
 ' Enumerate the Workspaces collection. 
 For Each wrkLoop In Workspaces 
 With wrkLoop 
 Debug.Print "Properties of " & .Name 
 ' Enumerate the Properties collection of the new 
 ' Workspace object. 
 For Each prpLoop In .Properties 
 On Error Resume Next 
 If prpLoop <> "" Then Debug.Print " " & _ 
 prpLoop.Name & " = " & prpLoop 
 On Error GoTo 0 
 Next prpLoop 
 End With 
 Next wrkLoop 
 
 wrkNewAcc.Close 
End Sub 
```

<br/>

<span data-ttu-id="5c508-p106">Cet exemple utilise la méthode **CreateWorkspace** pour créer un espace de travail Microsoft Access. Il répertorie ensuite les propriétés de l'espace de travail.</span><span class="sxs-lookup"><span data-stu-id="5c508-p106">This example uses the **CreateWorkspace** method to create a Microsoft Access workspace. It then lists the properties of theworkspace.</span></span>

```vb 
Sub CreateWorkspaceX() 
 
 Dim wrkAcc As Workspace 
 Dim wrkLoop As Workspace 
 Dim prpLoop As Property 
 
 
 DefaultType = dbUseJet 
 ' Create an unnamed Workspace object of the type 
 ' specified by the DefaultType property of DBEngine 
 ' (dbUseJet). 
 Set wrkAcc = CreateWorkspace("", "admin", "") 
 
 ' Enumerate Workspaces collection. 
 Debug.Print "Workspace objects in Workspaces collection:" 
 For Each wrkLoop In Workspaces 
 Debug.Print " " & wrkLoop.Name 
 Next wrkLoop 
 
 With wrkAcc 
 ' Enumerate Properties collection of Microsoft Access 
 ' workspace. 
 Debug.Print _ 
 "Properties of unnamed Microsoft Access workspace" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 
 wrkAcc.Close 
 
End Sub 
 
```

