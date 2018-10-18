---
<span data-ttu-id="46935-101"><<<<<<< Titre tête : conversion du Code DAO vers ADO TOCTitle : conversion du Code DAO vers ADO ms:assetid : 4720906b-d6b1-aa6d-3b18-ff828d16acae ms:mtpsurl : https://msdn.microsoft.com/library/Ff193201(v=office.15) ms:contentKeyID : ms.date 48544585 : 18/09/2015 === titre : convertir de DAO code ADO TOCTitle : code DAO convertir ADO ms:assetid : 4720906b-d6b1-aa6d-3b18-ff828d16acae ms:mtpsurl : https://msdn.microsoft.com/library/Ff193201(v=office.15) ms:contentKeyID : ms.date 48544585 : 10/16/2018</span><span class="sxs-lookup"><span data-stu-id="46935-101"><<<<<<< HEAD title: Converting DAO Code to ADO TOCTitle: Converting DAO Code to ADO ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15) ms:contentKeyID: 48544585 ms.date: 09/18/2015 ======= title: Convert DAO code to ADO TOCTitle: Convert DAO code to ADO ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15) ms:contentKeyID: 48544585 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="46935-102">maître mtps_version : v=office.15 f1_keywords :</span><span class="sxs-lookup"><span data-stu-id="46935-102">master mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="46935-103">vbaac10.chm5267115 f1_categories :</span><span class="sxs-lookup"><span data-stu-id="46935-103">vbaac10.chm5267115 f1_categories:</span></span>
- <span data-ttu-id="46935-104">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="46935-104">Office.Version=v15</span></span>
---

<span data-ttu-id="46935-105"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="46935-105"><<<<<<< HEAD</span></span>
# <a name="converting-dao-code-to-ado"></a><span data-ttu-id="46935-106">Conversion du code DAO vers ADO</span><span class="sxs-lookup"><span data-stu-id="46935-106">Converting DAO Code to ADO</span></span>
=======
# <a name="convert-dao-code-to-ado"></a><span data-ttu-id="46935-107">Conversion du code DAO vers ADO</span><span class="sxs-lookup"><span data-stu-id="46935-107">Convert DAO code to ADO</span></span>
>>>>>>> <span data-ttu-id="46935-108">master</span><span class="sxs-lookup"><span data-stu-id="46935-108">master</span></span>

<span data-ttu-id="46935-109">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="46935-109">**Applies to**: Access 2013 | Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="46935-110">Versions de la bibliothèque DAO antérieures à 3.6 ne sont pas fournies ou pris en charge dans Access.</span><span class="sxs-lookup"><span data-stu-id="46935-110">Versions of the DAO library prior to 3.6 are not provided or supported in Access.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="46935-111">DAO au mappage d’objets ADO</span><span class="sxs-lookup"><span data-stu-id="46935-111">DAO to ADO object map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="46935-112"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="46935-112"><strong>DAO</strong></span></span></p></th>
<span data-ttu-id="46935-113"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="46935-113"><<<<<<< HEAD</span></span>
<th><p><span data-ttu-id="46935-114"><strong>ADO (ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="46935-114"><strong>ADO(ADODB)</strong></span></span></p></th>
=======
<th><p><span data-ttu-id="46935-115"><strong>ADO (ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="46935-115"><strong>ADO (ADODB)</strong></span></span></p></th><span data-ttu-id="46935-116">
>>>>>>>forme de base</span><span class="sxs-lookup"><span data-stu-id="46935-116">
>>>>>>> master</span></span>
<th><p><span data-ttu-id="46935-117"><strong>Remarque</strong></span><span class="sxs-lookup"><span data-stu-id="46935-117"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46935-118">DBEngine</span><span class="sxs-lookup"><span data-stu-id="46935-118">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="46935-119">Aucune</span><span class="sxs-lookup"><span data-stu-id="46935-119">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46935-120">Workspace</span><span class="sxs-lookup"><span data-stu-id="46935-120">Workspace</span></span></p></td>
<td><p><span data-ttu-id="46935-121">Aucune</span><span class="sxs-lookup"><span data-stu-id="46935-121">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46935-122">Base de données</span><span class="sxs-lookup"><span data-stu-id="46935-122">Database</span></span></p></td>
<td><p><span data-ttu-id="46935-123">Connection</span><span class="sxs-lookup"><span data-stu-id="46935-123">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46935-124">Recordset</span><span class="sxs-lookup"><span data-stu-id="46935-124">Recordset</span></span></p></td>
<td><p><span data-ttu-id="46935-125">Recordset</span><span class="sxs-lookup"><span data-stu-id="46935-125">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46935-126">Dynaset-Type</span><span class="sxs-lookup"><span data-stu-id="46935-126">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="46935-127">Keyset</span><span class="sxs-lookup"><span data-stu-id="46935-127">Keyset</span></span></p></td>
<span data-ttu-id="46935-128"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="46935-128"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="46935-129">Extrait une série de pointeurs vers les enregistrements du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="46935-129">Retrieves a set of pointers to the records in the recordset</span></span></p></td>
=======
<td><p><span data-ttu-id="46935-130">Récupère un ensemble de pointeurs vers les enregistrements du jeu d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="46935-130">Retrieves a set of pointers to the records in the recordset.</span></span></p></td><span data-ttu-id="46935-131">
>>>>>>>forme de base</span><span class="sxs-lookup"><span data-stu-id="46935-131">
>>>>>>> master</span></span>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46935-132">Snapshot-Type</span><span class="sxs-lookup"><span data-stu-id="46935-132">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="46935-133">Static</span><span class="sxs-lookup"><span data-stu-id="46935-133">Static</span></span></p></td>
<span data-ttu-id="46935-134"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="46935-134"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="46935-135">Tous deux extraient des enregistrements complets mais un jeu d'enregistrements Static est actualisable.</span><span class="sxs-lookup"><span data-stu-id="46935-135">Both retrieve full records but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46935-136">Table-Type</span><span class="sxs-lookup"><span data-stu-id="46935-136">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="46935-137">Keyset avec l'option adCmdTableDirect</span><span class="sxs-lookup"><span data-stu-id="46935-137">Keyset with adCmdTableDirect Option</span></span></p></td>
=======
<td><p><span data-ttu-id="46935-138">Tous deux extraient des enregistrements complets mais un jeu d’enregistrements statique peut être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="46935-138">Both retrieve full records, but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46935-139">Table-Type</span><span class="sxs-lookup"><span data-stu-id="46935-139">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="46935-140">Keyset avec l’option adCmdTableDirect.</span><span class="sxs-lookup"><span data-stu-id="46935-140">Keyset with adCmdTableDirect option.</span></span></p></td><span data-ttu-id="46935-141">
>>>>>>>forme de base</span><span class="sxs-lookup"><span data-stu-id="46935-141">
>>>>>>> master</span></span>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46935-142">Champ</span><span class="sxs-lookup"><span data-stu-id="46935-142">Field</span></span></p></td>
<td><p><span data-ttu-id="46935-143">Champ</span><span class="sxs-lookup"><span data-stu-id="46935-143">Field</span></span></p></td>
<span data-ttu-id="46935-144"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="46935-144"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="46935-145">Quand référencée dans un jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="46935-145">When referred to in a recordset</span></span></p></td>
=======
<td><p><span data-ttu-id="46935-146">Quand référencée dans un jeu d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="46935-146">When referred to in a recordset.</span></span></p></td><span data-ttu-id="46935-147">
>>>>>>>forme de base</span><span class="sxs-lookup"><span data-stu-id="46935-147">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="46935-148">DAO</span><span class="sxs-lookup"><span data-stu-id="46935-148">DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="46935-149">Ouvrir un jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="46935-149">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="46935-150">Modifier un jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="46935-150">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="46935-151">ADO</span><span class="sxs-lookup"><span data-stu-id="46935-151">ADO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="46935-152">Ouvrir un jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="46935-152">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="46935-153">Modifier un jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="46935-153">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
<span data-ttu-id="46935-154"><<<<<<< Déplacement tête concentrer à partir de l’enregistrement en cours via **MoveNext, MoveLast, MoveFirst, MovePrevious** sans d’abord à l’aide de la méthode **CancelUpdate** exécutera implicitement la méthode **Update** .</span><span class="sxs-lookup"><span data-stu-id="46935-154"><<<<<<< HEAD Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method will implicitly execute the **Update** method.</span></span>
> <span data-ttu-id="46935-155">=== Déplacement du curseur à partir de l’enregistrement en cours via **MoveNext, MoveLast, MoveFirst, MovePrevious** sans utiliser préalablement la méthode **CancelUpdate** implicitement exécute la méthode de **mise à jour** .</span><span class="sxs-lookup"><span data-stu-id="46935-155">======= Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method implicitly executes the **Update** method.</span></span>
>>>>>>> <span data-ttu-id="46935-156">master</span><span class="sxs-lookup"><span data-stu-id="46935-156">master</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="46935-157">À propos des collaborateurs</span><span class="sxs-lookup"><span data-stu-id="46935-157">About the contributors</span></span>

<span data-ttu-id="46935-158">**Lien fourni par** la Communauté [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="46935-158">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="46935-159">UtterAccess est le premier forum d'aide et wiki de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="46935-159">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="46935-160">Choix entre DAO et ADO</span><span class="sxs-lookup"><span data-stu-id="46935-160">Choosing between DAO and ADO</span></span>](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<span data-ttu-id="46935-161"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="46935-161"><<<<<<< HEAD</span></span>

=======
<br/>
>>>>>>> <span data-ttu-id="46935-162">master</span><span class="sxs-lookup"><span data-stu-id="46935-162">master</span></span>

