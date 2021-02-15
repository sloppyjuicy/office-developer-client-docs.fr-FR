---
title: 'HelloData : une application ADO simple'
TOCTitle: 'HelloData: A simple ADO application'
ms:assetid: c271abeb-8865-81f9-db8e-47d3db87ad30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249950(v=office.15)
ms:contentKeyID: 48547554
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3c7d9be9b91b3f847516eb3c22aa37e46c8a551d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292019"
---
# <a name="hellodata-a-simple-ado-application"></a><span data-ttu-id="d3c58-102">HelloData : une application ADO simple</span><span class="sxs-lookup"><span data-stu-id="d3c58-102">HelloData: A simple ADO application</span></span>

<span data-ttu-id="d3c58-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3c58-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d3c58-p101">Pour jeter les bases de l'exploration de la bibliothèque ADO, prenons l'exemple d'une application ADO simple appelée « HelloData ». HelloData suit les quatre étapes principales des opérations ADO (obtention, examen, modification et mise à jour des données). Afin de se concentrer sur les points fondamentaux d'ADO et éviter toute complication du code, la gestion des erreurs sera réduite à sa plus simple expression dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="d3c58-p101">To lay the groundwork for an exploration of the ADO library, consider a simple ADO application called "HelloData." HelloData steps through each of the four major ADO operations (getting, examining, editing, and updating data). In order to focus on the fundamentals of ADO and prevent code clutter, minimal error handling is done in the example.</span></span>

<span data-ttu-id="d3c58-107">L'application interroge la base de données exemple Northwind incluse dans Microsoft SQL Server 2000.</span><span class="sxs-lookup"><span data-stu-id="d3c58-107">The application queries the Northwind sample database that is included with Microsoft SQL Server 2000.</span></span>

<span data-ttu-id="d3c58-108">**Pour exécuter HelloData**</span><span class="sxs-lookup"><span data-stu-id="d3c58-108">**To run HelloData**</span></span>

1.  <span data-ttu-id="d3c58-109">Créez un nouveau projet Visual Basic exécutable standard qui fait référence à la bibliothèque ADO 2.5.</span><span class="sxs-lookup"><span data-stu-id="d3c58-109">Create a new Standard Executable Visual Basic Project that references the ADO 2.5 library.</span></span>

2.  <span data-ttu-id="d3c58-110">Créez quatre boutons de commande en haut du formulaire, en définissant les propriétés **Name** et **Caption** avec les valeurs indiquées dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d3c58-110">Create four command buttons at the top of the form, setting the **Name** and **Caption** properties to the values shown in the table below.</span></span>

3.  <span data-ttu-id="d3c58-111">En dessous des boutons, ajoutez un **contrôle Microsoft DataGrid** (Msdatgrd.ocx).</span><span class="sxs-lookup"><span data-stu-id="d3c58-111">Below the buttons, add a **Microsoft DataGrid Control** (Msdatgrd.ocx).</span></span> <span data-ttu-id="d3c58-112">Le fichier Msdatgrd.ocx est fourni avec Visual Basic et se trouve dans votre répertoire \\ windows \\ system32 ou \\ winnt \\ system32.</span><span class="sxs-lookup"><span data-stu-id="d3c58-112">The Msdatgrd.ocx file comes with Visual Basic and is located in your \\windows\\system32 or \\winnt\\system32 directory.</span></span> <span data-ttu-id="d3c58-113">Pour ajouter le contrôle DataGrid à la Boîte à outils Visual Basic, sélectionnez **Composants** dans le menu **Projet**.</span><span class="sxs-lookup"><span data-stu-id="d3c58-113">To add the DataGrid control to your Visual Basic toolbox pane, select **Components...** from the **Project** menu.</span></span> <span data-ttu-id="d3c58-114">Activez ensuite la case à cocher en regard de « Microsoft DataGrid Control 6.0 (SP3) (OLEDB) » et cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d3c58-114">Then check the box next to "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" and click **OK**.</span></span> <span data-ttu-id="d3c58-115">Pour ajouter le contrôle au projet, faites glisser le contrôle DataGrid de la Boîte à outils vers le formulaire Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d3c58-115">To add the control to the project, drag the DataGrid control from the Toolbox to the Visual Basic form.</span></span>

4.  <span data-ttu-id="d3c58-p103">Créez une **zone de texte** sur le formulaire en dessous de la grille et définissez ses propriétés comme indiqué dans le tableau. Lorsque vous avez terminé, le formulaire doit être identique à celui illustré dans la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="d3c58-p103">Create a **TextBox** on the form below the grid and set its properties as shown in the table. The form should look similar to the following figure when you are finished.</span></span>

5.  <span data-ttu-id="d3c58-118">Enfin, copiez le code répertorié dans [HelloData Code](hellodata-code.md) et collez-le dans la fenêtre d’éditeur de code du formulaire.</span><span class="sxs-lookup"><span data-stu-id="d3c58-118">Finally, copy the code listed in [HelloData Code](hellodata-code.md) and paste it into the code editor window of the form.</span></span> <span data-ttu-id="d3c58-119">Appuyez sur **F5** pour exécuter le code.</span><span class="sxs-lookup"><span data-stu-id="d3c58-119">Press **F5** to run the code.</span></span>

> [!NOTE]
> <span data-ttu-id="d3c58-p105">[!REMARQUE] Dans l'exemple suivant, et dans ce guide, l'utilisateur « MyId » et le mot de passe « 123aBc » sont utilisés pour l'authentification auprès du serveur. Vous devrez remplacer ces valeurs par des informations d'authentification de connexion réelles pour votre serveur. Remplacez également la valeur « MyServer » par le nom de votre serveur.</span><span class="sxs-lookup"><span data-stu-id="d3c58-p105">In the following example, and throughout the guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server. You should substitute these values with valid logon credentials for your server. Also, substitute the "MyServer" value with the name of your server.</span></span>

<span data-ttu-id="d3c58-123">Pour obtenir une description détaillée du code, voir [HelloData Details](hellodata-details.md).</span><span class="sxs-lookup"><span data-stu-id="d3c58-123">For a detailed description of the code, see [HelloData Details](hellodata-details.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d3c58-124">Type de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3c58-124">Control Type</span></span></p></th>
<th><p><span data-ttu-id="d3c58-125">Propriété</span><span class="sxs-lookup"><span data-stu-id="d3c58-125">Property</span></span></p></th>
<th><p><span data-ttu-id="d3c58-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3c58-126">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3c58-127">Formulaire</span><span class="sxs-lookup"><span data-stu-id="d3c58-127">Form</span></span></p></td>
<td><p><span data-ttu-id="d3c58-128">Nom</span><span class="sxs-lookup"><span data-stu-id="d3c58-128">Name</span></span></p></td>
<td><p><span data-ttu-id="d3c58-129">Form1</span><span class="sxs-lookup"><span data-stu-id="d3c58-129">Form1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="d3c58-130">Hauteur</span><span class="sxs-lookup"><span data-stu-id="d3c58-130">Height</span></span></p></td>
<td><p><span data-ttu-id="d3c58-131">6500</span><span class="sxs-lookup"><span data-stu-id="d3c58-131">6500</span></span></p></td>
</tr>
<tr class="odd">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="d3c58-132">Largeur</span><span class="sxs-lookup"><span data-stu-id="d3c58-132">Width</span></span></p></td>
<td><p><span data-ttu-id="d3c58-133">6500</span><span class="sxs-lookup"><span data-stu-id="d3c58-133">6500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3c58-134">Grille de données MS</span><span class="sxs-lookup"><span data-stu-id="d3c58-134">MS DataGrid</span></span></p></td>
<td><p><span data-ttu-id="d3c58-135">Nom</span><span class="sxs-lookup"><span data-stu-id="d3c58-135">Name</span></span></p></td>
<td><p><span data-ttu-id="d3c58-136">grdDisplay1</span><span class="sxs-lookup"><span data-stu-id="d3c58-136">grdDisplay1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3c58-137">TextBox</span><span class="sxs-lookup"><span data-stu-id="d3c58-137">TextBox</span></span></p></td>
<td><p><span data-ttu-id="d3c58-138">Nom</span><span class="sxs-lookup"><span data-stu-id="d3c58-138">Name</span></span></p></td>
<td><p><span data-ttu-id="d3c58-139">txtDisplay1</span><span class="sxs-lookup"><span data-stu-id="d3c58-139">txtDisplay1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="d3c58-140">Multiligne</span><span class="sxs-lookup"><span data-stu-id="d3c58-140">Multiline</span></span></p></td>
<td><p><span data-ttu-id="d3c58-141">true</span><span class="sxs-lookup"><span data-stu-id="d3c58-141">true</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3c58-142">Bouton de commande</span><span class="sxs-lookup"><span data-stu-id="d3c58-142">Command Button</span></span></p></td>
<td><p><span data-ttu-id="d3c58-143">Nom</span><span class="sxs-lookup"><span data-stu-id="d3c58-143">Name</span></span></p></td>
<td><p><span data-ttu-id="d3c58-144">cmdGetData</span><span class="sxs-lookup"><span data-stu-id="d3c58-144">cmdGetData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="d3c58-145">Légende</span><span class="sxs-lookup"><span data-stu-id="d3c58-145">Caption</span></span></p></td>
<td><p><span data-ttu-id="d3c58-146">Get Data</span><span class="sxs-lookup"><span data-stu-id="d3c58-146">Get Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3c58-147">Bouton de commande</span><span class="sxs-lookup"><span data-stu-id="d3c58-147">Command Button</span></span></p></td>
<td><p><span data-ttu-id="d3c58-148">Nom</span><span class="sxs-lookup"><span data-stu-id="d3c58-148">Name</span></span></p></td>
<td><p><span data-ttu-id="d3c58-149">cmdExamineData</span><span class="sxs-lookup"><span data-stu-id="d3c58-149">cmdExamineData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="d3c58-150">Légende</span><span class="sxs-lookup"><span data-stu-id="d3c58-150">Caption</span></span></p></td>
<td><p><span data-ttu-id="d3c58-151">Examine Data</span><span class="sxs-lookup"><span data-stu-id="d3c58-151">Examine Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3c58-152">Bouton de commande</span><span class="sxs-lookup"><span data-stu-id="d3c58-152">Command Button</span></span></p></td>
<td><p><span data-ttu-id="d3c58-153">Nom</span><span class="sxs-lookup"><span data-stu-id="d3c58-153">Name</span></span></p></td>
<td><p><span data-ttu-id="d3c58-154">cmdEditData</span><span class="sxs-lookup"><span data-stu-id="d3c58-154">cmdEditData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="d3c58-155">Légende</span><span class="sxs-lookup"><span data-stu-id="d3c58-155">Caption</span></span></p></td>
<td><p><span data-ttu-id="d3c58-156">Edit Data</span><span class="sxs-lookup"><span data-stu-id="d3c58-156">Edit Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3c58-157">Bouton de commande</span><span class="sxs-lookup"><span data-stu-id="d3c58-157">Command Button</span></span></p></td>
<td><p><span data-ttu-id="d3c58-158">Nom</span><span class="sxs-lookup"><span data-stu-id="d3c58-158">Name</span></span></p></td>
<td><p><span data-ttu-id="d3c58-159">cmdUpdateData</span><span class="sxs-lookup"><span data-stu-id="d3c58-159">cmdUpdateData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="d3c58-160">Légende</span><span class="sxs-lookup"><span data-stu-id="d3c58-160">Caption</span></span></p></td>
<td><p><span data-ttu-id="d3c58-161">Update Data</span><span class="sxs-lookup"><span data-stu-id="d3c58-161">Update Data</span></span></p></td>
</tr>
</tbody>
</table>



