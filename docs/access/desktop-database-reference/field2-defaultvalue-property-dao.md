---
title: Propriété Field2.DefaultValue (DAO)
TOCTitle: DefaultValue Property
ms:assetid: 709c9580-520e-46ce-7d70-e409872184bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195744(v=office.15)
ms:contentKeyID: 48545563
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053121
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c0edef512eb6b4c099362e737a760624dcfc0b69
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928474"
---
# <a name="field2defaultvalue-property-dao"></a><span data-ttu-id="cdf96-102">Propriété Field2.DefaultValue (DAO)</span><span class="sxs-lookup"><span data-stu-id="cdf96-102">Field2.DefaultValue property (DAO)</span></span>


<span data-ttu-id="cdf96-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cdf96-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="cdf96-p101">Définit ou renvoie la valeur par défaut d'un objet **Field2**. Pour un objet **Field2** pas encore ajouté à la collection **[Fields](fields-collection-dao.md)**, cette propriété est en lecture-écriture (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="cdf96-p101">Sets or returns the default value of a **Field2** object. For a **Field2** object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="cdf96-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cdf96-106">Syntax</span></span>

<span data-ttu-id="cdf96-107">*expression* . DefaultValue</span><span class="sxs-lookup"><span data-stu-id="cdf96-107">*expression* .DefaultValue</span></span>

<span data-ttu-id="cdf96-108">*expression* Variable qui représente un objet **Field2** .</span><span class="sxs-lookup"><span data-stu-id="cdf96-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdf96-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="cdf96-109">Remarks</span></span>

<span data-ttu-id="cdf96-p102">Le paramètre ou la valeur de retour est une donnée de type **String** pouvant contenir 255 caractères maximum. Il peut s'agir de texte ou d'une expression. Dans ce dernier cas, le paramètre ne peut contenir ni fonction personnalisée, ni fonctions d'agrégation du moteur SQL de base de données Microsoft Access, ni référence à aucune requête, aucun formulaire ou tout autre objet **Field2**.</span><span class="sxs-lookup"><span data-stu-id="cdf96-p102">The setting or return value is a **String** data type that can contain a maximum of 255 characters. It can be either text or an expression. If the property setting is an expression, it can't contain user-defined functions, Microsoft Access database engine SQL aggregate functions, or references to queries, forms, or other **Field2** objects.</span></span>


> [!NOTE]
> <P><span data-ttu-id="cdf96-p103">[!REMARQUE] Vous pouvez également définir la propriété <STRONG>DefaultValue</STRONG> d'un objet <STRONG>Field2</STRONG> d'un objet <STRONG>TableDef</STRONG> sur une valeur spéciale appelée "GenUniqueID( )". Ce faisant, un nombre aléatoire est affecté à ce champ dès qu'un nouvel enregistrement est ajouté ou créé, créant ainsi un identificateur unique pour chaque enregistrement. La propriété <STRONG>Type</STRONG> du champ doit être <STRONG>Long</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="cdf96-p103">You can also set the <STRONG>DefaultValue</STRONG> property of a <STRONG>Field2</STRONG> object on a <STRONG>TableDef</STRONG> object to a special value called "GenUniqueID( )". This causes a random number to be assigned to this field whenever a new record is added or created, thereby giving each record a unique identifier. The field's <STRONG>Type</STRONG> property must be <STRONG>Long</STRONG>.</span></span></P>



<span data-ttu-id="cdf96-116">La disponibilité de la propriété **DefaultValue** dépend de l'objet contenant la collection **Fields**, comme illustré dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="cdf96-116">The availability of the **DefaultValue** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cdf96-117">Si la collection Fields appartient à un</span><span class="sxs-lookup"><span data-stu-id="cdf96-117">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="cdf96-118">La propriété DefaultValue est</span><span class="sxs-lookup"><span data-stu-id="cdf96-118">Then DefaultValue is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdf96-119">Objet Index</span><span class="sxs-lookup"><span data-stu-id="cdf96-119">Index object</span></span></p></td>
<td><p><span data-ttu-id="cdf96-120">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="cdf96-120">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf96-121">Objet QueryDef</span><span class="sxs-lookup"><span data-stu-id="cdf96-121">QueryDef object</span></span></p></td>
<td><p><span data-ttu-id="cdf96-122">En lecture seule</span><span class="sxs-lookup"><span data-stu-id="cdf96-122">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf96-123">Objet Recordset</span><span class="sxs-lookup"><span data-stu-id="cdf96-123">Recordset object</span></span></p></td>
<td><p><span data-ttu-id="cdf96-124">En lecture seule</span><span class="sxs-lookup"><span data-stu-id="cdf96-124">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf96-125">Objet Relation</span><span class="sxs-lookup"><span data-stu-id="cdf96-125">Relation object</span></span></p></td>
<td><p><span data-ttu-id="cdf96-126">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="cdf96-126">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf96-127">Objet TableDef</span><span class="sxs-lookup"><span data-stu-id="cdf96-127">TableDef object</span></span></p></td>
<td><p><span data-ttu-id="cdf96-128">En lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cdf96-128">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cdf96-p104">Lors de la création d'un nouvel enregistrement, le paramètre de propriété **DefaultValue** est automatiquement entré comme valeur du champ. Vous pouvez modifier la valeur du champ en définissant sa propriété **Value**.</span><span class="sxs-lookup"><span data-stu-id="cdf96-p104">When a new record is created, the **DefaultValue** property setting is automatically entered as the value for the field. You can change the field value by setting its **Value** property.</span></span>

<span data-ttu-id="cdf96-131">La propriété **DefaultValue** ne s'applique pas aux champs **AutoNumber** et **Long Binary**.</span><span class="sxs-lookup"><span data-stu-id="cdf96-131">The **DefaultValue** property doesn't apply to **AutoNumber** and **Long Binary** fields.</span></span>

## <a name="example"></a><span data-ttu-id="cdf96-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="cdf96-132">Example</span></span>

<span data-ttu-id="cdf96-p105">Cet exemple utilise la propriété **DefaultValue** pour alerter l'utilisateur de la valeur normale d'un champ au moment de l'entrée. Par ailleurs, il démontre comment les nouveaux enregistrements sont renseignés à l'aide de **DefaultValue** en l'absence de toute entrée. La fonction DefaultPrompt est indispensable pour l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="cdf96-p105">This example uses the **DefaultValue** property to alert the user of a field's normal value while prompting for input. In addition, it demonstrates how new records will be filled using **DefaultValue** in the absence of any other input. The DefaultPrompt function is required for this procedure to run.</span></span>

```vb
    Sub DefaultValueX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim strOldDefault As String 
     Dim rstEmployees As Recordset 
     Dim strMessage As String 
     Dim strCode As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     ' Store original DefaultValue information and set the 
     ' property to a new value. 
     strOldDefault = _ 
     tdfEmployees.Fields!PostalCode.DefaultValue 
     tdfEmployees.Fields!PostalCode.DefaultValue = "98052" 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     ' Add a new record to the Recordset. 
     .AddNew 
     !FirstName = "Bruce" 
     !LastName = "Oberg" 
     
     ' Get user input. If user enters something, the field 
     ' will be filled with that data; otherwise, it will be 
     ' filled with the DefaultValue information. 
     strMessage = "Enter postal code for " & vbCr & _ 
     !FirstName & " " & !LastName & ":" 
     strCode = DefaultPrompt(strMessage, !PostalCode) 
     If strCode <> "" Then !PostalCode = strCode 
     .Update 
     
     ' Go to new record and print information. 
     .Bookmark = .LastModified 
     Debug.Print " FirstName = " & !FirstName 
     Debug.Print " LastName = " & !LastName 
     Debug.Print " PostalCode = " & !PostalCode 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     .Close 
     End With 
     
     ' Restore original DefaultValue property because this is a 
     ' demonstration. 
     tdfEmployees.Fields!PostalCode.DefaultValue = _ 
     strOldDefault 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function DefaultPrompt(strPrompt As String, _ 
     fldTemp As Field2) As String 
     
     Dim strFullPrompt As String 
     
     ' Ask user for new DefaultValue setting for the specified 
     ' Field object. 
     strFullPrompt = strPrompt & vbCr & _ 
     "[Default = " & fldTemp.DefaultValue & _ 
     ", Cancel - use default]" 
     DefaultPrompt = InputBox(strFullPrompt) 
     
    End Function
```
