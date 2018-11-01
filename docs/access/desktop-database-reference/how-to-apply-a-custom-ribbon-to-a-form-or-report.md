---
title: Appliquer un ruban personnalisé à un formulaire ou à un rapport
TOCTitle: Apply a custom ribbon to a form or report
description: Comment appliquer des rubans personnalisés lors du chargement d’un formulaire ou un état dans Access 2013.
ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15)
ms:contentKeyID: 48545865
ms.date: 10/16/2018
mtps_version: v=office.15
ms.openlocfilehash: e494985054ffd91440f3aff6eb671b781a5f65d7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888824"
---
# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a><span data-ttu-id="da043-103">Appliquer un ruban personnalisé à un formulaire ou à un rapport</span><span class="sxs-lookup"><span data-stu-id="da043-103">Apply a custom ribbon to a form or report</span></span>

<span data-ttu-id="da043-104">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="da043-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="da043-105">Le ruban utilise le balisage XML déclaratif textuels qui simplifie la création et la personnalisation du ruban.</span><span class="sxs-lookup"><span data-stu-id="da043-105">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="da043-106">Avec quelques lignes de code XML, vous pouvez créer l’interface de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="da043-106">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="da043-107">Access fournit la flexibilité de la personnalisation de l’interface utilisateur du ruban.</span><span class="sxs-lookup"><span data-stu-id="da043-107">Access provides flexibility in customizing the ribbon user interface.</span></span> 

<span data-ttu-id="da043-108">Par exemple, marquage de personnalisation permettre être stockée dans une table, incorporé dans une procédure VBA, stocké dans une autre base de données Access ou liée à une feuille de calcul Excel.</span><span class="sxs-lookup"><span data-stu-id="da043-108">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="da043-109">Cette rubrique décrit comment appliquer des rubans personnalisés lors du chargement d’un formulaire ou un état.</span><span class="sxs-lookup"><span data-stu-id="da043-109">This topic describes how to apply customized ribbons when loading a form or report.</span></span>

## <a name="make-the-ribbon-customization-xml-available"></a><span data-ttu-id="da043-110">Disposition de la personnalisation du ruban XML</span><span class="sxs-lookup"><span data-stu-id="da043-110">Make the ribbon customization XML available</span></span>

### <a name="store-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="da043-111">Stocker l’extensibilité du ruban XML dans une table</span><span class="sxs-lookup"><span data-stu-id="da043-111">Store ribbon extensibility XML in a table</span></span>

<span data-ttu-id="da043-112">Une des méthodes que vous pouvez utiliser pour rendre disponibles des personnalisations de ruban consiste à stocker dans une table.</span><span class="sxs-lookup"><span data-stu-id="da043-112">One method that you can use to make ribbon customizations available is to store them in a table.</span></span> <span data-ttu-id="da043-113">Si vous stockez les personnalisations dans une table dénommée **RubansSysU**, les personnalisations peuvent être implémentées sans utiliser de macros ou du code VBA.</span><span class="sxs-lookup"><span data-stu-id="da043-113">If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="da043-114">**RubansSysU** est une table système créée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="da043-114">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="da043-115">Le tableau doit être créé en utilisant des noms de colonne spécifiques pour les personnalisations du ruban à mettre en œuvre.</span><span class="sxs-lookup"><span data-stu-id="da043-115">The table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="da043-116">La table ci-dessous contient les paramètres à utiliser lors de la création de la table **RubansSysU**.</span><span class="sxs-lookup"><span data-stu-id="da043-116">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="da043-117">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="da043-117">Column name</span></span></p></th>
<th><p><span data-ttu-id="da043-118">Type de données</span><span class="sxs-lookup"><span data-stu-id="da043-118">Data type</span></span></p></th>
<th><p><span data-ttu-id="da043-119">Description</span><span class="sxs-lookup"><span data-stu-id="da043-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da043-120"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="da043-120"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="da043-121">Texte</span><span class="sxs-lookup"><span data-stu-id="da043-121">Text</span></span></p></td>
<td><p><span data-ttu-id="da043-122">Contient le nom du ruban personnalisé devant être associé à cette personnalisation.</span><span class="sxs-lookup"><span data-stu-id="da043-122">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da043-123"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="da043-123"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="da043-124">Mémo</span><span class="sxs-lookup"><span data-stu-id="da043-124">Memo</span></span></p></td>
<td><p><span data-ttu-id="da043-125">Contient l’extensibilité du ruban (RibbonX) XML qui définit la personnalisation du ruban.</span><span class="sxs-lookup"><span data-stu-id="da043-125">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="load-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="da043-126">Charger le code XML d’extensibilité du ruban par programme</span><span class="sxs-lookup"><span data-stu-id="da043-126">Load ribbon extensibility XML programmatically</span></span>

<span data-ttu-id="da043-127">Vous pouvez utiliser la méthode **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** pour charger les personnalisations du ruban par programme.</span><span class="sxs-lookup"><span data-stu-id="da043-127">You can use the **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** method to load ribbon customizations programmatically.</span></span> <span data-ttu-id="da043-128">En règle générale, pour créer le ruban et disponibles pour l’application, vous créez tout d’abord un module dans la base de données avec une procédure qui appelle la méthode **LoadCustomUI** , en passant le nom du ruban et le balisage de personnalisation XML.</span><span class="sxs-lookup"><span data-stu-id="da043-128">Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="da043-129">Le balisage XML peut provenir d’un objet **Recordset** créé à partir d’une table, d’une source externe à la base de données, tel qu’un fichier XML que vous analysez dans une chaîne ou d’un balisage XML incorporé directement dans la procédure.</span><span class="sxs-lookup"><span data-stu-id="da043-129">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure.</span></span> <span data-ttu-id="da043-130">Vous pouvez créer différents rubans en utilisant plusieurs appels de la méthode **LoadCustomUI** , en passant un balisage XML différent dans la mesure où le nom de chaque ruban et l’attribut **id** des onglets constituant le ruban sont uniques.</span><span class="sxs-lookup"><span data-stu-id="da043-130">You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="da043-131">Une fois la procédure terminée, vous créez ensuite une macro AutoExec qui appelle la procédure à l'aide de l'action ExécuterCode.</span><span class="sxs-lookup"><span data-stu-id="da043-131">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action.</span></span> <span data-ttu-id="da043-132">Ainsi, lorsque l’application est démarrée, la méthode **LoadCustomUI** s’exécute automatiquement et tous les rubans personnalisés sont accessibles à l’application.</span><span class="sxs-lookup"><span data-stu-id="da043-132">That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

## <a name="assign-custom-ribbons-to-forms-or-reports"></a><span data-ttu-id="da043-133">Affecter des rubans personnalisés à des formulaires ou des États</span><span class="sxs-lookup"><span data-stu-id="da043-133">Assign custom ribbons to forms or reports</span></span>

1.  <span data-ttu-id="da043-134">Suivez le processus décrit précédemment pour rendre le ruban personnalisé disponible pour cette application.</span><span class="sxs-lookup"><span data-stu-id="da043-134">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="da043-135">Ouvrez le formulaire ou l'état en mode Création.</span><span class="sxs-lookup"><span data-stu-id="da043-135">Open the form or report in Design view.</span></span>

3.  <span data-ttu-id="da043-136">Sous l’onglet Création, cliquez sur **Feuille de propriétés**.</span><span class="sxs-lookup"><span data-stu-id="da043-136">On the Design tab, choose **Property Sheet**.</span></span>

4.  <span data-ttu-id="da043-137">Sous l’onglet **tous** de la fenêtre Propriétés, sélectionnez la liste **Nom du ruban** , puis sélectionnez un ruban.</span><span class="sxs-lookup"><span data-stu-id="da043-137">On the **All** tab of the Property window, choose the **Ribbon Name** list and then select a ribbon.</span></span>

5.  <span data-ttu-id="da043-138">Enregistrer, fermez et rouvrez le formulaire ou état.</span><span class="sxs-lookup"><span data-stu-id="da043-138">Save, close, and then reopen the form or report.</span></span> <span data-ttu-id="da043-139">Le ruban de l’interface utilisateur que vous avez sélectionné est affiché.</span><span class="sxs-lookup"><span data-stu-id="da043-139">The ribbon UI you selected is displayed.</span></span>


> [!NOTE]
> <span data-ttu-id="da043-140">Les onglets affichés dans l’interface utilisateur du ruban sont additive.</span><span class="sxs-lookup"><span data-stu-id="da043-140">The tabs displayed in the ribbon UI are additive.</span></span> <span data-ttu-id="da043-141">Autrement dit, sauf si vous spécifiquement masquez les onglets ou définissez l’attribut *Démarrer à partir de zéro* à **la valeur True**, les onglets affichés dans un formulaire ou interface utilisateur de ruban de l’état s’ajoutent aux onglets existants.</span><span class="sxs-lookup"><span data-stu-id="da043-141">That is, unless you specifically hide the tabs or set the *Start from Scratch* attribute to **True**, the tabs displayed in a form's or report's ribbon user interface are in addition to the existing tabs.</span></span>

> [!NOTE]
> <span data-ttu-id="da043-142">[!REMARQUE] Pour plus d'informations sur l'interface du ruban dans d'autres applications Office, consultez l'article [Vue d'ensemble du ruban Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="da043-142">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


