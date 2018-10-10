---
title: UpdateCriteriaEnum Enumeration (DAO)
TOCTitle: UpdateCriteriaEnum Enumeration
ms:assetid: 1f83a0c6-bdc8-9c3e-380b-524f611f6476
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845853(v=office.15)
ms:contentKeyID: 48543644
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7dc671458d53f6e40e27ff2dd338f010c09dc5ba
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470184"
---
# <a name="updatecriteriaenum-enumeration-dao"></a><span data-ttu-id="38f15-102">UpdateCriteriaEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="38f15-102">UpdateCriteriaEnum Enumeration (DAO)</span></span>


<span data-ttu-id="38f15-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="38f15-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="38f15-104">Cette énumération est utilisée avec la méthode **UpdateOptions** pour spécifier la construction d'une mise à jour par lot.</span><span class="sxs-lookup"><span data-stu-id="38f15-104">Used with the **UpdateOptions** method to specify how a batch update is constructed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="38f15-105">Nom</span><span class="sxs-lookup"><span data-stu-id="38f15-105">Name</span></span></p></th>
<th><p><span data-ttu-id="38f15-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="38f15-106">Value</span></span></p></th>
<th><p><span data-ttu-id="38f15-107">Description</span><span class="sxs-lookup"><span data-stu-id="38f15-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38f15-108">dbCriteriaAllCols</span><span class="sxs-lookup"><span data-stu-id="38f15-108">dbCriteriaAllCols</span></span></p></td>
<td><p><span data-ttu-id="38f15-109">4</span><span class="sxs-lookup"><span data-stu-id="38f15-109">4</span></span></p></td>
<td><p><span data-ttu-id="38f15-110">Utilise les colonnes clé et toutes les colonnes dans la clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="38f15-110">Uses the key column(s) and all the columns in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38f15-111">dbCriteriaDeleteInsert</span><span class="sxs-lookup"><span data-stu-id="38f15-111">dbCriteriaDeleteInsert</span></span></p></td>
<td><p><span data-ttu-id="38f15-112">16</span><span class="sxs-lookup"><span data-stu-id="38f15-112">16</span></span></p></td>
<td><p><span data-ttu-id="38f15-113">Utilise une instruction DELETE et une instruction INSERT pour chaque ligne modifiée.</span><span class="sxs-lookup"><span data-stu-id="38f15-113">Uses a pair of DELETE and INSERT statements for each modified row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38f15-114">dbCriteriaKey</span><span class="sxs-lookup"><span data-stu-id="38f15-114">dbCriteriaKey</span></span></p></td>
<td><p><span data-ttu-id="38f15-115">1</span><span class="sxs-lookup"><span data-stu-id="38f15-115">1</span></span></p></td>
<td><p><span data-ttu-id="38f15-116">Utilise les colonnes clé dans la clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="38f15-116">Uses just the key column(s) in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38f15-117">dbCriteriaModValues</span><span class="sxs-lookup"><span data-stu-id="38f15-117">dbCriteriaModValues</span></span></p></td>
<td><p><span data-ttu-id="38f15-118">2</span><span class="sxs-lookup"><span data-stu-id="38f15-118">2</span></span></p></td>
<td><p><span data-ttu-id="38f15-119">Utilise les colonnes clé et toutes les colonnes mises à jour dans la clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="38f15-119">Uses the key column(s) and all updated columns in the where clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38f15-120">dbCriteriaTimestamp</span><span class="sxs-lookup"><span data-stu-id="38f15-120">dbCriteriaTimestamp</span></span></p></td>
<td><p><span data-ttu-id="38f15-121">8</span><span class="sxs-lookup"><span data-stu-id="38f15-121">8</span></span></p></td>
<td><p><span data-ttu-id="38f15-122">Utilise la colonne horodateur si elle est disponible (génère une erreur d'exécution si aucune colonne horodateur ne se trouve dans le jeu de résultats).</span><span class="sxs-lookup"><span data-stu-id="38f15-122">Uses just the timestamp column if available (will generate a run-time error if no timestamp column is in the result set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38f15-123">dbCriteriaUpdate</span><span class="sxs-lookup"><span data-stu-id="38f15-123">dbCriteriaUpdate</span></span></p></td>
<td><p><span data-ttu-id="38f15-124">32</span><span class="sxs-lookup"><span data-stu-id="38f15-124">32</span></span></p></td>
<td><p><span data-ttu-id="38f15-125">Utilise une instruction UPDATE pour chaque ligne modifiée.</span><span class="sxs-lookup"><span data-stu-id="38f15-125">Uses an UPDATE statement for each modified row.</span></span></p></td>
</tr>
</tbody>
</table>

