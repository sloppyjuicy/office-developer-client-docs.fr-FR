---
title: Propriété Field2.AllowZeroLength (DAO)
TOCTitle: AllowZeroLength Property
ms:assetid: d3795634-527f-b4c5-b606-50f9945cac12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834791(v=office.15)
ms:contentKeyID: 48547908
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3125a5669ea8aa016d8554be0357572d56c08ecf
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721177"
---
# <a name="field2allowzerolength-property-dao"></a><span data-ttu-id="a7a91-102">Propriété Field2.AllowZeroLength (DAO)</span><span class="sxs-lookup"><span data-stu-id="a7a91-102">Field2.AllowZeroLength property (DAO)</span></span>


<span data-ttu-id="a7a91-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a7a91-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="a7a91-104">Définit ou renvoie une valeur qui indique si une chaîne vide ("") est un paramètre valide pour la propriété **[Value](field-value-property-dao.md)** de l'objet **Field2** avec un type de données Texte ou Mémo (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="a7a91-104">Sets or returns a value that indicates whether a zero-length string ("") is a valid setting for the **[Value](field-value-property-dao.md)** property of the **Field2** object with a Text or Memo data type (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="a7a91-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7a91-105">Syntax</span></span>

<span data-ttu-id="a7a91-106">*expression* . AllowZeroLength</span><span class="sxs-lookup"><span data-stu-id="a7a91-106">*expression* .AllowZeroLength</span></span>

<span data-ttu-id="a7a91-107">*expression* Variable qui représente un objet **Field2** .</span><span class="sxs-lookup"><span data-stu-id="a7a91-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7a91-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="a7a91-108">Remarks</span></span>

<span data-ttu-id="a7a91-109">Pour un objet pas encore ajouté à la collection **Fields**, cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a7a91-109">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="a7a91-110">Une fois que l'objet est ajouté à la collection **Fields**, la disponibilité de la propriété **AllowZeroLength** dépend de l'objet contenant la collection **Fields**, comme illustré dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a7a91-110">Once appended to a **Fields** collection, the availability of the **AllowZeroLength** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a7a91-111">Si la collection Fields appartient à un</span><span class="sxs-lookup"><span data-stu-id="a7a91-111">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="a7a91-112">Alors AllowZeroLength est</span><span class="sxs-lookup"><span data-stu-id="a7a91-112">Then AllowZeroLength is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a7a91-113">							objet <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="a7a91-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a7a91-114">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7a91-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7a91-115">							objet <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="a7a91-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a7a91-116">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7a91-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7a91-117">							objet <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="a7a91-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a7a91-118">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7a91-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7a91-119">							objet <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="a7a91-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a7a91-120">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7a91-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7a91-121">							objet <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="a7a91-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a7a91-122">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="a7a91-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a7a91-123">Vous pouvez utiliser cette propriété avec les propriétés **[Required](field-required-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)** ou **[ValidationRule](field-validationrule-property-dao.md)** pour valider une valeur d'un champ.</span><span class="sxs-lookup"><span data-stu-id="a7a91-123">You can use this property along with the **[Required](field-required-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)**, or **[ValidationRule](field-validationrule-property-dao.md)** property to validate a value in a field.</span></span>

## <a name="example"></a><span data-ttu-id="a7a91-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="a7a91-124">Example</span></span>

<span data-ttu-id="a7a91-p101">Dans cet exemple, la propriété **AllowZeroLength** permet à l'utilisateur de définir la valeur de **Field2** sur une chaîne vide. Dans ce cas, l'utilisateur peut faire la distinction entre un enregistrement dont les données sont inconnues et un enregistrement dont les données ne s'appliquent pas.</span><span class="sxs-lookup"><span data-stu-id="a7a91-p101">In this example, the **AllowZeroLength** property allows the user to set the value of a **Field2** to an empty string. In this situation, the user can distinguish between a record where data is not known and a record where the data does not apply.</span></span>

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
