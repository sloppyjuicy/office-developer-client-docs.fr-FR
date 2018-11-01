---
title: Field.Attributes Property (DAO)
TOCTitle: Attributes Property
ms:assetid: 8e6f6afb-1a89-7315-c129-cf7ff19e0ca9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197380(v=office.15)
ms:contentKeyID: 48546287
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: df396935f88301a9fee9df580a5cee01705f68aa
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885779"
---
# <a name="fieldattributes-property-dao"></a><span data-ttu-id="761a2-102">Field.Attributes Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="761a2-102">Field.Attributes Property (DAO)</span></span>


<span data-ttu-id="761a2-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="761a2-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="761a2-p101">Définit ou renvoie une valeur qui indique une ou plusieurs caractéristiques d'un objet **[Field](field-object-dao.md)**. Valeur de type **Long** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="761a2-p101">Sets or returns a value that indicates one or more characteristics of a **[Field](field-object-dao.md)** object. Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="761a2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="761a2-106">Syntax</span></span>

<span data-ttu-id="761a2-107">*expression* . Attributs</span><span class="sxs-lookup"><span data-stu-id="761a2-107">*expression* .Attributes</span></span>

<span data-ttu-id="761a2-108">*expression* Variable qui représente un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="761a2-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="761a2-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="761a2-109">Remarks</span></span>

<span data-ttu-id="761a2-110">La valeur spécifie les caractéristiques du champ représenté par l'objet **Field**. Il peut s'agir d'une combinaison des constantes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="761a2-110">The value specifies characteristics of the field represented by the **Field** object and can be a combination of these constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="761a2-111">Constant</span><span class="sxs-lookup"><span data-stu-id="761a2-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="761a2-112">Description</span><span class="sxs-lookup"><span data-stu-id="761a2-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="761a2-113"><strong>dbAutoIncrField</strong></span><span class="sxs-lookup"><span data-stu-id="761a2-113"><strong>dbAutoIncrField</strong></span></span></p></td>
<td><p><span data-ttu-id="761a2-114">La valeur de champ des nouveaux enregistrements est automatiquement incrémentée d’un entier long unique non modifiable (dans un espace de travail Microsoft Access, pris en charge uniquement par les tables de bases de données de moteur de base de données Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="761a2-114">The field value for new records is automatically incremented to a unique Long integer that can't be changed (in a Microsoft Access workspace, supported only for Microsoft Access database engine database tables).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="761a2-115"><strong>dbDescending</strong></span><span class="sxs-lookup"><span data-stu-id="761a2-115"><strong>dbDescending</strong></span></span></p></td>
<td><p><span data-ttu-id="761a2-p102">Le champ est trié dans l’ordre décroissant (Z à A ou 100 à 0). Cette option ne concerne qu’un objet <strong>Field</strong> dans une collection <strong>Fields</strong> d’un objet <strong>Index</strong>. Si vous omettez cette constante, le champ est trié dans l’ordre croissant (A à Z ou 0 à 100). Il s’agit de la valeur par défaut pour les champs <strong>Index</strong> et <strong>TableDef</strong> (espaces de travail Microsoft Access uniquement)..</span><span class="sxs-lookup"><span data-stu-id="761a2-p102">The field is sorted in descending (Z to A or 100 to 0) order; this option applies only to a <strong>Field</strong> object in a <strong>Fields</strong> collection of an <strong>Index</strong> object. If you omit this constant, the field is sorted in ascending (A to Z or 0 to 100) order. This is the default value for <strong>Index</strong> and <strong>TableDef</strong> fields (Microsoft Access workspaces only)..</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="761a2-119"><strong>dbFixedField</strong></span><span class="sxs-lookup"><span data-stu-id="761a2-119"><strong>dbFixedField</strong></span></span></p></td>
<td><p><span data-ttu-id="761a2-120">La taille du champ est fixe (par défaut pour les champs numériques).</span><span class="sxs-lookup"><span data-stu-id="761a2-120">The field size is fixed (default for Numeric fields).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="761a2-121"><strong>dbHyperlinkField</strong></span><span class="sxs-lookup"><span data-stu-id="761a2-121"><strong>dbHyperlinkField</strong></span></span></p></td>
<td><p><span data-ttu-id="761a2-122">Le champ contient un lien hypertexte (champs Mémo uniquement).</span><span class="sxs-lookup"><span data-stu-id="761a2-122">The field contains hyperlink information (Memo fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="761a2-123"><strong>dbSystemField</strong></span><span class="sxs-lookup"><span data-stu-id="761a2-123"><strong>dbSystemField</strong></span></span></p></td>
<td><p><span data-ttu-id="761a2-124">Le champ enregistre les informations de réplication pour les réplicas. Il est impossible de supprimer ce type de champ (espace de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="761a2-124">The field stores replication information for replicas; you can't delete this type of field (Microsoft Access workspace only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="761a2-125"><strong>dbUpdatableField</strong></span><span class="sxs-lookup"><span data-stu-id="761a2-125"><strong>dbUpdatableField</strong></span></span></p></td>
<td><p><span data-ttu-id="761a2-126">La valeur du champ peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="761a2-126">The field value can be changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="761a2-127"><strong>dbVariableField</strong></span><span class="sxs-lookup"><span data-stu-id="761a2-127"><strong>dbVariableField</strong></span></span></p></td>
<td><p><span data-ttu-id="761a2-128">La taille du champ est variable (champs Texte uniquement).</span><span class="sxs-lookup"><span data-stu-id="761a2-128">The field size is variable (Text fields only).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="761a2-p103">Dans le cas d'un objet qui n'est pas encore ajouté à une collection, cette propriété est en lecture/écriture. En ce qui concerne un objet **Field** ajouté, la disponibilité de la propriété **Attributes** dépend de l'objet qui contient la collection **Fields**.</span><span class="sxs-lookup"><span data-stu-id="761a2-p103">For an object not yet appended to a collection, this property is read/write. For an appended **Field** object, the availability of the **Attributes** property depends on the object that contains the **Fields** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="761a2-131">Si l'objet Field appartient à un</span><span class="sxs-lookup"><span data-stu-id="761a2-131">If the Field object belongs to an</span></span></p></th>
<th><p><span data-ttu-id="761a2-132">La propriété Attributes est</span><span class="sxs-lookup"><span data-stu-id="761a2-132">Then Attributes is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="761a2-133">objet <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="761a2-133"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="761a2-134">En lecture/écriture jusqu'à ce que l'objet <strong>TableDef</strong> auquel l'objet <strong>Index</strong> est ajouté soit ajouté à un objet <strong>Database</strong>. La propriété est alors en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="761a2-134">Read/write until the <strong>TableDef</strong> object that the <strong>Index</strong> object is appended to is appended to a <strong>Database</strong> object; then the property is read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="761a2-135">							objet <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="761a2-135"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="761a2-136">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="761a2-136">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="761a2-137">							objet <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="761a2-137"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="761a2-138">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="761a2-138">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="761a2-139">							objet <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="761a2-139"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="761a2-140">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="761a2-140">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="761a2-141">							objet <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="761a2-141"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="761a2-142">En lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="761a2-142">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="761a2-p104">Lorsque vous définissez plusieurs attributs, vous pouvez les combiner en additionnant les constantes appropriées. Toute valeur non valide est ignorée sans provoquer d'erreur.</span><span class="sxs-lookup"><span data-stu-id="761a2-p104">When you set multiple attributes, you can combine them by summing the appropriate constants. Any invalid values are ignored without producing an error.</span></span>

## <a name="example"></a><span data-ttu-id="761a2-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="761a2-145">Example</span></span>

<span data-ttu-id="761a2-146">Cet exemple affiche la propriété **Attributes** des objets **Field**, **Relation** et **TableDef** dans la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="761a2-146">This example displays the **Attributes** property for **Field**, **Relation**, and **TableDef** objects in the Northwind database.</span></span>

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field 
 Dim relLoop As Relation 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 
 ' Display the attributes of a TableDef object's 
 ' fields. 
 Debug.Print "Attributes of fields in " & _ 
 .TableDefs(0).Name & " table:" 
 For Each fldLoop In .TableDefs(0).Fields 
 Debug.Print " " & fldLoop.Name & " = " & _ 
 fldLoop.Attributes 
 Next fldLoop 
 
 ' Display the attributes of the Northwind database's 
 ' relations. 
 Debug.Print "Attributes of relations in " & _ 
 .Name & ":" 
 For Each relLoop In .Relations 
 Debug.Print " " & relLoop.Name & " = " & _ 
 relLoop.Attributes 
 Next relLoop 
 
 ' Display the attributes of the Northwind database's 
 ' tables. 
 Debug.Print "Attributes of tables in " & .Name & ":" 
 For Each tdfloop In .TableDefs 
 Debug.Print " " & tdfloop.Name & " = " & _ 
 tdfloop.Attributes 
 Next tdfloop 
 
 .Close 
 End With 
 
End Sub 
 
```

