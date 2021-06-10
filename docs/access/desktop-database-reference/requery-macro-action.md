---
title: Requery, action de macro
TOCTitle: Requery macro action
ms:assetid: 6dbdcae5-81b6-9925-4cad-64b178c23060
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195544(v=office.15)
ms:contentKeyID: 48545499
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm30402
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 8b90af8d1cda073ffa37022bb5db5e8cf8e3b978
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306705"
---
# <a name="requery-macro-action"></a><span data-ttu-id="dac39-102">Requery, action de macro</span><span class="sxs-lookup"><span data-stu-id="dac39-102">Requery macro action</span></span>

<span data-ttu-id="dac39-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dac39-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dac39-p101">Vous pouvez utiliser l'action **Actualiser** pour mettre à jour les données d'un contrôle spécifié de l'objet actif en actualisant la source du contrôle. Si aucun contrôle n'est spécifié, cette action actualise la source de l'objet lui-même. Utilisez cette action pour garantir que l'objet actif ou l'un de ses contrôles affiche les données les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="dac39-p101">You can use the **Requery** action to update the data in a specified control on the active object by requerying the source of the control. If no control is specified, this action requeries the source of the object itself. Use this action to ensure that the active object or one of its controls displays the most current data.</span></span>

## <a name="setting"></a><span data-ttu-id="dac39-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="dac39-107">Setting</span></span>

<span data-ttu-id="dac39-108">L’action **Actualiser** accepte l’argument suivant.</span><span class="sxs-lookup"><span data-stu-id="dac39-108">The **Requery** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dac39-109">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="dac39-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="dac39-110">Description</span><span class="sxs-lookup"><span data-stu-id="dac39-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dac39-111"><strong>Nom du contrôle</strong></span><span class="sxs-lookup"><span data-stu-id="dac39-111"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="dac39-p102">Nom du contrôle à mettre à jour. Entrez le nom du contrôle dans la zone <strong>Nom contrôle</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Vous devez utiliser uniquement le nom du contrôle, et non son identificateur complet, par exemple <strong>Formulaires</strong>!<em>nomformulaire</em>!<em>nomcontrôle</em>). Laissez cet argument vide pour actualiser la source de l’objet actif. Si l’objet actif est une feuille de données ou le jeu de résultats d’une requête, vous devez laisser cet argument vide.</span><span class="sxs-lookup"><span data-stu-id="dac39-p102">The name of the control you want to update. Enter the control name in the <strong>Control Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You should use only the name of the control, not the fully qualified identifier (such as <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>). Leave this argument blank to requery the source of the active object. If the active object is a datasheet or a query result set, you must leave this argument blank.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="dac39-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="dac39-117">Remarks</span></span>

<span data-ttu-id="dac39-118">L’action **Actualiser** effectue l’une des actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="dac39-118">The **Requery** action does one of the following:</span></span>

- <span data-ttu-id="dac39-119">Réexécute la requête sur laquelle est basé le contrôle ou l'objet.</span><span class="sxs-lookup"><span data-stu-id="dac39-119">Reruns the query on which the control or object is based.</span></span>

- <span data-ttu-id="dac39-120">Affiche les enregistrements nouveaux ou modifiés et enlève les éventuels enregistrements supprimés de la table sur laquelle est basé le contrôle ou l'objet.</span><span class="sxs-lookup"><span data-stu-id="dac39-120">Displays any new or changed records, and removes any deleted records from the table on which the control or object is based.</span></span>

> [!NOTE]
> <span data-ttu-id="dac39-121">[!REMARQUE] L'action **Actualiser** n'affecte pas la position du pointeur d'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="dac39-121">The **Requery** action does not affect the position of the record pointer.</span></span>

<span data-ttu-id="dac39-122">Les contrôles basés sur une requête ou une table comprennent :</span><span class="sxs-lookup"><span data-stu-id="dac39-122">Controls based on a query or table include:</span></span>

- <span data-ttu-id="dac39-123">zones de liste et zones de liste modifiable ;</span><span class="sxs-lookup"><span data-stu-id="dac39-123">List boxes and combo boxes.</span></span>

- <span data-ttu-id="dac39-124">contrôles de sous-formulaire ;</span><span class="sxs-lookup"><span data-stu-id="dac39-124">Subform controls.</span></span>

- <span data-ttu-id="dac39-125">des objets OLE, tels que des graphiques ;</span><span class="sxs-lookup"><span data-stu-id="dac39-125">OLE objects, such as charts.</span></span>

- <span data-ttu-id="dac39-126">des contrôles contenant des fonctions de domaine, telles que **DSum**.</span><span class="sxs-lookup"><span data-stu-id="dac39-126">Controls containing domain aggregate functions, such as **DSum**.</span></span>

<span data-ttu-id="dac39-127">Si le contrôle spécifié n'est pas basé sur une requête ou une table, cette action force un recalcul du contrôle.</span><span class="sxs-lookup"><span data-stu-id="dac39-127">If the specified control isn't based on a query or table, this action forces a recalculation of the control.</span></span>

<span data-ttu-id="dac39-p103">Si vous laissez l'argument **Nom du contrôle** vide, l'action **Actualiser** équivaut à appuyer sur Maj+F9 lorsque l'objet a le focus. Si un contrôle sous-formulaire a le focus, cette action actualise seulement la source du sous-formulaire (comme lorsque vous appuyez sur les touches Maj+F9).</span><span class="sxs-lookup"><span data-stu-id="dac39-p103">If you leave the **Control Name** argument blank, the **Requery** action has the same effect as pressing SHIFT+F9 when the object has the focus. If a subform control has the focus, this action requeries only the source of the subform (just as pressing SHIFT+F9 does).</span></span>

> [!NOTE]
> <span data-ttu-id="dac39-p104">[!REMARQUE] L'action **Actualiser** actualise la source du contrôle ou de l'objet. En revanche, l'action **Redessiner** redessine les contrôles dans l'objet spécifié mais n'actualise pas la base de données et n'affiche pas les nouveaux enregistrements. L'action **AfficherTousEnreg** actualise non seulement l'objet actif mais supprime également tous les filtres appliqués, ce que ne fait pas l'action **Actualiser**.</span><span class="sxs-lookup"><span data-stu-id="dac39-p104">The **Requery** action requeries the source of the control or object. In contrast, the **RepaintObject** action repaints controls in the specified object but doesn't requery the database or display new records. The **ShowAllRecords** action not only requeries the active object, but it also removes any applied filters, which the **Requery** action doesn't do.</span></span>

<span data-ttu-id="dac39-133">Pour actualiser un contrôle qui ne figure pas dans l'objet actif, vous devez utiliser la méthode **Requery** dans un module Visual Basic pour Applications (VBA), et non l'action **Actualiser** ou sa méthode **Requery** correspondante de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="dac39-133">If you want to requery a control that isn't on the active object, you must use the **Requery** method in a Visual Basic for Applications (VBA) module, not the **Requery** action or its corresponding **Requery** method of the **DoCmd** object.</span></span> <span data-ttu-id="dac39-134">La méthode **Requery** dans VBA est plus rapide que l'action **Actualiser** ou la méthode **DoCmd.Requery**.</span><span class="sxs-lookup"><span data-stu-id="dac39-134">The **Requery** method in VBA is faster than the **Requery** action or the **DoCmd.Requery** method.</span></span> <span data-ttu-id="dac39-135">En outre, lorsque vous utilisez l'action **Actualiser** ou la méthode **DoCmd.Requery**, Microsoft Access ferme la requête et la recharge à partir de la base de données tandis qu'avec la méthode **Requery**, réexécute la requête sans la fermer ni la charger.</span><span class="sxs-lookup"><span data-stu-id="dac39-135">In addition, when you use the **Requery** action or the **DoCmd.Requery** method, Microsoft Access closes the query and reloads it from the database, but when you use the **Requery** method, Access reruns the query without closing and reloading it.</span></span> <span data-ttu-id="dac39-136">Notez que la méthode ActiveX **Requery** de l’objet Data object (ADO) fonctionne de la même manière que la méthode **Requery** Access.</span><span class="sxs-lookup"><span data-stu-id="dac39-136">Note that the ActiveX Data object (ADO) **Requery** method works the same way as the Access **Requery** method.</span></span>

