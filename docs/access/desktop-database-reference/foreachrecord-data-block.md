---
title: Bloc de données PourChaqueEnregistrement
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 09a09a80773adecf760ae4610df30bbd5f36f3d6
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937525"
---
# <a name="foreachrecord-data-block"></a><span data-ttu-id="d9f53-102">Bloc de données PourChaqueEnregistrement</span><span class="sxs-lookup"><span data-stu-id="d9f53-102">ForEachRecord data block</span></span>


<span data-ttu-id="d9f53-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9f53-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d9f53-104">Un bloc de données **PourChaqueEnregistrement** répète un ensemble d’instructions pour chaque enregistrement dans un domaine.</span><span class="sxs-lookup"><span data-stu-id="d9f53-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span>

> [!NOTE]
> <span data-ttu-id="d9f53-105">[!REMARQUE] Le bloc de données **PourChaqueEnregistrement** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="d9f53-105">The **ForEachRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="d9f53-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d9f53-106">Setting</span></span>

<span data-ttu-id="d9f53-107">L'action **PourChaqueEnregistrement** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="d9f53-107">The **ForEachRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d9f53-108">Argument</span><span class="sxs-lookup"><span data-stu-id="d9f53-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="d9f53-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d9f53-109">Required</span></span></p></th>
<th><p><span data-ttu-id="d9f53-110">Description</span><span class="sxs-lookup"><span data-stu-id="d9f53-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9f53-111"><strong>In</strong></span><span class="sxs-lookup"><span data-stu-id="d9f53-111"><strong>In</strong></span></span></p></td>
<td><p><span data-ttu-id="d9f53-112">Oui</span><span class="sxs-lookup"><span data-stu-id="d9f53-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="d9f53-113">Une chaîne qui identifie le domaine d’enregistrements de fonctionner sur.</span><span class="sxs-lookup"><span data-stu-id="d9f53-113">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="d9f53-114">L’argument <em>dans</em> peut contenir le nom de la table, une requête sélection ou une instruction SQL.</span><span class="sxs-lookup"><span data-stu-id="d9f53-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p>

> [!NOTE]
> <span data-ttu-id="d9f53-115">Le domaine spécifié ne peut pas inclure de données stockées dans une table liée ou une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="d9f53-115">The specified domain cannot include data stored in a linked table or ODBC data source.</span></span>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9f53-116"><strong>Where Condition</strong></span><span class="sxs-lookup"><span data-stu-id="d9f53-116"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="d9f53-117">Non</span><span class="sxs-lookup"><span data-stu-id="d9f53-117">No</span></span></p></td>
<td><p><span data-ttu-id="d9f53-118">Une expression de chaîne utilisée pour limiter la plage de données sur lequel le bloc de données <strong>PourChaqueEnregistrement</strong> est effectuée.</span><span class="sxs-lookup"><span data-stu-id="d9f53-118">A string expression used to restrict the range of data on which the <strong>ForEachRecord</strong> data block is performed.</span></span> <span data-ttu-id="d9f53-119">Par exemple, critères est souvent équivalent à la clause WHERE d’une expression SQL sans le mot où.</span><span class="sxs-lookup"><span data-stu-id="d9f53-119">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="d9f53-120">Si l’argument critères est omis, le bloc de données <strong>PourChaqueEnregistrement</strong> opère sur l’intégralité du domaine spécifié par l’argument <em>dans</em> .</span><span class="sxs-lookup"><span data-stu-id="d9f53-120">If criteria is omitted, the <strong>ForEachRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="d9f53-121">Un champ qui est inclus dans les critères doit également être un champ <em>dans</em>.</span><span class="sxs-lookup"><span data-stu-id="d9f53-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9f53-122"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="d9f53-122"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="d9f53-123">Non</span><span class="sxs-lookup"><span data-stu-id="d9f53-123">No</span></span></p></td>
<td><p><span data-ttu-id="d9f53-124">Chaîne qui fournit un autre nom pour le domaine spécifié par l’argument <em>dans</em> .</span><span class="sxs-lookup"><span data-stu-id="d9f53-124">A string that provides an alternative name for the domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="d9f53-125">Souvent utilisés pour raccourcir le nom de table de références ultérieures éviter d’éventuelles références ambigus. Si <em>Alias</em> n’est pas spécifié, le nom de la table ou requête sera utilisé comme alias.</span><span class="sxs-lookup"><span data-stu-id="d9f53-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d9f53-126">Notes</span><span class="sxs-lookup"><span data-stu-id="d9f53-126">Remarks</span></span>

<span data-ttu-id="d9f53-127">Utilisez l'action **[QuitterPourChaqueEnregistrement](exitforeachrecord-macro-action.md)** pour quitter immédiatement un bloc de données **PourChaqueEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="d9f53-127">Use the **[ExitForEachRecord](exitforeachrecord-macro-action.md)** action to exit a **ForEachRecord** data block immediately.</span></span>

