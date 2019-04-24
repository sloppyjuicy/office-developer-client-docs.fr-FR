---
title: Recordset2. RecordCount, propriété (DAO)
TOCTitle: RecordCount Property
ms:assetid: 77852966-11e9-1773-6e58-53927b84c03b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196071(v=office.15)
ms:contentKeyID: 48545728
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052890
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c23de433f26b5a54b3fee5cc69f67a07b53f8a3b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309155"
---
# <a name="recordset2recordcount-property-dao"></a><span data-ttu-id="bb096-102">Recordset2. RecordCount, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="bb096-102">Recordset2.RecordCount property (DAO)</span></span>

<span data-ttu-id="bb096-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bb096-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bb096-p101">Renvoie le nombre d'enregistrements accédés dans un objet **[Recordset](recordset-object-dao.md)** ou le nombre total d'enregistrements dans un objet **Recordset** de type table ou un objet **[TableDef](tabledef-object-dao.md)**. Type **Long** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="bb096-p101">Returns the number of records accessed in a **[Recordset](recordset-object-dao.md)** object, or the total number of records in a table-type **Recordset** object. or **[TableDef](tabledef-object-dao.md)** object. Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb096-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb096-107">Syntax</span></span>

<span data-ttu-id="bb096-108">*expression* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="bb096-108">*expression* .RecordCount</span></span>

<span data-ttu-id="bb096-109">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="bb096-109">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb096-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="bb096-110">Remarks</span></span>

<span data-ttu-id="bb096-111">Utilisez la propriété **RecordCount** pour savoir à combien d’enregistrements dans un objet **Recordset** ou **TableDef** les utilisateurs ont accédé.</span><span class="sxs-lookup"><span data-stu-id="bb096-111">Use the **RecordCount** property to find out how many records in a **Recordset** or **TableDef** object have been accessed.</span></span> <span data-ttu-id="bb096-112">La propriété **RecordCount** n’indique pas le nombre d’enregistrements contenus dans un objet **Recordset** de type feuille de réponse dynamique, capture instantanée ou transfert uniquement avant que les utilisateurs aient accédé à tous les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="bb096-112">The **RecordCount** property doesn't indicate how many records are contained in a dynaset–, snapshot–, or forward–only–type **Recordset** object until all records have been accessed.</span></span> <span data-ttu-id="bb096-113">Après avoir accédé au dernier enregistrement, la propriété **RecordCount** indique le nombre total d'enregistrements non supprimés dans l'objet **Recordset** ou **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="bb096-113">Once the last record has been accessed, the **RecordCount** property indicates the total number of undeleted records in the **Recordset** or **TableDef** object.</span></span> <span data-ttu-id="bb096-114">Pour forcer l'accès au dernier enregistrement, appelez la méthode **[MoveLast](recordset2-movelast-method-dao.md)** sur l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="bb096-114">To force the last record to be accessed, use the **[MoveLast](recordset2-movelast-method-dao.md)** method on the **Recordset** object.</span></span> <span data-ttu-id="bb096-115">Vous pouvez également utiliser une fonction SQL **Count** pour déterminer le nombre approximatif d'enregistrements renvoyés par votre requête.</span><span class="sxs-lookup"><span data-stu-id="bb096-115">You can also use an SQL **Count** function to determine the approximate number of records your query will return.</span></span>

> [!NOTE]
> <span data-ttu-id="bb096-p103">[!REMARQUE] L'utilisation de la méthode **MoveLast** pour remplir un objet **Recordset** récemment ouvert affecte les performances. Sauf s'il est indispensable de connaître précisément la valeur de la propriété **RecordCount** dès l'ouverture d'un objet **Recordset**, il est préférable d'attendre que l'objet **Recordset** soit rempli avec d'autres sections de code avant de vérifier la valeur de la propriété **RecordCount**.</span><span class="sxs-lookup"><span data-stu-id="bb096-p103">Using the **MoveLast** method to populate a newly opened **Recordset** negatively impacts performance. Unless it is necessary to have an accurate **RecordCount** as soon as you open a **Recordset**, it's better to wait until you populate the **Recordset** with other portions of code before checking the **RecordCount** property.</span></span>

<span data-ttu-id="bb096-p104">À mesure que votre application supprime des enregistrements dans un objet **Recordset** de type feuille de réponse dynamique, la valeur de la propriété **RecordCount** diminue. Toutefois, les enregistrements supprimés par d'autres utilisateurs ne sont pas répercutés dans la propriété **RecordCount** tant que l'enregistrement actif est positionné sur un enregistrement supprimé. Si vous exécutez une transaction qui affecte la valeur de la propriété **RecordCount** et que vous annulez par la suite la transaction, la propriété **RecordCount** ne reflètera pas le nombre réel d'enregistrements restants.</span><span class="sxs-lookup"><span data-stu-id="bb096-p104">As your application deletes records in a dynaset-type **Recordset** object, the value of the **RecordCount** property decreases. However, records deleted by other users aren't reflected by the **RecordCount** property until the current record is positioned to a deleted record. If you execute a transaction that affects the **RecordCount** property setting and you subsequently roll back the transaction, the **RecordCount** property won't reflect the actual number of remaining records.</span></span>

<span data-ttu-id="bb096-121">La propriété **RecordCount** d’un objet **Recordset** de type capture instantanée ou transfert uniquement n’est pas concernée par les modifications apportées aux tables sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="bb096-121">The **RecordCount** property of a snapshot– or forward–only–type **Recordset** object isn't affected by changes in the underlying tables.</span></span>

<span data-ttu-id="bb096-122">Un objet **Recordset** ou **TableDef** sans enregistrement possède une propriété **RecordCount** égale à 0.</span><span class="sxs-lookup"><span data-stu-id="bb096-122">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="bb096-123">L'appel de la méthode **[Requery](recordset2-requery-method-dao.md)** sur un objet **Recordset** réinitialise la propriété **RecordCount** comme si la requête était réexécutée.</span><span class="sxs-lookup"><span data-stu-id="bb096-123">Using the **[Requery](recordset2-requery-method-dao.md)** method on a **Recordset** object resets the **RecordCount** property just as if the query were re-executed.</span></span>

## <a name="example"></a><span data-ttu-id="bb096-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="bb096-124">Example</span></span>

<span data-ttu-id="bb096-125">Cet exemple illustre la propriété **RecordCount** avec différents types de **Recordsets** avant et après leur remplissage.</span><span class="sxs-lookup"><span data-stu-id="bb096-125">This example demonstrates the **RecordCount** property with different types of **Recordsets** before and after they're populated.</span></span>

```vb
    Sub RecordCountX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Open table-type Recordset and show RecordCount 
     ' property. 
     Set rstEmployees = .OpenRecordset("Employees") 
     Debug.Print _ 
     "Table-type recordset from Employees table" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open dynaset-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open snapshot-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenSnapshot) 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open forward-only-type Recordset and show 
     ' RecordCount property before populating the 
     ' Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenForwardOnly) 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after calling the 
     ' MoveNext method. 
     rstEmployees.MoveNext 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table after MoveNext" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     .Close 
     End With 
     
    End Sub
```
