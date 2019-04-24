---
title: StartNewWorkflow, action de macro
TOCTitle: StartNewWorkflow macro action
ms:assetid: b3e81a11-b816-0eef-fc70-6d6da7a5a845
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822054(v=office.15)
ms:contentKeyID: 48547206
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm198223
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 1e37d72754531fc4dd51427eefb355a057d08073
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306397"
---
# <a name="startnewworkflow-macro-action"></a><span data-ttu-id="5675a-102">StartNewWorkflow, action de macro</span><span class="sxs-lookup"><span data-stu-id="5675a-102">StartNewWorkflow macro action</span></span>


<span data-ttu-id="5675a-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5675a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5675a-104">L'action **DémarrerNouveauFluxTravail** permet de lancer un nouveau flux de travail pour un élément dans une liste Microsoft SharePoint Foundation liée.</span><span class="sxs-lookup"><span data-stu-id="5675a-104">You can use the **StartNewWorkflow** action to start a new workflow for an item in a linked Microsoft SharePoint Foundation list.</span></span>

## <a name="setting"></a><span data-ttu-id="5675a-105">Setting</span><span class="sxs-lookup"><span data-stu-id="5675a-105">Setting</span></span>

<span data-ttu-id="5675a-106">L’action **DémarrerNouveauFluxTravail** utilise les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="5675a-106">The **StartNewWorkflow** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5675a-107">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="5675a-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="5675a-108">Description</span><span class="sxs-lookup"><span data-stu-id="5675a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5675a-109"><strong>Numéro d’enregistrement</strong></span><span class="sxs-lookup"><span data-stu-id="5675a-109"><strong>Record Number</strong></span></span></p></td>
<td><p><span data-ttu-id="5675a-110">Position de l'élément dans la liste SharePoint Foundation, en commençant par <strong>1</strong> pour le premier élément de la liste, <strong>2</strong> pour le deuxième élément, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="5675a-110">The position of the item in the SharePoint Foundation list, starting with <strong>1</strong> for the first item in the list, <strong>2</strong> for the second item, and so on.</span></span> <span data-ttu-id="5675a-111">Vous pouvez également entrer une expression pour cet argument.</span><span class="sxs-lookup"><span data-stu-id="5675a-111">You can also enter an expression for this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5675a-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="5675a-112">Remarks</span></span>

  - <span data-ttu-id="5675a-p102">L'action **DémarrerNouveauFluxTravail** ouvre la boîte de dialogue **Démarrer un nouveau flux de travail**. Cette boîte de dialogue affiche tous les flux de travail disponibles pour l'élément spécifié. Un flux de travail doit être défini pour la liste dans SharePoint Foundation avant d'être exécuté via cette action.</span><span class="sxs-lookup"><span data-stu-id="5675a-p102">The **StartNewWorkflow** action opens the **Start New Workflow** dialog box. This dialog box displays all workflows that are available for the specified item. A workflow must be defined for the list in SharePoint Foundation before you can start it using this action.</span></span>

  - <span data-ttu-id="5675a-p103">L'action **DémarrerNouveauFluxTravail** ne peut être utilisée qu'après l'ouverture et la sélection d'une liste SharePoint liée. Pour ouvrir et sélectionner la liste liée, utilisez l'action **OuvrirTable**. Si la liste est déjà ouverte, utilisez l'action **SélectionnerObjet** pour la sélectionner.</span><span class="sxs-lookup"><span data-stu-id="5675a-p103">The **StartNewWorkflow** action can only be used after a linked SharePoint list has been opened and selected. To open and select the linked list, use the **OpenTable** action. If the list is already open, use the **SelectObject** action to select it.</span></span>

  - <span data-ttu-id="5675a-119">Utiliser l'action **DémarrerNouveauFluxTravail** équivaut à cliquer avec le bouton droit sur une cellule d'une liste SharePoint liée, ouverte en mode Feuille de données, à pointer sur **Flux de travail**, puis à cliquer sur **Démarrer un nouveau flux de travail**.</span><span class="sxs-lookup"><span data-stu-id="5675a-119">The **StartNewWorkflow** action has the same effect as right-clicking any cell in a linked SharePoint list while it is open in Datasheet view, pointing to **Workflow**, and then clicking **Start New Workflow**.</span></span>

  - <span data-ttu-id="5675a-120">Pour exécuter l'action **DémarrerNouveauFluxTravail** dans un module VBA, utilisez la méthode **StartNewWorkflow** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="5675a-120">To run the **StartNewWorkflow** action in a VBA module, use the **StartNewWorkflow** method of the **DoCmd** object.</span></span>

