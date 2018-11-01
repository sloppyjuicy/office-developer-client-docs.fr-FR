---
title: Convertir le code DAO en code ADO
TOCTitle: Convert DAO code to ADO
ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15)
ms:contentKeyID: 48544585
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5267115
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 60baeabfce93c2987cb9621c7cc877a7525a954c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876742"
---
# <a name="convert-dao-code-to-ado"></a><span data-ttu-id="bce05-102">Convertir le code DAO en code ADO</span><span class="sxs-lookup"><span data-stu-id="bce05-102">Convert DAO code to ADO</span></span>

<span data-ttu-id="bce05-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bce05-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="bce05-104">Versions de la bibliothèque DAO antérieures à 3.6 ne sont pas fournies ou pris en charge dans Access.</span><span class="sxs-lookup"><span data-stu-id="bce05-104">Versions of the DAO library prior to 3.6 are not provided or supported in Access.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="bce05-105">DAO au mappage d’objets ADO</span><span class="sxs-lookup"><span data-stu-id="bce05-105">DAO to ADO object map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bce05-106"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="bce05-106"><strong>DAO</strong></span></span></p></th>
<th><p><span data-ttu-id="bce05-107"><strong>ADO (ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="bce05-107"><strong>ADO (ADODB)</strong></span></span></p></th>
<th><p><span data-ttu-id="bce05-108"><strong>Remarque</strong></span><span class="sxs-lookup"><span data-stu-id="bce05-108"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bce05-109">DBEngine</span><span class="sxs-lookup"><span data-stu-id="bce05-109">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="bce05-110">Aucune</span><span class="sxs-lookup"><span data-stu-id="bce05-110">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bce05-111">Workspace</span><span class="sxs-lookup"><span data-stu-id="bce05-111">Workspace</span></span></p></td>
<td><p><span data-ttu-id="bce05-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="bce05-112">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bce05-113">Base de données</span><span class="sxs-lookup"><span data-stu-id="bce05-113">Database</span></span></p></td>
<td><p><span data-ttu-id="bce05-114">Connection</span><span class="sxs-lookup"><span data-stu-id="bce05-114">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bce05-115">Recordset</span><span class="sxs-lookup"><span data-stu-id="bce05-115">Recordset</span></span></p></td>
<td><p><span data-ttu-id="bce05-116">Recordset</span><span class="sxs-lookup"><span data-stu-id="bce05-116">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bce05-117">Dynaset-Type</span><span class="sxs-lookup"><span data-stu-id="bce05-117">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="bce05-118">Keyset</span><span class="sxs-lookup"><span data-stu-id="bce05-118">Keyset</span></span></p></td>
<td><p><span data-ttu-id="bce05-119">Récupère un ensemble de pointeurs vers les enregistrements du jeu d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="bce05-119">Retrieves a set of pointers to the records in the recordset.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bce05-120">Snapshot-Type</span><span class="sxs-lookup"><span data-stu-id="bce05-120">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="bce05-121">Static</span><span class="sxs-lookup"><span data-stu-id="bce05-121">Static</span></span></p></td>
<td><p><span data-ttu-id="bce05-122">Tous deux extraient des enregistrements complets mais un jeu d’enregistrements statique peut être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="bce05-122">Both retrieve full records, but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bce05-123">Table-Type</span><span class="sxs-lookup"><span data-stu-id="bce05-123">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="bce05-124">Keyset avec l’option adCmdTableDirect.</span><span class="sxs-lookup"><span data-stu-id="bce05-124">Keyset with adCmdTableDirect option.</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bce05-125">Champ</span><span class="sxs-lookup"><span data-stu-id="bce05-125">Field</span></span></p></td>
<td><p><span data-ttu-id="bce05-126">Champ</span><span class="sxs-lookup"><span data-stu-id="bce05-126">Field</span></span></p></td>
<td><p><span data-ttu-id="bce05-127">Quand référencée dans un jeu d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="bce05-127">When referred to in a recordset.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="bce05-128">DAO</span><span class="sxs-lookup"><span data-stu-id="bce05-128">DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="bce05-129">Ouvrir un jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="bce05-129">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="bce05-130">Modifier un jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="bce05-130">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="bce05-131">ADO</span><span class="sxs-lookup"><span data-stu-id="bce05-131">ADO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="bce05-132">Ouvrir un jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="bce05-132">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="bce05-133">Modifier un jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="bce05-133">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> <span data-ttu-id="bce05-134">Le déplacement du curseur depuis l’enregistrement en cours via **MoveNext, MoveLast, MoveFirst, MovePrevious** sans utiliser préalablement la méthode **CancelUpdate** implicitement exécute la méthode de **mise à jour** .</span><span class="sxs-lookup"><span data-stu-id="bce05-134">Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method implicitly executes the **Update** method.</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="bce05-135">À propos des collaborateurs</span><span class="sxs-lookup"><span data-stu-id="bce05-135">About the contributors</span></span>

<span data-ttu-id="bce05-136">**Lien fourni par** la Communauté [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="bce05-136">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="bce05-137">UtterAccess est le premier forum d'aide et wiki de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bce05-137">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="bce05-138">Choix entre DAO et ADO</span><span class="sxs-lookup"><span data-stu-id="bce05-138">Choosing between DAO and ADO</span></span>](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<br/>

