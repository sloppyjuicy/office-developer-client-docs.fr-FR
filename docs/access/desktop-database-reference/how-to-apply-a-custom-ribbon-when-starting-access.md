---
title: Appliquer un ruban personnalisé au démarrage d’Access
TOCTitle: Apply a custom ribbon when starting Access
ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15)
ms:contentKeyID: 48546659
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 575834f818386a7ba536e826fff2b7da00b324d5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472597"
---
# <a name="apply-a-custom-ribbon-when-starting-access"></a><span data-ttu-id="7eaa8-102">Appliquer un ruban personnalisé au démarrage d’Access</span><span class="sxs-lookup"><span data-stu-id="7eaa8-102">Apply a custom ribbon when starting Access</span></span>

<span data-ttu-id="7eaa8-103">**S’applique à :** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7eaa8-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="7eaa8-104">Le ruban utilise le balisage XML déclaratif textuels qui simplifie la création et la personnalisation du ruban.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-104">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="7eaa8-105">Avec quelques lignes de code XML, vous pouvez créer l’interface de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-105">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="7eaa8-106">Access fournit une flexibilité considérable pour personnaliser l’interface utilisateur du ruban.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-106">Access provides tremendous flexibility in customizing the ribbon UI.</span></span> <span data-ttu-id="7eaa8-107">Par exemple, marquage de personnalisation permettre être stockée dans une table, incorporé dans une procédure VBA, stocké dans une autre base de données Access ou liée à une feuille de calcul Excel.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-107">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="7eaa8-108">Cette rubrique décrit comment appliquer des rubans personnalisés lors de l’ouverture d’une base de données.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-108">This topic describes how to apply customized ribbons when opening a database.</span></span>

## <a name="making-the-ribbon-customization-xml-available"></a><span data-ttu-id="7eaa8-109">Disposition de la personnalisation du ruban XML</span><span class="sxs-lookup"><span data-stu-id="7eaa8-109">Making the Ribbon Customization XML Available</span></span>

### <a name="storing-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="7eaa8-110">Stockage d’extensibilité du ruban XML dans une Table</span><span class="sxs-lookup"><span data-stu-id="7eaa8-110">Storing Ribbon Extensibility XML in a Table</span></span>

<span data-ttu-id="7eaa8-111">Une des méthodes que vous pouvez utiliser pour rendre disponibles des personnalisations de ruban consiste à stocker dans une table.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-111">One method that you can use to make ribbon customizations available is to store them in a table.</span></span> <span data-ttu-id="7eaa8-112">Si vous stockez les personnalisations dans une table dénommée **RubansSysU**, les personnalisations peuvent être implémentées sans utiliser de macros ou du code VBA.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-112">If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="7eaa8-113">**RubansSysU** est une table système créée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-113">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="7eaa8-114">Le tableau doit être créé en utilisant des noms de colonne spécifique afin que les personnalisations du ruban à mettre en œuvre.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-114">The table must be created using specific column names in order for the ribbon customizations to be implemented.</span></span> <span data-ttu-id="7eaa8-115">La table ci-dessous contient les paramètres à utiliser lors de la création de la table **RubansSysU**.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-115">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7eaa8-116">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="7eaa8-116">Column Name</span></span></p></th>
<th><p><span data-ttu-id="7eaa8-117">Type de données</span><span class="sxs-lookup"><span data-stu-id="7eaa8-117">Data Type</span></span></p></th>
<th><p><span data-ttu-id="7eaa8-118">Description</span><span class="sxs-lookup"><span data-stu-id="7eaa8-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7eaa8-119"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="7eaa8-119"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="7eaa8-120">Texte</span><span class="sxs-lookup"><span data-stu-id="7eaa8-120">Text</span></span></p></td>
<td><p><span data-ttu-id="7eaa8-121">Contient le nom du ruban personnalisé devant être associé à cette personnalisation.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-121">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eaa8-122"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="7eaa8-122"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="7eaa8-123">Mémo</span><span class="sxs-lookup"><span data-stu-id="7eaa8-123">Memo</span></span></p></td>
<td><p><span data-ttu-id="7eaa8-124">Contient le XML d'extensibilité du ruban (RibbonX) qui définit la personnalisation du ruban.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-124">Contains the Ribbon Extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="loading-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="7eaa8-125">Chargement extensibilité du ruban XML par programmation</span><span class="sxs-lookup"><span data-stu-id="7eaa8-125">Loading Ribbon Extensibility XML Programmatically</span></span>

<span data-ttu-id="7eaa8-126">Vous pouvez utiliser la méthode **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** pour charger les personnalisations du ruban par programme.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-126">You can use the **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** method to load ribbon customizations programmatically.</span></span> <span data-ttu-id="7eaa8-127">En règle générale, pour créer le ruban et disponibles pour l’application, vous créez tout d’abord un module dans la base de données avec une procédure qui appelle la méthode **LoadCustomUI** , en passant le nom du ruban et le balisage de personnalisation XML.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-127">Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="7eaa8-128">Le balisage XML peut provenir d’un objet **Recordset** créé à partir d’une table, d’une source externe à la base de données, tel qu’un fichier XML que vous analysez dans une chaîne ou d’un balisage XML incorporé directement dans la procédure.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-128">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure.</span></span> <span data-ttu-id="7eaa8-129">Vous pouvez créer différents rubans en utilisant plusieurs appels de la méthode **LoadCustomUI** , en passant un balisage XML différent dans la mesure où le nom de chaque ruban et l’attribut **id** des onglets constituant le ruban sont uniques.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-129">You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="7eaa8-130">Une fois la procédure terminée, vous créez ensuite une macro AutoExec qui appelle la procédure à l'aide de l'action ExécuterCode.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-130">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action.</span></span> <span data-ttu-id="7eaa8-131">Ainsi, lorsque l’application est démarrée, la méthode **LoadCustomUI** s’exécute automatiquement et tous les rubans personnalisés sont accessibles à l’application.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-131">That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

## <a name="applying-customized-ribbons-when-access-starts"></a><span data-ttu-id="7eaa8-132">Appliquer des rubans personnalisés au démarrage d’Access</span><span class="sxs-lookup"><span data-stu-id="7eaa8-132">Applying Customized Ribbons When Access Starts</span></span>

<span data-ttu-id="7eaa8-133">Pour appliquer une interface utilisateur personnalisée de sorte qu’il soit disponible au démarrage de l’application, utilisez la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="7eaa8-133">To apply a custom UI so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="7eaa8-134">Suivez la procédure décrite précédemment pour rendre les rubans personnalisés accessibles à l’application.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-134">Follow the process described previously to make the customized ribbons available to the application.</span></span>

2.  <span data-ttu-id="7eaa8-135">Fermez er redémarrez l'application.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-135">Close and then restart the application.</span></span>

3.  <span data-ttu-id="7eaa8-136">Cliquez sur le **Bouton Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") , puis sur **Options Access**.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-136">Click the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then click **Access Options**.</span></span>

4.  <span data-ttu-id="7eaa8-137">Cliquez sur l’option de **Base de données actuelle** puis, dans la section **Options de la barre d’outils et du ruban** , cliquez sur la liste **Nom du ruban** et sélectionnez un ruban.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-137">Click the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, click the **Ribbon Name** list and select a ribbon.</span></span>

5.  <span data-ttu-id="7eaa8-138">Maintenant, fermez et redémarrez l’application.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-138">Now close and restart the application.</span></span> <span data-ttu-id="7eaa8-139">L’interface utilisateur que vous avez sélectionné est affiché.</span><span class="sxs-lookup"><span data-stu-id="7eaa8-139">The UI you selected is displayed.</span></span>

> [!NOTE]
> <span data-ttu-id="7eaa8-140">[!REMARQUE] Pour plus d'informations sur l'interface du ruban dans d'autres applications Office, consultez l'article [Vue d'ensemble du ruban Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="7eaa8-140">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


