---
title: PourChaqueEnregistrement, bloc de données
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84ab685b946e390645027790e5b1402561527ab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292327"
---
# <a name="foreachrecord-data-block"></a><span data-ttu-id="fe272-102">PourChaqueEnregistrement, bloc de données</span><span class="sxs-lookup"><span data-stu-id="fe272-102">ForEachRecord data block</span></span>

<span data-ttu-id="fe272-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe272-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fe272-104">Un bloc de données **PourChaqueEnregistrement** répète un ensemble d'instructions pour chaque enregistrement dans un domaine.</span><span class="sxs-lookup"><span data-stu-id="fe272-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span>

> [!NOTE]
> <span data-ttu-id="fe272-105">Le bloc de données **PourChaqueEnregistrement** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="fe272-105">The **ForEachRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="fe272-106">Setting</span><span class="sxs-lookup"><span data-stu-id="fe272-106">Setting</span></span>

<span data-ttu-id="fe272-107">L’action **PourChaqueEnregistrement** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="fe272-107">The **ForEachRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe272-108">Argument</span><span class="sxs-lookup"><span data-stu-id="fe272-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="fe272-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="fe272-109">Required</span></span></p></th>
<th><p><span data-ttu-id="fe272-110">Description</span><span class="sxs-lookup"><span data-stu-id="fe272-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe272-111"><strong>Dans</strong></span><span class="sxs-lookup"><span data-stu-id="fe272-111"><strong>In</strong></span></span></p></td>
<td><p><span data-ttu-id="fe272-112">Oui</span><span class="sxs-lookup"><span data-stu-id="fe272-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="fe272-113">Chaîne qui identifie le domaine d’enregistrements sur lequel opérer.</span><span class="sxs-lookup"><span data-stu-id="fe272-113">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="fe272-114">L'argument <em>dans</em> peut contenir le nom de la table, une requête sélection ou une instruction SQL.</span><span class="sxs-lookup"><span data-stu-id="fe272-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p><p><span data-ttu-id="fe272-115"><strong>Remarque</strong>: le domaine spécifié ne peut pas inclure de données stockées dans une table liée ou une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="fe272-115"><strong>NOTE</strong>: The specified domain cannot include data stored in a linked table or ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe272-116"><strong>Condition Where</strong></span><span class="sxs-lookup"><span data-stu-id="fe272-116"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="fe272-117">Non</span><span class="sxs-lookup"><span data-stu-id="fe272-117">No</span></span></p></td>
<td><p><span data-ttu-id="fe272-118">Expression de chaîne servant à limiter la plage de données sur laquelle le bloc de données <strong>PourChaqueEnregistrement</strong> est exécuté.</span><span class="sxs-lookup"><span data-stu-id="fe272-118">A string expression used to restrict the range of data on which the <strong>ForEachRecord</strong> data block is performed.</span></span> <span data-ttu-id="fe272-119">Par exemple, les critères sont souvent équivalents à la clause WHERE dans une expression SQL, sans le mot WHERE.</span><span class="sxs-lookup"><span data-stu-id="fe272-119">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="fe272-120">En cas d'omission de critère, le bloc de données <strong>PourChaqueEnregistrement</strong> s'applique à l'ensemble du domaine spécifié par l'argument <em>in</em> .</span><span class="sxs-lookup"><span data-stu-id="fe272-120">If criteria is omitted, the <strong>ForEachRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="fe272-121">Tout champ inclus dans les critères doit également être un champ dans <em>In</em>.</span><span class="sxs-lookup"><span data-stu-id="fe272-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe272-122"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="fe272-122"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="fe272-123">Non</span><span class="sxs-lookup"><span data-stu-id="fe272-123">No</span></span></p></td>
<td><p><span data-ttu-id="fe272-124">Chaîne qui fournit un autre nom pour le domaine spécifié par l'argument <em>dans</em> .</span><span class="sxs-lookup"><span data-stu-id="fe272-124">A string that provides an alternative name for the domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="fe272-125">Souvent utilisé pour raccourcir le nom de la table pour les références ultérieures afin d'éviter d'éventuelles références ambiguës. Si <em>alias</em> n'est pas spécifié, le nom de la table ou de la requête sera utilisé comme alias.</span><span class="sxs-lookup"><span data-stu-id="fe272-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fe272-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="fe272-126">Remarks</span></span>

<span data-ttu-id="fe272-127">Utilisez l'action **[QuitterPourChaqueEnregistrement](exitforeachrecord-macro-action.md)** pour quitter immédiatement un bloc de données **PourChaqueEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="fe272-127">Use the **[ExitForEachRecord](exitforeachrecord-macro-action.md)** action to exit a **ForEachRecord** data block immediately.</span></span>

