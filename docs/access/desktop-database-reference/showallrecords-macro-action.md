---
title: ShowAllRecords, action de macro
TOCTitle: ShowAllRecords macro action
ms:assetid: 6f9741ad-0440-4b8d-abea-009063c111f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195587(v=office.15)
ms:contentKeyID: 48545538
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 201b284a56fbd3030b41a95424b41c73ee13e385
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308644"
---
# <a name="showallrecords-macro-action"></a><span data-ttu-id="f3eab-102">ShowAllRecords, action de macro</span><span class="sxs-lookup"><span data-stu-id="f3eab-102">ShowAllRecords macro action</span></span>


<span data-ttu-id="f3eab-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3eab-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="f3eab-104">Vous pouvez utiliser l'action **AfficherTousEnreg** pour supprimer tout filtre appliqué de la table active, du jeu de résultats de la requête ou du formulaire, et afficher tous les enregistrements de la table ou du jeu de résultats, ou tous les enregistrements de la table ou de la requête sous-jacente du formulaire.</span><span class="sxs-lookup"><span data-stu-id="f3eab-104">You can use the **ShowAllRecords** action to remove any applied filter from the active table, query result set, or form, and display all records in the table or result set or all records in the form's underlying table or query.</span></span>

## <a name="setting"></a><span data-ttu-id="f3eab-105">Setting</span><span class="sxs-lookup"><span data-stu-id="f3eab-105">Setting</span></span>

<span data-ttu-id="f3eab-106">L'action **AfficherTousEnreg** ne possède aucun argument.</span><span class="sxs-lookup"><span data-stu-id="f3eab-106">The **ShowAllRecords** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3eab-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="f3eab-107">Remarks</span></span>

<span data-ttu-id="f3eab-108">Vous pouvez utiliser cette action pour vous assurer que tous les enregistrements (y compris les enregistrements modifiés ou nouveaux) sont affichés pour une table, un jeu de résultats de requête ou un formulaire.</span><span class="sxs-lookup"><span data-stu-id="f3eab-108">You can use this action to ensure that all records (including any changed or new records) are displayed for a table, query result set, or form.</span></span> <span data-ttu-id="f3eab-109">Cette action entraîne une rérogation des enregistrements d'un formulaire ou d'un sous-formulaire.</span><span class="sxs-lookup"><span data-stu-id="f3eab-109">This action causes a requery of the records for a form or subform.</span></span>

<span data-ttu-id="f3eab-110">Vous pouvez également utiliser cette action pour supprimer un filtre appliqué à l'aide de l'action **AppliquerFiltre** , de la commande **filtre** de l'onglet **Accueil** ou de l'argument **nom du filtre** ou **condition WHERE** de l'action **OuvrirFormulaire** .</span><span class="sxs-lookup"><span data-stu-id="f3eab-110">You can also use this action to remove any filter that was applied with the **ApplyFilter** action, the **Filter** command on the **Home** tab, or the **Filter Name** or **Where Condition** argument of the **OpenForm** action.</span></span>

<span data-ttu-id="f3eab-111">Cette action équivaut à cliquer sur basculer le **filtre** sous l'onglet **Accueil** , ou à cliquer avec le bouton droit sur le champ filtré, puis à cliquer sur **effacer le filtre de...** en mode formulaire, en mode page ou en mode feuille de type de base de type.</span><span class="sxs-lookup"><span data-stu-id="f3eab-111">This action has the same effect as clicking **Toggle Filter** on the **Home** tab, or right-clicking the filtered field and clicking **Clear filter from...** in Form view, Layout view, or Datasheet view.</span></span>

<span data-ttu-id="f3eab-112">Pour exécuter l'action **AfficherTousEnreg** dans un module Visual Basic pour applications (VBA), utilisez la méthode **ShowAllRecords** de l'objet **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="f3eab-112">To run the **ShowAllRecords** action in a Visual Basic for Applications (VBA) module, use the **ShowAllRecords** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="f3eab-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="f3eab-113">Example</span></span>

<span data-ttu-id="f3eab-114">**Appliquer un filtre à l'aide d'une macro**</span><span class="sxs-lookup"><span data-stu-id="f3eab-114">**Apply a filter by using a macro**</span></span>

<span data-ttu-id="f3eab-p102">La macro suivante contient un ensemble d'actions, chacune filtrant les enregistrements d'un formulaire Répertoire téléphonique clients. Elle illustre l'utilisation des actions **AppliquerFiltre**, **AfficherTousEnreg** et **AtteindreContrôle**. Elle montre également l'utilisation de conditions pour déterminer quel bouton bascule d'un groupe d'options a été sélectionné sur le formulaire. Chaque ligne d'action est associée à un bouton bascule qui sélectionne le jeu d'enregistrements commençant par A, B, C, etc., ou tous les enregistrements. Cette macro doit être attachée à l'événement **AprèsMAJ** du groupe d'options FiltresNomsSociétés.</span><span class="sxs-lookup"><span data-stu-id="f3eab-p102">The following macro contains a set of actions, each of which filters the records for a Customer Phone List form. It shows the use of the **ApplyFilter**, **ShowAllRecords**, and **GoToControl** actions. It also shows the use of conditions to determine which toggle button in an option group has been selected on the form. Each action row is associated with a toggle button that selects the set of records starting with A, B, C, and so on, or all records. This macro should be attached to the **AfterUpdate** event of the CompanyNameFilter option group.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f3eab-120">Condition</span><span class="sxs-lookup"><span data-stu-id="f3eab-120">Condition</span></span></p></th>
<th><p><span data-ttu-id="f3eab-121">Action</span><span class="sxs-lookup"><span data-stu-id="f3eab-121">Action</span></span></p></th>
<th><p><span data-ttu-id="f3eab-122">Arguments : Paramètre</span><span class="sxs-lookup"><span data-stu-id="f3eab-122">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="f3eab-123">Commentaire</span><span class="sxs-lookup"><span data-stu-id="f3eab-123">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3eab-124">[Filtres de nom de société] = 1</span><span class="sxs-lookup"><span data-stu-id="f3eab-124">[Company Name Filters] =1</span></span></p></td>
<td><p><span data-ttu-id="f3eab-125"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="f3eab-125"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="f3eab-126"><strong>Condition WHERE</strong>: [nom de la société &quot;] comme [AÀÁÂÃÄ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="f3eab-126"><strong>Where Condition</strong>: [Company Name] Like &quot;[AÀÁÂÃÄ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="f3eab-127">Filtre les noms de sociétés commençant par A, À, Á, Â, Ã ou Ä.</span><span class="sxs-lookup"><span data-stu-id="f3eab-127">Filter for company names that start with A, À, Á, Â, Ã, or Ä.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3eab-128">[Filtres de nom de société] = 2</span><span class="sxs-lookup"><span data-stu-id="f3eab-128">[Company Name Filters] =2</span></span></p></td>
<td><p><span data-ttu-id="f3eab-129"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="f3eab-129"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="f3eab-130"><strong>Condition WHERE</strong>: [nom de la société &quot;] comme B \*&quot;</span><span class="sxs-lookup"><span data-stu-id="f3eab-130"><strong>Where Condition</strong>: [Company Name] Like &quot;B\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="f3eab-131">Filtre les noms de sociétés commençant par B.</span><span class="sxs-lookup"><span data-stu-id="f3eab-131">Filter for company names that start with B.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3eab-132">[Filtres de nom de société] = 3</span><span class="sxs-lookup"><span data-stu-id="f3eab-132">[Company Name Filters] =3</span></span></p></td>
<td><p><span data-ttu-id="f3eab-133"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="f3eab-133"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="f3eab-134"><strong>Condition WHERE</strong>: [nom de la société &quot;] comme [CÇ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="f3eab-134"><strong>Where Condition</strong>: [Company Name] Like &quot;[CÇ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="f3eab-135">Filtre les noms de sociétés commençant par C ou Ç.</span><span class="sxs-lookup"><span data-stu-id="f3eab-135">Filter for company names that start with C or Ç.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3eab-136">... Les lignes d’action pour les lettres D à Y ont le même format que pour les lettres A à C ...</span><span class="sxs-lookup"><span data-stu-id="f3eab-136">... Action rows for D through Y have the same format as A through C ...</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3eab-137">[Filtres de nom de société] = 26</span><span class="sxs-lookup"><span data-stu-id="f3eab-137">[Company Name Filters] =26</span></span></p></td>
<td><p><span data-ttu-id="f3eab-138"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="f3eab-138"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="f3eab-139"><strong>Condition WHERE</strong>: [nom de la société &quot;] comme [ZÆØÅ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="f3eab-139"><strong>Where Condition</strong>: [Company Name] Like &quot;[ZÆØÅ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="f3eab-140">Filtre les noms de sociétés commençant par Z, Æ, Ø ou Å.</span><span class="sxs-lookup"><span data-stu-id="f3eab-140">Filter for company names that start with Z, Æ, Ø, or Å.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3eab-141">[Filtres de nom de société] = 27</span><span class="sxs-lookup"><span data-stu-id="f3eab-141">[Company Name Filters] =27</span></span></p></td>
<td><p><span data-ttu-id="f3eab-142"><strong>ShowAllRecords</strong></span><span class="sxs-lookup"><span data-stu-id="f3eab-142"><strong>ShowAllRecords</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="f3eab-143">Affiche tous les enregistrements</span><span class="sxs-lookup"><span data-stu-id="f3eab-143">Show all records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3eab-144">[RecordsetClone]. RecordCount &gt;0</span><span class="sxs-lookup"><span data-stu-id="f3eab-144">[RecordsetClone].[RecordCount]&gt;0</span></span></p></td>
<td><p><span data-ttu-id="f3eab-145"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="f3eab-145"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="f3eab-146"><strong>Nom du contrôle</strong>: NomSociété</span><span class="sxs-lookup"><span data-stu-id="f3eab-146"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="f3eab-147">Si des enregistrements sont renvoyés pour la lettre sélectionnée, déplace le focus sur le contrôle NomSociété.</span><span class="sxs-lookup"><span data-stu-id="f3eab-147">If records are returned for the selected letter, move focus to the CompanyName control.</span></span></p></td>
</tr>
</tbody>
</table>

