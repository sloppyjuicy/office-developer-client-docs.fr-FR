---
title: RecordsetOptionEnum, énumération (DAO)
TOCTitle: RecordsetOptionEnum Enumeration
ms:assetid: 3a9d8664-dcb6-cb60-7cf6-e229eb699ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192649(v=office.15)
ms:contentKeyID: 48544266
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: b9e2a69f6952feb892de736e7ff3c3ca94e9da64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307181"
---
# <a name="recordsetoptionenum-enumeration-dao"></a><span data-ttu-id="3e3b6-102">RecordsetOptionEnum, énumération (DAO)</span><span class="sxs-lookup"><span data-stu-id="3e3b6-102">RecordsetOptionEnum Enumeration (DAO)</span></span>


<span data-ttu-id="3e3b6-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3e3b6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3e3b6-104">Utilisée avec la **OpenRecordset** méthode permettant de spécifier les caractéristiques d’une nouvelle **jeu d’enregistrements** objet.</span><span class="sxs-lookup"><span data-stu-id="3e3b6-104">Used with the **OpenRecordset** method to specify characteristics of a new **Recordset** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3e3b6-105">Nom</span><span class="sxs-lookup"><span data-stu-id="3e3b6-105">Name</span></span></p></th>
<th><p><span data-ttu-id="3e3b6-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e3b6-106">Value</span></span></p></th>
<th><p><span data-ttu-id="3e3b6-107">Description</span><span class="sxs-lookup"><span data-stu-id="3e3b6-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e3b6-108">dbAppendOnly</span><span class="sxs-lookup"><span data-stu-id="3e3b6-108">dbAppendOnly</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-109">8</span><span class="sxs-lookup"><span data-stu-id="3e3b6-109">8.</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-110">Permet à utilisateur d’ajouter de nouveaux enregistrements à la feuille de réponse dynamique, mais empêche l’utilisateur de lire les enregistrements existants.</span><span class="sxs-lookup"><span data-stu-id="3e3b6-110">Allows user to add new records to the dynaset, but prevents user from reading existing records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e3b6-111">dbConsistent</span><span class="sxs-lookup"><span data-stu-id="3e3b6-111">dbConsistent</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-112">32</span><span class="sxs-lookup"><span data-stu-id="3e3b6-112">3.2</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-113">Applique des mises à jour uniquement à ces champs qui n’affectera pas les autres enregistrements dans la feuille de réponse dynamique (feuille de réponse dynamique - et -type instantané uniquement).</span><span class="sxs-lookup"><span data-stu-id="3e3b6-113">Applies updates only to those fields that will not affect other records in the dynaset (dynaset- and snapshot-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e3b6-114">dbDenyRead</span><span class="sxs-lookup"><span data-stu-id="3e3b6-114">dbDenyRead</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-115">2</span><span class="sxs-lookup"><span data-stu-id="3e3b6-115">2.</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-116">Empêche les autres utilisateurs de lire les enregistrements du jeu d’enregistrements (type tableau uniquement).</span><span class="sxs-lookup"><span data-stu-id="3e3b6-116">Prevents other users from reading Recordset records (table-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e3b6-117">dbDenyWrite</span><span class="sxs-lookup"><span data-stu-id="3e3b6-117">dbDenyWrite</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-118">1</span><span class="sxs-lookup"><span data-stu-id="3e3b6-118">-1</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-119">Empêche les autres utilisateurs de modifier les enregistrements du jeu d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="3e3b6-119">Prevents other users from changing Recordset records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e3b6-120">dbExecDirect</span><span class="sxs-lookup"><span data-stu-id="3e3b6-120">dbExecDirect</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-121">2048</span><span class="sxs-lookup"><span data-stu-id="3e3b6-121">2048 MB</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-122">Exécute la requête sans appelant tout d’abord la fonction SQLPrepare ODBC.</span><span class="sxs-lookup"><span data-stu-id="3e3b6-122">Executes the query without first calling the SQLPrepare ODBC function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e3b6-123">dbFailOnError</span><span class="sxs-lookup"><span data-stu-id="3e3b6-123">dbFailOnError</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-124">128</span><span class="sxs-lookup"><span data-stu-id="3e3b6-124">128 GB</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-125">Annule les mises à jour si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="3e3b6-125">Rolls back updates if an error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e3b6-126">dbForwardOnly</span><span class="sxs-lookup"><span data-stu-id="3e3b6-126">dbForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-127">256</span><span class="sxs-lookup"><span data-stu-id="3e3b6-127">validAccesses: 256</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-128">Crée un défilement vers l’avant uniquement instantané type jeu d’enregistrements (type instantané uniquement).</span><span class="sxs-lookup"><span data-stu-id="3e3b6-128">Creates a forward-only scrolling snapshot-type Recordset (snapshot-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e3b6-129">dbInconsistent</span><span class="sxs-lookup"><span data-stu-id="3e3b6-129">dbInconsistent</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-130">16</span><span class="sxs-lookup"><span data-stu-id="3e3b6-130">1.6</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-131">Applique les mises à jour à tous les champs de feuille de réponse dynamique, même si d’autres enregistrements sont concerné (feuille de réponse dynamique - et -type instantané uniquement).</span><span class="sxs-lookup"><span data-stu-id="3e3b6-131">Applies updates to all dynaset fields, even if other records are affected (dynaset- and snapshot-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e3b6-132">dbReadOnly</span><span class="sxs-lookup"><span data-stu-id="3e3b6-132">dbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-133">4</span><span class="sxs-lookup"><span data-stu-id="3e3b6-133">4.</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-134">Ouvre le jeu d’enregistrements en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3e3b6-134">Opens the Recordset as read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e3b6-135">dbRunAsync</span><span class="sxs-lookup"><span data-stu-id="3e3b6-135">dbRunAsync</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-136">1024</span><span class="sxs-lookup"><span data-stu-id="3e3b6-136">1024 attachments4</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-137">Exécute la requête de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="3e3b6-137">Executes the query asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e3b6-138">dbSeeChanges</span><span class="sxs-lookup"><span data-stu-id="3e3b6-138">dbSeeChanges</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-139">512</span><span class="sxs-lookup"><span data-stu-id="3e3b6-139">5.12</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-140">Génère une erreur d'exécution si un autre utilisateur modifie les données que vous-même êtes en train de modifier (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="3e3b6-140">Generates a run-time error if another user is changing data you are editing (dynaset-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e3b6-141">dbSQLPassThrough</span><span class="sxs-lookup"><span data-stu-id="3e3b6-141">dbSQLPassThrough</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-142">64</span><span class="sxs-lookup"><span data-stu-id="3e3b6-142">6.4</span></span></p></td>
<td><p><span data-ttu-id="3e3b6-143">Envoie une instruction SQL à une base de données ODBC (type instantané uniquement).</span><span class="sxs-lookup"><span data-stu-id="3e3b6-143">Sends an SQL statement to an ODBC database (snapshot-type only).</span></span></p></td>
</tr>
</tbody>
</table>

