---
title: Propriété Recordset2.transactions (DAO)
TOCTitle: Transactions Property
ms:assetid: f2169565-f782-4089-0e4b-bc5d58d37db5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836614(v=office.15)
ms:contentKeyID: 48548642
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 85d6f1af274c342270660143d18f4706d74fcd66
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919786"
---
# <a name="recordset2transactions-property-dao"></a><span data-ttu-id="baa7d-102">Propriété Recordset2.transactions (DAO)</span><span class="sxs-lookup"><span data-stu-id="baa7d-102">Recordset2.Transactions property (DAO)</span></span>


<span data-ttu-id="baa7d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="baa7d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="baa7d-p101">Renvoie une valeur qui indique si un objet prend en charge les transactions. Valeur **Boolean** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="baa7d-p101">Returns a value that indicates whether an object supports transactions. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="baa7d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="baa7d-106">Syntax</span></span>

<span data-ttu-id="baa7d-107">*expression* . Transactions</span><span class="sxs-lookup"><span data-stu-id="baa7d-107">*expression* .Transactions</span></span>

<span data-ttu-id="baa7d-108">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="baa7d-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="baa7d-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="baa7d-109">Remarks</span></span>

<span data-ttu-id="baa7d-110">Dans un espace de travail Microsoft Access, vous pouvez également utiliser la propriété **Transactions** avec des objets **Recordset** de type table ou feuille de réponse dynamique.</span><span class="sxs-lookup"><span data-stu-id="baa7d-110">In a Microsoft Access workspace, you can also use the **Transactions** property with dynaset- or table-type **Recordset** objects.</span></span> <span data-ttu-id="baa7d-111">Objets **[Recordset](recordset-object-dao.md)** de type instantané et avant uniquement renvoient toujours **False**.</span><span class="sxs-lookup"><span data-stu-id="baa7d-111">Snapshot- and forward–only–type **[Recordset](recordset-object-dao.md)** objects always return **False**.</span></span>

<span data-ttu-id="baa7d-p103">Si un objet **Recordset** de type table ou feuille de réponse dynamique est basé sur une table de moteur de base de données Microsoft Access, la propriété **Transactions** a la valeur **True** et vous pouvez utiliser des transactions. Il se peut que d'autres moteurs de base de données ne prennent pas en charge les transactions. Ainsi, vous ne pouvez pas utiliser des transactions dans un objet **Recordset** de type feuille de réponse dynamique basé sur une table Paradox.</span><span class="sxs-lookup"><span data-stu-id="baa7d-p103">If a dynaset- or table-type **Recordset** is based on a Microsoft Access database engine table, the **Transactions** property is **True** and you can use transactions. Other database engines may not support transactions. For example, you can't use transactions in a dynaset-type **Recordset** object based on a Paradox table.</span></span>

<span data-ttu-id="baa7d-p104">Vérifiez la propriété **Transactions** avant d'utiliser la méthode **[BeginTrans](dbengine-begintrans-method-dao.md)** sur l'objet [**Workspace**](workspace-object-dao.md) de l'objet **Recordset** pour vous assurer que les transactions sont prises en charge. L'appel des méthodes **BeginTrans**, **CommitTrans** ou **Rollback** sur un objet non pris en charge n'a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="baa7d-p104">Check the **Transactions** property before using the **[BeginTrans](dbengine-begintrans-method-dao.md)** method on the **Recordset** object's **[Workspace](workspace-object-dao.md)** object to make sure that transactions are supported. Using the **BeginTrans**, **CommitTrans**, or **Rollback** methods on an unsupported object has no effect.</span></span>

## <a name="example"></a><span data-ttu-id="baa7d-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="baa7d-117">Example</span></span>

<span data-ttu-id="baa7d-118">Cet exemple illustre la propriété **Transactions** dans des espaces de travail Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="baa7d-118">This example demonstrates the **Transactions** property in Microsoft Access workspaces.</span></span>

```vb 
Sub TransactionsX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim conPubs As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Open two different Recordset objects and display the 
 ' Transactions property of each. 
 
 Debug.Print "Opening Microsoft Access table-type " & _ 
 "recordset..." 
 Set rstTemp = dbsNorthwind.OpenRecordset( _ 
 "Employees", dbOpenTable) 
 Debug.Print " Transactions = " & rstTemp.Transactions 
 
 Debug.Print "Opening forward-only-type " & _ 
 "recordset where the source is an SQL statement..." 
 Set rstTemp = dbsNorthwind.OpenRecordset( _ 
 "SELECT * FROM Employees", dbOpenForwardOnly) 
 Debug.Print " Transactions = " & rstTemp.Transactions 
 
 rstTemp.Close 
 dbsNorthwind.Close 
 conPubs.Close 
 wrkAcc.Close 
End Sub 
 
```

