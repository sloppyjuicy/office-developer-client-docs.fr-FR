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
ms.openlocfilehash: 5986b8e891b42ce37cb68d8ce06e7f33feba1b8f
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937728"
---
# <a name="gotorecord-macro-action"></a><span data-ttu-id="f0b21-102">GoToRecord, action de macro</span><span class="sxs-lookup"><span data-stu-id="f0b21-102">GoToRecord macro action</span></span>


<span data-ttu-id="f0b21-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0b21-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f0b21-104">Utilisez l'action **AtteindreEnregistrement** pour que l'enregistrement spécifié devienne l'enregistrement actif dans le jeu de résultats d'une requête, d'une table ou d'un formulaire ouvert.</span><span class="sxs-lookup"><span data-stu-id="f0b21-104">You can use the **GoToRecord** action to make the specified record the current record in an open table, form, or query result set.</span></span>

## <a name="setting"></a><span data-ttu-id="f0b21-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0b21-105">Setting</span></span>

<span data-ttu-id="f0b21-106">L'action **AtteindreEnregistrement** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="f0b21-106">The **GoToRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f0b21-107">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="f0b21-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f0b21-108">Description</span><span class="sxs-lookup"><span data-stu-id="f0b21-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0b21-109"><strong>Type d'objet</strong></span><span class="sxs-lookup"><span data-stu-id="f0b21-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="f0b21-p101">Type d’objet qui contient l’enregistrement que vous souhaitez rendre actif. Cliquez sur <strong>Table</strong>, <strong>Requête</strong>, <strong>Formulaire</strong>, <strong>Vue serveur</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong> dans la zone <strong>Type d’objet</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Laissez cet argument vide pour sélectionner l’objet actif.</span><span class="sxs-lookup"><span data-stu-id="f0b21-p101">The type of object that contains the record you want to make current. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Server View</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. Leave this argument blank to select the active object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0b21-113"><strong>Nom de l'objet</strong></span><span class="sxs-lookup"><span data-stu-id="f0b21-113"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="f0b21-p102">Nom de l’objet qui contient l’enregistrement que vous souhaitez rendre actif. La zone <strong>Nom de l’objet</strong> affiche tous les objets de la base de données active correspondant au type sélectionné par l’argument <strong>Type d’objet</strong>. Si vous laissez l’argument <strong>Type d’objet</strong> vide, laissez également celui-ci vide.</span><span class="sxs-lookup"><span data-stu-id="f0b21-p102">The name of the object that contains the record you want to make the current record. The <strong>Object Name</strong> box shows all objects in the current database of the type selected by the <strong>Object Type</strong> argument. If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0b21-117"><strong>Record</strong></span><span class="sxs-lookup"><span data-stu-id="f0b21-117"><strong>Record</strong></span></span></p></td>
<td><p><span data-ttu-id="f0b21-p103">Enregistrement que vous souhaitez rendre actif. Cliquez sur <strong>Précédent</strong>, <strong>Suivant</strong>, <strong>Premier</strong>, <strong>Dernier</strong>, <strong>Atteindre</strong> ou <strong>Nouveau</strong> dans la zone <strong>Enregistrement</strong>. La valeur par défaut est <strong>Suivant</strong>.</span><span class="sxs-lookup"><span data-stu-id="f0b21-p103">The record to make the current record. Click <strong>Previous</strong>, <strong>Next</strong>, <strong>First</strong>, <strong>Last</strong>, <strong>Go To</strong>, or <strong>New</strong> in the <strong>Record</strong> box. The default is <strong>Next</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0b21-121"><strong>Offset</strong></span><span class="sxs-lookup"><span data-stu-id="f0b21-121"><strong>Offset</strong></span></span></p></td>
<td><p><span data-ttu-id="f0b21-122">Entier ou expression qui correspond à un entier.</span><span class="sxs-lookup"><span data-stu-id="f0b21-122">An integer or expression that evaluates to an integer.</span></span> <span data-ttu-id="f0b21-123">Une expression doit être précédée d’un signe égal (<strong>=</strong>).</span><span class="sxs-lookup"><span data-stu-id="f0b21-123">An expression must be preceded by an equal sign (<strong>=</strong>).</span></span> <span data-ttu-id="f0b21-124">Cet argument spécifie l’enregistrement à activer l’enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="f0b21-124">This argument specifies the record to make the current record.</span></span> <span data-ttu-id="f0b21-125">Vous pouvez utiliser l’argument <strong>décalage</strong> de deux manières :</span><span class="sxs-lookup"><span data-stu-id="f0b21-125">You can use the <strong>Offset</strong> argument in two ways:</span></span></p>
<ul>
<li><p><span data-ttu-id="f0b21-126">Lorsque l’argument <strong>Enregistrement</strong> a la valeur <strong>Suivant</strong> ou <strong>Précédent</strong>, Microsoft Office Access 2007 avance ou recule du nombre d’enregistrements spécifié dans l’argument <strong>Référence</strong>.</span><span class="sxs-lookup"><span data-stu-id="f0b21-126">When the <strong>Record</strong> argument is <strong>Next</strong> or <strong>Previous</strong>, Microsoft Office Access 2007 moves the number of records forward or backward specified in the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="f0b21-p105">Lorsque l’argument <strong>Enregistrement</strong> est défini sur <strong>Atteindre</strong>, Access accède à l’enregistrement dont le numéro est égal à la valeur de l’argument <strong>Référence</strong>. Le numéro de l’enregistrement est indiqué dans la zone de numéro d’enregistrement en bas de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f0b21-p105">When the <strong>Record</strong> argument is <strong>Go To</strong>, Access moves to the record with the number equal to the <strong>Offset</strong> argument. The record number is shown in the record number box at the bottom of the window.</span></span></p></li>
</ul>

> [!NOTE]
> <span data-ttu-id="f0b21-p106">Si vous utilisez le paramètre **Premier**, **Dernier** ou **Nouveau** pour l’argument **Enregistrement**, Access ignore l’argument **Référence**. Si vous entrez une valeur trop élevée pour l’argument **Référence**, Access affiche un message d’erreur. Vous ne pouvez pas entrer de nombres négatifs pour l’argument **Référence**.</span><span class="sxs-lookup"><span data-stu-id="f0b21-p106">If you use the **First**, **Last**, or **New** setting for the **Record** argument, Access ignores the **Offset** argument. If you enter an **Offset** argument that is too large, Access displays an error message. You can't enter negative numbers for the **Offset** argument.</span></span>


<p></p>
<ul>
<li><p><span data-ttu-id="f0b21-132">Lorsque l’argument <strong>Enregistrement</strong> a la valeur <strong>Suivant</strong> ou <strong>Précédent</strong>, Microsoft Office Access 2007 avance ou recule du nombre d’enregistrements spécifié dans l’argument <strong>Référence</strong>.</span><span class="sxs-lookup"><span data-stu-id="f0b21-132">When the <strong>Record</strong> argument is <strong>Next</strong> or <strong>Previous</strong>, Microsoft Office Access 2007 moves the number of records forward or backward specified in the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="f0b21-p107">Lorsque l’argument <strong>Enregistrement</strong> est défini sur <strong>Atteindre</strong>, Access accède à l’enregistrement dont le numéro est égal à la valeur de l’argument <strong>Référence</strong>. Le numéro de l’enregistrement est indiqué dans la zone de numéro d’enregistrement en bas de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f0b21-p107">When the <strong>Record</strong> argument is <strong>Go To</strong>, Access moves to the record with the number equal to the <strong>Offset</strong> argument. The record number is shown in the record number box at the bottom of the window.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f0b21-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="f0b21-135">Remarks</span></span>

<span data-ttu-id="f0b21-136">Si un contrôle particulier d'un enregistrement a le focus, cette action laisse le focus dans le même contrôle pour le nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f0b21-136">If the focus is in a particular control in a record, this action leaves it in the same control for the new record.</span></span>

<span data-ttu-id="f0b21-137">Vous pouvez utiliser le paramètre **Nouveau** dans l'argument **Enregistrement** pour passer à l'enregistrement vide à la fin d'un formulaire ou d'une table de manière à pouvoir entrer de nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="f0b21-137">You can use the **New** setting for the **Record** argument to move to the blank record at the end of a form or table so you can enter new data.</span></span>

<span data-ttu-id="f0b21-p108">Cette action équivaut à cliquer sur la flèche sous le bouton **Rechercher** de l'onglet **Accueil**, puis à cliquer sur **Atteindre**. Les sous-commandes **Premier**, **Dernier**, **Suivant**, **Précédent** et **Nouvel enregistrement** de la commande **Atteindre** ont le même effet sur l'objet sélectionné que les paramètres **Premier**, **Dernier**, **Suivant**, **Précédent** et **Nouveau** de l'argument **Enregistrement**. Vous pouvez également atteindre des enregistrements en utilisant les boutons de navigation en bas de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f0b21-p108">This action is similar to clicking the arrow below the **Find** button on the **Home** tab and then clicking **Go To**. The **First**, **Last**, **Next**, **Previous**, and **New Record** subcommands of the **Go To** command have the same effect on the selected object as the **First**, **Last**, **Next**, **Previous**, and **New** settings for the **Record** argument. You can also move to records by using the navigation buttons at the bottom of the window.</span></span>

<span data-ttu-id="f0b21-141">Vous pouvez utiliser l'action **AtteindreEnregistrement** pour rendre actif un enregistrement d'un formulaire masqué si vous spécifiez le formulaire masqué dans les arguments **Type d'objet** et **Nom de l'objet**.</span><span class="sxs-lookup"><span data-stu-id="f0b21-141">You can use the **GoToRecord** action to make a record on a hidden form the current record if you specify the hidden form in the **Object Type** and **Object Name** arguments.</span></span>

<span data-ttu-id="f0b21-142">Pour exécuter l'action **AtteindreEnregistrement** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **GoToRecord** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="f0b21-142">To run the **GoToRecord** action in a Visual Basic for Applications (VBA) module, use the **GoToRecord** method of the **DoCmd** object.</span></span>

