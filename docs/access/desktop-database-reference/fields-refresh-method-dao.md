---
title: Fields.Refresh, méthode (DAO)
TOCTitle: Refresh Method
ms:assetid: d08597d8-bad6-523b-a083-d824f85b64bc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834723(v=office.15)
ms:contentKeyID: 48547844
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 09218fae470646ab04ecfb5427004e56183e46ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292509"
---
# <a name="fieldsrefresh-method-dao"></a><span data-ttu-id="39eb9-102">Fields.Refresh, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="39eb9-102">Fields.Refresh method (DAO)</span></span>


<span data-ttu-id="39eb9-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="39eb9-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="39eb9-104">Met à jour les objets dans la collection spécifiée pour refléter le schéma actuel de la base de données.</span><span class="sxs-lookup"><span data-stu-id="39eb9-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="39eb9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39eb9-105">Syntax</span></span>

<span data-ttu-id="39eb9-106">*.* Actualiser</span><span class="sxs-lookup"><span data-stu-id="39eb9-106">*expression* .Refresh</span></span>

<span data-ttu-id="39eb9-107">*expression* Variable qui représente un objet **Fields**.</span><span class="sxs-lookup"><span data-stu-id="39eb9-107">*expression* A variable that represents a **Fields** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="39eb9-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="39eb9-108">Remarks</span></span>

<span data-ttu-id="39eb9-p101">Pour déterminer la position utilisée par le moteur de base de données Microsoft Access pour les objets **Field** dans la collection **Fields** d'un objet **QueryDef**, **Recordset** ou **TableDef**, utilisez la propriété **OrdinalPosition** de chaque objet **Field**. La modification de la propriété **OrdinalPosition** d'un objet **Field** ne peut pas modifier l'ordre des objets **Field** dans la collection tant que vous n'utilisez pas la méthode **Refresh**.</span><span class="sxs-lookup"><span data-stu-id="39eb9-p101">To determine the position that the Microsoft Access database engine uses for **Field** objects in the **Fields** collection of a **QueryDef**, **Recordset**, or **TableDef** object, use the **OrdinalPosition** property of each **Field** object. Changing the **OrdinalPosition** property of a **Field** object may not change the order of the **Field** objects in the collection until you use the **Refresh** method</span></span>

<span data-ttu-id="39eb9-p102">Utilisez la méthode **Refresh** dans les environnements multi-utilisateurs dans lesquels les autres utilisateurs peuvent modifier la base de données. Vous avez peut-être besoin également de l'utiliser dans des collections concernées indirectement par les modifications apportées à la base de données. Par exemple, si vous modifiez une collection **Users**, il est peut-être nécessaire d'actualiser une collection **Groups** avant d'utiliser cette collection **Groups**.</span><span class="sxs-lookup"><span data-stu-id="39eb9-p102">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="39eb9-p103">Une collection est remplie d'objets la première fois qu'elle est nommée. Elle ne reflète pas automatiquement les modifications suivantes effectuées par d'autres utilisateurs. Si un autre utilisateur est susceptible de modifier une collection, utilisez la méthode Refresh dans la collection immédiatement avant d'effectuer une tâche dans l'application qui considère la présence ou l'absence d'un objet déterminé dans la collection. Cela permet de s'assurer que la collection est aussi à jour que possible. Par ailleurs, l'utilisation de la méthode Refresh peut ralentir inutilement les performances.</span><span class="sxs-lookup"><span data-stu-id="39eb9-p103">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

## <a name="example"></a><span data-ttu-id="39eb9-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="39eb9-118">Example</span></span>

<span data-ttu-id="39eb9-p104">Dans cet exemple, la méthode **Refresh** est utilisée pour mettre à jour la collection **Fields** de la table Catégories à l'aide des modifications des données **OrdinalPosition**. L'ordre de la collection **Fields** ne change qu'après utilisation de la méthode **Refresh**.</span><span class="sxs-lookup"><span data-stu-id="39eb9-p104">This example uses the **Refresh** method to update the **Fields** collection of the Categories table based on changes to the **OrdinalPosition** data. The order of the **Fields** in the collection changes only after the **Refresh** method is used.</span></span>

```vb
    Sub RefreshX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldLoop As Field 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Categories") 
     
     With tdfEmployees 
     ' Display original OrdinalPosition data and store it 
     ' in an array. 
     Debug.Print _ 
     "Original OrdinalPosition data in TableDef." 
     ReDim aintPosition(0 To .Fields.Count - 1) As Integer 
     ReDim astrFieldName(0 To .Fields.Count - 1) As String 
     For intTemp = 0 To .Fields.Count - 1 
     aintPosition(intTemp) = _ 
     .Fields(intTemp).OrdinalPosition 
     astrFieldName(intTemp) = .Fields(intTemp).Name 
     Debug.Print , aintPosition(intTemp), _ 
     astrFieldName(intTemp) 
     Next intTemp 
     
     ' Change OrdinalPosition data. 
     For Each fldLoop In .Fields 
     fldLoop.OrdinalPosition = _ 
     100 - fldLoop.OrdinalPosition 
     Next fldLoop 
     Set fldLoop = Nothing 
     
     ' Print new data. 
     Debug.Print "New OrdinalPosition data before Refresh." 
     For Each fldLoop In .Fields 
     Debug.Print , fldLoop.OrdinalPosition, fldLoop.Name 
     Next fldLoop 
     
     .Fields.Refresh 
     
     ' Print new data, showing how the field order has been 
     ' changed. 
     Debug.Print "New OrdinalPosition data after Refresh." 
     For Each fldLoop In .Fields 
     Debug.Print , fldLoop.OrdinalPosition, fldLoop.Name 
     Next fldLoop 
     
     ' Restore original OrdinalPosition data. 
     For intTemp = 0 To .Fields.Count - 1 
     .Fields(astrFieldName(intTemp)).OrdinalPosition = _ 
     aintPosition(intTemp) 
     Next intTemp 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
