---
title: Field. DefaultValue, propriété (DAO)
TOCTitle: DefaultValue Property
ms:assetid: 8a1c558b-c8f6-757d-c595-4e50b9b6ae3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197092(v=office.15)
ms:contentKeyID: 48546185
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 18fb4d3a4427db2b407b6a20507339fe83665c97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293118"
---
# <a name="fielddefaultvalue-property-dao"></a>Field. DefaultValue, propriété (DAO)


**S’applique à** : Access 2013, Office 2013


Définit ou renvoie la valeur par défaut d'un objet **[Field](field-object-dao.md)**. Cette propriété est en lecture-écriture si l'objet **Field** n'est pas encore ajouté à la collection **[Fields](fields-collection-dao.md)** (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . DefaultValue

*expression* Variable qui représente un objet **Field** .

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur renvoyée est un type de données **String** qui peut contenir jusqu'à 255 caractères. Il peut s'agir de texte ou d'une expression. Dans le cas d'une expression, celle-ci ne peut pas contenir de fonctions définies par l'utilisateur, de fonctions d'agrégation SQL du moteur de base de données Microsoft Access ou de références à des requêtes, des formulaires ou d'autres objets **Field**.


> [!NOTE]
> [!REMARQUE] Vous pouvez également définir la propriété **DefaultValue** d'un objet **Field** dans un objet [TableDef](tabledef-object-dao.md) sur une valeur spéciale appelée « GenUniqueID( ) ». Ce faisant, un nombre aléatoire est affecté à ce champ dès qu'un nouvel enregistrement est ajouté ou créé, créant ainsi un identificateur unique pour chaque enregistrement. La propriété [Type](field-type-property-dao.md) du champ doit être **Long**.


La disponibilité de la propriété **DefaultValue** dépend de l'objet contenant la collection **Fields**, comme illustré dans le tableau suivant.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Si la collection Fields appartient à un</p></th>
<th><p>La propriété DefaultValue est</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Objet Index</p></td>
<td><p>Non pris en charge</p></td>
</tr>
<tr class="even">
<td><p>Objet QueryDef</p></td>
<td><p>Lecture seule</p></td>
</tr>
<tr class="odd">
<td><p>Objet Recordset</p></td>
<td><p>Lecture seule</p></td>
</tr>
<tr class="even">
<td><p>Objet Relation</p></td>
<td><p>Non reconnu</p></td>
</tr>
<tr class="odd">
<td><p>Objet TableDef</p></td>
<td><p>En lecture-écriture.</p></td>
</tr>
</tbody>
</table>


Lors de la création d'un enregistrement, le paramètre de la propriété **DefaultValue** est automatiquement entré comme valeur du champ. Pour modifier la valeur du champ, vous pouvez définir la propriété **[Value](field-value-property-dao.md)**.

La propriété **DefaultValue** ne s'applique pas aux champs **AutoNumber** et **Long Binary**.

## <a name="example"></a>Exemple

Cet exemple utilise la propriété **DefaultValue** pour alerter l'utilisateur de la valeur normale d'un champ au moment de l'entrée. Par ailleurs, il démontre comment les nouveaux enregistrements sont renseignés à l'aide de **DefaultValue** en l'absence de toute entrée. La fonction DefaultPrompt est indispensable pour l'exécution de cette procédure.

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
     fldTemp As Field) As String 
     
     Dim strFullPrompt As String 
     
     ' Ask user for new DefaultValue setting for the specified 
     ' Field object. 
     strFullPrompt = strPrompt & vbCr & _ 
     "[Default = " & fldTemp.DefaultValue & _ 
     ", Cancel - use default]" 
     DefaultPrompt = InputBox(strFullPrompt) 
     
    End Function
```
