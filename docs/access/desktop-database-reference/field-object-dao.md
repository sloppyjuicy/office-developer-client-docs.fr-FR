---
title: 'Field Object : DAO (Data Access Objects)'
TOCTitle: Field Object
ms:assetid: 47282ce2-9b49-ccf9-ad37-c4bb25cfd037
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193203(v=office.15)
ms:contentKeyID: 48544587
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c58896fb0d0a5c5a28844fdd3a6df922dd587f32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293041"
---
# <a name="field-object-dao"></a><span data-ttu-id="19a19-102">Field Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="19a19-102">Field Object (DAO)</span></span>

<span data-ttu-id="19a19-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="19a19-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="19a19-104">Un objet **Field** représente une colonne de données avec un type de données courantes et un ensemble commun de propriétés.</span><span class="sxs-lookup"><span data-stu-id="19a19-104">A **Field** object represents a column of data with a common data type and a common set of properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="19a19-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="19a19-105">Remarks</span></span>

<span data-ttu-id="19a19-p101">Les collections **Fields** des objets **Index**, **QueryDef**, **Relation** et **TableDef** contiennent les spécifications pour les champs que représentent ces objets. La collection **Fields** d'un objet **Recordset** représente les objets **Field** sur une ligne de données ou dans un enregistrement. Vous utilisez les objets **Field** dans un objet **Recordset** pour lire et définir des valeurs pour les champs dans l'enregistrement actuel de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="19a19-p101">The **Fields** collections of **Index**, **QueryDef**, **Relation**, and **TableDef** objects contain the specifications for the fields those objects represent. The **Fields** collection of a **Recordset** object represents the **Field** objects in a row of data, or in a record. You use the **Field** objects in a **Recordset** object to read and set values for the fields in the current record of the **Recordset** object.</span></span>

<span data-ttu-id="19a19-p102">Dans un espace de travail Microsoft Access, vous manipulez un champ à l'aide d'un objet **Field** et de ses méthodes et propriétés. Par exemple, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="19a19-p102">In a Microsoft Access workspacee, you manipulate a field using a **Field** object and its methods and properties. For example, you can:</span></span>

  - <span data-ttu-id="19a19-111">Utiliser la propriété **OrdinalPosition** pour définir ou renvoyer l'ordre de présentation de l'objet **Field** dans une collection **Fields**.</span><span class="sxs-lookup"><span data-stu-id="19a19-111">Use the **OrdinalPosition** property to set or return the presentation order of the **Field** object in a **Fields** collection.</span></span>

  - <span data-ttu-id="19a19-112">Utiliser la propriété **Value** d'un champ dans un objet **Recordset** pour définir ou renvoyer les données stockées.</span><span class="sxs-lookup"><span data-stu-id="19a19-112">Use the **Value** property of a field in a **Recordset** object to set or return stored data.</span></span>

  - <span data-ttu-id="19a19-113">Utiliser les méthodes **AppendChunk** et **GetChunk** et la propriété **FieldSize** pour obtenir ou définir une valeur dans un champ Objet OLE ou Mémo d'un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="19a19-113">Use the **AppendChunk** and **GetChunk** methods and the **FieldSize** property to get or set a value in an OLE Object or Memo field of a **Recordset** object.</span></span>

  - <span data-ttu-id="19a19-114">Utiliser les propriétés **Type**, **Size** et **Attributes** pour déterminer le type de données qui peut être stocké dans le champ.</span><span class="sxs-lookup"><span data-stu-id="19a19-114">Use the **Type**, **Size**, and **Attributes** properties to determine the type of data that can be stored in the field.</span></span>

  - <span data-ttu-id="19a19-115">Utiliser les propriétés **SourceField** et **SourceTable** pour déterminer la source originale des données.</span><span class="sxs-lookup"><span data-stu-id="19a19-115">Use the **SourceField** and **SourceTable** properties to determine the original source of the data.</span></span>

  - <span data-ttu-id="19a19-116">Utiliser la propriété **ForeignName** pour définir ou renvoyer des informations sur un champ externe dans un objet **Relation**.</span><span class="sxs-lookup"><span data-stu-id="19a19-116">Use the **ForeignName** property to set or return information about a foreign field in a **Relation** object.</span></span>

  - <span data-ttu-id="19a19-117">Utiliser les propriétés **AllowZeroLength**, **DefaultValue**, **Required**, **ValidateOnSet**, **ValidationRule** ou **ValidationText** pour définir ou renvoyer les conditions de validation.</span><span class="sxs-lookup"><span data-stu-id="19a19-117">Use the **AllowZeroLength**, **DefaultValue**, **Required**, **ValidateOnSet**, **ValidationRule**, or **ValidationText** properties to set or return validation conditions.</span></span>

  - <span data-ttu-id="19a19-118">Utiliser la propriété **DefaultValue** d'un champ dans un objet **TableDef** pour définir la valeur par défaut pour ce champ lorsque de nouveaux enregistrements sont ajoutés.</span><span class="sxs-lookup"><span data-stu-id="19a19-118">Use the **DefaultValue** property of a field on a **TableDef** object to set the default value for this field when new records are added.</span></span>

<span data-ttu-id="19a19-119">Pour créer un objet **Field** dans un objet **Index**, **TableDef** ou **Relation**, utilisez la méthode **CreateField**.</span><span class="sxs-lookup"><span data-stu-id="19a19-119">To create a new **Field** object in an **Index**, **TableDef**, or **Relation** object, use the **CreateField** method.</span></span>

<span data-ttu-id="19a19-p103">Lorsque vous accédez à un objet **Field** dans le cadre d'un objet **Recordset**, les données de l'enregistrement actif sont affichées dans la propriété **Value** de l'objet **Field**. Pour manipuler les données dans l'objet **Recordset**, vous ne référencez généralement pas directement la collection **Fields**. Au lieu de cela, vous référencez indirectement la propriété **Value** de l'objet **Field** dans la collection **Fields** de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="19a19-p103">When you access a **Field** object as part of a **Recordset** object, data from the current record is visible in the **Field** object's **Value** property. To manipulate data in the **Recordset** object, you don't usually reference the **Fields** collection directly; instead, you indirectly reference the **Value** property of the **Field** object in the **Fields** collection of the **Recordset** object.</span></span>

<span data-ttu-id="19a19-122">Pour faire référence à un objet **Field** dans une collection par son numéro ordinal ou par son paramètre de propriété **Name**Name, utilisez l'une formes de syntaxe suivantes :</span><span class="sxs-lookup"><span data-stu-id="19a19-122">To refer to a **Field** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="19a19-123">**Fields**(0)</span><span class="sxs-lookup"><span data-stu-id="19a19-123">**Fields**(0)</span></span>

- <span data-ttu-id="19a19-124">**Fields**("nom")</span><span class="sxs-lookup"><span data-stu-id="19a19-124">**Fields**("name")</span></span>

- <span data-ttu-id="19a19-125">**Fields**\!\[nom\]</span><span class="sxs-lookup"><span data-stu-id="19a19-125">**Fields**\!\[name\]</span></span>

<span data-ttu-id="19a19-p104">Avec les mêmes formes de syntaxe, vous pouvez également renvoyer à la propriété **Value** d'un objet **Field** que vous créez et ajoutez à une collection **Fields**. Le contexte de la référence de champ détermine si vous faites référence à l'objet **Field** ou à la propriété **Value** de l'objet **Field**.</span><span class="sxs-lookup"><span data-stu-id="19a19-p104">With the same syntax forms, you can also refer to the **Value** property of a **Field** object that you create and append to a **Fields** collection. The context of the field reference will determine whether you are referring to the **Field** object or the **Value** property of the **Field** object.</span></span>

## <a name="example"></a><span data-ttu-id="19a19-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="19a19-128">Example</span></span>

<span data-ttu-id="19a19-p105">Cet exemple indique les propriétés valides pour un objet **Field** en fonction de l'emplacement de l'objet **Field** (par exemple, la collection **Fields** d'un objet **TableDef**, la collection **Fields** d'un objet **QueryDef**, etc.). La procédure FieldOutput est nécessaire à l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="19a19-p105">This example shows what properties are valid for a **Field** object depending on where the **Field** resides (for example, the **Fields** collection of a **TableDef**, the **Fields** collection of a **QueryDef**, and so forth). The FieldOutput procedure is required for this procedure to run.</span></span>

```vb
    Sub FieldX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim fldTableDef As Field 
     Dim fldQueryDef As Field 
     Dim fldRecordset As Field 
     Dim fldRelation As Field 
     Dim fldIndex As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Assign a Field object from different Fields 
     ' collections to object variables. 
     Set fldTableDef = _ 
     dbsNorthwind.TableDefs(0).Fields(0) 
     Set fldQueryDef =dbsNorthwind.QueryDefs(0).Fields(0) 
     Set fldRecordset = rstEmployees.Fields(0) 
     Set fldRelation =dbsNorthwind.Relations(0).Fields(0) 
     Set fldIndex = _ 
     dbsNorthwind.TableDefs(0).Indexes(0).Fields(0) 
     
     ' Print report. 
     FieldOutput "TableDef", fldTableDef 
     FieldOutput "QueryDef", fldQueryDef 
     FieldOutput "Recordset", fldRecordset 
     FieldOutput "Relation", fldRelation 
     FieldOutput "Index", fldIndex 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub FieldOutput(strTemp As String, fldTemp As Field) 
     ' Report function for FieldX. 
     
     Dim prpLoop As Property 
     
     Debug.Print "Valid Field properties in " & strTemp 
     
     ' Enumerate Properties collection of passed Field 
     ' object. 
     For Each prpLoop In fldTemp.Properties 
     ' Some properties are invalid in certain 
     ' contexts (the Value property in the Fields 
     ' collection of a TableDef for example). Any 
     ' attempt to use an invalid property will 
     ' trigger an error. 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " = " & _ 
     prpLoop.Value 
     On Error GoTo 0 
     Next prpLoop 
     
    End Sub 
```

<br/>

<span data-ttu-id="19a19-p106">Cet exemple utilise la méthode **CreateField** pour créer trois objets **Fields** pour un objet **TableDef**. Il affiche ensuite les propriétés de ces objets **Field**, qui sont automatiquement définies par la méthode **CreateField** (les propriétés dont les valeurs sont vides lors de la création de **Field** ne sont pas affichées).</span><span class="sxs-lookup"><span data-stu-id="19a19-p106">This example uses the **CreateField** method to create three **Fields** for a new **TableDef**. It then displays the properties of those **Field** objects that are automatically set by the **CreateField** method. (Properties whose values are empty at the time of **Field** creation are not shown.)</span></span>

```vb
    Sub CreateFieldX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
     
     ' Create and append new Field objects for the new 
     ' TableDef object. 
     With tdfNew 
     ' The CreateField method will set a default Size 
     ' for a new Field object if one is not specified. 
     .Fields.Append .CreateField("TextField", dbText) 
     .Fields.Append .CreateField("IntegerField", dbInteger) 
     .Fields.Append .CreateField("DateField", dbDate) 
     End With 
     
     dbsNorthwind.TableDefs.Append tdfNew 
     
     Debug.Print "Properties of new Fields in " & tdfNew.Name 
     
     ' Enumerate Fields collection to show the properties of 
     ' the new Field objects. 
     For Each fldLoop In tdfNew.Fields 
     Debug.Print " " & fldLoop.Name 
     
     For Each prpLoop In fldLoop.Properties 
     ' Properties that are invalid in the context of 
     ' TableDefs will trigger an error if an attempt 
     ' is made to read their values. 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     On Error GoTo 0 
     Next prpLoop 
     
     Next fldLoop 
     
     ' Delete new TableDef because this is a demonstration. 
     dbsNorthwind.TableDefs.Delete tdfNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
