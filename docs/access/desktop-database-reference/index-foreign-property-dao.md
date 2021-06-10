---
title: Index.Foreign, propriété (DAO)
TOCTitle: Foreign Property
ms:assetid: 81272436-a506-4b72-fd28-2d68e76d6d9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196489(v=office.15)
ms:contentKeyID: 48545943
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052974
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a3c6adfaf9648147a763f997ce2a91aadc4f7637
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291816"
---
# <a name="indexforeign-property-dao"></a><span data-ttu-id="fdafd-102">Index.Foreign, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="fdafd-102">Index.Foreign property (DAO)</span></span>

<span data-ttu-id="fdafd-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fdafd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fdafd-p101">Renvoie une valeur qui indique si un objet **[Index](index-object-dao.md)** représente une clé étrangère d'une table (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="fdafd-p101">Returns a value that indicates whether an **[Index](index-object-dao.md)** object represents a foreign key in a table (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="fdafd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fdafd-106">Syntax</span></span>

<span data-ttu-id="fdafd-107">*.* Étranger</span><span class="sxs-lookup"><span data-stu-id="fdafd-107">*expression* .Foreign</span></span>

<span data-ttu-id="fdafd-108">*expression* Variable qui représente un objet **Index.**</span><span class="sxs-lookup"><span data-stu-id="fdafd-108">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdafd-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="fdafd-109">Remarks</span></span>

<span data-ttu-id="fdafd-110">La valeur de retour est une donnée de type **Boolean** qui renvoie **True** si l'objet **Index** représente un clé étrangère.</span><span class="sxs-lookup"><span data-stu-id="fdafd-110">The return value is a **Boolean** data type that returns **True** if the **Index** object represents a foreign key.</span></span>

<span data-ttu-id="fdafd-111">Une clé étrangère consiste en un ou plusieurs champs d'une table étrangère qui identifient de manière unique toutes les lignes d'une table primaire.</span><span class="sxs-lookup"><span data-stu-id="fdafd-111">A foreign key consists of one or more fields in a foreign table that uniquely identify all rows in a primary table.</span></span>

<span data-ttu-id="fdafd-112">Le moteur de base de données Microsoft Access crée un objet **Index** pour la table étrangère et définit la propriété **Foreign** lorsque vous créez une relation qui impose l'intégrité référentielle.</span><span class="sxs-lookup"><span data-stu-id="fdafd-112">The Microsoft Access database engine creates an **Index** object for the foreign table and sets the **Foreign** property when you create a relationship that enforces referential integrity.</span></span>

## <a name="example"></a><span data-ttu-id="fdafd-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="fdafd-113">Example</span></span>

<span data-ttu-id="fdafd-p102">Cet exemple illustre comment la propriété **Foreign** permet d'identifier les objets **Index** d'une **TableDef** faisant office d'index de clé. Ces derniers sont créés par le moteur de base de données Microsoft Access lors de la création d'une **Relation**. Le nom par défaut des index de clés étrangères est le nom de la table primaire suivi de celui de la table étrangère. La fonction ForeignOutput est indispensable pour l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="fdafd-p102">This example shows how the **Foreign** property can indicate which **Index** objects in a **TableDef** are foreign key indexes. Such indexes are created by the Microsoft Access database engine when a **Relation** is created. The default name for the foreign key indexes is the name of the primary table plus the name of the foreign table. The ForeignOutput function is required for this procedure to run.</span></span>

```vb
    Sub ForeignX() 
     
     Dim dbsNorthwind As Database 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Print report on foreign key indexes from two 
     ' TableDef objects and a QueryDef object. 
     ForeignOutput .TableDefs!Products 
     ForeignOutput .TableDefs!Orders 
     ForeignOutput .TableDefs![Order Details] 
     
     .Close 
     End With 
     
    End Sub 
     
    Function ForeignOutput(tdfTemp As TableDef) 
     
     Dim idxLoop As Index 
     
     With tdfTemp 
     Debug.Print "Indexes in " & .Name & " TableDef" 
     ' Enumerate the Indexes collection of the specified 
     ' TableDef object. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Debug.Print " Foreign = " & idxLoop.Foreign 
     Next idxLoop 
     End With 
     
    End Function
```
