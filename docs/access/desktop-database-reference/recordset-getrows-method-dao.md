---
title: Méthode Recordset.GetRows (DAO)
TOCTitle: GetRows Method
ms:assetid: 59f6e4f0-e7b1-db60-31c7-3338b66d3345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194427(v=office.15)
ms:contentKeyID: 48545031
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053362
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1b0df2371ec9da675346cc24fd53d602cf69a170
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931238"
---
# <a name="recordsetgetrows-method-dao"></a><span data-ttu-id="14438-102">Méthode Recordset.GetRows (DAO)</span><span class="sxs-lookup"><span data-stu-id="14438-102">Recordset.GetRows method (DAO)</span></span>


<span data-ttu-id="14438-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="14438-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="14438-104">Récupère plusieurs lignes d'un objet **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="14438-104">Retrieves multiple rows from a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="14438-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14438-105">Syntax</span></span>

<span data-ttu-id="14438-106">*expression* . GetRows (***NumRows***)</span><span class="sxs-lookup"><span data-stu-id="14438-106">*expression* .GetRows(***NumRows***)</span></span>

<span data-ttu-id="14438-107">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="14438-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="14438-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14438-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="14438-109">Name</span><span class="sxs-lookup"><span data-stu-id="14438-109">Name</span></span></p></th>
<th><p><span data-ttu-id="14438-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="14438-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="14438-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="14438-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="14438-112">Description</span><span class="sxs-lookup"><span data-stu-id="14438-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14438-113">NumRows</span><span class="sxs-lookup"><span data-stu-id="14438-113">NumRows</span></span></p></td>
<td><p><span data-ttu-id="14438-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="14438-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="14438-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="14438-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="14438-116">Nombre de lignes à récupérer.</span><span class="sxs-lookup"><span data-stu-id="14438-116">The number of rows to retrieve.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="14438-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="14438-117">Return value</span></span>

<span data-ttu-id="14438-118">Variant</span><span class="sxs-lookup"><span data-stu-id="14438-118">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="14438-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="14438-119">Remarks</span></span>

<span data-ttu-id="14438-p101">Utilisez la méthode **GetRows** pour copier des enregistrements d'un objet **Recordset**. **GetRows** renvoie un tableau à deux dimensions. Le premier indice identifie le champ, tandis que le second identifie le numéro de ligne. Par exemple, intField représente le champ et intRecord identifie le numéro de ligne :</span><span class="sxs-lookup"><span data-stu-id="14438-p101">Use the **GetRows** method to copy records from a **Recordset**. **GetRows** returns a two-dimensional array. The first subscript identifies the field and the second identifies the row number. For example, intField represents the field, and intRecord identifies the row number:</span></span>

<span data-ttu-id="14438-124">avarRecords se transforme (intField, intRecord)</span><span class="sxs-lookup"><span data-stu-id="14438-124">avarRecords(intField, intRecord)</span></span>

<span data-ttu-id="14438-125">Pour obtenir la valeur du premier champ dans la deuxième ligne renvoyée, utilisez un code semblable à celui-ci :</span><span class="sxs-lookup"><span data-stu-id="14438-125">To get the first field value in the second row returned, use code like the following:</span></span>

<span data-ttu-id="14438-126">Champ1 = avarRecords(0,1)</span><span class="sxs-lookup"><span data-stu-id="14438-126">field1 = avarRecords(0,1)</span></span>

<span data-ttu-id="14438-127">Pour obtenir la valeur du deuxième champ dans la première ligne, utilisez un code semblable à celui-ci :</span><span class="sxs-lookup"><span data-stu-id="14438-127">To get the second field value in the first row, use code like the following:</span></span>

<span data-ttu-id="14438-128">Field2 = avarRecords(1,0)</span><span class="sxs-lookup"><span data-stu-id="14438-128">field2 = avarRecords(1,0)</span></span>

<span data-ttu-id="14438-129">La variable avarRecords se transforme automatiquement en tableau à deux dimensions lorsque **GetRows** renvoie les données.</span><span class="sxs-lookup"><span data-stu-id="14438-129">The avarRecords variable automatically becomes a two-dimensional array when **GetRows** returns data.</span></span>

<span data-ttu-id="14438-130">Si vous demandez plus de lignes que ce qui est disponible, **GetRows** renvoie uniquement le nombre de lignes disponibles.</span><span class="sxs-lookup"><span data-stu-id="14438-130">If you request more rows than are available, then **GetRows** returns only the number of available rows.</span></span> <span data-ttu-id="14438-131">Vous pouvez utiliser la fonction **UBound** de Visual Basic pour Applications pour déterminer le nombre de lignes réellement récupérées par **GetRows**, car la taille du tableau est définie pour correspondre au nombre de lignes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="14438-131">You can use the Visual Basic for Applications **UBound** function to determine how many rows **GetRows** actually retrieved, because the array is sized to fit the number of returned rows.</span></span> <span data-ttu-id="14438-132">Par exemple, si vous avez renvoyé les résultats dans un **Variant** appelé varA, vous pourriez utiliser le code suivant pour déterminer le nombre de lignes réellement renvoyé :</span><span class="sxs-lookup"><span data-stu-id="14438-132">For example, if you returned the results into a **Variant** called varA, you could use the following code to determine how many rows were actually returned:</span></span>

<span data-ttu-id="14438-133">numReturned = UBound(varA,2) + 1</span><span class="sxs-lookup"><span data-stu-id="14438-133">numReturned = UBound(varA,2) + 1</span></span>

<span data-ttu-id="14438-p103">Vous devez utiliser « +1 », car la première ligne renvoyée se trouve dans l'élément 0 du tableau. Le nombre de lignes que vous pouvez extraire est limité par la quantité de mémoire disponible. Vous ne devez pas utiliser **GetRows** pour extraire une table entière dans un tableau si celle-ci est volumineuse.</span><span class="sxs-lookup"><span data-stu-id="14438-p103">You need to use "+ 1" because the first row returned is in the 0 element of the array. The number of rows that you can retrieve is constrained by the amount of available memory. You shouldn't use **GetRows** to retrieve an entire table into an array if it is large.</span></span>

<span data-ttu-id="14438-137">Étant donné que la méthode **GetRows** renvoie tous les champs du **Recordset** dans le tableau, y compris les champs Memo et Long Binary, vous pouvez utiliser une requête qui restreint les champs renvoyés.</span><span class="sxs-lookup"><span data-stu-id="14438-137">Because **GetRows** returns all fields of the **Recordset** into the array, including Memo and Long Binary fields, you might want to use a query that restricts the fields returned.</span></span>

<span data-ttu-id="14438-138">Une fois que vous avez appelé la méthode **GetRows**, l'enregistrement actif est positionné au niveau de la ligne non lue suivante.</span><span class="sxs-lookup"><span data-stu-id="14438-138">After you call **GetRows**, the current record is positioned at the next unread row.</span></span> <span data-ttu-id="14438-139">Autrement dit, **GetRows** a le même effet sur l’enregistrement actif que NumLignes **déplacer** .</span><span class="sxs-lookup"><span data-stu-id="14438-139">That is, **GetRows** has the same effect on the current record as **Move** numrows.</span></span>

<span data-ttu-id="14438-p105">Si vous tentez de récupérer toutes les lignes à l'aide de plusieurs appels de la méthode **GetRows**, utilisez la propriété **[EOF](recordset-eof-property-dao.md)** pour vous assurer que vous êtes à la fin du **Recordset**. La méthode **GetRows** renvoie moins de lignes que le nombre demandé si elle est à la fin du **Recordset** ou si elle ne peut pas récupérer une ligne dans la plage demandée. Par exemple, si vous tentez de récupérer 10 enregistrements, mais que vous ne pouvez pas récupérer le cinquième, **GetRows** renvoie quatre enregistrements et rend le cinquième enregistrement actif. Cela ne génère pas une erreur d'exécution. Cela peut se produire si un autre utilisateur supprime un enregistrement dans un **Recordset** de type feuille de réponse dynamique. Consultez l'exemple pour savoir comment traiter ce problème.</span><span class="sxs-lookup"><span data-stu-id="14438-p105">If you are trying to retrieve all the rows by using multiple **GetRows** calls, use the **[EOF](recordset-eof-property-dao.md)** property to be sure that you're at the end of the **Recordset**. **GetRows** returns less than the number requested if it's at the end of the **Recordset**, or if it can't retrieve a row in the range requested. For example, if you're trying to retrieve 10 records, but you can't retrieve the fifth record, **GetRows** returns four records and makes the fifth record the current record. This will not generate a run-time error. This might occur if another user deletes a record in a dynaset-type **Recordset**. See the example for a demonstration of how to handle this.</span></span>

## <a name="example"></a><span data-ttu-id="14438-146">Exemple</span><span class="sxs-lookup"><span data-stu-id="14438-146">Example</span></span>

<span data-ttu-id="14438-p106">Cet exemple utilise la méthode **GetRows** pour récupérer un nombre spécifié de lignes à partir d'un **Recordset** et pour insérer les données obtenues dans un tableau. La méthode **GetRows** renverra moins de lignes que le nombre voulu dans deux cas : si la **fin de fichier** a été atteinte ou si la méthode **GetRows** a tenté de récupérer un enregistrement qui a été supprimé par un autre utilisateur. La fonction renvoie **False** uniquement dans le deuxième cas. La fonction GetRowsOK est obligatoire pour exécuter cette procédure.</span><span class="sxs-lookup"><span data-stu-id="14438-p106">This example uses the **GetRows** method to retrieve a specified number of rows from a **Recordset** and to fill an array with the resulting data. The **GetRows** method will return fewer than the desired number of rows in two cases: either if **EOF** has been reached, or if **GetRows** tried to retrieve a record that was deleted by another user. The function returns **False** only if the second case occurs. The GetRowsOK function is required for this procedure to run.</span></span>

```vb
    Sub GetRowsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
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
     
    Function GetRowsOK(rstTemp As Recordset, _ 
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
