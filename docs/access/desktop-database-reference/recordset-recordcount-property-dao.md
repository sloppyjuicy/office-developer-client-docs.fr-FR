---
title: Propriété Recordset.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: aa1fed4f-ca51-918f-0a46-2b755b5f861a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821452(v=office.15)
ms:contentKeyID: 48546941
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ecaddcb30428b167811ab1eafcec149deb4da3ba
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891302"
---
# <a name="recordsetrecordcount-property-dao"></a><span data-ttu-id="b9834-102">Propriété Recordset.RecordCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="b9834-102">Recordset.RecordCount Property (DAO)</span></span>


<span data-ttu-id="b9834-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b9834-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b9834-p101">Renvoie le nombre d'enregistrements accédés dans un objet **[Recordset](recordset-object-dao.md)** ou le nombre total d'enregistrements dans un objet **Recordset** de type table ou un objet **[TableDef](tabledef-object-dao.md)**. Type **Long** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b9834-p101">Returns the number of records accessed in a **[Recordset](recordset-object-dao.md)** object, or the total number of records in a table-type **Recordset** object. or **[TableDef](tabledef-object-dao.md)** object. Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9834-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9834-107">Syntax</span></span>

<span data-ttu-id="b9834-108">*expression* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="b9834-108">*expression* .RecordCount</span></span>

<span data-ttu-id="b9834-109">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="b9834-109">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9834-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="b9834-110">Remarks</span></span>

<span data-ttu-id="b9834-111">Utilisez la propriété **RecordCount** pour déterminer le nombre d'enregistrements accédés dans un objet **Recordset** ou **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="b9834-111">Use the **RecordCount** property to find out how many records in a **Recordset** or **TableDef** object have been accessed.</span></span> <span data-ttu-id="b9834-112">La propriété **RecordCount** n’indique pas le nombre d’enregistrements contenu dans un objet **Recordset** de type avant uniquement, instantané ou feuille de réponse dynamique jusqu'à ce que tous les enregistrements ont accédé.</span><span class="sxs-lookup"><span data-stu-id="b9834-112">The **RecordCount** property doesn't indicate how many records are contained in a dynaset–, snapshot–, or forward–only–type **Recordset** object until all records have been accessed.</span></span> <span data-ttu-id="b9834-113">Après avoir accédé au dernier enregistrement, la propriété **RecordCount** indique le nombre total d'enregistrements non supprimés dans l'objet **Recordset** ou **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="b9834-113">Once the last record has been accessed, the **RecordCount** property indicates the total number of undeleted records in the **Recordset** or **TableDef** object.</span></span> <span data-ttu-id="b9834-114">Pour forcer l'accès au dernier enregistrement, appelez la méthode **[MoveLast](recordset-movelast-method-dao.md)** sur l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b9834-114">To force the last record to be accessed, use the **[MoveLast](recordset-movelast-method-dao.md)** method on the **Recordset** object.</span></span> <span data-ttu-id="b9834-115">Vous pouvez également utiliser une fonction SQL **Count** pour déterminer le nombre approximatif d'enregistrements renvoyés par votre requête.</span><span class="sxs-lookup"><span data-stu-id="b9834-115">You can also use an SQL **Count** function to determine the approximate number of records your query will return.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b9834-p103">[!REMARQUE] L'utilisation de la méthode <STRONG>MoveLast</STRONG> pour remplir un objet <STRONG>Recordset</STRONG> récemment ouvert affecte les performances. Sauf s'il est indispensable de connaître précisément la valeur de la propriété <STRONG>RecordCount</STRONG> dès l'ouverture d'un objet <STRONG>Recordset</STRONG>, il est préférable d'attendre que l'objet <STRONG>Recordset</STRONG> soit rempli avec d'autres sections de code avant de vérifier la valeur de la propriété <STRONG>RecordCount</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="b9834-p103">Using the <STRONG>MoveLast</STRONG> method to populate a newly opened <STRONG>Recordset</STRONG> negatively impacts performance. Unless it is necessary to have an accurate <STRONG>RecordCount</STRONG> as soon as you open a <STRONG>Recordset</STRONG>, it's better to wait until you populate the <STRONG>Recordset</STRONG> with other portions of code before checking the <STRONG>RecordCount</STRONG> property.</span></span></P>



<span data-ttu-id="b9834-p104">À mesure que votre application supprime des enregistrements dans un objet **Recordset** de type feuille de réponse dynamique, la valeur de la propriété **RecordCount** diminue. Toutefois, les enregistrements supprimés par d'autres utilisateurs ne sont pas répercutés dans la propriété **RecordCount** tant que l'enregistrement actif est positionné sur un enregistrement supprimé. Si vous exécutez une transaction qui affecte la valeur de la propriété **RecordCount** et que vous annulez par la suite la transaction, la propriété **RecordCount** ne reflètera pas le nombre réel d'enregistrements restants.</span><span class="sxs-lookup"><span data-stu-id="b9834-p104">As your application deletes records in a dynaset-type **Recordset** object, the value of the **RecordCount** property decreases. However, records deleted by other users aren't reflected by the **RecordCount** property until the current record is positioned to a deleted record. If you execute a transaction that affects the **RecordCount** property setting and you subsequently roll back the transaction, the **RecordCount** property won't reflect the actual number of remaining records.</span></span>

<span data-ttu-id="b9834-121">La propriété **RecordCount** d’un objet **Recordset** de type instantané ou avant uniquement n’est pas affectée par les modifications apportées aux tables sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="b9834-121">The **RecordCount** property of a snapshot– or forward–only–type **Recordset** object isn't affected by changes in the underlying tables.</span></span>

<span data-ttu-id="b9834-122">Un objet **Recordset** ou **TableDef** sans enregistrement possède une propriété **RecordCount** égale à 0.</span><span class="sxs-lookup"><span data-stu-id="b9834-122">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="b9834-123">L'appel de la méthode **[Requery](recordset-requery-method-dao.md)** sur un objet **Recordset** réinitialise la propriété **RecordCount** comme si la requête était réexécutée.</span><span class="sxs-lookup"><span data-stu-id="b9834-123">Using the **[Requery](recordset-requery-method-dao.md)** method on a **Recordset** object resets the **RecordCount** property just as if the query were re-executed.</span></span>

## <a name="example"></a><span data-ttu-id="b9834-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="b9834-124">Example</span></span>

<span data-ttu-id="b9834-125">Cet exemple illustre la propriété **RecordCount** avec différents types d'objets **Recordsets** avant et après qu'ils ont été remplis.</span><span class="sxs-lookup"><span data-stu-id="b9834-125">This example demonstrates the **RecordCount** property with different types of **Recordsets** before and after they're populated.</span></span>

```vb
    Sub RecordCountX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
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
