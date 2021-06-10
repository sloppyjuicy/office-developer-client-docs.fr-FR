---
title: Recordset2.RecordCount, propriété (DAO)
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
# <a name="recordset2recordcount-property-dao"></a><span data-ttu-id="4eb18-102">Recordset2.RecordCount, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="4eb18-102">Recordset2.RecordCount property (DAO)</span></span>

<span data-ttu-id="4eb18-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4eb18-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4eb18-p101">Renvoie le nombre d'enregistrements accédés dans un objet **[Recordset](recordset-object-dao.md)** ou le nombre total d'enregistrements dans un objet **Recordset** de type table ou un objet **[TableDef](tabledef-object-dao.md)**. Type **Long** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="4eb18-p101">Returns the number of records accessed in a **[Recordset](recordset-object-dao.md)** object, or the total number of records in a table-type **Recordset** object. or **[TableDef](tabledef-object-dao.md)** object. Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eb18-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4eb18-107">Syntax</span></span>

<span data-ttu-id="4eb18-108">*expression* .RecordCount</span><span class="sxs-lookup"><span data-stu-id="4eb18-108">*expression* .RecordCount</span></span>

<span data-ttu-id="4eb18-109">*expression* Variable qui représente un **objet Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="4eb18-109">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4eb18-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="4eb18-110">Remarks</span></span>

<span data-ttu-id="4eb18-111">Utilisez le **RecordCount** propriété pour déterminer le nombre d’enregistrements dans une **jeu d’enregistrements** ou **TableDef** objet aient été accédé.</span><span class="sxs-lookup"><span data-stu-id="4eb18-111">Use the **RecordCount** property to find out how many records in a **Recordset** or **TableDef** object have been accessed.</span></span> <span data-ttu-id="4eb18-112">Le **RecordCount** propriété n’indique pas combien enregistrements sont contenus dans un type vers l’avant uniquement, instantané – ou feuille de réponse dynamique **jeu d’enregistrements** objet jusqu'à ce que tous les enregistrements ont été consultés.</span><span class="sxs-lookup"><span data-stu-id="4eb18-112">The **RecordCount** property doesn't indicate how many records are contained in a dynaset–, snapshot–, or forward–only–type **Recordset** object until all records have been accessed.</span></span> <span data-ttu-id="4eb18-113">Une fois le dernier enregistrement a été accédé, le **RecordCount** propriété indique le nombre total d’enregistrements non supprimés dans la **jeu d’enregistrements** ou **TableDef** objet.</span><span class="sxs-lookup"><span data-stu-id="4eb18-113">Once the last record has been accessed, the **RecordCount** property indicates the total number of undeleted records in the **Recordset** or **TableDef** object.</span></span> <span data-ttu-id="4eb18-114">Pour forcer le dernier enregistrement pour pouvoir y accéder, utilisez la **[MoveLast](recordset2-movelast-method-dao.md)** méthode sur le **jeu d’enregistrements** objet.</span><span class="sxs-lookup"><span data-stu-id="4eb18-114">To force the last record to be accessed, use the **[MoveLast](recordset2-movelast-method-dao.md)** method on the **Recordset** object.</span></span> <span data-ttu-id="4eb18-115">Vous pouvez également utiliser une SQL **Count** fonction pour déterminer le nombre d’enregistrements votre requête renverra approximatif.</span><span class="sxs-lookup"><span data-stu-id="4eb18-115">You can also use an SQL **Count** function to determine the approximate number of records your query will return.</span></span>

> [!NOTE]
> <span data-ttu-id="4eb18-p103">À l’aide de la **MoveLast** méthode pour renseigner nouvellement ouverte **jeu d’enregistrements** négatif affecte les performances. Sauf s’il est nécessaire de disposer d’un précises **RecordCount** dès que vous ouvrez un **jeu d’enregistrements**, il est préférable de Patientez jusqu'à ce que vous renseigner le **jeu d’enregistrements** avec d’autres certaines parties du code avant de les chercher la **RecordCount** propriété.</span><span class="sxs-lookup"><span data-stu-id="4eb18-p103">Using the **MoveLast** method to populate a newly opened **Recordset** negatively impacts performance. Unless it is necessary to have an accurate **RecordCount** as soon as you open a **Recordset**, it's better to wait until you populate the **Recordset** with other portions of code before checking the **RecordCount** property.</span></span>

<span data-ttu-id="4eb18-p104">Comme votre application supprime les enregistrements dans un type de feuille de réponse dynamique **jeu d’enregistrements** objet, la valeur de la **RecordCount** propriété diminue. Toutefois, les enregistrements supprimés par d’autres utilisateurs ne sont pas répercutées par le **RecordCount** propriété jusqu'à ce que l’enregistrement actif est positionné à un enregistrement supprimé. Si vous exécutez une transaction qui affecte la **RecordCount** paramètre de la propriété et vous lambda restaurez la transaction le **RecordCount** propriété ne reflète pas le nombre actuel de enregistrements restants.</span><span class="sxs-lookup"><span data-stu-id="4eb18-p104">As your application deletes records in a dynaset-type **Recordset** object, the value of the **RecordCount** property decreases. However, records deleted by other users aren't reflected by the **RecordCount** property until the current record is positioned to a deleted record. If you execute a transaction that affects the **RecordCount** property setting and you subsequently roll back the transaction, the **RecordCount** property won't reflect the actual number of remaining records.</span></span>

<span data-ttu-id="4eb18-121">Le **RecordCount** propriété d’un instantané – ou transférer – uniquement – type **jeu d’enregistrements** objet n’est pas affecté par les modifications apportées dans les tables sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="4eb18-121">The **RecordCount** property of a snapshot– or forward–only–type **Recordset** object isn't affected by changes in the underlying tables.</span></span>

<span data-ttu-id="4eb18-122">A **jeu d’enregistrements** ou **TableDef** de l’objet sans enregistrement contient un **RecordCount** paramètre de la propriété de 0.</span><span class="sxs-lookup"><span data-stu-id="4eb18-122">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="4eb18-123">À l’aide de la **[interroger à nouveau](recordset2-requery-method-dao.md)** méthode sur un **jeu d’enregistrements** objet réinitialisation le **RecordCount** propriété simplement comme si la requête nouveau exécutée.</span><span class="sxs-lookup"><span data-stu-id="4eb18-123">Using the **[Requery](recordset2-requery-method-dao.md)** method on a **Recordset** object resets the **RecordCount** property just as if the query were re-executed.</span></span>

## <a name="example"></a><span data-ttu-id="4eb18-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="4eb18-124">Example</span></span>

<span data-ttu-id="4eb18-125">Cet exemple illustre la **RecordCount** propriété avec différents types de **jeux d’enregistrements** qui précèdent et suivent qu’ils sont remplis.</span><span class="sxs-lookup"><span data-stu-id="4eb18-125">This example demonstrates the **RecordCount** property with different types of **Recordsets** before and after they're populated.</span></span>

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
