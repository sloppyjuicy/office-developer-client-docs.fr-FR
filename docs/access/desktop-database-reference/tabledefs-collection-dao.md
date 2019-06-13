---
title: TableDefs, collection (DAO)
TOCTitle: TableDefs Collection
ms:assetid: a2986b02-0437-d6ac-7bbb-c43f5225c3fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820997(v=office.15)
ms:contentKeyID: 48546766
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f16f44b57a690aa58efdff9b00341df5023c293f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314174"
---
# <a name="tabledefs-collection-dao"></a><span data-ttu-id="8f741-102">TableDefs, collection (DAO)</span><span class="sxs-lookup"><span data-stu-id="8f741-102">TableDefs Collection (DAO)</span></span>

<span data-ttu-id="8f741-103">**S’applique à** : Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8f741-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8f741-104">Une collection **TableDefs** contient tous les objets **TableDef** stockés dans une base de données (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="8f741-104">A **TableDefs** collection contains all stored **TableDef** objects in a database (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="8f741-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="8f741-105">Remarks</span></span>

<span data-ttu-id="8f741-106">Vous pouvez manipuler une définition de table à l’aide de l’objet **TableDef** et de ses méthodes et propriétés.</span><span class="sxs-lookup"><span data-stu-id="8f741-106">You manipulate a table definition using a **TableDef** object and its methods and properties.</span></span>

<span data-ttu-id="8f741-107">La collection par défaut d’un objet **Database** est la collection **TableDefs**.</span><span class="sxs-lookup"><span data-stu-id="8f741-107">The default collection of a **Database** object is the **TableDefs** collection.</span></span>

<span data-ttu-id="8f741-108">Pour faire référence à un objet **TableDef** dans une collection par son nombre ordinal ou par son paramètre de propriété **Name**, utilisez l’une des formes de syntaxe suivantes :</span><span class="sxs-lookup"><span data-stu-id="8f741-108">To refer to a **TableDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="8f741-109">**TableDefs**(0)</span><span class="sxs-lookup"><span data-stu-id="8f741-109">**TableDefs**(0)</span></span>

<span data-ttu-id="8f741-110">**TableDefs**("nom")</span><span class="sxs-lookup"><span data-stu-id="8f741-110">**TableDefs**("name")</span></span>

<span data-ttu-id="8f741-111">**TableDefs**\!\[nom\]</span><span class="sxs-lookup"><span data-stu-id="8f741-111">**TableDefs**\!\[name\]</span></span>

<span data-ttu-id="8f741-112">**Liens fournis par** la communauté [UtterAccess](https://www.utteraccess.com).</span><span class="sxs-lookup"><span data-stu-id="8f741-112">**Links provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="8f741-113">UtterAccess est le forum d’aide et wiki de Microsoft Access de référence.</span><span class="sxs-lookup"><span data-stu-id="8f741-113">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

  - [<span data-ttu-id="8f741-114">Ré-éditeur de liens, serveurs principaux multiples</span><span class="sxs-lookup"><span data-stu-id="8f741-114">Re-Linker Multi-Backends</span></span>](https://www.utteraccess.com/wiki/index.php/re-linker_multi-backends)

  - [<span data-ttu-id="8f741-115">Remplacer/recréer un lien entre les données en direct, de test et locales</span><span class="sxs-lookup"><span data-stu-id="8f741-115">Swap/Relink Between LIVE, TEST and LOCAL Data</span></span>](https://www.utteraccess.com/forum/swap-relink-live-test-t1328573.html)

## <a name="example"></a><span data-ttu-id="8f741-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="8f741-116">Example</span></span>

<span data-ttu-id="8f741-p102">Cet exemple crée un objet **TableDef** et l’ajoute à la collection **TableDefs** de l’objet de la base de données Northwind. Il énumère ensuite les collections **TableDefs** et **Properties** du nouvel objet **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="8f741-p102">This example creates a new **TableDef** object and appends it to the **TableDefs** collection of the Northwind Database object. It then enumerates the **TableDefs** collection and the **Properties** collection of the new **TableDef**.</span></span>

```vb
    Sub TableDefX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfNew As TableDef 
       Dim tdfLoop As TableDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new TableDef object, append Field objects  
       ' to its Fields collection, and append TableDef  
       ' object to the TableDefs collection of the  
       ' Database object. 
       Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
       tdfNew.Fields.Append tdfNew.CreateField("Date", dbDate) 
       dbsNorthwind.TableDefs.Append tdfNew 
     
       With dbsNorthwind 
          Debug.Print .TableDefs.Count & _ 
             " TableDefs in " & .Name 
     
          ' Enumerate TableDefs collection. 
          For Each tdfLoop In .TableDefs 
             Debug.Print "  " & tdfLoop.Name 
          Next tdfLoop 
     
          With tdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new 
             ' TableDef object, only printing properties 
             ' with non-empty values. 
             For Each prpLoop In .Properties 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          End With 
     
          ' Delete new TableDef since this is a  
          ' demonstration. 
          .TableDefs.Delete tdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="8f741-119">Cet exemple crée un objet **TableDef** dans la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="8f741-119">This example creates a new **TableDef** object in the Northwind database.</span></span>

```vb 
Sub CreateTableDefX() 
 
   Dim dbsNorthwind As Database 
   Dim tdfNew As TableDef 
   Dim prpLoop As Property 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
   ' Create a new TableDef object. 
   Set tdfNew = dbsNorthwind.CreateTableDef("Contacts") 
 
   With tdfNew 
      ' Create fields and append them to the new TableDef  
      ' object. This must be done before appending the  
      ' TableDef object to the TableDefs collection of the  
      ' Northwind database. 
      .Fields.Append .CreateField("FirstName", dbText) 
      .Fields.Append .CreateField("LastName", dbText) 
      .Fields.Append .CreateField("Phone", dbText) 
      .Fields.Append .CreateField("Notes", dbMemo) 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "before appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
      ' Append the new TableDef object to the Northwind  
      ' database. 
      dbsNorthwind.TableDefs.Append tdfNew 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "after appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
   End With 
 
   ' Delete new TableDef object since this is a  
   ' demonstration. 
   dbsNorthwind.TableDefs.Delete "Contacts" 
 
   dbsNorthwind.Close 
 
```



