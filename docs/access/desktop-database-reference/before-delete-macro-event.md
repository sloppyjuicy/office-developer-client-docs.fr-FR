---
title: Avant la suppression, événement de macro
TOCTitle: Before Delete Macro Event
ms:assetid: 1a8d3457-5c59-d13e-ada9-6ecd33dfd5b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845672(v=office.15)
ms:contentKeyID: 48543520
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm186077
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7863f8500a81014f3c70b5547fb363c46803f4f1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471336"
---
# <a name="before-delete-macro-event"></a><span data-ttu-id="9a83e-102">Avant la suppression, événement de macro</span><span class="sxs-lookup"><span data-stu-id="9a83e-102">Before Delete Macro Event</span></span>

<span data-ttu-id="9a83e-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a83e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9a83e-104">L'événement **Avant la suppression** se produit lorsqu'un enregistrement est supprimé, mais avant la validation de la modification.</span><span class="sxs-lookup"><span data-stu-id="9a83e-104">The **Before Delete** event occurs when a record is deleted, but before the change is committed.</span></span>

> [!NOTE]
> <span data-ttu-id="9a83e-105">[!REMARQUE] L'événement **Avant la suppression** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="9a83e-105">The **Before Delete** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a83e-106">Notes</span><span class="sxs-lookup"><span data-stu-id="9a83e-106">Remarks</span></span>

<span data-ttu-id="9a83e-107">Utilisez l'événement **Avant la suppression** pour effectuer toute action souhaitée avant qu'un enregistrement soit modifié.</span><span class="sxs-lookup"><span data-stu-id="9a83e-107">Use the **Before Delete** event to perform any actions that you want to occur before a record is deleted.</span></span> <span data-ttu-id="9a83e-108">**Avant la modification** s'utilise couramment pour effectuer une validation et pour déclencher des messages d'erreur personnalisés.</span><span class="sxs-lookup"><span data-stu-id="9a83e-108">The **Before Change** is commonly used to perform validation and to raise custom error messages.</span></span>

<span data-ttu-id="9a83e-109">Vous pouvez accéder à une valeur dans l’enregistrement à supprimer à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9a83e-109">You can access a value in the record to be deleted by using the following syntax:</span></span>

`[Old].[Field Name]`

<span data-ttu-id="9a83e-110">Par exemple, pour accéder à la valeur du champ QuantityInStock dans l’enregistrement à supprimer, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9a83e-110">For example, to access the value of the QuantityInStock field in the record to be deleted, use the following syntax:</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="9a83e-111">Les valeurs contenues dans l'enregistrement à supprimer sont supprimées définitivement lorsque l'événement **Avant la suppression** se termine.</span><span class="sxs-lookup"><span data-stu-id="9a83e-111">The values contained in the record to be deleted are deleted permanently when the **Before Delete** event ends.</span></span>

<span data-ttu-id="9a83e-112">Vous pouvez annuler l'événement **Avant la suppression** à l'aide de l'action **DéclencherErreur**.</span><span class="sxs-lookup"><span data-stu-id="9a83e-112">You can cancel the **Before Delete** event by using the **RaiseError** action.</span></span> <span data-ttu-id="9a83e-113">Lorsqu’une erreur se produit, les modifications contenues dans l’événement **Avant la suppression** sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="9a83e-113">When an error is raised, the changes contained in the **Before Delete** event are discarded.</span></span>

<span data-ttu-id="9a83e-114">Le tableau suivant répertorie les commandes de macros qui peuvent être utilisées dans l'événement **Avant la suppression**.</span><span class="sxs-lookup"><span data-stu-id="9a83e-114">The following table lists macro commands that can be used in the **Before Delete** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a83e-115">Type de commande</span><span class="sxs-lookup"><span data-stu-id="9a83e-115">Command Type</span></span></p></th>
<th><p><span data-ttu-id="9a83e-116">Commande</span><span class="sxs-lookup"><span data-stu-id="9a83e-116">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a83e-117">Déroulement de programme</span><span class="sxs-lookup"><span data-stu-id="9a83e-117">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="9a83e-118"><a href="comment-macro-statement.md">Comment, instruction de macro</a></span><span class="sxs-lookup"><span data-stu-id="9a83e-118"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a83e-119">Déroulement de programme</span><span class="sxs-lookup"><span data-stu-id="9a83e-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="9a83e-120"><a href="group-macro-statement.md">Group, instruction de macro</a></span><span class="sxs-lookup"><span data-stu-id="9a83e-120"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a83e-121">Déroulement de programme</span><span class="sxs-lookup"><span data-stu-id="9a83e-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="9a83e-122"><a href="if-then-else-macro-block.md">If...Then...Else, bloc de macro</a></span><span class="sxs-lookup"><span data-stu-id="9a83e-122"><a href="if-then-else-macro-block.md">If...Then...Else Macro Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a83e-123">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="9a83e-123">Data Block</span></span></p></td>
<td><p><span data-ttu-id="9a83e-124"><a href="lookuprecord-data-block.md">Action de Macro RechercherEnregistrement</a></span><span class="sxs-lookup"><span data-stu-id="9a83e-124"><a href="lookuprecord-data-block.md">LookupRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a83e-125">Action de données</span><span class="sxs-lookup"><span data-stu-id="9a83e-125">Data Action</span></span></p></td>
<td><p><span data-ttu-id="9a83e-126"><a href="clearmacroerror-macro-action.md">EffacerMacroErreur, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="9a83e-126"><a href="clearmacroerror-macro-action.md">ClearMacroError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a83e-127">Action de données</span><span class="sxs-lookup"><span data-stu-id="9a83e-127">Data Action</span></span></p></td>
<td><p><span data-ttu-id="9a83e-128"><a href="onerror-macro-action.md">SurErreur, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="9a83e-128"><a href="onerror-macro-action.md">OnError Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a83e-129">Action de données</span><span class="sxs-lookup"><span data-stu-id="9a83e-129">Data Action</span></span></p></td>
<td><p><span data-ttu-id="9a83e-130"><a href="raiseerror-macro-action.md">DéclencherErreur, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="9a83e-130"><a href="raiseerror-macro-action.md">RaiseError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a83e-131">Action de données</span><span class="sxs-lookup"><span data-stu-id="9a83e-131">Data Action</span></span></p></td>
<td><p><span data-ttu-id="9a83e-132"><a href="setlocalvar-macro-action.md">DéfinirVarLocale, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="9a83e-132"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a83e-133">Action de données</span><span class="sxs-lookup"><span data-stu-id="9a83e-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="9a83e-134"><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="9a83e-134"><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9a83e-135">Pour créer une macro de données qui capture l'événement **Avant la suppression**, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="9a83e-135">To create a Data macro that captures the **Before Delete** event, use the following steps.</span></span>

1.  <span data-ttu-id="9a83e-136">Ouvrez la table pour laquelle vous souhaitez capturer l'événement **Avant la suppression**.</span><span class="sxs-lookup"><span data-stu-id="9a83e-136">Open the table for which you want to capture the **Before Delete** event.</span></span>

2.  <span data-ttu-id="9a83e-137">Sous l’onglet **Table** , dans le groupe **Événements avant** , sélectionnez **Avant la suppression**.</span><span class="sxs-lookup"><span data-stu-id="9a83e-137">On the **Table** tab, in the **Before Events** group, select **Before Delete**.</span></span>

