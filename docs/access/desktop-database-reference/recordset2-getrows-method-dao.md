---
title: Recordset2.GetRows, méthode (DAO)
TOCTitle: GetRows Method
ms:assetid: e5c0a082-e9d2-359f-fed5-835ab91d2311
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835959(v=office.15)
ms:contentKeyID: 48548367
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b3598710f74c84e2e97f35de31a30dccc4944421
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63718082"
---
# <a name="recordset2getrows-method-dao"></a>Recordset2.GetRows, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Récupère plusieurs lignes à partir d’un objet **[Recordset](recordset-object-dao.md)** .

## <a name="syntax"></a>Syntaxe

*expression* .GetRows(***NumRows***)

*expression* Variable qui représente un **objet Recordset2** .

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Obligatoire/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>NumRows</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Nombre de lignes à récupérer.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valeur renvoyée

Variant

## <a name="remarks"></a>Remarques

Utilisez la méthode **GetRows** pour copier des enregistrements d'un objet **Recordset**. **GetRows** renvoie un tableau à deux dimensions. Le premier indice identifie le champ, tandis que le second identifie le numéro de ligne. Par exemple, `intField` représente le champ et `intRecord` identifie le numéro de ligne :

`avarRecords(intField, intRecord)`

Pour obtenir la valeur du premier champ de la deuxième ligne en renvoi, utilisez un code semblable à celui-ci :

`field1 = avarRecords(0,1)`

Pour obtenir la valeur du deuxième champ de la première ligne, utilisez un code analogue au suivant :

`field2 = avarRecords(1,0)`

La variable avarRecords devient automatiquement un tableau matriciel à deux dimensions quand **GetRows** renvoie des données.

Si vous demandez plus de lignes qu'il n'y en a de disponibles, **GetRows** ne renvoie que le nombre de lignes disponibles. Vous pouvez utiliser la fonction **UBound** de Visual Basic pour Applications pour déterminer le nombre de lignes que **GetRows** a extrait réellement, car le tableau est dimensionné en fonction du nombre de lignes renvoyées. Par exemple, si vous avez renvoyé les résultats dans un objet **Variant** appelé varA, vous pouvez utiliser le code suivant pour déterminer le nombre de lignes réellement renvoyées :

`numReturned = UBound(varA,2) + 1`

Vous devez utiliser « +1 », car la première ligne renvoyée se trouve dans l'élément 0 du tableau. Le nombre de lignes que vous pouvez extraire est limité par la quantité de mémoire disponible. Vous ne devez pas utiliser **GetRows** pour extraire une table entière dans un tableau si celle-ci est volumineuse.

Étant donné que **GetRows** renvoie tous les champs de l'objet **Recordset** dans le tableau, y compris les champs de type Memo et Long Binary, il est recommandé d'utiliser une requête qui limite le nombre de champs renvoyés.

Suite à l'appel de **GetRows**, l'enregistrement actif est positionné au niveau de la ligne non lue suivante. Autrement dit, **GetRows** a le même effet sur l’enregistrement actuel que **Movenumrows**.

Si vous tentez d'extraire toutes les lignes en recourant à plusieurs appels **GetRows**, utilisez la propriété **[EOF](recordset2-eof-property-dao.md)** pour être certain d'atteindre la fin de l'objet **Recordset**. La méthode **GetRows** renvoie un nombre de lignes inférieur à ce qui a été demandé si elle se trouve à la fin de l'objet **Recordset**, ou si elle ne peut pas extraire une ligne dans la plage demandée. Par exemple, si vous essayez d'extraire 10 enregistrements mais que vous ne pouvez pas extraire le cinquième, **GetRows** renvoie quatre enregistrements et le cinquième devient l'enregistrement actif. Cela ne génère pas d'erreur d'exécution. En revanche, il pourra s'en produire une si un autre utilisateur supprime un enregistrement dans un objet **Recordset** de type feuille de réponse dynamique. Reportez-vous à l'exemple pour savoir comment traiter ce problème.

## <a name="example"></a>Exemple

Cet exemple de code montre comment utiliser la méthode **GetRows** pour extraire un nombre déterminé de lignes d'un objet **Recordset** et pour remplir un tableau avec les données résultantes. La méthode **GetRows** peut renvoyer un nombre de lignes inférieur au nombre souhaité dans deux cas : si **EOF** a été atteint ou si **GetRows** a tenté d'extraire un enregistrement qui a été supprimé par un autre utilisateur. La fonction ne renvoie la valeur **False** que dans le deuxième cas. La fonction GetRowsOK est nécessaire à l'exécution de cette procédure.

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
