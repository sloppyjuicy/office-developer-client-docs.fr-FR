---
title: RecordsetOptionEnum, énumération (DAO)
TOCTitle: RecordsetOptionEnum Enumeration
ms:assetid: 3a9d8664-dcb6-cb60-7cf6-e229eb699ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192649(v=office.15)
ms:contentKeyID: 48544266
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 75b69adbe8c3851afa33f729a108ac579f84c683
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947139"
---
# <a name="recordsetoptionenum-enumeration-dao"></a><span data-ttu-id="5ae6b-102">RecordsetOptionEnum, énumération (DAO)</span><span class="sxs-lookup"><span data-stu-id="5ae6b-102">RecordsetOptionEnum enumeration (DAO)</span></span>


<span data-ttu-id="5ae6b-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5ae6b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5ae6b-104">Utilisée avec la méthode **OpenRecordset** pour spécifier les caractéristiques d'un nouvel objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="5ae6b-104">Used with the **OpenRecordset** method to specify characteristics of a new **Recordset** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5ae6b-105">Nom</span><span class="sxs-lookup"><span data-stu-id="5ae6b-105">Name</span></span></p></th>
<th><p><span data-ttu-id="5ae6b-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ae6b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="5ae6b-107">Description</span><span class="sxs-lookup"><span data-stu-id="5ae6b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ae6b-108">dbAppendOnly</span><span class="sxs-lookup"><span data-stu-id="5ae6b-108">dbAppendOnly</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-109">8</span><span class="sxs-lookup"><span data-stu-id="5ae6b-109">8</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-110">Autorise l'utilisateur à ajouter de nouveaux enregistrements à la feuille de réponse dynamique mais l'empêche de lire les enregistrements existants.</span><span class="sxs-lookup"><span data-stu-id="5ae6b-110">Allows user to add new records to the dynaset, but prevents user from reading existing records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ae6b-111">dbConsistent</span><span class="sxs-lookup"><span data-stu-id="5ae6b-111">dbConsistent</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-112">32</span><span class="sxs-lookup"><span data-stu-id="5ae6b-112">32</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-113">Applique les mises à jour aux champs qui n'affecteront pas d'autres champs de la feuille de réponse dynamique (jeu d'enregistrements de type feuille de réponse dynamique ou instantané uniquement).</span><span class="sxs-lookup"><span data-stu-id="5ae6b-113">Applies updates only to those fields that will not affect other records in the dynaset (dynaset- and snapshot-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ae6b-114">dbDenyRead</span><span class="sxs-lookup"><span data-stu-id="5ae6b-114">dbDenyRead</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-115">2</span><span class="sxs-lookup"><span data-stu-id="5ae6b-115">2</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-116">Empêche d'autres utilisateurs de lire les enregistrements du jeu d'enregistrements (de type table uniquement).</span><span class="sxs-lookup"><span data-stu-id="5ae6b-116">Prevents other users from reading Recordset records (table-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ae6b-117">dbDenyWrite</span><span class="sxs-lookup"><span data-stu-id="5ae6b-117">dbDenyWrite</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-118">1</span><span class="sxs-lookup"><span data-stu-id="5ae6b-118">1</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-119">Empêche d'autres utilisateurs de modifier les enregistrements du jeu d'enregistrements.</span><span class="sxs-lookup"><span data-stu-id="5ae6b-119">Prevents other users from changing Recordset records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ae6b-120">dbExecDirect</span><span class="sxs-lookup"><span data-stu-id="5ae6b-120">dbExecDirect</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-121">2048</span><span class="sxs-lookup"><span data-stu-id="5ae6b-121">2048</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-122">Exécute la requête sans appeler d'abord la fonction ODBC SQLPrepare.</span><span class="sxs-lookup"><span data-stu-id="5ae6b-122">Executes the query without first calling the SQLPrepare ODBC function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ae6b-123">dbFailOnError</span><span class="sxs-lookup"><span data-stu-id="5ae6b-123">dbFailOnError</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-124">128</span><span class="sxs-lookup"><span data-stu-id="5ae6b-124">128</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-125">Restaure les mises à jour si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="5ae6b-125">Rolls back updates if an error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ae6b-126">dbForwardOnly</span><span class="sxs-lookup"><span data-stu-id="5ae6b-126">dbForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-127">256</span><span class="sxs-lookup"><span data-stu-id="5ae6b-127">256</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-128">Crée un jeu d'enregistrements de type instantané à déplacement vers l'avant (jeu d'enregistrements de type instantané uniquement).</span><span class="sxs-lookup"><span data-stu-id="5ae6b-128">Creates a forward-only scrolling snapshot-type Recordset (snapshot-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ae6b-129">dbInconsistent</span><span class="sxs-lookup"><span data-stu-id="5ae6b-129">dbInconsistent</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-130">16</span><span class="sxs-lookup"><span data-stu-id="5ae6b-130">16</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-131">Applique les mises à jour à tous les champs de la feuille de réponse dynamique, et ce même si d'autres enregistrements sont affectés (jeu d'enregistrements de type feuille de réponse dynamique ou instantané uniquement).</span><span class="sxs-lookup"><span data-stu-id="5ae6b-131">Applies updates to all dynaset fields, even if other records are affected (dynaset- and snapshot-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ae6b-132">peut entraîner</span><span class="sxs-lookup"><span data-stu-id="5ae6b-132">dbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-133">4</span><span class="sxs-lookup"><span data-stu-id="5ae6b-133">4</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-134">Ouvre le jeu d'enregistrements en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="5ae6b-134">Opens the Recordset as read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ae6b-135">dbRunAsync</span><span class="sxs-lookup"><span data-stu-id="5ae6b-135">dbRunAsync</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-136">1024</span><span class="sxs-lookup"><span data-stu-id="5ae6b-136">1024</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-137">Exécute la requête de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="5ae6b-137">Executes the query asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ae6b-138">dbSeeChanges</span><span class="sxs-lookup"><span data-stu-id="5ae6b-138">dbSeeChanges</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-139">512</span><span class="sxs-lookup"><span data-stu-id="5ae6b-139">512</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-140">Génère une erreur d'exécution si un autre utilisateur change les données que vous êtes en train de modifier (jeu d'enregistrements de type feuille de réponse dynamique uniquement).</span><span class="sxs-lookup"><span data-stu-id="5ae6b-140">Generates a run-time error if another user is changing data you are editing (dynaset-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ae6b-141">dbSQLPassThrough</span><span class="sxs-lookup"><span data-stu-id="5ae6b-141">dbSQLPassThrough</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-142">64</span><span class="sxs-lookup"><span data-stu-id="5ae6b-142">64</span></span></p></td>
<td><p><span data-ttu-id="5ae6b-143">Envoie une instruction SQL à une base de données ODBC (jeu d'enregistrements de type instantané uniquement).</span><span class="sxs-lookup"><span data-stu-id="5ae6b-143">Sends an SQL statement to an ODBC database (snapshot-type only).</span></span></p></td>
</tr>
</tbody>
</table>

