---
title: ImportSharePointList, action de macro
TOCTitle: ImportSharePointList macro action
ms:assetid: 6a633d7d-d81d-0e2e-6c1c-706a552c1bf2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195403(v=office.15)
ms:contentKeyID: 48545429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152234
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: df77d2375b66df907832b6ff2717427ae54a35a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291858"
---
# <a name="importsharepointlist-macro-action"></a><span data-ttu-id="f8411-102">ImportSharePointList, action de macro</span><span class="sxs-lookup"><span data-stu-id="f8411-102">ImportSharePointList macro action</span></span>

<span data-ttu-id="f8411-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8411-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f8411-104">L'action **ImporterListeSharePoint** permet d'importer ou de lier des données à partir d'un site Microsoft SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="f8411-104">You can use the **ImportSharePointList** action to import or link data from a Microsoft SharePoint Foundation site.</span></span>

> [!NOTE]
> <span data-ttu-id="f8411-105">Cette action ne sera pas autorisée si la base de données n’est pas approuvée.</span><span class="sxs-lookup"><span data-stu-id="f8411-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="f8411-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f8411-106">Setting</span></span>

<span data-ttu-id="f8411-107">L’action **ImporterListeSharePoint** utilise les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f8411-107">The **ImportSharePointList** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f8411-108">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="f8411-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f8411-109">Description</span><span class="sxs-lookup"><span data-stu-id="f8411-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8411-110"><strong>Type de transfert</strong></span><span class="sxs-lookup"><span data-stu-id="f8411-110"><strong>Transfer Type</strong></span></span></p></td>
<td><p><span data-ttu-id="f8411-111">Sélectionnez le type de transfert.</span><span class="sxs-lookup"><span data-stu-id="f8411-111">Select the type of transfer.</span></span></p>
<ul>
<li><p><span data-ttu-id="f8411-112">Sélectionnez <strong>Importer</strong> pour copier les données SharePoint Foundation dans un tableau dans Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="f8411-112">Select <strong>Import</strong> to copy the SharePoint Foundation data into a table in Microsoft Access.</span></span> <span data-ttu-id="f8411-113">Les mises à jour des données dans Access n'ont pas d'incidence sur les données dans SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="f8411-113">Updates to the data in Access do not affect the data in SharePoint Foundation.</span></span> <span data-ttu-id="f8411-114">De même, les mises à jour des données dans SharePoint Foundation n'affectent pas les données dans Access.</span><span class="sxs-lookup"><span data-stu-id="f8411-114">Likewise, updates to the data in SharePoint Foundation do not affect the data in Access.</span></span></p></li>
<li><p><span data-ttu-id="f8411-115">Sélectionnez <strong>lien</strong> pour créer une table attachée dans Access qui lie les données dans SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="f8411-115">Select <strong>Link</strong> to create a linked table in Access that links to the data in SharePoint Foundation.</span></span> <span data-ttu-id="f8411-116">Les mises à jour des données dans Access sont reflétées dans SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="f8411-116">Updates to the data in Access are reflected in SharePoint Foundation.</span></span> <span data-ttu-id="f8411-117">De même, les mises à jour des données dans SharePoint Foundation sont reflétées dans Access.</span><span class="sxs-lookup"><span data-stu-id="f8411-117">Likewise, updates to the data in SharePoint Foundation are reflected in Access.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8411-118"><strong>Adresse du site</strong></span><span class="sxs-lookup"><span data-stu-id="f8411-118"><strong>Site Address</strong></span></span></p></td>
<td><p><span data-ttu-id="f8411-119">Entrez le chemin d’accès complet au site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f8411-119">Enter the full path of the SharePoint site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8411-120"><strong>ID de liste</strong></span><span class="sxs-lookup"><span data-stu-id="f8411-120"><strong>List ID</strong></span></span></p></td>
<td><p><span data-ttu-id="f8411-121">Entrez le nom ou GUID de la liste à transférer.</span><span class="sxs-lookup"><span data-stu-id="f8411-121">Enter the name or GUID of the list to be transferred.</span></span> <span data-ttu-id="f8411-122">Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f8411-122">Required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8411-123"><strong>ID de vue</strong></span><span class="sxs-lookup"><span data-stu-id="f8411-123"><strong>View ID</strong></span></span></p></td>
<td><p><span data-ttu-id="f8411-p104">Entrez le GUID de l’affichage de la liste que vous souhaitez utiliser. Omettez cet argument pour transférer toutes les lignes et colonnes de la liste.</span><span class="sxs-lookup"><span data-stu-id="f8411-p104">Enter the GUID of the view for the list you want to use. Leave this argument blank to transfer all rows and columns in the list.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8411-126"><strong>Nom de la table</strong></span><span class="sxs-lookup"><span data-stu-id="f8411-126"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="f8411-127">Entrez le nom à afficher pour la table ou la table attachée dans Access.</span><span class="sxs-lookup"><span data-stu-id="f8411-127">Enter the name you want displayed for the table or linked table in Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8411-128"><strong>Valeurs d’affichage Liste de choix</strong></span><span class="sxs-lookup"><span data-stu-id="f8411-128"><strong>Get Lookup Display Values</strong></span></span></p></td>
<td><p><span data-ttu-id="f8411-129">Cliquez sur <strong>Oui</strong> si les valeurs d’affichage des champs de recherche doivent être transférées à la place de l’identificateur utilisé pour effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="f8411-129">Select <strong>Yes</strong> to transfer display values for Lookup fields instead of the ID used to perform the lookup.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f8411-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="f8411-130">Remarks</span></span>

- <span data-ttu-id="f8411-131">L'exécution de cette action équivaut à cliquer sur **Liste SharePoint** dans le groupe **Importer** de l'onglet **Données externes**. Les arguments utilisés pour l'action correspondent à vos choix dans l'Assistant Données externes.</span><span class="sxs-lookup"><span data-stu-id="f8411-131">This action has the same effect as clicking **SharePoint List** in the **Import** group on the **External Data** tab. The arguments for the action correspond to the choices you make in the Get External Data Wizard.</span></span>

- <span data-ttu-id="f8411-132">Pour exécuter l'action **ImporterListeSharePoint** dans un module VBA, utilisez la méthode **TransferSharePointList** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="f8411-132">To run the **ImportSharePointList** action in a VBA module, use the **TransferSharePointList** method of the **DoCmd** object.</span></span>

- <span data-ttu-id="f8411-133">Si vous spécifiez une liste ou un affichage qui n'existe pas, aucune erreur ne se produit, mais aucune donnée n'est transférée.</span><span class="sxs-lookup"><span data-stu-id="f8411-133">If you specify a nonexistent list or view, no error occurs, and no data is transferred.</span></span>

- <span data-ttu-id="f8411-p105">Le GUID d'une liste ou d'un affichage est un identificateur unique hexadécimal qui identifie cette liste ou cet affichage. Le GUID doit respecter le format suivant, où chaque « F » est un nombre hexadécimal (de 0 à 9 ou de A à F).</span><span class="sxs-lookup"><span data-stu-id="f8411-p105">A GUID is a unique hexadecimal identifier for a list or a view. A GUID must be entered in the following format, where each "F" is a hexadecimal number (0 through 9 or A through F).</span></span>
    
  `{FFFFFFFF-FFFF-FFFF-FFFF-FFFFFFFFFFFF}`
    
  <span data-ttu-id="f8411-136">Pour obtenir le GUID d'une liste ou d'un affichage à partir du site SharePoint, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="f8411-136">You can obtain the GUID for a list or view from the SharePoint site by using the following procedure:</span></span>
    
  1. <span data-ttu-id="f8411-137">Ouvrez la liste dans SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="f8411-137">Open the list in SharePoint Foundation.</span></span>
    
  2. <span data-ttu-id="f8411-138">Si l'affichage que vous recherchez n'est pas dans la liste, cliquez sur la flèche de la liste déroulante **Affichage** et sélectionnez l'affichage voulu.</span><span class="sxs-lookup"><span data-stu-id="f8411-138">If the view you want is not displayed, click the **View** drop-down arrow and then select the view you want.</span></span>
    
  3. <span data-ttu-id="f8411-139">Cliquez sur la flèche de la liste déroulante **Affichage**, puis sélectionnez **Modifier cet affichage**.L'adresse dans la barre d'adresse du navigateur contient les GUID de la liste et de l'affichage.</span><span class="sxs-lookup"><span data-stu-id="f8411-139">Click the **View** drop-down arrow and then select **Modify this View**.The address in the browser's address bar contains the GUIDs for both the list and the view.</span></span> <span data-ttu-id="f8411-140">Le GUID de la liste est à la suite de **Liste=** et celui de l'affichage est à la suite de **Affichage=**.</span><span class="sxs-lookup"><span data-stu-id="f8411-140">The GUID for the list follows **List=**, and the GUID for the view follows **View=**.</span></span> <span data-ttu-id="f8411-141">Cependant, dans l'adresse, chaque caractère **{** (accolade de gauche) est représenté par la chaîne **%7B**, chaque caractère **-** (tiret) est représenté par la chaîne **%2D** et chaque caractère **}** (accolade de droite) est représenté par la chaîne **%7D**.</span><span class="sxs-lookup"><span data-stu-id="f8411-141">However, in the address, each **{** (left brace) character is represented by the string **%7B**, each **-** (hyphen) character is represented by the string **%2D**, and each **}** (right brace) character is represented by the string **%7D**.</span></span> <span data-ttu-id="f8411-142">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="f8411-142">For example:</span></span>
        
     `https://MySite12/_layouts/ViewEdit.aspx?List=%7B2A82A404%2D5529%2D47DC%2DAE13%2DAC1D9BC0A84F%7D&View=%7B357B4FE6%2D44CF%2D4275%2DB91F%2D46558301579B%7D`
        
  <span data-ttu-id="f8411-143">Avant de pouvoir utiliser les GUID de l'adresse comme arguments dans cette action de macro, vous devez remplacer chaque chaîne **% 7B** par le caractère **{** , remplacer chaque chaîne **% 2D** par le **-** caractère et remplacer chaque chaîne **% 7D** par la chaîne **}** .</span><span class="sxs-lookup"><span data-stu-id="f8411-143">Before you can use the GUIDs from the address as arguments in this macro action, you must replace each **%7B** string with the **{** character, replace each **%2D** string with the **-** character, and replace each **%7D** string with the **}** character.</span></span> <span data-ttu-id="f8411-144">N'incluez pas le caractère **&** (et commercial) qui suit la chaîne **%7D** dans le GUID de la liste.</span><span class="sxs-lookup"><span data-stu-id="f8411-144">Do not include the **&** (ampersand) character that follows the **%7D** string in the list GUID.</span></span>

