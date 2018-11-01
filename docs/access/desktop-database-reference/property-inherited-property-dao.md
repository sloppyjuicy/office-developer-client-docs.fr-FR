---
title: Property.Inherited Property (DAO)
TOCTitle: Inherited Property
ms:assetid: 10e624db-2301-b9be-beca-6e8caccf7274
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845349(v=office.15)
ms:contentKeyID: 48543304
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052991
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7768ec3048c14962154fa8ba54f391a9a8a10e66
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887977"
---
# <a name="propertyinherited-property-dao"></a><span data-ttu-id="fe933-102">Property.Inherited Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="fe933-102">Property.Inherited Property (DAO)</span></span>


<span data-ttu-id="fe933-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe933-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="fe933-104">Renvoie une valeur qui indique si un objet **[Property](property-object-dao.md)** est hérité d'un objet sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="fe933-104">Returns a value that indicates whether a **[Property](property-object-dao.md)** object is inherited from an underlying object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe933-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe933-105">Syntax</span></span>

<span data-ttu-id="fe933-106">*expression* . Hérité</span><span class="sxs-lookup"><span data-stu-id="fe933-106">*expression* .Inherited</span></span>

<span data-ttu-id="fe933-107">*expression* Variable qui représente un objet **Property** .</span><span class="sxs-lookup"><span data-stu-id="fe933-107">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe933-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="fe933-108">Remarks</span></span>

<span data-ttu-id="fe933-109">Pour les objets **Property** intégrés qui représentent des propriétés prédéfinies, la seule valeur de retour possible est **False**.</span><span class="sxs-lookup"><span data-stu-id="fe933-109">For built-in **Property** objects that represent predefined properties, the only possible return value is **False**.</span></span>

<span data-ttu-id="fe933-p101">La propriété **Inherited** permet de déterminer si un objet **Property** défini par l'utilisateur a été créé pour l'objet auquel il s'applique ou si l'objet **Property** a été hérité d'un autre objet. Par exemple, supposons que vous créez un nouvel objet **Property** pour un objet **[QueryDef](querydef-object-dao.md)** et que vous ouvrez ensuite un objet **[Recordset](recordset-object-dao.md)** à partir de l'objet **QueryDef**. Ce nouvel objet **Property** fait partie de la collection [**Properties**](properties-collection-dao.md) de l'objet **Recordset** et sa propriété **Inherited** est définie sur **True** car la propriété a été créée pour l'objet **QueryDef** et non pour l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="fe933-p101">You can use the **Inherited** property to determine whether a user-defined **Property** was created for the object it applies to, or whether the **Property** was inherited from another object. For example, suppose you create a new **Property** for a **[QueryDef](querydef-object-dao.md)** object and then open a **[Recordset](recordset-object-dao.md)** object from the **QueryDef** object. This new **Property** will be part of the **Recordset** object's **[Properties](properties-collection-dao.md)** collection, and its **Inherited** property will be set to **True** because the property was created for the **QueryDef** object, not the **Recordset** object.</span></span>

## <a name="example"></a><span data-ttu-id="fe933-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="fe933-113">Example</span></span>

<span data-ttu-id="fe933-114">Cet exemple utilise la propriété **Inherited** pour déterminer si un objet **Property** défini par l'utilisateur a été créé pour un objet **Recordset** ou pour un autre objet sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="fe933-114">This example use the **Inherited** property to determine if a user-defined **Property** object was created for a **Recordset** object or for some underlying object.</span></span>

```vb 
Sub InheritedX() 
 
 Dim dbsNorthwind As Database 
 Dim tdfTest As TableDef 
 Dim rstTest As Recordset 
 Dim prpNew As Property 
 Dim prpLoop As Property 
 
 ' Create a new property for a saved TableDef object, then 
 ' open a recordset from that TableDef object. 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set tdfTest = dbsNorthwind.TableDefs(0) 
 Set prpNew = tdfTest.CreateProperty("NewProperty", _ 
 dbBoolean, True) 
 tdfTest.Properties.Append prpNew 
 Set rstTest = tdfTest.OpenRecordset(dbOpenForwardOnly) 
 
 ' Show Name and Inherited property of the new Property 
 ' object in the TableDef. 
 Debug.Print "NewProperty of " & tdfTest.Name & _ 
 " TableDef:" 
 Debug.Print " Inherited = " & _ 
 tdfTest.Properties("NewProperty").Inherited 
 
 ' Show Name and Inherited property of the new Property 
 ' object in the Recordset. 
 Debug.Print "NewProperty of " & rstTest.Name & _ 
 " Recordset:" 
 Debug.Print " Inherited = " & _ 
 rstTest.Properties("NewProperty").Inherited 
 
 ' Delete new TableDef because this is a demonstration. 
 tdfTest.Properties.Delete prpNew.Name 
 dbsNorthwind.Close 
 
End Sub 
 
```

