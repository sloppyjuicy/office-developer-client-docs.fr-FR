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
localization_priority: Priority
ms.openlocfilehash: 77d56efd63d6a0841b595f12456baa808751706e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720337"
---
# <a name="convert-dao-code-to-ado"></a><span data-ttu-id="c2883-102">Convertir le code DAO en code ADO</span><span class="sxs-lookup"><span data-stu-id="c2883-102">Convert DAO code to ADO</span></span>

<span data-ttu-id="c2883-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2883-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="c2883-104">Versions de la bibliothèque DAO antérieures à 3.6 ne sont pas fournies ou pris en charge dans Access.</span><span class="sxs-lookup"><span data-stu-id="c2883-104">Versions of the DAO library prior to 3.6 are not provided or supported in Access.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="c2883-105">DAO au mappage d’objets ADO</span><span class="sxs-lookup"><span data-stu-id="c2883-105">DAO to ADO object map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c2883-106"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="c2883-106"><strong>DAO</strong></span></span></p></th>
<th><p><span data-ttu-id="c2883-107"><strong>ADO (ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="c2883-107"><strong>ADO (ADODB)</strong></span></span></p></th>
<th><p><span data-ttu-id="c2883-108"><strong>Remarque</strong></span><span class="sxs-lookup"><span data-stu-id="c2883-108"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c2883-109">DBEngine</span><span class="sxs-lookup"><span data-stu-id="c2883-109">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="c2883-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="c2883-110">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2883-111">Workspace</span><span class="sxs-lookup"><span data-stu-id="c2883-111">Workspace</span></span></p></td>
<td><p><span data-ttu-id="c2883-112">Aucun</span><span class="sxs-lookup"><span data-stu-id="c2883-112">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2883-113">Base de données</span><span class="sxs-lookup"><span data-stu-id="c2883-113">Database</span></span></p></td>
<td><p><span data-ttu-id="c2883-114">Connection</span><span class="sxs-lookup"><span data-stu-id="c2883-114">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2883-115">Recordset</span><span class="sxs-lookup"><span data-stu-id="c2883-115">Recordset</span></span></p></td>
<td><p><span data-ttu-id="c2883-116">Recordset</span><span class="sxs-lookup"><span data-stu-id="c2883-116">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2883-117">Dynaset-Type</span><span class="sxs-lookup"><span data-stu-id="c2883-117">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="c2883-118">Keyset</span><span class="sxs-lookup"><span data-stu-id="c2883-118">Keyset</span></span></p></td>
<td><p><span data-ttu-id="c2883-119">Récupère un ensemble de pointeurs vers les enregistrements du jeu d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="c2883-119">Retrieves a set of pointers to the records in the recordset.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2883-120">Snapshot-Type</span><span class="sxs-lookup"><span data-stu-id="c2883-120">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="c2883-121">Static</span><span class="sxs-lookup"><span data-stu-id="c2883-121">Static</span></span></p></td>
<td><p><span data-ttu-id="c2883-122">Tous deux extraient des enregistrements complets mais un jeu d’enregistrements statique peut être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="c2883-122">Both retrieve full records, but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2883-123">Table-Type</span><span class="sxs-lookup"><span data-stu-id="c2883-123">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="c2883-124">Keyset avec l’option adCmdTableDirect.</span><span class="sxs-lookup"><span data-stu-id="c2883-124">Keyset with adCmdTableDirect option.</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2883-125">Champ</span><span class="sxs-lookup"><span data-stu-id="c2883-125">Field</span></span></p></td>
<td><p><span data-ttu-id="c2883-126">Champ</span><span class="sxs-lookup"><span data-stu-id="c2883-126">Field</span></span></p></td>
<td><p><span data-ttu-id="c2883-127">Quand référencée dans un jeu d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="c2883-127">When referred to in a recordset.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="c2883-128">DAO</span><span class="sxs-lookup"><span data-stu-id="c2883-128">DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="c2883-129">Ouvrir un jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="c2883-129">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="c2883-130">Modifier un jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="c2883-130">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="c2883-131">ADO</span><span class="sxs-lookup"><span data-stu-id="c2883-131">ADO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="c2883-132">Ouvrir un jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="c2883-132">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="c2883-133">Modifier un jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="c2883-133">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> <span data-ttu-id="c2883-134">Le déplacement du curseur depuis l’enregistrement en cours via **MoveNext, MoveLast, MoveFirst, MovePrevious** sans utiliser préalablement la méthode **CancelUpdate** implicitement exécute la méthode de **mise à jour** .</span><span class="sxs-lookup"><span data-stu-id="c2883-134">Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method implicitly executes the **Update** method.</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="c2883-135">À propos des collaborateurs</span><span class="sxs-lookup"><span data-stu-id="c2883-135">About the contributors</span></span>

<span data-ttu-id="c2883-136">**Lien fourni par** la Communauté [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="c2883-136">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="c2883-137">UtterAccess est un forum d’aide et wiki de Microsoft Access réputé.</span><span class="sxs-lookup"><span data-stu-id="c2883-137">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="c2883-138">Choix entre DAO et ADO</span><span class="sxs-lookup"><span data-stu-id="c2883-138">Choosing between DAO and ADO</span></span>](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<br/>

