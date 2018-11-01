---
title: Field2.DefaultValue Property (DAO)
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
ms.openlocfilehash: a70e5d1c19f4d92c4494071f78192ffb4e543ad7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882384"
---
# <a name="field2defaultvalue-property-dao"></a>Field2.DefaultValue Property (DAO)


**S’applique à**: Access 2013, Office 2013


Définit ou renvoie la valeur par défaut d'un objet **Field2**. Pour un objet **Field2** pas encore ajouté à la collection **[Fields](fields-collection-dao.md)**, cette propriété est en lecture-écriture (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . DefaultValue

*expression* Variable qui représente un objet **Field2** .

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur de retour est une donnée de type **String** pouvant contenir 255 caractères maximum. Il peut s'agir de texte ou d'une expression. Dans ce dernier cas, le paramètre ne peut contenir ni fonction personnalisée, ni fonctions d'agrégation du moteur SQL de base de données Microsoft Access, ni référence à aucune requête, aucun formulaire ou tout autre objet **Field2**.


> [!NOTE]
> <P>[!REMARQUE] Vous pouvez également définir la propriété <STRONG>DefaultValue</STRONG> d'un objet <STRONG>Field2</STRONG> d'un objet <STRONG>TableDef</STRONG> sur une valeur spéciale appelée "GenUniqueID( )". Ce faisant, un nombre aléatoire est affecté à ce champ dès qu'un nouvel enregistrement est ajouté ou créé, créant ainsi un identificateur unique pour chaque enregistrement. La propriété <STRONG>Type</STRONG> du champ doit être <STRONG>Long</STRONG>.</P>



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
<td><p>Non reconnu</p></td>
</tr>
<tr class="even">
<td><p>Objet QueryDef</p></td>
<td><p>En lecture seule</p></td>
</tr>
<tr class="odd">
<td><p>Objet Recordset</p></td>
<td><p>En lecture seule</p></td>
</tr>
<tr class="even">
<td><p>Objet Relation</p></td>
<td><p>Non reconnu</p></td>
</tr>
<tr class="odd">
<td><p>Objet TableDef</p></td>
<td><p>En lecture/écriture</p></td>
</tr>
</tbody>
</table>


Lors de la création d'un nouvel enregistrement, le paramètre de propriété **DefaultValue** est automatiquement entré comme valeur du champ. Vous pouvez modifier la valeur du champ en définissant sa propriété **Value**.

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
