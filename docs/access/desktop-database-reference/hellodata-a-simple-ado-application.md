---
title: 'HelloData : une application ADO simple'
TOCTitle: 'HelloData: A Simple ADO Application'
ms:assetid: c271abeb-8865-81f9-db8e-47d3db87ad30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249950(v=office.15)
ms:contentKeyID: 48547554
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9e70d611f351cf3ff073a1ad91e359a08e026295
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863296"
---
# <a name="hellodata-a-simple-ado-application"></a><span data-ttu-id="d04f3-102">HelloData : une application ADO simple</span><span class="sxs-lookup"><span data-stu-id="d04f3-102">HelloData: A Simple ADO Application</span></span>


<span data-ttu-id="d04f3-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d04f3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d04f3-p101">Pour jeter les bases de l'exploration de la bibliothèque ADO, prenons l'exemple d'une application ADO simple appelée « HelloData ». HelloData suit les quatre étapes principales des opérations ADO (obtention, examen, modification et mise à jour des données). Afin de se concentrer sur les points fondamentaux d'ADO et éviter toute complication du code, la gestion des erreurs sera réduite à sa plus simple expression dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="d04f3-p101">To lay the groundwork for an exploration of the ADO library, consider a simple ADO application called "HelloData." HelloData steps through each of the four major ADO operations (getting, examining, editing, and updating data). In order to focus on the fundamentals of ADO and prevent code clutter, minimal error handling is done in the example.</span></span>

<span data-ttu-id="d04f3-107">L'application interroge la base de données exemple Northwind incluse dans Microsoft SQL Server 2000.</span><span class="sxs-lookup"><span data-stu-id="d04f3-107">The application queries the Northwind sample database that is included with Microsoft SQL Server 2000.</span></span>

<span data-ttu-id="d04f3-108">**Pour exécuter HelloData**</span><span class="sxs-lookup"><span data-stu-id="d04f3-108">**To run HelloData**</span></span>

1.  <span data-ttu-id="d04f3-109">Créez un nouveau projet Visual Basic exécutable standard qui fait référence à la bibliothèque ADO 2.5.</span><span class="sxs-lookup"><span data-stu-id="d04f3-109">Create a new Standard Executable Visual Basic Project that references the ADO 2.5 library.</span></span>

2.  <span data-ttu-id="d04f3-110">Créez quatre boutons de commande en haut du formulaire, en définissant les propriétés **Name** et **Caption** avec les valeurs indiquées dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d04f3-110">Create four command buttons at the top of the form, setting the **Name** and **Caption** properties to the values shown in the table below.</span></span>

3.  <span data-ttu-id="d04f3-111">En dessous des boutons, ajoutez un **contrôle Microsoft DataGrid** (Msdatgrd.ocx).</span><span class="sxs-lookup"><span data-stu-id="d04f3-111">Below the buttons, add a **Microsoft DataGrid Control** (Msdatgrd.ocx).</span></span> <span data-ttu-id="d04f3-112">Ce fichier est fourni avec Visual Basic et se trouve dans votre \\windows\\system32 ou \\winnt\\répertoire system32.</span><span class="sxs-lookup"><span data-stu-id="d04f3-112">The Msdatgrd.ocx file comes with Visual Basic and is located in your \\windows\\system32 or \\winnt\\system32 directory.</span></span> <span data-ttu-id="d04f3-113">Pour ajouter le contrôle DataGrid à la Boîte à outils Visual Basic, sélectionnez **Composants** dans le menu **Projet**.</span><span class="sxs-lookup"><span data-stu-id="d04f3-113">To add the DataGrid control to your Visual Basic toolbox pane, select **Components...** from the **Project** menu.</span></span> <span data-ttu-id="d04f3-114">Activez ensuite la case à cocher en regard de « Microsoft DataGrid Control 6.0 (SP3) (OLEDB) » et cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d04f3-114">Then check the box next to "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" and click **OK**.</span></span> <span data-ttu-id="d04f3-115">Pour ajouter le contrôle au projet, faites glisser le contrôle DataGrid de la Boîte à outils vers le formulaire Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d04f3-115">To add the control to the project, drag the DataGrid control from the Toolbox to the Visual Basic form.</span></span>

4.  <span data-ttu-id="d04f3-p103">Créez une **zone de texte** sur le formulaire en dessous de la grille et définissez ses propriétés comme indiqué dans le tableau. Lorsque vous avez terminé, le formulaire doit être identique à celui illustré dans la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="d04f3-p103">Create a **TextBox** on the form below the grid and set its properties as shown in the table. The form should look similar to the following figure when you are finished.</span></span>

5.  <span data-ttu-id="d04f3-118">Enfin, copiez le code figurant dans le [HelloData Code](hellodata-code.md) et collez-le dans la fenêtre de l’éditeur de code du formulaire.</span><span class="sxs-lookup"><span data-stu-id="d04f3-118">Finally, copy the code listed in [HelloData Code](hellodata-code.md) and paste it into the code editor window of the form.</span></span> <span data-ttu-id="d04f3-119">Appuyez sur **F5** pour exécuter le code.</span><span class="sxs-lookup"><span data-stu-id="d04f3-119">Press **F5** to run the code.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d04f3-p105">[!REMARQUE] Dans l'exemple suivant, et dans ce guide, l'utilisateur « MyId » et le mot de passe « 123aBc » sont utilisés pour l'authentification auprès du serveur. Vous devrez remplacer ces valeurs par des informations d'authentification de connexion réelles pour votre serveur. Remplacez également la valeur « MyServer » par le nom de votre serveur.</span><span class="sxs-lookup"><span data-stu-id="d04f3-p105">In the following example, and throughout the guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server. You should substitute these values with valid logon credentials for your server. Also, substitute the "MyServer" value with the name of your server.</span></span></P>



<span data-ttu-id="d04f3-123">Pour obtenir une description détaillée du code, voir les [Informations détaillées sur HelloData](hellodata-details.md).</span><span class="sxs-lookup"><span data-stu-id="d04f3-123">For a detailed description of the code, see [HelloData Details](hellodata-details.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d04f3-124">Type de contrôle</span><span class="sxs-lookup"><span data-stu-id="d04f3-124">Control Type</span></span></p></th>
<th><p><span data-ttu-id="d04f3-125">Propriété</span><span class="sxs-lookup"><span data-stu-id="d04f3-125">Property</span></span></p></th>
<th><p><span data-ttu-id="d04f3-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="d04f3-126">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d04f3-127">Formulaire</span><span class="sxs-lookup"><span data-stu-id="d04f3-127">Form</span></span></p></td>
<td><p><span data-ttu-id="d04f3-128">Name</span><span class="sxs-lookup"><span data-stu-id="d04f3-128">Name</span></span></p></td>
<td><p><span data-ttu-id="d04f3-129">Form1</span><span class="sxs-lookup"><span data-stu-id="d04f3-129">Form1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="d04f3-130">Height</span><span class="sxs-lookup"><span data-stu-id="d04f3-130">Height</span></span></p></td>
<td><p><span data-ttu-id="d04f3-131">6500</span><span class="sxs-lookup"><span data-stu-id="d04f3-131">6500</span></span></p></td>
</tr>
<tr class="odd">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="d04f3-132">Width</span><span class="sxs-lookup"><span data-stu-id="d04f3-132">Width</span></span></p></td>
<td><p><span data-ttu-id="d04f3-133">6500</span><span class="sxs-lookup"><span data-stu-id="d04f3-133">6500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04f3-134">Grille de données MS</span><span class="sxs-lookup"><span data-stu-id="d04f3-134">MS DataGrid</span></span></p></td>
<td><p><span data-ttu-id="d04f3-135">Name</span><span class="sxs-lookup"><span data-stu-id="d04f3-135">Name</span></span></p></td>
<td><p><span data-ttu-id="d04f3-136">grdDisplay1</span><span class="sxs-lookup"><span data-stu-id="d04f3-136">grdDisplay1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04f3-137">Zone de texte</span><span class="sxs-lookup"><span data-stu-id="d04f3-137">TextBox</span></span></p></td>
<td><p><span data-ttu-id="d04f3-138">Name</span><span class="sxs-lookup"><span data-stu-id="d04f3-138">Name</span></span></p></td>
<td><p><span data-ttu-id="d04f3-139">txtDisplay1</span><span class="sxs-lookup"><span data-stu-id="d04f3-139">txtDisplay1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="d04f3-140">Multiline</span><span class="sxs-lookup"><span data-stu-id="d04f3-140">Multiline</span></span></p></td>
<td><p><span data-ttu-id="d04f3-141">true</span><span class="sxs-lookup"><span data-stu-id="d04f3-141">true</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04f3-142">Bouton de commande</span><span class="sxs-lookup"><span data-stu-id="d04f3-142">Command Button</span></span></p></td>
<td><p><span data-ttu-id="d04f3-143">Name</span><span class="sxs-lookup"><span data-stu-id="d04f3-143">Name</span></span></p></td>
<td><p><span data-ttu-id="d04f3-144">cmdGetData</span><span class="sxs-lookup"><span data-stu-id="d04f3-144">cmdGetData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="d04f3-145">Caption</span><span class="sxs-lookup"><span data-stu-id="d04f3-145">Caption</span></span></p></td>
<td><p><span data-ttu-id="d04f3-146">Get Data</span><span class="sxs-lookup"><span data-stu-id="d04f3-146">Get Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04f3-147">Bouton de commande</span><span class="sxs-lookup"><span data-stu-id="d04f3-147">Command Button</span></span></p></td>
<td><p><span data-ttu-id="d04f3-148">Name</span><span class="sxs-lookup"><span data-stu-id="d04f3-148">Name</span></span></p></td>
<td><p><span data-ttu-id="d04f3-149">cmdExamineData</span><span class="sxs-lookup"><span data-stu-id="d04f3-149">cmdExamineData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="d04f3-150">Caption</span><span class="sxs-lookup"><span data-stu-id="d04f3-150">Caption</span></span></p></td>
<td><p><span data-ttu-id="d04f3-151">Examine Data</span><span class="sxs-lookup"><span data-stu-id="d04f3-151">Examine Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04f3-152">Bouton de commande</span><span class="sxs-lookup"><span data-stu-id="d04f3-152">Command Button</span></span></p></td>
<td><p><span data-ttu-id="d04f3-153">Name</span><span class="sxs-lookup"><span data-stu-id="d04f3-153">Name</span></span></p></td>
<td><p><span data-ttu-id="d04f3-154">cmdEditData</span><span class="sxs-lookup"><span data-stu-id="d04f3-154">cmdEditData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="d04f3-155">Caption</span><span class="sxs-lookup"><span data-stu-id="d04f3-155">Caption</span></span></p></td>
<td><p><span data-ttu-id="d04f3-156">Edit Data</span><span class="sxs-lookup"><span data-stu-id="d04f3-156">Edit Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04f3-157">Bouton de commande</span><span class="sxs-lookup"><span data-stu-id="d04f3-157">Command Button</span></span></p></td>
<td><p><span data-ttu-id="d04f3-158">Name</span><span class="sxs-lookup"><span data-stu-id="d04f3-158">Name</span></span></p></td>
<td><p><span data-ttu-id="d04f3-159">cmdUpdateData</span><span class="sxs-lookup"><span data-stu-id="d04f3-159">cmdUpdateData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="d04f3-160">Caption</span><span class="sxs-lookup"><span data-stu-id="d04f3-160">Caption</span></span></p></td>
<td><p><span data-ttu-id="d04f3-161">Update Data</span><span class="sxs-lookup"><span data-stu-id="d04f3-161">Update Data</span></span></p></td>
</tr>
</tbody>
</table>



