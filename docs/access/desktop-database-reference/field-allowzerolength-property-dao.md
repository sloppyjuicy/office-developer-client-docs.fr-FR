---
title: Propriété Field.AllowZeroLength (DAO)
TOCTitle: AllowZeroLength Property
ms:assetid: 5103a905-9258-e088-0210-857372f41c3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193832(v=office.15)
ms:contentKeyID: 48544807
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052962
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3bee3b9457f2c5187432c1aad6cd1837e70eadae
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926296"
---
# <a name="fieldallowzerolength-property-dao"></a><span data-ttu-id="945d2-102">Propriété Field.AllowZeroLength (DAO)</span><span class="sxs-lookup"><span data-stu-id="945d2-102">Field.AllowZeroLength property (DAO)</span></span>

<span data-ttu-id="945d2-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="945d2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="945d2-104">Définit ou renvoie une valeur qui indique si une chaîne nulle ("") est un paramètre valide pour la propriété **[Value](field-value-property-dao.md)** de l'objet **[Field](field-object-dao.md)** avec un type de données Texte ou Mémo (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="945d2-104">Sets or returns a value that indicates whether a zero-length string ("") is a valid setting for the **[Value](field-value-property-dao.md)** property of the **[Field](field-object-dao.md)** object with a Text or Memo data type (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="945d2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="945d2-105">Syntax</span></span>

<span data-ttu-id="945d2-106">*expression* . AllowZeroLength</span><span class="sxs-lookup"><span data-stu-id="945d2-106">*expression* .AllowZeroLength</span></span>

<span data-ttu-id="945d2-107">*expression* Variable qui représente un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="945d2-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="945d2-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="945d2-108">Remarks</span></span>

<span data-ttu-id="945d2-109">Pour un objet pas encore ajouté à la collection **Fields**, cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="945d2-109">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="945d2-110">Une fois que l'objet est ajouté à la collection **Fields**, la disponibilité de la propriété **AllowZeroLength** dépend de l'objet contenant la collection **Fields**, comme illustré dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="945d2-110">Once appended to a **Fields** collection, the availability of the **AllowZeroLength** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="945d2-111">Si la collection Fields appartient à un</span><span class="sxs-lookup"><span data-stu-id="945d2-111">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="945d2-112">Alors AllowZeroLength est</span><span class="sxs-lookup"><span data-stu-id="945d2-112">Then AllowZeroLength is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="945d2-113">							objet <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="945d2-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="945d2-114">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="945d2-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="945d2-115">							objet <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="945d2-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="945d2-116">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="945d2-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="945d2-117">							objet <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="945d2-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="945d2-118">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="945d2-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="945d2-119">							objet <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="945d2-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="945d2-120">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="945d2-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="945d2-121">							objet <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="945d2-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="945d2-122">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="945d2-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="945d2-123">Vous pouvez utiliser cette propriété avec les propriétés **[Required](field-required-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)** ou **[ValidationRule](field-validationrule-property-dao.md)** pour valider une valeur d'un champ.</span><span class="sxs-lookup"><span data-stu-id="945d2-123">You can use this property along with the **[Required](field-required-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)**, or **[ValidationRule](field-validationrule-property-dao.md)** property to validate a value in a field.</span></span>

## <a name="example"></a><span data-ttu-id="945d2-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="945d2-124">Example</span></span>

<span data-ttu-id="945d2-p101">Dans l'exemple ci-dessous, la propriété **AllowZeroLength** permet de définir la valeur d'un objet **Field** sur une chaîne vide. Dans ce cas, il est possible d'établir une distinction entre un enregistrement dont les données sont inconnues et un enregistrement où les données ne s'appliquent pas.</span><span class="sxs-lookup"><span data-stu-id="945d2-p101">In this example, the **AllowZeroLength** property allows the user to set the value of a **Field** to an empty string. In this situation, the user can distinguish between a record where data is not known and a record where the data does not apply.</span></span>

```vb
    Sub AllowZeroLengthX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldTemp As Field 
     Dim rstEmployees As Recordset 
     Dim strMessage As String 
     Dim strInput As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Employees") 
     ' Create a new Field object and append it to the Fields 
     ' collection of the Employees table. 
     Set fldTemp = tdfEmployees.CreateField("FaxPhone", _ 
     dbText, 24) 
     fldTemp.AllowZeroLength = True 
     tdfEmployees.Fields.Append fldTemp 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Get user input. 
     .Edit 
     strMessage = "Enter fax number for " & _ 
     !FirstName & " " & !LastName & "." & vbCr & _ 
     "[? - unknown, X - has no fax]" 
     strInput = UCase(InputBox(strMessage)) 
     If strInput <> "" Then 
     Select Case strInput 
     Case "?" 
     !FaxPhone = Null 
     Case "X" 
     !FaxPhone = "" 
     Case Else 
     !FaxPhone = strInput 
     End Select 
     
     .Update 
     
     ' Print report. 
     Debug.Print "Name - Fax number" 
     Debug.Print !FirstName & " " & !LastName & " - "; 
     
     If IsNull(!FaxPhone) Then 
     Debug.Print "[Unknown]" 
     Else 
     If !FaxPhone = "" Then 
     Debug.Print "[Has no fax]" 
     Else 
     Debug.Print !FaxPhone 
     End If 
     End If 
     
     Else 
     .CancelUpdate 
     End If 
     
     .Close 
     End With 
     
     ' Delete new field because this is a demonstration. 
     tdfEmployees.Fields.Delete fldTemp.Name 
     dbsNorthwind.Close 
     
    End Sub
```
