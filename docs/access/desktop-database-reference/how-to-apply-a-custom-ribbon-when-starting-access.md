---
title: Appliquer un ruban personnalisé au démarrage d’Access
TOCTitle: Apply a custom ribbon when starting Access
description: Comment appliquer des rubans personnalisés lors de l’ouverture d’une base de données dans Access 2013.
ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15)
ms:contentKeyID: 48546659
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 0acd99a498a74f098b08814e9f11d49b28bae097
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709620"
---
# <a name="apply-a-custom-ribbon-when-starting-access"></a><span data-ttu-id="f5634-103">Appliquer un ruban personnalisé au démarrage d’Access</span><span class="sxs-lookup"><span data-stu-id="f5634-103">Apply a custom ribbon when starting Access</span></span>

<span data-ttu-id="f5634-104">**S’applique à :** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f5634-104">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="f5634-105">Le ruban utilise le balisage XML déclaratif textuels qui simplifie la création et la personnalisation du ruban.</span><span class="sxs-lookup"><span data-stu-id="f5634-105">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="f5634-106">Avec quelques lignes de code XML, vous pouvez créer l’interface de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f5634-106">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="f5634-107">Access fournit une flexibilité considérable pour personnaliser l’interface utilisateur du ruban.</span><span class="sxs-lookup"><span data-stu-id="f5634-107">Access provides tremendous flexibility in customizing the ribbon UI.</span></span> <span data-ttu-id="f5634-108">Par exemple, marquage de personnalisation permettre être stockée dans une table, incorporé dans une procédure VBA, stocké dans une autre base de données Access ou liée à une feuille de calcul Excel.</span><span class="sxs-lookup"><span data-stu-id="f5634-108">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="f5634-109">Cette rubrique décrit comment appliquer des rubans personnalisés lors de l’ouverture d’une base de données.</span><span class="sxs-lookup"><span data-stu-id="f5634-109">This topic describes how to apply customized ribbons when opening a database.</span></span>

## <a name="make-the-ribbon-customization-xml-available"></a><span data-ttu-id="f5634-110">Disposition de la personnalisation du ruban XML</span><span class="sxs-lookup"><span data-stu-id="f5634-110">Make the ribbon customization XML available</span></span>

### <a name="store-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="f5634-111">Stocker l’extensibilité du ruban XML dans une table</span><span class="sxs-lookup"><span data-stu-id="f5634-111">Store ribbon extensibility XML in a table</span></span>

<span data-ttu-id="f5634-112">Une des méthodes que vous pouvez utiliser pour rendre disponibles des personnalisations de ruban consiste à stocker dans une table.</span><span class="sxs-lookup"><span data-stu-id="f5634-112">One method that you can use to make ribbon customizations available is to store them in a table.</span></span> <span data-ttu-id="f5634-113">Si vous stockez les personnalisations dans une table dénommée **RubansSysU**, les personnalisations peuvent être implémentées sans utiliser de macros ou du code VBA.</span><span class="sxs-lookup"><span data-stu-id="f5634-113">If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="f5634-114">**RubansSysU** est une table système créée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f5634-114">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="f5634-115">Le tableau doit être créé en utilisant des noms de colonne spécifiques pour les personnalisations du ruban à mettre en œuvre.</span><span class="sxs-lookup"><span data-stu-id="f5634-115">The table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="f5634-116">La table ci-dessous contient les paramètres à utiliser lors de la création de la table **RubansSysU**.</span><span class="sxs-lookup"><span data-stu-id="f5634-116">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f5634-117">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="f5634-117">Column name</span></span></p></th>
<th><p><span data-ttu-id="f5634-118">Type de données</span><span class="sxs-lookup"><span data-stu-id="f5634-118">Data type</span></span></p></th>
<th><p><span data-ttu-id="f5634-119">Description</span><span class="sxs-lookup"><span data-stu-id="f5634-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f5634-120"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="f5634-120"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="f5634-121">Texte</span><span class="sxs-lookup"><span data-stu-id="f5634-121">Text</span></span></p></td>
<td><p><span data-ttu-id="f5634-122">Contient le nom du ruban personnalisé devant être associé à cette personnalisation.</span><span class="sxs-lookup"><span data-stu-id="f5634-122">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5634-123"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="f5634-123"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="f5634-124">Mémo</span><span class="sxs-lookup"><span data-stu-id="f5634-124">Memo</span></span></p></td>
<td><p><span data-ttu-id="f5634-125">Contient l’extensibilité du ruban (RibbonX) XML qui définit la personnalisation du ruban.</span><span class="sxs-lookup"><span data-stu-id="f5634-125">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="load-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="f5634-126">Charger le code XML d’extensibilité du ruban par programme</span><span class="sxs-lookup"><span data-stu-id="f5634-126">Load ribbon extensibility XML programmatically</span></span>

<span data-ttu-id="f5634-127">Vous pouvez utiliser la méthode **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** pour charger les personnalisations du ruban par programme.</span><span class="sxs-lookup"><span data-stu-id="f5634-127">You can use the **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** method to load ribbon customizations programmatically.</span></span> <span data-ttu-id="f5634-128">En règle générale, pour créer le ruban et disponibles pour l’application, vous créez tout d’abord un module dans la base de données avec une procédure qui appelle la méthode **LoadCustomUI** , en passant le nom du ruban et le balisage de personnalisation XML.</span><span class="sxs-lookup"><span data-stu-id="f5634-128">Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="f5634-129">Le balisage XML peut provenir d’un objet **Recordset** créé à partir d’une table, d’une source externe à la base de données, tel qu’un fichier XML que vous analysez dans une chaîne ou d’un balisage XML incorporé directement dans la procédure.</span><span class="sxs-lookup"><span data-stu-id="f5634-129">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure.</span></span> <span data-ttu-id="f5634-130">Vous pouvez créer différents rubans en utilisant plusieurs appels de la méthode **LoadCustomUI** , en passant un balisage XML différent dans la mesure où le nom de chaque ruban et l’attribut **id** des onglets constituant le ruban sont uniques.</span><span class="sxs-lookup"><span data-stu-id="f5634-130">You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="f5634-131">Une fois la procédure terminée, vous créez ensuite une macro AutoExec qui appelle la procédure à l'aide de l'action ExécuterCode.</span><span class="sxs-lookup"><span data-stu-id="f5634-131">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action.</span></span> <span data-ttu-id="f5634-132">Ainsi, lorsque l’application est démarrée, la méthode **LoadCustomUI** s’exécute automatiquement et tous les rubans personnalisés sont accessibles à l’application.</span><span class="sxs-lookup"><span data-stu-id="f5634-132">That way, when the application is started, the **LoadCustomUI** method is automatically executed, and all of the custom ribbons are made available to the application.</span></span>

## <a name="apply-customized-ribbons-when-access-starts"></a><span data-ttu-id="f5634-133">Appliquer des rubans personnalisés au démarrage d’Access</span><span class="sxs-lookup"><span data-stu-id="f5634-133">Apply customized ribbons when Access starts</span></span>

<span data-ttu-id="f5634-134">Pour appliquer une interface utilisateur personnalisée de sorte qu’il soit disponible au démarrage de l’application, utilisez la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="f5634-134">To apply a custom UI so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="f5634-135">Suivez la procédure décrite précédemment pour rendre les rubans personnalisés accessibles à l’application.</span><span class="sxs-lookup"><span data-stu-id="f5634-135">Follow the process described previously to make the customized ribbons available to the application.</span></span>

2.  <span data-ttu-id="f5634-136">Fermez er redémarrez l'application.</span><span class="sxs-lookup"><span data-stu-id="f5634-136">Close and then restart the application.</span></span>

3.  <span data-ttu-id="f5634-137">Cliquez sur le **Bouton Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") , puis sur **Options Access**.</span><span class="sxs-lookup"><span data-stu-id="f5634-137">Choose the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then choose **Access Options**.</span></span>

4.  <span data-ttu-id="f5634-138">Choisissez l’option de **Base de données actuelle** puis, dans la section **Options de la barre d’outils et du ruban** , cliquez sur la liste **Nom du ruban** et sélectionnez un ruban.</span><span class="sxs-lookup"><span data-stu-id="f5634-138">Choose the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, choose the **Ribbon Name** list and select a ribbon.</span></span>

5.  <span data-ttu-id="f5634-139">Maintenant, fermez et redémarrez l’application.</span><span class="sxs-lookup"><span data-stu-id="f5634-139">Now close and restart the application.</span></span> <span data-ttu-id="f5634-140">L’interface utilisateur que vous avez sélectionné est affiché.</span><span class="sxs-lookup"><span data-stu-id="f5634-140">The UI you selected is displayed.</span></span>

> [!NOTE]
> <span data-ttu-id="f5634-141">[!REMARQUE] Pour plus d'informations sur l'interface du ruban dans d'autres applications Office, consultez l'article [Vue d'ensemble du ruban Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="f5634-141">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


