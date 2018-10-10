---
title: Conversion du code DAO vers ADO
TOCTitle: Converting DAO Code to ADO
ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15)
ms:contentKeyID: 48544585
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5267115
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7039d9322956e4fcbca4081eff75868ccf306e25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469097"
---
# <a name="converting-dao-code-to-ado"></a><span data-ttu-id="90b23-102">Conversion du code DAO vers ADO</span><span class="sxs-lookup"><span data-stu-id="90b23-102">Converting DAO Code to ADO</span></span>

<span data-ttu-id="90b23-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="90b23-103">**Applies to**: Access 2013 | Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="90b23-104">Versions de la bibliothèque DAO antérieures à 3.6 ne sont pas fournies ou pris en charge dans Access.</span><span class="sxs-lookup"><span data-stu-id="90b23-104">Versions of the DAO library prior to 3.6 are not provided or supported in Access.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="90b23-105">DAO au mappage d’objets ADO</span><span class="sxs-lookup"><span data-stu-id="90b23-105">DAO to ADO object map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="90b23-106"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="90b23-106"><strong>DAO</strong></span></span></p></th>
<th><p><span data-ttu-id="90b23-107"><strong>ADO (ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="90b23-107"><strong>ADO(ADODB)</strong></span></span></p></th>
<th><p><span data-ttu-id="90b23-108"><strong>Remarque</strong></span><span class="sxs-lookup"><span data-stu-id="90b23-108"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90b23-109">DBEngine</span><span class="sxs-lookup"><span data-stu-id="90b23-109">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="90b23-110">Aucune</span><span class="sxs-lookup"><span data-stu-id="90b23-110">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90b23-111">Workspace</span><span class="sxs-lookup"><span data-stu-id="90b23-111">Workspace</span></span></p></td>
<td><p><span data-ttu-id="90b23-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="90b23-112">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90b23-113">Base de données</span><span class="sxs-lookup"><span data-stu-id="90b23-113">Database</span></span></p></td>
<td><p><span data-ttu-id="90b23-114">Connection</span><span class="sxs-lookup"><span data-stu-id="90b23-114">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90b23-115">Recordset</span><span class="sxs-lookup"><span data-stu-id="90b23-115">Recordset</span></span></p></td>
<td><p><span data-ttu-id="90b23-116">Recordset</span><span class="sxs-lookup"><span data-stu-id="90b23-116">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90b23-117">Dynaset-Type</span><span class="sxs-lookup"><span data-stu-id="90b23-117">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="90b23-118">Keyset</span><span class="sxs-lookup"><span data-stu-id="90b23-118">Keyset</span></span></p></td>
<td><p><span data-ttu-id="90b23-119">Extrait une série de pointeurs vers les enregistrements du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="90b23-119">Retrieves a set of pointers to the records in the recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90b23-120">Snapshot-Type</span><span class="sxs-lookup"><span data-stu-id="90b23-120">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="90b23-121">Static</span><span class="sxs-lookup"><span data-stu-id="90b23-121">Static</span></span></p></td>
<td><p><span data-ttu-id="90b23-122">Tous deux extraient des enregistrements complets mais un jeu d'enregistrements Static est actualisable.</span><span class="sxs-lookup"><span data-stu-id="90b23-122">Both retrieve full records but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90b23-123">Table-Type</span><span class="sxs-lookup"><span data-stu-id="90b23-123">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="90b23-124">Keyset avec l'option adCmdTableDirect</span><span class="sxs-lookup"><span data-stu-id="90b23-124">Keyset with adCmdTableDirect Option</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90b23-125">Field</span><span class="sxs-lookup"><span data-stu-id="90b23-125">Field</span></span></p></td>
<td><p><span data-ttu-id="90b23-126">Field</span><span class="sxs-lookup"><span data-stu-id="90b23-126">Field</span></span></p></td>
<td><p><span data-ttu-id="90b23-127">Quand référencée dans un jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="90b23-127">When referred to in a recordset</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="90b23-128">DAO</span><span class="sxs-lookup"><span data-stu-id="90b23-128">DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="90b23-129">Ouvrir un jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="90b23-129">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="90b23-130">Modifier un jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="90b23-130">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="90b23-131">ADO</span><span class="sxs-lookup"><span data-stu-id="90b23-131">ADO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="90b23-132">Ouvrir un jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="90b23-132">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="90b23-133">Modifier un jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="90b23-133">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> <span data-ttu-id="90b23-134">Le déplacement du curseur depuis l'enregistrement en cours via **MoveNext, MoveLast, MoveFirst, MovePrevious** sans utiliser préalablement la méthode **CancelUpdate** exécutera implicitement la méthode **Update**.</span><span class="sxs-lookup"><span data-stu-id="90b23-134">Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method will implicitly execute the **Update** method.</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="90b23-135">À propos des collaborateurs</span><span class="sxs-lookup"><span data-stu-id="90b23-135">About the contributors</span></span>

<span data-ttu-id="90b23-136">**Lien fourni par** la Communauté [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="90b23-136">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="90b23-137">UtterAccess est le premier forum d'aide et wiki de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="90b23-137">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="90b23-138">Choix entre DAO et ADO</span><span class="sxs-lookup"><span data-stu-id="90b23-138">Choosing between DAO and ADO</span></span>](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)



