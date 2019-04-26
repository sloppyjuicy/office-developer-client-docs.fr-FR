---
title: Objet Database (DAO)
TOCTitle: Database Object
ms:assetid: 6cf2ddf8-3957-a15e-5eeb-85f81c1e415e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195520(v=office.15)
ms:contentKeyID: 48545482
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm0
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: c23772c54f2f980b8d10d4afc352687935840752
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294836"
---
# <a name="database-object-dao"></a><span data-ttu-id="5a824-102">Objet Database (DAO)</span><span class="sxs-lookup"><span data-stu-id="5a824-102">Database Object (DAO)</span></span>

<span data-ttu-id="5a824-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5a824-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5a824-104">Un objet **Database** représente une base de données ouverte.</span><span class="sxs-lookup"><span data-stu-id="5a824-104">A **Database** object represents an open database.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a824-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="5a824-105">Remarks</span></span>

<span data-ttu-id="5a824-p101">L’objet **Database**, ainsi que ses méthodes et propriétés, permet de manipuler une base de données ouverte. Dans tous les types de base de données, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="5a824-p101">You use the **Database** object and its methods and properties to manipulate an open database. In any type of database, you can:</span></span>

  - <span data-ttu-id="5a824-108">Utiliser la méthode **Execute** pour exécuter une requête d’action.</span><span class="sxs-lookup"><span data-stu-id="5a824-108">Use the **Execute** method to run an action query.</span></span>

  - <span data-ttu-id="5a824-109">Définir la propriété **Connect** pour établir une connexion avec une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="5a824-109">Set the **Connect** property to establish a connection to an ODBC data source.</span></span>

  - <span data-ttu-id="5a824-110">Définir la propriété **QueryTimeout** pour limiter le temps d’attente pour l’exécution d’une requête dans une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="5a824-110">Set the **QueryTimeout** property to limit the length of time to wait for a query to execute against an ODBC data source.</span></span>

  - <span data-ttu-id="5a824-111">Utiliser la propriété **RecordsAffected** pour déterminer le nombre d’enregistrements qui ont été modifiés par une requête Action.</span><span class="sxs-lookup"><span data-stu-id="5a824-111">Use the **RecordsAffected** property to determine how many records were changed by an action query.</span></span>

  - <span data-ttu-id="5a824-112">Utiliser la méthode **OpenRecordset** pour exécuter une requête Select et créer un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="5a824-112">Use the **OpenRecordset** method to execute a select query and create a **Recordset** object.</span></span>

  - <span data-ttu-id="5a824-113">Utiliser la propriété **Version** pour déterminer la version de moteur de base de données qui a créé la base de données.</span><span class="sxs-lookup"><span data-stu-id="5a824-113">Use the **Version** property to determine which version of a database engine created the database.</span></span>

<span data-ttu-id="5a824-p102">Avec une base de données de moteur de base de données Microsoft Access, vous pouvez également utiliser d’autres méthodes, propriétés et collections pour manipuler un objet **Database**, mais aussi créer, modifier ou obtenir des informations se rapportant à ses tables, requêtes et relations. Par exemple, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="5a824-p102">With a Microsoft Access database engine database, you can also use other methods, properties, and collections to manipulate a **Database** object, as well as create, modify, or get information about its tables, queries, and relationships. For example, you can:</span></span>

  - <span data-ttu-id="5a824-116">Utiliser les méthodes **CreateTableDef** et **CreateRelation** pour créer respectivement des tables et des relations.</span><span class="sxs-lookup"><span data-stu-id="5a824-116">Use the **CreateTableDef** and **CreateRelation** methods to create tables and relations, respectively.</span></span>

  - <span data-ttu-id="5a824-117">Utiliser la méthode **CreateProperty** pour définir de nouvelles propriétés **Database**.</span><span class="sxs-lookup"><span data-stu-id="5a824-117">Use the **CreateProperty** method to define new **Database** properties.</span></span>

  - <span data-ttu-id="5a824-118">Utiliser la méthode **CreateQueryDef** pour créer une définition de requête persistante ou temporaire.</span><span class="sxs-lookup"><span data-stu-id="5a824-118">Use the **CreateQueryDef** method to create a persistent or temporary query definition.</span></span>

  - <span data-ttu-id="5a824-119">Utiliser les méthodes **MakeReplica**, **Synchronize** et **PopulatePartial** pour créer et synchroniser des réplicas partiels ou complets de votre base de données.</span><span class="sxs-lookup"><span data-stu-id="5a824-119">Use **MakeReplica**, **Synchronize**, and **PopulatePartial** methods to create and synchronize full or partial replicas of your database.</span></span>

  - <span data-ttu-id="5a824-120">Définir la propriété **CollatingOrder** pour définir l’ordre de tri alphabétique des champs de caractères dans différentes langues.</span><span class="sxs-lookup"><span data-stu-id="5a824-120">Set the **CollatingOrder** property to establish the alphabetic sorting order for character-based fields in different languages.</span></span>

<span data-ttu-id="5a824-121">Vous utilisez la méthode **CreateDatabase** pour créer un objet **Database** persistant, qui est automatiquement ajouté à la collection **Databases**, et donc pour l’enregistrer sur le disque.</span><span class="sxs-lookup"><span data-stu-id="5a824-121">You use the **CreateDatabase** method to create a persistent **Database** object that is automatically appended to the **Databases** collection, thereby saving it to disk.</span></span>

<span data-ttu-id="5a824-122">Vous n’avez pas besoin de spécifier l’objet **DBEngine** lorsque vous utilisez la méthode **OpenDatabase**.</span><span class="sxs-lookup"><span data-stu-id="5a824-122">You don't need to specify the **DBEngine** object when you use the **OpenDatabase** method.</span></span>

<span data-ttu-id="5a824-p103">L’ouverture d’une base de données avec des tables liées ne définit pas automatiquement des liaisons vers les fichiers externes spécifiés. Vous devez référencer les objets **TableDef** ou **Field** de la table, ou ouvrir un objet **Recordset**. Si vous ne pouvez pas définir de liaisons vers ces tables, une erreur pouvant être interceptée se produit.</span><span class="sxs-lookup"><span data-stu-id="5a824-p103">Opening a database with linked tables doesn't automatically establish links to the specified external files. You must either reference the table's **TableDef** or **Field** objects or open a **Recordset** object. If you can't establish links to these tables, a trappable error occurs. You may also need permission to access the database, or another user might have the database opened exclusively. In these cases, trappable errors occur.</span></span>

<span data-ttu-id="5a824-p104">Lorsqu’une procédure qui déclare un objet **Database** a été exécutée, les objets **Database** locaux sont fermés avec les objets **Recordset** ouverts. Toutes les mises à jour en attente sont perdues et les transactions en attente sont annulées, mais aucune erreur pouvant être interceptée ne se produit. Vous devez terminer explicitement les transactions en attente ou modifier et fermer les objets **Recordset** et **Database** avant de quitter les procédures qui déclarent ces variables d’objet localement.</span><span class="sxs-lookup"><span data-stu-id="5a824-p104">When a procedure that declares a **Database** object has executed, local **Database** objects are closed along with any open **Recordset** objects. Any pending updates are lost and any pending transactions are rolled back, but no trappable error occurs. You should explicitly complete any pending transactions or edits and close **Recordset** objects and **Database** objects before exiting procedures that declare these object variables locally.</span></span>

<span data-ttu-id="5a824-p105">Lorsque vous utilisez l’une des méthodes de transaction (**BeginTrans**, **CommitTrans** ou **Rollback**) dans l’objet **Workspace**, ces transactions s’appliquent à toutes les bases de données ouvertes dans l’objet **Workspace** dans lequel l’objet **Database** a été ouvert. Si vous souhaitez utiliser des transactions indépendantes, vous devez d’abord ouvrir un autre objet **Workspace**, puis ouvrir un autre objet **Database** dans cet objet **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="5a824-p105">When you use one of the transaction methods (**BeginTrans**, **CommitTrans**, or **Rollback**) on the **Workspace** object, these transactions apply to all databases opened on the **Workspace** from which the **Database** object was opened. If you want to use independent transactions, you must first open an additional **Workspace** object, and then open another **Database** object in that **Workspace** object.</span></span>


> [!NOTE]
> <span data-ttu-id="5a824-p106">Vous pouvez ouvrir la même source de données ou la même base de données plusieurs fois, en créant des noms dupliqués dans la collection **Databases**. Vous devez affecter des objets **Database** à des variables d’objet et les désigner par nom de variable.</span><span class="sxs-lookup"><span data-stu-id="5a824-p106">You can open the same data source or database more than once, creating duplicate names in the **Databases** collection. You should assign **Database** objects to object variables and refer to them by variable name.</span></span>



## <a name="example"></a><span data-ttu-id="5a824-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="5a824-135">Example</span></span>

<span data-ttu-id="5a824-p107">Cet exemple crée un objet **Database** et ouvre un objet **Database** existant dans l’objet **Workspace** par défaut. Ensuite, il énumère la collection **Database** et la collection **Properties** de chaque objet **Database**.</span><span class="sxs-lookup"><span data-stu-id="5a824-p107">This example creates a new **Database** object and opens an existing **Database** object in the default **Workspace** object. Then it enumerates the **Database** collection and the **Properties** collection of each **Database** object.</span></span>

```vb 
Sub DatabaseObjectX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsNew As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 Set wrkAcc = CreateWorkspace("AccessWorkspace", "admin", _ 
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

<span data-ttu-id="5a824-138">Cet exemple utilise **CreateDatabase** pour créer un objet **Database** chiffré.</span><span class="sxs-lookup"><span data-stu-id="5a824-138">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

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
