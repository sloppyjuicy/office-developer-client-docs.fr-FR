---
title: Action de Macro ShowAllRecords
TOCTitle: ShowAllRecords Macro Action
ms:assetid: 6f9741ad-0440-4b8d-abea-009063c111f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195587(v=office.15)
ms:contentKeyID: 48545538
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b6482bcd34562e13e1783f8e0702718eeaed0b0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881733"
---
# <a name="showallrecords-macro-action"></a><span data-ttu-id="c640f-102">Action de Macro ShowAllRecords</span><span class="sxs-lookup"><span data-stu-id="c640f-102">ShowAllRecords Macro Action</span></span>


<span data-ttu-id="c640f-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c640f-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="c640f-104">Vous pouvez utiliser l’action **AfficherTousEnreg** pour supprimer n’importe quel filtre appliqué à la table active, le jeu de résultats de requête ou le formulaire et afficher tous les enregistrements dans l’ensemble de la table ou les résultats ou tous les enregistrements dans la table sous-jacente du formulaire ou de la requête.</span><span class="sxs-lookup"><span data-stu-id="c640f-104">You can use the **ShowAllRecords** action to remove any applied filter from the active table, query result set, or form, and display all records in the table or result set or all records in the form's underlying table or query.</span></span>

## <a name="setting"></a><span data-ttu-id="c640f-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c640f-105">Setting</span></span>

<span data-ttu-id="c640f-106">L’action **AfficherTousEnreg** ne possède aucun argument.</span><span class="sxs-lookup"><span data-stu-id="c640f-106">The **ShowAllRecords** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="c640f-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="c640f-107">Remarks</span></span>

<span data-ttu-id="c640f-108">Vous pouvez utiliser cette action pour vous assurer que tous les enregistrements (y compris les enregistrements modifiés ou nouveaux) d’une table, un jeu de résultats de requête ou un formulaire sont affichés.</span><span class="sxs-lookup"><span data-stu-id="c640f-108">You can use this action to ensure that all records (including any changed or new records) are displayed for a table, query result set, or form.</span></span> <span data-ttu-id="c640f-109">Cette action entraîne une actualisation des enregistrements pour un formulaire ou un sous-formulaire.</span><span class="sxs-lookup"><span data-stu-id="c640f-109">This action causes a requery of the records for a form or subform.</span></span>

<span data-ttu-id="c640f-110">Vous pouvez également utiliser cette action pour supprimer n’importe quel filtre appliqué avec l’action **AppliquerFiltre** , la commande **filtrer** sous l’onglet **accueil** , ou le **Nom du filtre** ou l’argument **Condition Where** de l’action **OuvrirFormulaire** .</span><span class="sxs-lookup"><span data-stu-id="c640f-110">You can also use this action to remove any filter that was applied with the **ApplyFilter** action, the **Filter** command on the **Home** tab, or the **Filter Name** or **Where Condition** argument of the **OpenForm** action.</span></span>

<span data-ttu-id="c640f-111">Cette action a le même effet qu’en cliquant sur **Basculer le filtre** sous l’onglet **accueil** , ou cliquez sur le champ filtré et cliquez sur **Effacer le filtre de...** en mode formulaire, en mode ou mode feuille de données.</span><span class="sxs-lookup"><span data-stu-id="c640f-111">This action has the same effect as clicking **Toggle Filter** on the **Home** tab, or right-clicking the filtered field and clicking **Clear filter from...** in Form view, Layout view, or Datasheet view.</span></span>

<span data-ttu-id="c640f-112">Pour exécuter l’action **AfficherTousEnreg** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **ShowAllRecords** de l’objet **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="c640f-112">To run the **ShowAllRecords** action in a Visual Basic for Applications (VBA) module, use the **ShowAllRecords** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="c640f-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="c640f-113">Example</span></span>

<span data-ttu-id="c640f-114">**Appliquer un filtre à l'aide d'une macro**</span><span class="sxs-lookup"><span data-stu-id="c640f-114">**Apply a filter by using a macro**</span></span>

<span data-ttu-id="c640f-p102">La macro suivante contient un ensemble d'actions, chacune filtrant les enregistrements d'un formulaire Répertoire téléphonique clients. Elle illustre l'utilisation des actions **AppliquerFiltre**, **AfficherTousEnreg** et **AtteindreContrôle**. Elle montre également l'utilisation de conditions pour déterminer quel bouton bascule d'un groupe d'options a été sélectionné sur le formulaire. Chaque ligne d'action est associée à un bouton bascule qui sélectionne le jeu d'enregistrements commençant par A, B, C, etc., ou tous les enregistrements. Cette macro doit être attachée à l'événement **AprèsMAJ** du groupe d'options FiltresNomsSociétés.</span><span class="sxs-lookup"><span data-stu-id="c640f-p102">The following macro contains a set of actions, each of which filters the records for a Customer Phone List form. It shows the use of the **ApplyFilter**, **ShowAllRecords**, and **GoToControl** actions. It also shows the use of conditions to determine which toggle button in an option group has been selected on the form. Each action row is associated with a toggle button that selects the set of records starting with A, B, C, and so on, or all records. This macro should be attached to the **AfterUpdate** event of the CompanyNameFilter option group.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c640f-120">Condition</span><span class="sxs-lookup"><span data-stu-id="c640f-120">Condition</span></span></p></th>
<th><p><span data-ttu-id="c640f-121">Action</span><span class="sxs-lookup"><span data-stu-id="c640f-121">Action</span></span></p></th>
<th><p><span data-ttu-id="c640f-122">Arguments : Paramètre</span><span class="sxs-lookup"><span data-stu-id="c640f-122">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="c640f-123">Commentaire</span><span class="sxs-lookup"><span data-stu-id="c640f-123">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c640f-124">[Filtres nom société] = 1</span><span class="sxs-lookup"><span data-stu-id="c640f-124">[Company Name Filters] =1</span></span></p></td>
<td><p><span data-ttu-id="c640f-125"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="c640f-125"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="c640f-126"><strong>Condition Where</strong>: [nom de société] comme &quot;[AÀÁÂÃÄ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="c640f-126"><strong>Where Condition</strong>: [Company Name] Like &quot;[AÀÁÂÃÄ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="c640f-127">Filtre les noms de sociétés commençant par A, À, Á, Â, Ã ou Ä.</span><span class="sxs-lookup"><span data-stu-id="c640f-127">Filter for company names that start with A, À, Á, Â, Ã, or Ä.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c640f-128">[Filtres nom société] = 2</span><span class="sxs-lookup"><span data-stu-id="c640f-128">[Company Name Filters] =2</span></span></p></td>
<td><p><span data-ttu-id="c640f-129"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="c640f-129"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="c640f-130"><strong>Condition Where</strong>: [nom de société] comme &quot;B \*&quot;</span><span class="sxs-lookup"><span data-stu-id="c640f-130"><strong>Where Condition</strong>: [Company Name] Like &quot;B\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="c640f-131">Filtre les noms de sociétés commençant par B.</span><span class="sxs-lookup"><span data-stu-id="c640f-131">Filter for company names that start with B.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c640f-132">[Filtres nom société] = 3</span><span class="sxs-lookup"><span data-stu-id="c640f-132">[Company Name Filters] =3</span></span></p></td>
<td><p><span data-ttu-id="c640f-133"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="c640f-133"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="c640f-134"><strong>Condition Where</strong>: [nom de société] comme &quot;[CÇ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="c640f-134"><strong>Where Condition</strong>: [Company Name] Like &quot;[CÇ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="c640f-135">Filtre les noms de sociétés commençant par C ou Ç.</span><span class="sxs-lookup"><span data-stu-id="c640f-135">Filter for company names that start with C or Ç.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c640f-136">... Les lignes d’action pour les lettres D à Y ont le même format que pour les lettres A à C ...</span><span class="sxs-lookup"><span data-stu-id="c640f-136">... Action rows for D through Y have the same format as A through C ...</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c640f-137">[Filtres nom société] = 26</span><span class="sxs-lookup"><span data-stu-id="c640f-137">[Company Name Filters] =26</span></span></p></td>
<td><p><span data-ttu-id="c640f-138"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="c640f-138"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="c640f-139"><strong>Condition Where</strong>: [nom de société] comme &quot;[ZÆØÅ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="c640f-139"><strong>Where Condition</strong>: [Company Name] Like &quot;[ZÆØÅ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="c640f-140">Filtre les noms de sociétés commençant par Z, Æ, Ø ou Å.</span><span class="sxs-lookup"><span data-stu-id="c640f-140">Filter for company names that start with Z, Æ, Ø, or Å.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c640f-141">[Filtres nom société] = 27</span><span class="sxs-lookup"><span data-stu-id="c640f-141">[Company Name Filters] =27</span></span></p></td>
<td><p><span data-ttu-id="c640f-142"><strong>ShowAllRecords</strong></span><span class="sxs-lookup"><span data-stu-id="c640f-142"><strong>ShowAllRecords</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="c640f-143">Affiche tous les enregistrements</span><span class="sxs-lookup"><span data-stu-id="c640f-143">Show all records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c640f-144">[RecordsetClone]. [RecordCount] &gt;0</span><span class="sxs-lookup"><span data-stu-id="c640f-144">[RecordsetClone].[RecordCount]&gt;0</span></span></p></td>
<td><p><span data-ttu-id="c640f-145"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="c640f-145"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="c640f-146"><strong>Nom du contrôle</strong>: NomSociété</span><span class="sxs-lookup"><span data-stu-id="c640f-146"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="c640f-147">Si des enregistrements sont renvoyés pour la lettre sélectionnée, déplace le focus sur le contrôle NomSociété.</span><span class="sxs-lookup"><span data-stu-id="c640f-147">If records are returned for the selected letter, move focus to the CompanyName control.</span></span></p></td>
</tr>
</tbody>
</table>

