---
title: WorkflowTasks, action de macro
TOCTitle: WorkflowTasks macro action
ms:assetid: 4b299681-b45b-f6d1-2cfe-ebf01712bfc1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193503(v=office.15)
ms:contentKeyID: 48544684
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm8454
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 921396edd480e06194d1c3dcbb683aa8556553e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306005"
---
# <a name="workflowtasks-macro-action"></a><span data-ttu-id="d2420-102">WorkflowTasks, action de macro</span><span class="sxs-lookup"><span data-stu-id="d2420-102">WorkflowTasks macro action</span></span>


<span data-ttu-id="d2420-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2420-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2420-104">L’action **TâchesFluxTravail** permet d’afficher la boîte de dialogue **Tâche du flux de travail**.</span><span class="sxs-lookup"><span data-stu-id="d2420-104">You can use the **WorkflowTasks** action to display the **Workflow Task** dialog box.</span></span>

## <a name="setting"></a><span data-ttu-id="d2420-105">Setting</span><span class="sxs-lookup"><span data-stu-id="d2420-105">Setting</span></span>

<span data-ttu-id="d2420-106">L’action **TâchesFluxTravail** utilise l’argument suivant :</span><span class="sxs-lookup"><span data-stu-id="d2420-106">The **WorkflowTasks** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d2420-107">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="d2420-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d2420-108">Description</span><span class="sxs-lookup"><span data-stu-id="d2420-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2420-109"><strong>Numéro d’enregistrement</strong></span><span class="sxs-lookup"><span data-stu-id="d2420-109"><strong>Record Number</strong></span></span></p></td>
<td><p><span data-ttu-id="d2420-110">Position de l’élément dans la liste Microsoft SharePoint Foundation, en commençant par <strong>1</strong> pour le premier élément de la liste, <strong>2</strong> pour le deuxième élément, etc.</span><span class="sxs-lookup"><span data-stu-id="d2420-110">The position of the item in the Microsoft SharePoint Foundation list, starting with <strong>1</strong> for the first item in the list, <strong>2</strong> for the second item, and so on.</span></span> <span data-ttu-id="d2420-111">Vous pouvez également entrer une expression pour cet argument.</span><span class="sxs-lookup"><span data-stu-id="d2420-111">You can also enter an expression for this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d2420-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="d2420-112">Remarks</span></span>

  - <span data-ttu-id="d2420-p102">L'action **TâchesFluxTravail** ouvre la boîte de dialogue **Tâches de flux de travail** qui affiche toutes les tâches disponibles pour l'élément spécifié. Un flux de travail doit être défini pour la liste dans SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="d2420-p102">The **WorkflowTasks** action opens the **Workflow Tasks** dialog box. This dialog box displays all tasks that are available for the specified item. A workflow must be defined for the list in SharePoint Foundation.</span></span>

  - <span data-ttu-id="d2420-p103">L'action **TâchesFluxTravail** ne peut être utilisée qu'après l'ouverture et la sélection d'une liste SharePoint Foundation liée. Pour ouvrir et sélectionner la liste liée, utilisez l'action **OuvrirTable**. Si la liste est déjà ouverte, utilisez l'action **SélectionnerObjet** pour la sélectionner.</span><span class="sxs-lookup"><span data-stu-id="d2420-p103">The **WorkflowTasks** action can only be used after a linked SharePoint Foundation list has been opened and selected. To open and select the linked list, use the **OpenTable** action. If the list is already open, use the **SelectObject** action to select it.</span></span>

  - <span data-ttu-id="d2420-119">Utiliser l'action **TâchesFluxTravail** équivaut à cliquer avec le bouton droit sur une cellule d'une liste SharePoint Foundation , ouverte en mode Feuille de données, à pointer sur **Flux de travail**, puis à cliquer sur **Tâches de flux de travail**.</span><span class="sxs-lookup"><span data-stu-id="d2420-119">The **WorkflowTasks** action has the same effect as right-clicking any cell in a linked SharePoint Foundation list while it is open in datasheet view, pointing to **Workflow**, and then clicking **Workflow Tasks**.</span></span>

  - <span data-ttu-id="d2420-120">Pour exécuter l'action **TâchesFluxTravail** dans un module VBA, utilisez la méthode **WorkflowTasks** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="d2420-120">To run the **WorkflowTasks** action in a VBA module, use the **WorkflowTasks** method of the **DoCmd** object.</span></span>

