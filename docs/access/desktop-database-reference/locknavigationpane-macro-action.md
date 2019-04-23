---
title: LockNavigationPane, action de macro
TOCTitle: LockNavigationPane macro action
ms:assetid: abf7a989-c7cf-3efa-8df4-3c5b075d0e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821487(v=office.15)
ms:contentKeyID: 48546986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm172454
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7f6ee19edaf2efdc03301e98e709db6dd69f101a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289870"
---
# <a name="locknavigationpane-macro-action"></a><span data-ttu-id="b2673-102">LockNavigationPane, action de macro</span><span class="sxs-lookup"><span data-stu-id="b2673-102">LockNavigationPane macro action</span></span>


<span data-ttu-id="b2673-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2673-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b2673-104">Utilisez l'action **VerrouillerVoletNavigation** pour empêcher les utilisateurs de supprimer des objets de base de données qui sont affichés dans le volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="b2673-104">You can use the **LockNavigationPane** action to prevent users from deleting database objects that are displayed in the Navigation Pane.</span></span>

## <a name="setting"></a><span data-ttu-id="b2673-105">Setting</span><span class="sxs-lookup"><span data-stu-id="b2673-105">Setting</span></span>

<span data-ttu-id="b2673-106">L’action **VerrouillerVoletNavigation** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="b2673-106">The **LockNavigationPane** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b2673-107">Argument d’action</span><span class="sxs-lookup"><span data-stu-id="b2673-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b2673-108">Description</span><span class="sxs-lookup"><span data-stu-id="b2673-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2673-109"><strong>Lock</strong></span><span class="sxs-lookup"><span data-stu-id="b2673-109"><strong>Lock</strong></span></span></p></td>
<td><p><span data-ttu-id="b2673-110">Sélectionnez <strong>Oui</strong> pour verrouiller le volet de navigation ou <strong>Non</strong> pour déverrouiller le volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="b2673-110">Select <strong>Yes</strong> to lock the Navigation Pane, or <strong>No</strong> to unlock the Navigation Pane.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b2673-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="b2673-111">Remarks</span></span>

<span data-ttu-id="b2673-p101">Verrouiller le volet de navigation vous empêche de supprimer des objets de base de données ou de les couper pour les placer dans le Presse-papiers. En revanche, cette action ne vous empêche *pas* d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2673-p101">Locking the Navigation Pane prevents you from deleting database objects or cutting database objects to the clipboard. It does *not* prevent you from performing any of the following operations:</span></span>

  - <span data-ttu-id="b2673-114">copier des objets de base de données dans le Presse-papiers ;</span><span class="sxs-lookup"><span data-stu-id="b2673-114">Copying database objects to the clipboard</span></span>

  - <span data-ttu-id="b2673-115">coller des objets de base de données à partir du Presse-papiers ;</span><span class="sxs-lookup"><span data-stu-id="b2673-115">Pasting database objects from the clipboard</span></span>

  - <span data-ttu-id="b2673-116">afficher ou masquer le volet de navigation ;</span><span class="sxs-lookup"><span data-stu-id="b2673-116">Displaying or hiding the Navigation Pane</span></span>

  - <span data-ttu-id="b2673-117">sélectionner d'autres modèles d'organisation du volet de navigation ;</span><span class="sxs-lookup"><span data-stu-id="b2673-117">Selecting different Navigation Pane organization schemes</span></span>

  - <span data-ttu-id="b2673-118">afficher ou masquer des sections du volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="b2673-118">Showing or hiding sections of the Navigation Pane</span></span>

<span data-ttu-id="b2673-119">Pour exécuter l'action **VerrouillerVoletNavigation** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **LockNavigationPane** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="b2673-119">To run the **LockNavigationPane** action in a VBA module, use the **LockNavigationPane** method of the **DoCmd** object.</span></span>

