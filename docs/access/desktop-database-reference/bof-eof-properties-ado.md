---
<span data-ttu-id="bf81a-101"><<<<<<< Titre tête : BOF, EOF propriétés (ADO) TOCTitle : BOF, EOF propriétés (ADO) === titre : BOF, propriétés EOF (ADO) TOCTitle : BOF, propriétés EOF (ADO)</span><span class="sxs-lookup"><span data-stu-id="bf81a-101"><<<<<<< HEAD title: BOF, EOF Properties (ADO) TOCTitle: BOF, EOF Properties (ADO) ======= title: BOF, EOF properties (ADO) TOCTitle: BOF, EOF properties (ADO)</span></span>
>>>>>>> <span data-ttu-id="bf81a-102">Master ms:assetid : f797e140-5572-1a4d-9afc-285f6a3868a8 ms:mtpsurl : https://msdn.microsoft.com/library/JJ250260(v=office.15) ms:contentKeyID : ms.date 48548768 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="bf81a-102">master ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15) ms:contentKeyID: 48548768 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="bf81a-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="bf81a-103"><<<<<<< HEAD</span></span>
# <a name="bof-eof-properties-ado"></a><span data-ttu-id="bf81a-104">BOF, EOF, propriétés (ADO)</span><span class="sxs-lookup"><span data-stu-id="bf81a-104">BOF, EOF Properties (ADO)</span></span>
=======
# <a name="bof-eof-properties-ado"></a><span data-ttu-id="bf81a-105">BOF, propriétés EOF (ADO)</span><span class="sxs-lookup"><span data-stu-id="bf81a-105">BOF, EOF properties (ADO)</span></span>
>>>>>>> <span data-ttu-id="bf81a-106">master</span><span class="sxs-lookup"><span data-stu-id="bf81a-106">master</span></span>


<span data-ttu-id="bf81a-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf81a-107">**Applies to**: Access 2013 | Office 2013</span></span>

  - <span data-ttu-id="bf81a-108">**BOF**  Indique que la position d'enregistrement actuelle se trouve avant le premier enregistrement d'un objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="bf81a-108">**BOF** — Indicates that the current record position is before the first record in a [Recordset](recordset-object-ado.md) object.</span></span>

  - <span data-ttu-id="bf81a-109">**EOF**  Indique que la position d'enregistrement actuelle se trouve après le dernier enregistrement d'un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="bf81a-109">**EOF** — Indicates that the current record position is after the last record in a **Recordset** object.</span></span>

<span data-ttu-id="bf81a-110"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="bf81a-110"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="bf81a-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bf81a-111">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="bf81a-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bf81a-112">Return value</span></span>
>>>>>>> <span data-ttu-id="bf81a-113">master</span><span class="sxs-lookup"><span data-stu-id="bf81a-113">master</span></span>

<span data-ttu-id="bf81a-114">Les propriétés **BOF** et **EOF** retournent des valeurs de type **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="bf81a-114">The **BOF** and **EOF** properties return **Boolean** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf81a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="bf81a-115">Remarks</span></span>

<span data-ttu-id="bf81a-116">Utilisez les propriétés **BOF** et **EOF** pour déterminer si un objet **Recordset** contient des enregistrements ou si vous avez dépassé les limites d'un objet **Recordset** lorsque vous vous déplacez d'un enregistrement à l'autre.</span><span class="sxs-lookup"><span data-stu-id="bf81a-116">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="bf81a-117">La propriété **BOF** retourne la valeur **True** (-1) si la position d'enregistrement actuelle se trouve avant le premier enregistrement et la valeur **False** (0) si la position d'enregistrement actuelle se trouve au niveau du premier enregistrement ou après celui-ci.</span><span class="sxs-lookup"><span data-stu-id="bf81a-117">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="bf81a-118">La propriété **EOF** renvoie la valeur **True** si la position d'enregistrement actuelle se trouve après le dernier enregistrement et la valeur **False** si la position d'enregistrement actuelle se trouve au niveau du dernier enregistrement ou avant celui-ci.</span><span class="sxs-lookup"><span data-stu-id="bf81a-118">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="bf81a-119">Si l'une des propriétés **BOF** ou **EOF** a la valeur **True**, il n'y a pas d'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="bf81a-119">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="bf81a-p101">Si vous ouvrez un objet **Recordset** qui ne contient pas d’enregistrement, les propriétés **BOF** et **EOF** ont la valeur **True** (reportez-vous à la propriété [RecordCount](recordcount-property-ado.md) pour plus d’informations sur cet état d’un objet **Recordset**). Lorsque vous ouvrez un objet **Recordset** qui contient au moins un enregistrement, le premier enregistrement correspond au dernier enregistrement et les propriétés **BOF** et **EOF** ont la valeur **False**.</span><span class="sxs-lookup"><span data-stu-id="bf81a-p101">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True** (see the [RecordCount](recordcount-property-ado.md) property for more information about this state of a **Recordset**). When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="bf81a-122">Si vous supprimez le dernier enregistrement encore présent dans l'objet **Recordset**, les propriétés **BOF** et **EOF** peuvent conserver la valeur **False** jusqu'à ce que vous tentiez de repositionner l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="bf81a-122">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="bf81a-123">Ce tableau répertorie les méthodes **Move** autorisées avec les différentes combinaisons des propriétés **BOF** et **EOF**.</span><span class="sxs-lookup"><span data-stu-id="bf81a-123">This table shows which **Move** methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="bf81a-124">MoveFirst,</span><span class="sxs-lookup"><span data-stu-id="bf81a-124">MoveFirst,</span></span><br />
<span data-ttu-id="bf81a-125">MoveLast</span><span class="sxs-lookup"><span data-stu-id="bf81a-125">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="bf81a-126">MovePrevious,</span><span class="sxs-lookup"><span data-stu-id="bf81a-126">MovePrevious,</span></span><br />
<span data-ttu-id="bf81a-127">Déplacer &lt; 0</span><span class="sxs-lookup"><span data-stu-id="bf81a-127">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="bf81a-128">Move 0</span><span class="sxs-lookup"><span data-stu-id="bf81a-128">Move 0</span></span></p></th>
<th><p><span data-ttu-id="bf81a-129">MoveNext,</span><span class="sxs-lookup"><span data-stu-id="bf81a-129">MoveNext,</span></span><br />
<span data-ttu-id="bf81a-130">Déplacer &gt; 0</span><span class="sxs-lookup"><span data-stu-id="bf81a-130">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf81a-131"><strong>BOF = True,</strong></span><span class="sxs-lookup"><span data-stu-id="bf81a-131"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="bf81a-132">
<strong>EOF = False</strong></span><span class="sxs-lookup"><span data-stu-id="bf81a-132">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="bf81a-133">Autorisé</span><span class="sxs-lookup"><span data-stu-id="bf81a-133">Allowed</span></span></p></td>
<td><p><span data-ttu-id="bf81a-134">Erreur</span><span class="sxs-lookup"><span data-stu-id="bf81a-134">Error</span></span></p></td>
<td><p><span data-ttu-id="bf81a-135">Erreur</span><span class="sxs-lookup"><span data-stu-id="bf81a-135">Error</span></span></p></td>
<td><p><span data-ttu-id="bf81a-136">Autorisé</span><span class="sxs-lookup"><span data-stu-id="bf81a-136">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf81a-137"><strong>BOF = False,</strong></span><span class="sxs-lookup"><span data-stu-id="bf81a-137"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="bf81a-138">
<strong>EOF = True</strong></span><span class="sxs-lookup"><span data-stu-id="bf81a-138">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="bf81a-139">Autorisé</span><span class="sxs-lookup"><span data-stu-id="bf81a-139">Allowed</span></span></p></td>
<td><p><span data-ttu-id="bf81a-140">Autorisé</span><span class="sxs-lookup"><span data-stu-id="bf81a-140">Allowed</span></span></p></td>
<td><p><span data-ttu-id="bf81a-141">Erreur</span><span class="sxs-lookup"><span data-stu-id="bf81a-141">Error</span></span></p></td>
<td><p><span data-ttu-id="bf81a-142">Erreur</span><span class="sxs-lookup"><span data-stu-id="bf81a-142">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf81a-143">Les deux propriétés ont la valeur <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="bf81a-143">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="bf81a-144">Erreur</span><span class="sxs-lookup"><span data-stu-id="bf81a-144">Error</span></span></p></td>
<td><p><span data-ttu-id="bf81a-145">Erreur</span><span class="sxs-lookup"><span data-stu-id="bf81a-145">Error</span></span></p></td>
<td><p><span data-ttu-id="bf81a-146">Erreur</span><span class="sxs-lookup"><span data-stu-id="bf81a-146">Error</span></span></p></td>
<td><p><span data-ttu-id="bf81a-147">Erreur</span><span class="sxs-lookup"><span data-stu-id="bf81a-147">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf81a-148">Les deux propriétés ont la valeur <strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="bf81a-148">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="bf81a-149">Autorisé</span><span class="sxs-lookup"><span data-stu-id="bf81a-149">Allowed</span></span></p></td>
<td><p><span data-ttu-id="bf81a-150">Autorisé</span><span class="sxs-lookup"><span data-stu-id="bf81a-150">Allowed</span></span></p></td>
<td><p><span data-ttu-id="bf81a-151">Autorisé</span><span class="sxs-lookup"><span data-stu-id="bf81a-151">Allowed</span></span></p></td>
<td><p><span data-ttu-id="bf81a-152">Autorisé</span><span class="sxs-lookup"><span data-stu-id="bf81a-152">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bf81a-153">Même si une méthode **Move** est autorisée, rien ne garantit que la méthode parviendra à localiser un enregistrement. Cela signifie uniquement que l'appel de la méthode **Move** spécifiée ne génère pas d'erreur.</span><span class="sxs-lookup"><span data-stu-id="bf81a-153">Allowing a **Move** method doesn't guarantee that the method will successfully locate a record; it only means that calling the specified **Move** method won't generate an error.</span></span>

<span data-ttu-id="bf81a-154">Le tableau ci-dessous répertorie les valeurs prises par les propriétés **BOF** et **EOF** lorsque vous appelez différentes méthodes **Move** et que vous ne parvenez pas à trouver un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="bf81a-154">The following table shows what happens to the **BOF** and **EOF** property settings when you call various **Move** methods but are unable to successfully locate a record.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="bf81a-155">BOF</span><span class="sxs-lookup"><span data-stu-id="bf81a-155">BOF</span></span></p></th>
<th><p><span data-ttu-id="bf81a-156">EOF</span><span class="sxs-lookup"><span data-stu-id="bf81a-156">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf81a-157"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="bf81a-157"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="bf81a-158">La valeur <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="bf81a-158">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="bf81a-159">La valeur <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="bf81a-159">Set to <strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf81a-160"><strong>Move</strong> 0</span><span class="sxs-lookup"><span data-stu-id="bf81a-160"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="bf81a-161">Aucune modification</span><span class="sxs-lookup"><span data-stu-id="bf81a-161">No change</span></span></p></td>
<td><p><span data-ttu-id="bf81a-162">Aucune modification</span><span class="sxs-lookup"><span data-stu-id="bf81a-162">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf81a-163"><strong>MovePrevious</strong>, <strong>déplacer</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="bf81a-163"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="bf81a-164">Prend la valeur <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="bf81a-164">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="bf81a-165">Aucune modification</span><span class="sxs-lookup"><span data-stu-id="bf81a-165">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf81a-166"><strong>MoveNext</strong>, <strong>déplacer</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="bf81a-166"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="bf81a-167">Aucune modification</span><span class="sxs-lookup"><span data-stu-id="bf81a-167">No change</span></span></p></td>
<td><p><span data-ttu-id="bf81a-168">Prend la valeur <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="bf81a-168">Set to <strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

