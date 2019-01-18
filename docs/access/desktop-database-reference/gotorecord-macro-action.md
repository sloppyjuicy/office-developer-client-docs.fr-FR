---
title: GoToRecord, action de macro
TOCTitle: GoToRecord macro action
ms:assetid: 76f936de-739b-63be-9b28-5b0e111408e6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196037(v=office.15)
ms:contentKeyID: 48545712
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm58124
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7534ae84b57d14450009865ea330a4c54d4cfb44
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708479"
---
# <a name="gotorecord-macro-action"></a><span data-ttu-id="5717e-102">GoToRecord, action de macro</span><span class="sxs-lookup"><span data-stu-id="5717e-102">GoToRecord macro action</span></span>


<span data-ttu-id="5717e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5717e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5717e-104">Utilisez l'action **AtteindreEnregistrement** pour que l'enregistrement spécifié devienne l'enregistrement actif dans le jeu de résultats d'une requête, d'une table ou d'un formulaire ouvert.</span><span class="sxs-lookup"><span data-stu-id="5717e-104">You can use the **GoToRecord** action to make the specified record the current record in an open table, form, or query result set.</span></span>

## <a name="setting"></a><span data-ttu-id="5717e-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="5717e-105">Setting</span></span>

<span data-ttu-id="5717e-106">L'action **AtteindreEnregistrement** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="5717e-106">The **GoToRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5717e-107">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="5717e-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="5717e-108">Description</span><span class="sxs-lookup"><span data-stu-id="5717e-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5717e-109"><strong>Type d'objet</strong></span><span class="sxs-lookup"><span data-stu-id="5717e-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="5717e-p101">Type d’objet qui contient l’enregistrement que vous souhaitez rendre actif. Cliquez sur <strong>Table</strong>, <strong>Requête</strong>, <strong>Formulaire</strong>, <strong>Vue serveur</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong> dans la zone <strong>Type d’objet</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Laissez cet argument vide pour sélectionner l’objet actif.</span><span class="sxs-lookup"><span data-stu-id="5717e-p101">The type of object that contains the record you want to make current. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Server View</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. Leave this argument blank to select the active object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5717e-113"><strong>Nom de l'objet</strong></span><span class="sxs-lookup"><span data-stu-id="5717e-113"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="5717e-p102">Nom de l’objet qui contient l’enregistrement que vous souhaitez rendre actif. La zone <strong>Nom de l’objet</strong> affiche tous les objets de la base de données active correspondant au type sélectionné par l’argument <strong>Type d’objet</strong>. Si vous laissez l’argument <strong>Type d’objet</strong> vide, laissez également celui-ci vide.</span><span class="sxs-lookup"><span data-stu-id="5717e-p102">The name of the object that contains the record you want to make the current record. The <strong>Object Name</strong> box shows all objects in the current database of the type selected by the <strong>Object Type</strong> argument. If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5717e-117"><strong>Record</strong></span><span class="sxs-lookup"><span data-stu-id="5717e-117"><strong>Record</strong></span></span></p></td>
<td><p><span data-ttu-id="5717e-p103">Enregistrement que vous souhaitez rendre actif. Cliquez sur <strong>Précédent</strong>, <strong>Suivant</strong>, <strong>Premier</strong>, <strong>Dernier</strong>, <strong>Atteindre</strong> ou <strong>Nouveau</strong> dans la zone <strong>Enregistrement</strong>. La valeur par défaut est <strong>Suivant</strong>.</span><span class="sxs-lookup"><span data-stu-id="5717e-p103">The record to make the current record. Click <strong>Previous</strong>, <strong>Next</strong>, <strong>First</strong>, <strong>Last</strong>, <strong>Go To</strong>, or <strong>New</strong> in the <strong>Record</strong> box. The default is <strong>Next</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5717e-121"><strong>Offset</strong></span><span class="sxs-lookup"><span data-stu-id="5717e-121"><strong>Offset</strong></span></span></p></td>
<td><p><span data-ttu-id="5717e-122">Entier ou expression qui correspond à un entier.</span><span class="sxs-lookup"><span data-stu-id="5717e-122">An integer or expression that evaluates to an integer.</span></span> <span data-ttu-id="5717e-123">Une expression doit être précédée d’un signe égal (<strong>=</strong>).</span><span class="sxs-lookup"><span data-stu-id="5717e-123">An expression must be preceded by an equal sign (<strong>=</strong>).</span></span> <span data-ttu-id="5717e-124">Cet argument spécifie l’enregistrement à activer l’enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="5717e-124">This argument specifies the record to make the current record.</span></span> <span data-ttu-id="5717e-125">Vous pouvez utiliser l’argument <strong>décalage</strong> de deux manières :</span><span class="sxs-lookup"><span data-stu-id="5717e-125">You can use the <strong>Offset</strong> argument in two ways:</span></span></p>
<ul>
<li><p><span data-ttu-id="5717e-126">Lorsque l’argument <strong>Enregistrement</strong> a la valeur <strong>Suivant</strong> ou <strong>Précédent</strong>, Microsoft Office Access 2007 avance ou recule du nombre d’enregistrements spécifié dans l’argument <strong>Référence</strong>.</span><span class="sxs-lookup"><span data-stu-id="5717e-126">When the <strong>Record</strong> argument is <strong>Next</strong> or <strong>Previous</strong>, Microsoft Office Access 2007 moves the number of records forward or backward specified in the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="5717e-p105">Lorsque l’argument <strong>Enregistrement</strong> est défini sur <strong>Atteindre</strong>, Access accède à l’enregistrement dont le numéro est égal à la valeur de l’argument <strong>Référence</strong>. Le numéro de l’enregistrement est indiqué dans la zone de numéro d’enregistrement en bas de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5717e-p105">When the <strong>Record</strong> argument is <strong>Go To</strong>, Access moves to the record with the number equal to the <strong>Offset</strong> argument. The record number is shown in the record number box at the bottom of the window.</span></span></p>
<p><span data-ttu-id="5717e-129"><strong>Remarque</strong>: Si vous utilisez le <strong>premier</strong>, <strong>dernier</strong>ou <strong>Nouveau</strong> paramètre pour l’argument <strong>enregistrement</strong> , Access ignore l’argument <strong>décalage</strong> .</span><span class="sxs-lookup"><span data-stu-id="5717e-129"><strong>NOTE</strong>: If you use the <strong>First</strong>, <strong>Last</strong>, or <strong>New</strong> setting for the <strong>Record</strong> argument, Access ignores the <strong>Offset</strong> argument.</span></span> <span data-ttu-id="5717e-130">Si vous entrez un argument <strong>décalage</strong> trop grande, Access affiche un message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="5717e-130">If you enter an <strong>Offset</strong> argument that is too large, Access displays an error message.</span></span> <span data-ttu-id="5717e-131">Vous ne pouvez pas entrer les nombres négatifs pour l’argument <strong>décalage</strong> .</span><span class="sxs-lookup"><span data-stu-id="5717e-131">You can't enter negative numbers for the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="5717e-132">Lorsque l’argument <strong>Enregistrement</strong> a la valeur <strong>Suivant</strong> ou <strong>Précédent</strong>, Microsoft Office Access 2007 avance ou recule du nombre d’enregistrements spécifié dans l’argument <strong>Référence</strong>.</span><span class="sxs-lookup"><span data-stu-id="5717e-132">When the <strong>Record</strong> argument is <strong>Next</strong> or <strong>Previous</strong>, Microsoft Office Access 2007 moves the number of records forward or backward specified in the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="5717e-p107">Lorsque l’argument <strong>Enregistrement</strong> est défini sur <strong>Atteindre</strong>, Access accède à l’enregistrement dont le numéro est égal à la valeur de l’argument <strong>Référence</strong>. Le numéro de l’enregistrement est indiqué dans la zone de numéro d’enregistrement en bas de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5717e-p107">When the <strong>Record</strong> argument is <strong>Go To</strong>, Access moves to the record with the number equal to the <strong>Offset</strong> argument. The record number is shown in the record number box at the bottom of the window.</span></span></p></li>
</ul>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5717e-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="5717e-135">Remarks</span></span>

<span data-ttu-id="5717e-136">Si un contrôle particulier d'un enregistrement a le focus, cette action laisse le focus dans le même contrôle pour le nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="5717e-136">If the focus is in a particular control in a record, this action leaves it in the same control for the new record.</span></span>

<span data-ttu-id="5717e-137">Vous pouvez utiliser le paramètre **Nouveau** dans l'argument **Enregistrement** pour passer à l'enregistrement vide à la fin d'un formulaire ou d'une table de manière à pouvoir entrer de nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="5717e-137">You can use the **New** setting for the **Record** argument to move to the blank record at the end of a form or table so you can enter new data.</span></span>

<span data-ttu-id="5717e-p108">Cette action équivaut à cliquer sur la flèche sous le bouton **Rechercher** de l'onglet **Accueil**, puis à cliquer sur **Atteindre**. Les sous-commandes **Premier**, **Dernier**, **Suivant**, **Précédent** et **Nouvel enregistrement** de la commande **Atteindre** ont le même effet sur l'objet sélectionné que les paramètres **Premier**, **Dernier**, **Suivant**, **Précédent** et **Nouveau** de l'argument **Enregistrement**. Vous pouvez également atteindre des enregistrements en utilisant les boutons de navigation en bas de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5717e-p108">This action is similar to clicking the arrow below the **Find** button on the **Home** tab and then clicking **Go To**. The **First**, **Last**, **Next**, **Previous**, and **New Record** subcommands of the **Go To** command have the same effect on the selected object as the **First**, **Last**, **Next**, **Previous**, and **New** settings for the **Record** argument. You can also move to records by using the navigation buttons at the bottom of the window.</span></span>

<span data-ttu-id="5717e-141">Vous pouvez utiliser l'action **AtteindreEnregistrement** pour rendre actif un enregistrement d'un formulaire masqué si vous spécifiez le formulaire masqué dans les arguments **Type d'objet** et **Nom de l'objet**.</span><span class="sxs-lookup"><span data-stu-id="5717e-141">You can use the **GoToRecord** action to make a record on a hidden form the current record if you specify the hidden form in the **Object Type** and **Object Name** arguments.</span></span>

<span data-ttu-id="5717e-142">Pour exécuter l'action **AtteindreEnregistrement** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **GoToRecord** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="5717e-142">To run the **GoToRecord** action in a Visual Basic for Applications (VBA) module, use the **GoToRecord** method of the **DoCmd** object.</span></span>

