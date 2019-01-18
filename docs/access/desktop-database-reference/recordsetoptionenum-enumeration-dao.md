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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717278"
---
# <a name="recordsetoptionenum-enumeration-dao"></a><span data-ttu-id="1708a-102">RecordsetOptionEnum, énumération (DAO)</span><span class="sxs-lookup"><span data-stu-id="1708a-102">RecordsetOptionEnum enumeration (DAO)</span></span>


<span data-ttu-id="1708a-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1708a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1708a-104">Utilisée avec la méthode **OpenRecordset** pour spécifier les caractéristiques d'un nouvel objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="1708a-104">Used with the **OpenRecordset** method to specify characteristics of a new **Recordset** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1708a-105">Nom</span><span class="sxs-lookup"><span data-stu-id="1708a-105">Name</span></span></p></th>
<th><p><span data-ttu-id="1708a-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="1708a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="1708a-107">Description</span><span class="sxs-lookup"><span data-stu-id="1708a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1708a-108">dbAppendOnly</span><span class="sxs-lookup"><span data-stu-id="1708a-108">dbAppendOnly</span></span></p></td>
<td><p><span data-ttu-id="1708a-109">8</span><span class="sxs-lookup"><span data-stu-id="1708a-109">8</span></span></p></td>
<td><p><span data-ttu-id="1708a-110">Autorise l'utilisateur à ajouter de nouveaux enregistrements à la feuille de réponse dynamique mais l'empêche de lire les enregistrements existants.</span><span class="sxs-lookup"><span data-stu-id="1708a-110">Allows user to add new records to the dynaset, but prevents user from reading existing records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1708a-111">dbConsistent</span><span class="sxs-lookup"><span data-stu-id="1708a-111">dbConsistent</span></span></p></td>
<td><p><span data-ttu-id="1708a-112">32</span><span class="sxs-lookup"><span data-stu-id="1708a-112">32</span></span></p></td>
<td><p><span data-ttu-id="1708a-113">Applique les mises à jour aux champs qui n'affecteront pas d'autres champs de la feuille de réponse dynamique (jeu d'enregistrements de type feuille de réponse dynamique ou instantané uniquement).</span><span class="sxs-lookup"><span data-stu-id="1708a-113">Applies updates only to those fields that will not affect other records in the dynaset (dynaset- and snapshot-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1708a-114">dbDenyRead</span><span class="sxs-lookup"><span data-stu-id="1708a-114">dbDenyRead</span></span></p></td>
<td><p><span data-ttu-id="1708a-115">2</span><span class="sxs-lookup"><span data-stu-id="1708a-115">2</span></span></p></td>
<td><p><span data-ttu-id="1708a-116">Empêche d'autres utilisateurs de lire les enregistrements du jeu d'enregistrements (de type table uniquement).</span><span class="sxs-lookup"><span data-stu-id="1708a-116">Prevents other users from reading Recordset records (table-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1708a-117">dbDenyWrite</span><span class="sxs-lookup"><span data-stu-id="1708a-117">dbDenyWrite</span></span></p></td>
<td><p><span data-ttu-id="1708a-118">1</span><span class="sxs-lookup"><span data-stu-id="1708a-118">1</span></span></p></td>
<td><p><span data-ttu-id="1708a-119">Empêche d'autres utilisateurs de modifier les enregistrements du jeu d'enregistrements.</span><span class="sxs-lookup"><span data-stu-id="1708a-119">Prevents other users from changing Recordset records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1708a-120">dbExecDirect</span><span class="sxs-lookup"><span data-stu-id="1708a-120">dbExecDirect</span></span></p></td>
<td><p><span data-ttu-id="1708a-121">2048</span><span class="sxs-lookup"><span data-stu-id="1708a-121">2048</span></span></p></td>
<td><p><span data-ttu-id="1708a-122">Exécute la requête sans appeler d'abord la fonction ODBC SQLPrepare.</span><span class="sxs-lookup"><span data-stu-id="1708a-122">Executes the query without first calling the SQLPrepare ODBC function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1708a-123">dbFailOnError</span><span class="sxs-lookup"><span data-stu-id="1708a-123">dbFailOnError</span></span></p></td>
<td><p><span data-ttu-id="1708a-124">128</span><span class="sxs-lookup"><span data-stu-id="1708a-124">128</span></span></p></td>
<td><p><span data-ttu-id="1708a-125">Restaure les mises à jour si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="1708a-125">Rolls back updates if an error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1708a-126">dbForwardOnly</span><span class="sxs-lookup"><span data-stu-id="1708a-126">dbForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="1708a-127">256</span><span class="sxs-lookup"><span data-stu-id="1708a-127">256</span></span></p></td>
<td><p><span data-ttu-id="1708a-128">Crée un jeu d'enregistrements de type instantané à déplacement vers l'avant (jeu d'enregistrements de type instantané uniquement).</span><span class="sxs-lookup"><span data-stu-id="1708a-128">Creates a forward-only scrolling snapshot-type Recordset (snapshot-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1708a-129">dbInconsistent</span><span class="sxs-lookup"><span data-stu-id="1708a-129">dbInconsistent</span></span></p></td>
<td><p><span data-ttu-id="1708a-130">16</span><span class="sxs-lookup"><span data-stu-id="1708a-130">16</span></span></p></td>
<td><p><span data-ttu-id="1708a-131">Applique les mises à jour à tous les champs de la feuille de réponse dynamique, et ce même si d'autres enregistrements sont affectés (jeu d'enregistrements de type feuille de réponse dynamique ou instantané uniquement).</span><span class="sxs-lookup"><span data-stu-id="1708a-131">Applies updates to all dynaset fields, even if other records are affected (dynaset- and snapshot-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1708a-132">peut entraîner</span><span class="sxs-lookup"><span data-stu-id="1708a-132">dbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="1708a-133">4</span><span class="sxs-lookup"><span data-stu-id="1708a-133">4</span></span></p></td>
<td><p><span data-ttu-id="1708a-134">Ouvre le jeu d'enregistrements en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1708a-134">Opens the Recordset as read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1708a-135">dbRunAsync</span><span class="sxs-lookup"><span data-stu-id="1708a-135">dbRunAsync</span></span></p></td>
<td><p><span data-ttu-id="1708a-136">1024</span><span class="sxs-lookup"><span data-stu-id="1708a-136">1024</span></span></p></td>
<td><p><span data-ttu-id="1708a-137">Exécute la requête de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="1708a-137">Executes the query asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1708a-138">dbSeeChanges</span><span class="sxs-lookup"><span data-stu-id="1708a-138">dbSeeChanges</span></span></p></td>
<td><p><span data-ttu-id="1708a-139">512</span><span class="sxs-lookup"><span data-stu-id="1708a-139">512</span></span></p></td>
<td><p><span data-ttu-id="1708a-140">Génère une erreur d'exécution si un autre utilisateur change les données que vous êtes en train de modifier (jeu d'enregistrements de type feuille de réponse dynamique uniquement).</span><span class="sxs-lookup"><span data-stu-id="1708a-140">Generates a run-time error if another user is changing data you are editing (dynaset-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1708a-141">dbSQLPassThrough</span><span class="sxs-lookup"><span data-stu-id="1708a-141">dbSQLPassThrough</span></span></p></td>
<td><p><span data-ttu-id="1708a-142">64</span><span class="sxs-lookup"><span data-stu-id="1708a-142">64</span></span></p></td>
<td><p><span data-ttu-id="1708a-143">Envoie une instruction SQL à une base de données ODBC (jeu d'enregistrements de type instantané uniquement).</span><span class="sxs-lookup"><span data-stu-id="1708a-143">Sends an SQL statement to an ODBC database (snapshot-type only).</span></span></p></td>
</tr>
</tbody>
</table>

