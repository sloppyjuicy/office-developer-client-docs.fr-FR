---
title: Recordset2.GetRows Method (DAO)
TOCTitle: GetRows Method
ms:assetid: e5c0a082-e9d2-359f-fed5-835ab91d2311
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835959(v=office.15)
ms:contentKeyID: 48548367
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 34f6aa2ddd052a9a9ea885c76b5f62b825e8a9e5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469145"
---
# <a name="recordset2getrows-method-dao"></a>Recordset2.GetRows Method (DAO)


**S’applique à**: Access 2013 | Office 2013

Récupère plusieurs lignes d'un objet **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Syntaxe

*expression* . GetRows (***NumRows***)

*expression* Variable qui représente un objet **Recordset2** .

### <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Obligatoire/Facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>NumRows</p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Nombre de lignes à récupérer.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valeur renvoyée

Variante

## <a name="remarks"></a>Remarques

Utilisez la méthode **GetRows** pour copier des enregistrements d'un objet **Recordset**. **GetRows** renvoie un tableau à deux dimensions. Le premier indice identifie le champ, tandis que le second identifie le numéro de ligne. Par exemple, intField représente le champ et intRecord identifie le numéro de ligne :

avarRecords se transforme (intField, intRecord)

Pour obtenir la valeur du premier champ dans la deuxième ligne renvoyée, utilisez un code semblable à celui-ci :

Champ1 = avarRecords(0,1)

Pour obtenir la valeur du deuxième champ dans la première ligne, utilisez un code semblable à celui-ci :

Field2 = avarRecords(1,0)

La variable avarRecords se transforme automatiquement en tableau à deux dimensions lorsque **GetRows** renvoie les données.

Si vous demandez plus de lignes que ce qui est disponible, **GetRows** renvoie uniquement le nombre de lignes disponibles. Vous pouvez utiliser la fonction **UBound** de Visual Basic pour Applications pour déterminer le nombre de lignes réellement récupérées par **GetRows**, car la taille du tableau est définie pour correspondre au nombre de lignes renvoyées. Par exemple, si vous avez renvoyé les résultats dans un **Variant** appelé varA, vous pourriez utiliser le code suivant pour déterminer le nombre de lignes réellement renvoyé :

numReturned = UBound(varA,2) + 1

Vous devez utiliser « +1 », car la première ligne renvoyée se trouve dans l'élément 0 du tableau. Le nombre de lignes que vous pouvez extraire est limité par la quantité de mémoire disponible. Vous ne devez pas utiliser **GetRows** pour extraire une table entière dans un tableau si celle-ci est volumineuse.

Étant donné que la méthode **GetRows** renvoie tous les champs du **Recordset** dans le tableau, y compris les champs Memo et Long Binary, vous pouvez utiliser une requête qui restreint les champs renvoyés.

Une fois que vous avez appelé la méthode **GetRows**, l'enregistrement actif est positionné au niveau de la ligne non lue suivante. Autrement dit, **GetRows** a le même effet sur l’enregistrement actif que NumLignes **déplacer**.

Si vous tentez de récupérer toutes les lignes à l'aide de plusieurs appels de la méthode **GetRows**, utilisez la propriété **[EOF](recordset2-eof-property-dao.md)** pour vous assurer que vous êtes à la fin du **Recordset**. La méthode **GetRows** renvoie moins de lignes que le nombre demandé si elle est à la fin du **Recordset** ou si elle ne peut pas récupérer une ligne dans la plage demandée. Par exemple, si vous tentez de récupérer 10 enregistrements, mais que vous ne pouvez pas récupérer le cinquième, **GetRows** renvoie quatre enregistrements et rend le cinquième enregistrement actif. Cela ne génère pas une erreur d'exécution. Cela peut se produire si un autre utilisateur supprime un enregistrement dans un **Recordset** de type feuille de réponse dynamique. Consultez l'exemple pour savoir comment traiter ce problème.

## <a name="example"></a>Exemple

Cet exemple utilise la méthode **GetRows** pour récupérer un nombre spécifié de lignes à partir d'un **Recordset** et pour insérer les données obtenues dans un tableau. La méthode **GetRows** renverra moins de lignes que le nombre voulu dans deux cas : si la **fin de fichier** a été atteinte ou si la méthode **GetRows** a tenté de récupérer un enregistrement qui a été supprimé par un autre utilisateur. La fonction renvoie **False** uniquement dans le deuxième cas. La fonction GetRowsOK est obligatoire pour exécuter cette procédure.

```vb
    Sub GetRowsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strMessage As String 
     Dim intRows As Integer 
     Dim avarRecords As Variant 
     Dim intRecord As Integer 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
     "SELECT FirstName, LastName, Title " & _ 
     "FROM Employees ORDER BY LastName", dbOpenSnapshot) 
     
     With rstEmployees 
     Do While True 
     ' Get user input for number of rows. 
     strMessage = "Enter number of rows to retrieve." 
     intRows = Val(InputBox(strMessage)) 
     
     If intRows <= 0 Then Exit Do 
     
     ' If GetRowsOK is successful, print the results, 
     ' noting if the end of the file was reached. 
     If GetRowsOK(rstEmployees, intRows, _ 
     avarRecords) Then 
     If intRows > UBound(avarRecords, 2) + 1 Then 
     Debug.Print "(Not enough records in " & _ 
     "Recordset to retrieve " & intRows & _ 
     " rows.)" 
     End If 
     Debug.Print UBound(avarRecords, 2) + 1 & _ 
     " records found." 
     
     ' Print the retrieved data. 
     For intRecord = 0 To UBound(avarRecords, 2) 
     Debug.Print " " & _ 
     avarRecords(0, intRecord) & " " & _ 
     avarRecords(1, intRecord) & ", " & _ 
     avarRecords(2, intRecord) 
     Next intRecord 
     Else 
     ' Assuming the GetRows error was due to data 
     ' changes by another user, use Requery to 
     ' refresh the Recordset and start over. 
     If .Restartable Then 
     If MsgBox("GetRows failed--retry?", _ 
     vbYesNo) = vbYes Then 
     .Requery 
     Else 
     Debug.Print "GetRows failed!" 
     Exit Do 
     End If 
     Else 
     Debug.Print "GetRows failed! " & _ 
     "Recordset not Restartable!" 
     Exit Do 
     End If 
     End If 
     
     ' Because using GetRows leaves the current record 
     ' pointer at the last record accessed, move the 
     ' pointer back to the beginning of the Recordset 
     ' before looping back for another search. 
     .MoveFirst 
     Loop 
     End With 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function GetRowsOK(rstTemp As Recordset2, _ 
     intNumber As Integer, avarData As Variant) As Boolean 
     
     ' Store results of GetRows method in array. 
     avarData = rstTemp.GetRows(intNumber) 
     ' Return False only if fewer than the desired number of 
     ' rows were returned, but not because the end of the 
     ' Recordset was reached. 
     If intNumber > UBound(avarData, 2) + 1 And _ 
     Not rstTemp.EOF Then 
     GetRowsOK = False 
     Else 
     GetRowsOK = True 
     End If 
     
    End Function
```
