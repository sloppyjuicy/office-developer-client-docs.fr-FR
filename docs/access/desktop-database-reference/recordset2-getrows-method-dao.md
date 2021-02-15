---
title: Recordset2.GetRows, méthode (DAO)
TOCTitle: GetRows Method
ms:assetid: e5c0a082-e9d2-359f-fed5-835ab91d2311
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835959(v=office.15)
ms:contentKeyID: 48548367
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d7b20e2f41074e9f12198477a6abf2f1f1f9f719
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309414"
---
# <a name="recordset2getrows-method-dao"></a><span data-ttu-id="74f13-102">Recordset2.GetRows, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="74f13-102">Recordset2.GetRows method (DAO)</span></span>

<span data-ttu-id="74f13-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="74f13-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="74f13-104">Récupère plusieurs lignes à partir d’un objet **[Recordset](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="74f13-104">Retrieves multiple rows from a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="74f13-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74f13-105">Syntax</span></span>

<span data-ttu-id="74f13-106">*expression* .GetRows(***NumRows***)</span><span class="sxs-lookup"><span data-stu-id="74f13-106">*expression* .GetRows(***NumRows***)</span></span>

<span data-ttu-id="74f13-107">*expression* Variable qui représente un **objet Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="74f13-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="74f13-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74f13-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="74f13-109">Nom</span><span class="sxs-lookup"><span data-stu-id="74f13-109">Name</span></span></p></th>
<th><p><span data-ttu-id="74f13-110">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="74f13-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="74f13-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="74f13-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="74f13-112">Description</span><span class="sxs-lookup"><span data-stu-id="74f13-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74f13-113"><em>NumRows</em></span><span class="sxs-lookup"><span data-stu-id="74f13-113"><em>NumRows</em></span></span></p></td>
<td><p><span data-ttu-id="74f13-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="74f13-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="74f13-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="74f13-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="74f13-116">Nombre de lignes à récupérer.</span><span class="sxs-lookup"><span data-stu-id="74f13-116">The number of rows to retrieve.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="74f13-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="74f13-117">Return value</span></span>

<span data-ttu-id="74f13-118">Variant</span><span class="sxs-lookup"><span data-stu-id="74f13-118">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="74f13-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="74f13-119">Remarks</span></span>

<span data-ttu-id="74f13-120">Utilisez la méthode **GetRows** pour copier des enregistrements d'un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="74f13-120">Use the **GetRows** method to copy records from a **Recordset**.</span></span> <span data-ttu-id="74f13-121">**GetRows** renvoie un tableau à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="74f13-121">**GetRows** returns a two-dimensional array.</span></span> <span data-ttu-id="74f13-122">Le premier indice identifie le champ, tandis que le second identifie le numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="74f13-122">The first subscript identifies the field and the second identifies the row number.</span></span> <span data-ttu-id="74f13-123">Par exemple, `intField` représente le champ et `intRecord` identifie le numéro de ligne :</span><span class="sxs-lookup"><span data-stu-id="74f13-123">For example, `intField` represents the field, and `intRecord` identifies the row number:</span></span>

`avarRecords(intField, intRecord)`

<span data-ttu-id="74f13-124">Pour obtenir la valeur du premier champ de la deuxième ligne en renvoi, utilisez un code semblable à celui-ci :</span><span class="sxs-lookup"><span data-stu-id="74f13-124">To get the first field value in the second row returned, use code like the following:</span></span>

`field1 = avarRecords(0,1)`

<span data-ttu-id="74f13-125">Pour obtenir la valeur du deuxième champ de la première ligne, utilisez un code analogue au suivant :</span><span class="sxs-lookup"><span data-stu-id="74f13-125">To get the second field value in the first row, use code like the following:</span></span>

`field2 = avarRecords(1,0)`

<span data-ttu-id="74f13-126">La variable avarRecords devient automatiquement un tableau matriciel à deux dimensions quand **GetRows** renvoie des données.</span><span class="sxs-lookup"><span data-stu-id="74f13-126">The avarRecords variable automatically becomes a two-dimensional array when **GetRows** returns data.</span></span>

<span data-ttu-id="74f13-127">Si vous demandez plus de lignes qu'il n'y en a de disponibles, **GetRows** ne renvoie que le nombre de lignes disponibles.</span><span class="sxs-lookup"><span data-stu-id="74f13-127">If you request more rows than are available, then **GetRows** returns only the number of available rows.</span></span> <span data-ttu-id="74f13-128">Vous pouvez utiliser la fonction **UBound** de Visual Basic pour Applications pour déterminer le nombre de lignes que **GetRows** extrait réellement, car le tableau est dimensionné en fonction du nombre de lignes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="74f13-128">You can use the Visual Basic for Applications **UBound** function to determine how many rows **GetRows** actually retrieved, because the array is sized to fit the number of returned rows.</span></span> <span data-ttu-id="74f13-129">Par exemple, si vous avez renvoyé les résultats dans une **Variant** appelée varA, vous pouvez utiliser le code suivant pour déterminer le nombre de lignes réellement renvoyées :</span><span class="sxs-lookup"><span data-stu-id="74f13-129">For example, if you returned the results into a **Variant** called varA, you could use the following code to determine how many rows were actually returned:</span></span>

`numReturned = UBound(varA,2) + 1`

<span data-ttu-id="74f13-130">Vous devez utiliser « + 1 », car la première ligne renvoyée est l’élément 0 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="74f13-130">You need to use "+ 1" because the first row returned is in the 0 element of the array.</span></span> <span data-ttu-id="74f13-131">Le nombre de lignes que vous pouvez extraire est limité par la quantité de mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="74f13-131">The number of rows that you can retrieve is constrained by the amount of available memory.</span></span> <span data-ttu-id="74f13-132">Vous ne devez pas utiliser **GetRows** pour extraire une table entière dans un tableau si celle-ci est volumineuse.</span><span class="sxs-lookup"><span data-stu-id="74f13-132">You shouldn't use **GetRows** to retrieve an entire table into an array if it is large.</span></span>

<span data-ttu-id="74f13-133">Étant donné que **GetRows** renvoie tous les champs de l'objet **Recordset** dans le tableau, y compris les champs de type Memo et Long Binary, il est recommandé d'utiliser une requête qui limite le nombre de champs renvoyés.</span><span class="sxs-lookup"><span data-stu-id="74f13-133">Because **GetRows** returns all fields of the **Recordset** into the array, including Memo and Long Binary fields, you might want to use a query that restricts the fields returned.</span></span>

<span data-ttu-id="74f13-134">Suite à l'appel de **GetRows**, l'enregistrement actif est positionné au niveau de la ligne non lue suivante.</span><span class="sxs-lookup"><span data-stu-id="74f13-134">After you call **GetRows**, the current record is positioned at the next unread row.</span></span> <span data-ttu-id="74f13-135">Autrement dit, **GetRows** a le même effet sur l’enregistrement actuel que **move** numrows.</span><span class="sxs-lookup"><span data-stu-id="74f13-135">That is, **GetRows** has the same effect on the current record as **Move** numrows.</span></span>

<span data-ttu-id="74f13-p105">Si vous tentez d'extraire toutes les lignes en recourant à plusieurs appels **GetRows**, utilisez la propriété **[EOF](recordset2-eof-property-dao.md)** pour être certain d'atteindre la fin de l'objet **Recordset**. La méthode **GetRows** renvoie un nombre de lignes inférieur à ce qui a été demandé si elle se trouve à la fin de l'objet **Recordset**, ou si elle ne peut pas extraire une ligne dans la plage demandée. Par exemple, si vous essayez d'extraire 10 enregistrements mais que vous ne pouvez pas extraire le cinquième, **GetRows** renvoie quatre enregistrements et le cinquième devient l'enregistrement actif. Cela ne génère pas d'erreur d'exécution. En revanche, il pourra s'en produire une si un autre utilisateur supprime un enregistrement dans un objet **Recordset** de type feuille de réponse dynamique. Reportez-vous à l'exemple pour savoir comment traiter ce problème.</span><span class="sxs-lookup"><span data-stu-id="74f13-p105">If you are trying to retrieve all the rows by using multiple **GetRows** calls, use the **[EOF](recordset2-eof-property-dao.md)** property to be sure that you're at the end of the **Recordset**. **GetRows** returns less than the number requested if it's at the end of the **Recordset**, or if it can't retrieve a row in the range requested. For example, if you're trying to retrieve 10 records, but you can't retrieve the fifth record, **GetRows** returns four records and makes the fifth record the current record. This will not generate a run-time error. This might occur if another user deletes a record in a dynaset-type **Recordset**. See the example for a demonstration of how to handle this.</span></span>

## <a name="example"></a><span data-ttu-id="74f13-142">Exemple</span><span class="sxs-lookup"><span data-stu-id="74f13-142">Example</span></span>

<span data-ttu-id="74f13-p106">Cet exemple de code montre comment utiliser la méthode **GetRows** pour extraire un nombre déterminé de lignes d'un objet **Recordset** et pour remplir un tableau avec les données résultantes. La méthode **GetRows** peut renvoyer un nombre de lignes inférieur au nombre souhaité dans deux cas : si **EOF** a été atteint ou si **GetRows** a tenté d'extraire un enregistrement qui a été supprimé par un autre utilisateur. La fonction ne renvoie la valeur **False** que dans le deuxième cas. La fonction GetRowsOK est nécessaire à l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="74f13-p106">This example uses the **GetRows** method to retrieve a specified number of rows from a **Recordset** and to fill an array with the resulting data. The **GetRows** method will return fewer than the desired number of rows in two cases: either if **EOF** has been reached, or if **GetRows** tried to retrieve a record that was deleted by another user. The function returns **False** only if the second case occurs. The GetRowsOK function is required for this procedure to run.</span></span>

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
