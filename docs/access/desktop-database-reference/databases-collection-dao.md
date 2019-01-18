---
title: Collection de bases de données (DAO)
TOCTitle: Databases Collection
ms:assetid: 988ae6f5-ec15-cd1c-191d-f295624425f4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197944(v=office.15)
ms:contentKeyID: 48546493
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dbaa0fe7aaa50c8aec582e2f03cd2849268816b9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715549"
---
# <a name="databases-collection-dao"></a><span data-ttu-id="1b822-102">Collection de bases de données (DAO)</span><span class="sxs-lookup"><span data-stu-id="1b822-102">Databases collection (DAO)</span></span>

<span data-ttu-id="1b822-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b822-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1b822-104">Une collection **Databases** contient tous les objets **Database** ouverts ou créés dans un objet **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="1b822-104">A **Databases** collection contains all open **Database** objects opened or created in a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b822-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="1b822-105">Remarks</span></span>

<span data-ttu-id="1b822-p101">Lorsque vous ouvrez un objet **Database** existant ou en créez un nouveau dans un objet **Workspace**, il est automatiquement ajouté à la collection **Databases**. Lorsque vous fermez un objet **Database** à l'aide de la méthode **[Close](connection-close-method-dao.md)**, il est supprimé de la collection **Databases** mais pas du disque. Il convient de fermer tous les objets **Recordset** ouverts avant de fermer un objet **Database**.</span><span class="sxs-lookup"><span data-stu-id="1b822-p101">When you open an existing **Database** object or create a new one from a **Workspace**, it is automatically appended to the **Databases** collection. When you close a **Database** object with the **[Close](connection-close-method-dao.md)** method, it is removed from the **Databases** collection but not deleted from disk. You should close all open **Recordset** objects before closing a **Database** object.</span></span>

<span data-ttu-id="1b822-109">Dans un espace de travail Microsoft Access, la propriété **Name** d'une base de données est une chaîne qui spécifie le chemin d'accès au fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="1b822-109">In a Microsoft Access workspace, the **Name** property setting of a database is a string that specifies the path of the database file.</span></span>

<span data-ttu-id="1b822-110">Pour faire référence à un objet **Database** d'une collection par son numéro ordinal ou par son paramètre de propriété **Name**, utilisez l'une des syntaxes suivantes :</span><span class="sxs-lookup"><span data-stu-id="1b822-110">To refer to a **Database** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="1b822-111">**Databases**(0)</span><span class="sxs-lookup"><span data-stu-id="1b822-111">**Databases**(0)</span></span>

- <span data-ttu-id="1b822-112">**Bases de données** («*nom*»)</span><span class="sxs-lookup"><span data-stu-id="1b822-112">**Databases**("*name*")</span></span>

- <span data-ttu-id="1b822-113">**Bases de données**\!\[*nom*\]</span><span class="sxs-lookup"><span data-stu-id="1b822-113">**Databases**\!\[*name*\]</span></span>

> [!NOTE]
> <span data-ttu-id="1b822-p102">[!REMARQUE] Vous pouvez ouvrir la même source ou base de données plusieurs fois, ce qui crée des noms dupliqués dans la collection **Databases**. Il convient d'affecter des objets **Database** aux variables d'objet et de s'y référer par nom de variables.</span><span class="sxs-lookup"><span data-stu-id="1b822-p102">You can open the same data source or database more than once, creating duplicate names in the **Databases** collection. You should assign **Database** objects to object variables and refer to them by variable name.</span></span>

## <a name="example"></a><span data-ttu-id="1b822-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="1b822-116">Example</span></span>

<span data-ttu-id="1b822-p103">Cet exemple crée un objet **Database** et ouvre un objet **Database** existant dans l'objet **Workspace** par défaut. Ensuite, il énumère la collection **Database** et la collection **Properties** de chaque objet **Database**.</span><span class="sxs-lookup"><span data-stu-id="1b822-p103">This example creates a new **Database** object and opens an existing **Database** object in the default **Workspace** object. Then it enumerates the **Database** collection and the **Properties** collection of each **Database** object.</span></span>

```vb 
Sub DatabaseObjectX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsNew As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 Set wrkAcc = CreateWorkspace("AccWorkspace", "admin", _ 
 "", dbUseJet) 
 
 ' Make sure there isn't already a file with the name of 
 ' the new database. 
 If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
 
 ' Create a new database with the specified 
 ' collating order. 
 Set dbsNew = wrkAcc.CreateDatabase("NewDB.mdb", _ 
 dbLangGeneral) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Enumerate the Databases collection. 
 For Each dbsLoop In wrkAcc.Databases 
 With dbsLoop 
 Debug.Print "Properties of " & .Name 
 ' Enumerate the Properties collection of each 
 ' Database object. 
 For Each prpLoop In .Properties 
 If prpLoop <> "" Then Debug.Print " " & _ 
 prpLoop.Name & " = " & prpLoop 
 Next prpLoop 
 End With 
 Next dbsLoop 
 
 dbsNew.Close 
 dbsNorthwind.Close 
 wrkAcc.Close 
 
End Sub 
 
```

<br/>

<span data-ttu-id="1b822-119">Cet exemple utilise **CreateDatabase** pour créer un objet **Database** chiffré.</span><span class="sxs-lookup"><span data-stu-id="1b822-119">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

```vb
    Sub CreateDatabaseX() 
     
     Dim wrkDefault As Workspace 
     Dim dbsNew As DATABASE 
     Dim prpLoop As Property 
     
     ' Get default Workspace. 
     Set wrkDefault = DBEngine.Workspaces(0) 
     
     ' Make sure there isn't already a file with the name of 
     ' the new database. 
     If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
     
     ' Create a new encrypted database with the specified 
     ' collating order. 
     Set dbsNew = wrkDefault.CreateDatabase("NewDB.mdb", _ 
     dbLangGeneral, dbEncrypt) 
     
     With dbsNew 
     Debug.Print "Properties of " & .Name 
     ' Enumerate the Properties collection of the new 
     ' Database object. 
     For Each prpLoop In .Properties 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     Next prpLoop 
     End With 
     
     dbsNew.Close 
     
    End Sub
```
