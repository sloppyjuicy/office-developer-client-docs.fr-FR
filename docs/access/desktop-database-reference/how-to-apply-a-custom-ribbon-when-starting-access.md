---
title: Appliquer un ruban personnalisé au démarrage d’Access
TOCTitle: Apply a custom ribbon when starting Access
description: Découvrez comment appliquer des rubans personnalisés lorsque vous ouvrez une base de données dans Access 2013.
ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15)
ms:contentKeyID: 48546659
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 0acd99a498a74f098b08814e9f11d49b28bae097
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291956"
---
# <a name="apply-a-custom-ribbon-when-starting-access"></a><span data-ttu-id="a963f-103">Appliquer un ruban personnalisé au démarrage d’Access</span><span class="sxs-lookup"><span data-stu-id="a963f-103">Apply a custom ribbon when starting Access</span></span>

<span data-ttu-id="a963f-104">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a963f-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a963f-105">Le ruban utilise un balisage XML déclaratif basé sur texte, qui simplifie la création et la personnalisation du ruban.</span><span class="sxs-lookup"><span data-stu-id="a963f-105">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="a963f-106">Avec quelques lignes de XML, vous pouvez créer simplement l’interface idéale pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a963f-106">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="a963f-107">Access fournit une grande flexibilité lors de la personnalisation du ruban de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a963f-107">Access provides tremendous flexibility in customizing the ribbon UI.</span></span> <span data-ttu-id="a963f-108">Par exemple, un balisage de personnalisation peut être stocké dans un tableau, incorporé dans une procédure VBA, stocké dans une autre base de données Access ou lié à une feuille de calcul Excel.</span><span class="sxs-lookup"><span data-stu-id="a963f-108">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="a963f-109">Découvrez comment appliquer des rubans personnalisés lorsque vous ouvrez une base de données.</span><span class="sxs-lookup"><span data-stu-id="a963f-109">This topic describes how to apply customized ribbons when opening a database.</span></span>

## <a name="make-the-ribbon-customization-xml-available"></a><span data-ttu-id="a963f-110">Rendre disponible la personnalisation du ruban XML</span><span class="sxs-lookup"><span data-stu-id="a963f-110">Make the ribbon customization XML available</span></span>

### <a name="store-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="a963f-111">Stocker extensibilité du ruban XML dans un tableau</span><span class="sxs-lookup"><span data-stu-id="a963f-111">Store ribbon extensibility XML in a table</span></span>

<span data-ttu-id="a963f-112">Une méthode que vous pouvez utiliser pour rendre des personnalisations du ruban disponible consiste à les stocker dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="a963f-112">One method that you can use to make ribbon customizations available is to store them in a table.</span></span> <span data-ttu-id="a963f-113">Si vous stockez les personnalisations dans un tableau nommé **USysRibbons**, les personnalisations peuvent être mises en œuvre sans utiliser des macros ou du code VBA.</span><span class="sxs-lookup"><span data-stu-id="a963f-113">If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="a963f-114">**USysRibbons** est un tableau système créé par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a963f-114">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="a963f-115">Ce tableau doit être créé en utilisant des noms de colonnes spécifiques afin que les personnalisations du ruban soient implémentées.</span><span class="sxs-lookup"><span data-stu-id="a963f-115">The USysRibbons table must be created using specific column names in order for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="a963f-116">Le tableau suivant répertorie les paramètres à utiliser lors de la création du tableau**USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="a963f-116">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a963f-117">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="a963f-117">Column name</span></span></p></th>
<th><p><span data-ttu-id="a963f-118">Type de données</span><span class="sxs-lookup"><span data-stu-id="a963f-118">Data type</span></span></p></th>
<th><p><span data-ttu-id="a963f-119">Description</span><span class="sxs-lookup"><span data-stu-id="a963f-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a963f-120"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="a963f-120"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="a963f-121">Text</span><span class="sxs-lookup"><span data-stu-id="a963f-121">Text</span></span></p></td>
<td><p><span data-ttu-id="a963f-122">Contient le nom du ruban personnalisé devant être associé à cette personnalisation.</span><span class="sxs-lookup"><span data-stu-id="a963f-122">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a963f-123"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="a963f-123"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="a963f-124">Mémo</span><span class="sxs-lookup"><span data-stu-id="a963f-124">Memo</span></span></p></td>
<td><p><span data-ttu-id="a963f-125">Contient le XML d'extensibilité du ruban (RibbonX) qui définit la personnalisation du ruban.</span><span class="sxs-lookup"><span data-stu-id="a963f-125">Contains the Ribbon Extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="load-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="a963f-126">Charger extensibilité du ruban XML par programme</span><span class="sxs-lookup"><span data-stu-id="a963f-126">Load ribbon extensibility XML programmatically</span></span>

<span data-ttu-id="a963f-127">Vous pouvez utiliser la méthode\*\* [LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI) \*\* permettant de charger les personnalisations de ruban par programme.</span><span class="sxs-lookup"><span data-stu-id="a963f-127">You can use the **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** method to load ribbon customizations programmatically.</span></span> <span data-ttu-id="a963f-128">En règle générale, pour créer le ruban et le mettre à la disposition de l’application, vous devez tout d’abord créer un module dans la base de données avec une procédure qui appelle la méthode **LoadCustomUI**, laquelle transmet le nom du Ruban et le code de personnalisation XML.</span><span class="sxs-lookup"><span data-stu-id="a963f-128">Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the\*\* LoadCustomUI\*\* method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="a963f-129">Le code XML peut provenir d’un objet **Recordset** créé à partir d’une table, d’une source externe à la base de données (comme un fichier XML que vous analysez dans un objet de type String) ou de code XML incorporé directement dans la procédure.</span><span class="sxs-lookup"><span data-stu-id="a963f-129">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure.</span></span> <span data-ttu-id="a963f-130">Vous pouvez rendre plusieurs rubans disponibles à l'aide de plusieurs appels à la méthode **LoadCustomUI**, autre balisage XML, dans la mesure où le nom de chaque ruban et l'attribut **id** des onglets constituant le ruban sont uniques.</span><span class="sxs-lookup"><span data-stu-id="a963f-130">You can make different ribbons available by using multiple calls to the **LoadCustomUI** method, passing in different XML markup, as long as the name of each ribbon and the id attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="a963f-131">Une fois la procédure terminée, vous créez une macro AutoExec qui appelle la procédure à l’aide de l’action ExécuterCode.</span><span class="sxs-lookup"><span data-stu-id="a963f-131">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action.</span></span> <span data-ttu-id="a963f-132">Ainsi, lorsque l'application est lancée, la méthode **LoadCustomUI** s'exécute automatiquement et tous les rubans personnalisés sont accessibles à l'application.</span><span class="sxs-lookup"><span data-stu-id="a963f-132">That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application</span></span>

## <a name="apply-customized-ribbons-when-access-starts"></a><span data-ttu-id="a963f-133">Appliquer des rubans personnalisés lorsque Access démarre</span><span class="sxs-lookup"><span data-stu-id="a963f-133">Apply customized ribbons when Access starts</span></span>

<span data-ttu-id="a963f-134">Pour appliquer un ruban personnalisé disponible au démarrage de l'application, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="a963f-134">To apply a custom ribbon so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="a963f-135">Exécutez la procédure décrite plus haut pour rendre les rubans personnalisés accessibles à l’application.</span><span class="sxs-lookup"><span data-stu-id="a963f-135">Follow the process described earlier to make the customized ribbons available to the application.</span></span>

2.  <span data-ttu-id="a963f-136">Quittez et redémarrez l’application.</span><span class="sxs-lookup"><span data-stu-id="a963f-136">Close and then restart the application.</span></span>

3.  <span data-ttu-id="a963f-137">Sélectionnez le **bouton Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") , puis **Access Options**.</span><span class="sxs-lookup"><span data-stu-id="a963f-137">Choose the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then choose **Access Options**.</span></span>

4.  <span data-ttu-id="a963f-138">Cliquez sur l'option **Base de données active**, dans la section **Options de la barre d'outils et du ruban**, puis sur la liste **Nom du ruban** et sélectionnez un ruban.</span><span class="sxs-lookup"><span data-stu-id="a963f-138">Click **Current Database** and then, in the **Ribbon and Toolbar Options** section, click the **Ribbon Name** list and select a ribbon.</span></span>

5.  <span data-ttu-id="a963f-139">Quittez et redémarrez l’application.</span><span class="sxs-lookup"><span data-stu-id="a963f-139">Now close and restart the application.</span></span> <span data-ttu-id="a963f-140">L’interface utilisateur que vous avez sélectionnée est affichée.</span><span class="sxs-lookup"><span data-stu-id="a963f-140">The UI you selected is displayed.</span></span>

> [!NOTE]
> <span data-ttu-id="a963f-141">Pour plus d'informations sur l'interface du ruban dans d'autres applications Office, consultez l'article [Vue d'ensemble du ruban Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="a963f-141">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


