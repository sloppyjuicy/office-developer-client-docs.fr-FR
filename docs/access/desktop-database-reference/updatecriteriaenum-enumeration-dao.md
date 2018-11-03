---
title: UpdateCriteriaEnum, énumération (DAO)
TOCTitle: UpdateCriteriaEnum Enumeration
ms:assetid: 1f83a0c6-bdc8-9c3e-380b-524f611f6476
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845853(v=office.15)
ms:contentKeyID: 48543644
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d6160c53dd1cab26b2b92ec023f28158635d7081
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944465"
---
# <a name="updatecriteriaenum-enumeration-dao"></a><span data-ttu-id="60009-102">UpdateCriteriaEnum, énumération (DAO)</span><span class="sxs-lookup"><span data-stu-id="60009-102">UpdateCriteriaEnum enumeration (DAO)</span></span>


<span data-ttu-id="60009-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="60009-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="60009-104">Cette énumération est utilisée avec la méthode **UpdateOptions** pour spécifier la construction d'une mise à jour par lot.</span><span class="sxs-lookup"><span data-stu-id="60009-104">Used with the **UpdateOptions** method to specify how a batch update is constructed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60009-105">Nom</span><span class="sxs-lookup"><span data-stu-id="60009-105">Name</span></span></p></th>
<th><p><span data-ttu-id="60009-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="60009-106">Value</span></span></p></th>
<th><p><span data-ttu-id="60009-107">Description</span><span class="sxs-lookup"><span data-stu-id="60009-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60009-108">dbCriteriaAllCols</span><span class="sxs-lookup"><span data-stu-id="60009-108">dbCriteriaAllCols</span></span></p></td>
<td><p><span data-ttu-id="60009-109">4</span><span class="sxs-lookup"><span data-stu-id="60009-109">4</span></span></p></td>
<td><p><span data-ttu-id="60009-110">Utilise les colonnes clé et toutes les colonnes dans la clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="60009-110">Uses the key column(s) and all the columns in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60009-111">dbCriteriaDeleteInsert</span><span class="sxs-lookup"><span data-stu-id="60009-111">dbCriteriaDeleteInsert</span></span></p></td>
<td><p><span data-ttu-id="60009-112">16</span><span class="sxs-lookup"><span data-stu-id="60009-112">16</span></span></p></td>
<td><p><span data-ttu-id="60009-113">Utilise une instruction DELETE et une instruction INSERT pour chaque ligne modifiée.</span><span class="sxs-lookup"><span data-stu-id="60009-113">Uses a pair of DELETE and INSERT statements for each modified row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60009-114">dbCriteriaKey</span><span class="sxs-lookup"><span data-stu-id="60009-114">dbCriteriaKey</span></span></p></td>
<td><p><span data-ttu-id="60009-115">1</span><span class="sxs-lookup"><span data-stu-id="60009-115">1</span></span></p></td>
<td><p><span data-ttu-id="60009-116">Utilise les colonnes clé dans la clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="60009-116">Uses just the key column(s) in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60009-117">dbCriteriaModValues</span><span class="sxs-lookup"><span data-stu-id="60009-117">dbCriteriaModValues</span></span></p></td>
<td><p><span data-ttu-id="60009-118">2</span><span class="sxs-lookup"><span data-stu-id="60009-118">2</span></span></p></td>
<td><p><span data-ttu-id="60009-119">Utilise les colonnes clé et toutes les colonnes mises à jour dans la clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="60009-119">Uses the key column(s) and all updated columns in the where clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60009-120">dbCriteriaTimestamp</span><span class="sxs-lookup"><span data-stu-id="60009-120">dbCriteriaTimestamp</span></span></p></td>
<td><p><span data-ttu-id="60009-121">8</span><span class="sxs-lookup"><span data-stu-id="60009-121">8</span></span></p></td>
<td><p><span data-ttu-id="60009-122">Utilise la colonne horodateur si elle est disponible (génère une erreur d'exécution si aucune colonne horodateur ne se trouve dans le jeu de résultats).</span><span class="sxs-lookup"><span data-stu-id="60009-122">Uses just the timestamp column if available (will generate a run-time error if no timestamp column is in the result set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60009-123">dbCriteriaUpdate</span><span class="sxs-lookup"><span data-stu-id="60009-123">dbCriteriaUpdate</span></span></p></td>
<td><p><span data-ttu-id="60009-124">32</span><span class="sxs-lookup"><span data-stu-id="60009-124">32</span></span></p></td>
<td><p><span data-ttu-id="60009-125">Utilise une instruction UPDATE pour chaque ligne modifiée.</span><span class="sxs-lookup"><span data-stu-id="60009-125">Uses an UPDATE statement for each modified row.</span></span></p></td>
</tr>
</tbody>
</table>

