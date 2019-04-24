---
title: Before Delete, événement de macro
TOCTitle: Before Delete macro event
ms:assetid: 1a8d3457-5c59-d13e-ada9-6ecd33dfd5b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845672(v=office.15)
ms:contentKeyID: 48543520
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm186077
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2b2a4f978a4af2ba79cab7807f0142d35d7d30c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296912"
---
# <a name="before-delete-macro-event"></a><span data-ttu-id="b9cdf-102">Before Delete, événement de macro</span><span class="sxs-lookup"><span data-stu-id="b9cdf-102">Before Delete macro event</span></span>

<span data-ttu-id="b9cdf-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b9cdf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b9cdf-104">L'événement **Avant la suppression** se produit lorsqu'un enregistrement est supprimé, mais avant la validation de la modification.</span><span class="sxs-lookup"><span data-stu-id="b9cdf-104">The **Before Delete** event occurs when a record is deleted, but before the change is committed.</span></span>

> [!NOTE]
> <span data-ttu-id="b9cdf-105">L’événement **Avant la suppression** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="b9cdf-105">The **Before Delete** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9cdf-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="b9cdf-106">Remarks</span></span>

<span data-ttu-id="b9cdf-107">Utilisez l'événement **Avant la suppression** pour effectuer toute action souhaitée avant qu'un enregistrement soit modifié.</span><span class="sxs-lookup"><span data-stu-id="b9cdf-107">Use the **Before Delete** event to perform any actions that you want to occur before a record is deleted.</span></span> <span data-ttu-id="b9cdf-108">**Avant la modification** s’utilise couramment pour effectuer une validation et pour déclencher des messages d’erreur personnalisés.</span><span class="sxs-lookup"><span data-stu-id="b9cdf-108">The **Before Change** is commonly used to perform validation and to raise custom error messages.</span></span>

<span data-ttu-id="b9cdf-109">Vous pouvez accéder à une valeur dans l'enregistrement à supprimer à l'aide de la syntaxe suivante:</span><span class="sxs-lookup"><span data-stu-id="b9cdf-109">You can access a value in the record to be deleted by using the following syntax:</span></span>

`[Old].[Field Name]`

<span data-ttu-id="b9cdf-110">Par exemple, pour accéder à la valeur du champ QuantityInStock dans l'enregistrement à supprimer, utilisez la syntaxe suivante:</span><span class="sxs-lookup"><span data-stu-id="b9cdf-110">For example, to access the value of the QuantityInStock field in the record to be deleted, use the following syntax:</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="b9cdf-111">Les valeurs contenues dans l'enregistrement à supprimer sont supprimées définitivement lorsque l'événement **Avant la suppression** se termine.</span><span class="sxs-lookup"><span data-stu-id="b9cdf-111">The values contained in the record to be deleted are deleted permanently when the **Before Delete** event ends.</span></span>

<span data-ttu-id="b9cdf-112">Vous pouvez annuler l'événement **Avant la suppression** à l'aide de l'action **DéclencherErreur**.</span><span class="sxs-lookup"><span data-stu-id="b9cdf-112">You can cancel the **Before Delete** event by using the **RaiseError** action.</span></span> <span data-ttu-id="b9cdf-113">Lorsqu'une erreur est générée, les modifications contenues dans l'événement **avant la suppression** sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="b9cdf-113">When an error is raised, the changes contained in the **Before Delete** event are discarded.</span></span>

<span data-ttu-id="b9cdf-114">Le tableau suivant répertorie les commandes de macros qui peuvent être utilisées dans l'événement **Avant la suppression**.</span><span class="sxs-lookup"><span data-stu-id="b9cdf-114">The following table lists macro commands that can be used in the **Before Delete** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9cdf-115">Type de commande</span><span class="sxs-lookup"><span data-stu-id="b9cdf-115">Command Type</span></span></p></th>
<th><p><span data-ttu-id="b9cdf-116">Command</span><span class="sxs-lookup"><span data-stu-id="b9cdf-116">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9cdf-117">Déroulement de programme</span><span class="sxs-lookup"><span data-stu-id="b9cdf-117">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="b9cdf-118"><a href="comment-macro-statement.md">Comment, instruction de macro</a></span><span class="sxs-lookup"><span data-stu-id="b9cdf-118"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9cdf-119">Déroulement de programme</span><span class="sxs-lookup"><span data-stu-id="b9cdf-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="b9cdf-120"><a href="group-macro-statement.md">Group, instruction de macro</a></span><span class="sxs-lookup"><span data-stu-id="b9cdf-120"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9cdf-121">Déroulement de programme</span><span class="sxs-lookup"><span data-stu-id="b9cdf-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="b9cdf-122"><a href="if-then-else-macro-block.md">If...Then...Else, bloc de macro</a></span><span class="sxs-lookup"><span data-stu-id="b9cdf-122"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9cdf-123">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="b9cdf-123">Data Block</span></span></p></td>
<td><p><span data-ttu-id="b9cdf-124"><a href="lookuprecord-data-block.md">RechercherEnregistrement, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="b9cdf-124"><a href="lookuprecord-data-block.md">LookupRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9cdf-125">Action de données</span><span class="sxs-lookup"><span data-stu-id="b9cdf-125">Data Action</span></span></p></td>
<td><p><span data-ttu-id="b9cdf-126"><a href="clearmacroerror-macro-action.md">ClearMacroError, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="b9cdf-126"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9cdf-127">Action de données</span><span class="sxs-lookup"><span data-stu-id="b9cdf-127">Data Action</span></span></p></td>
<td><p><span data-ttu-id="b9cdf-128"><a href="onerror-macro-action.md">OnError, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="b9cdf-128"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9cdf-129">Action de données</span><span class="sxs-lookup"><span data-stu-id="b9cdf-129">Data Action</span></span></p></td>
<td><p><span data-ttu-id="b9cdf-130"><a href="raiseerror-macro-action.md">RaiseError, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="b9cdf-130"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9cdf-131">Action de données</span><span class="sxs-lookup"><span data-stu-id="b9cdf-131">Data Action</span></span></p></td>
<td><p><span data-ttu-id="b9cdf-132"><a href="setlocalvar-macro-action.md">SetLocalVar, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="b9cdf-132"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9cdf-133">Action de données</span><span class="sxs-lookup"><span data-stu-id="b9cdf-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="b9cdf-134"><a href="stopmacro-macro-action.md">StopMacro, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="b9cdf-134"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b9cdf-135">Pour créer une macro de données qui capture l'événement **Avant la suppression**, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="b9cdf-135">To create a Data macro that captures the **Before Delete** event, use the following steps.</span></span>

1.  <span data-ttu-id="b9cdf-136">Ouvrez la table pour laquelle vous souhaitez capturer l'événement **Avant la suppression**.</span><span class="sxs-lookup"><span data-stu-id="b9cdf-136">Open the table for which you want to capture the **Before Delete** event.</span></span>

2.  <span data-ttu-id="b9cdf-137">Sous l'onglet **table** , dans le groupe **événements avant** , sélectionnez **avant de supprimer**.</span><span class="sxs-lookup"><span data-stu-id="b9cdf-137">On the **Table** tab, in the **Before Events** group, select **Before Delete**.</span></span>

