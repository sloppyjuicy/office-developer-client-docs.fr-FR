---
<span data-ttu-id="4ab46-101">titre : appliquer un ruban personnalisé à un formulaire ou un état TOCTitle : appliquer un ruban personnalisé à un formulaire ou un état <<<<<<< ms:assetid tête : 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 ms:mtpsurl : https://msdn.microsoft.com/library/Ff196428(v=office.15) ms:contentKeyID : ms.date 48545865 : 18/09/2015 === === description : comment appliquer des rubans personnalisés lors du chargement d’un formulaire ou un état dans Access 2013.</span><span class="sxs-lookup"><span data-stu-id="4ab46-101">title: Apply a custom ribbon to a form or report TOCTitle: Apply a custom ribbon to a form or report <<<<<<< HEAD ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15) ms:contentKeyID: 48545865 ms.date: 09/18/2015 ======= description: How to apply customized ribbons when loading a form or report in Access 2013.</span></span>
<span data-ttu-id="4ab46-102">MS:AssetId : 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 ms:mtpsurl : https://msdn.microsoft.com/library/Ff196428(v=office.15) ms:contentKeyID : ms.date 48545865 : 10/16/2018</span><span class="sxs-lookup"><span data-stu-id="4ab46-102">ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15) ms:contentKeyID: 48545865 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="4ab46-103">maître mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="4ab46-103">master mtps_version: v=office.15</span></span>
---

# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a><span data-ttu-id="4ab46-104">Appliquer un ruban personnalisé à un formulaire ou un état</span><span class="sxs-lookup"><span data-stu-id="4ab46-104">Apply a custom ribbon to a form or report</span></span>

<span data-ttu-id="4ab46-105"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="4ab46-105"><<<<<<< HEAD</span></span>

<span data-ttu-id="4ab46-106">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ab46-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4ab46-107">Le ruban utilise le balisage XML déclaratif textuels qui simplifie la création et la personnalisation du ruban.</span><span class="sxs-lookup"><span data-stu-id="4ab46-107">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="4ab46-108">Avec quelques lignes de code XML, vous pouvez créer l’interface de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4ab46-108">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="4ab46-109">Access fournit la flexibilité de la personnalisation de l’interface utilisateur du ruban.</span><span class="sxs-lookup"><span data-stu-id="4ab46-109">Access provides flexibility in customizing the ribbon user interface.</span></span> <span data-ttu-id="4ab46-110">Par exemple, marquage de personnalisation permettre être stockée dans une table, incorporé dans une procédure VBA, stocké dans une autre base de données Access ou liée à une feuille de calcul Excel.</span><span class="sxs-lookup"><span data-stu-id="4ab46-110">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="4ab46-111">Cette rubrique décrit comment appliquer des rubans personnalisés lors du chargement d’un formulaire ou un état.</span><span class="sxs-lookup"><span data-stu-id="4ab46-111">This topic describes how to apply customized ribbons when loading a form or report.</span></span>

## <a name="making-the-ribbon-customization-xml-available"></a><span data-ttu-id="4ab46-112">Disposition de la personnalisation du ruban XML</span><span class="sxs-lookup"><span data-stu-id="4ab46-112">Making the Ribbon Customization XML Available</span></span>

<span data-ttu-id="4ab46-113">**Stockage d’extensibilité du ruban XML dans une Table**</span><span class="sxs-lookup"><span data-stu-id="4ab46-113">**Storing Ribbon Extensibility XML in a Table**</span></span>

<span data-ttu-id="4ab46-114">Une des méthodes que vous pouvez utiliser pour rendre disponibles des personnalisations de ruban consiste à stocker dans une table.</span><span class="sxs-lookup"><span data-stu-id="4ab46-114">One method that you can use to make ribbon customizations available is to store them in a table.</span></span> <span data-ttu-id="4ab46-115">Si vous stockez les personnalisations dans une table dénommée **RubansSysU**, les personnalisations peuvent être implémentées sans utiliser de macros ou du code VBA.</span><span class="sxs-lookup"><span data-stu-id="4ab46-115">If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<a name="usysribbons-is-a-user-created-system-table-the-table-must-be-created-using-specific-column-names-in-order-for-the-ribbon-customizations-to-be-implemented-the-following-table-lists-the-settings-to-use-when-creating-the-usysribbons-table"></a><span data-ttu-id="4ab46-116">**RubansSysU** est une table système créée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4ab46-116">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="4ab46-117">Le tableau doit être créé en utilisant des noms de colonne spécifique afin que les personnalisations du ruban à mettre en œuvre.</span><span class="sxs-lookup"><span data-stu-id="4ab46-117">The table must be created using specific column names in order for the ribbon customizations to be implemented.</span></span> <span data-ttu-id="4ab46-118">La table ci-dessous contient les paramètres à utiliser lors de la création de la table **RubansSysU**.</span><span class="sxs-lookup"><span data-stu-id="4ab46-118">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
=======
<span data-ttu-id="4ab46-119">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ab46-119">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4ab46-120">Le ruban utilise le balisage XML déclaratif textuels qui simplifie la création et la personnalisation du ruban.</span><span class="sxs-lookup"><span data-stu-id="4ab46-120">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="4ab46-121">Avec quelques lignes de code XML, vous pouvez créer l’interface de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4ab46-121">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="4ab46-122">Access fournit la flexibilité de la personnalisation de l’interface utilisateur du ruban.</span><span class="sxs-lookup"><span data-stu-id="4ab46-122">Access provides flexibility in customizing the ribbon user interface.</span></span> 

<span data-ttu-id="4ab46-123">Par exemple, marquage de personnalisation permettre être stockée dans une table, incorporé dans une procédure VBA, stocké dans une autre base de données Access ou liée à une feuille de calcul Excel.</span><span class="sxs-lookup"><span data-stu-id="4ab46-123">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="4ab46-124">Cette rubrique décrit comment appliquer des rubans personnalisés lors du chargement d’un formulaire ou un état.</span><span class="sxs-lookup"><span data-stu-id="4ab46-124">This topic describes how to apply customized ribbons when loading a form or report.</span></span>

## <a name="make-the-ribbon-customization-xml-available"></a><span data-ttu-id="4ab46-125">Disposition de la personnalisation du ruban XML</span><span class="sxs-lookup"><span data-stu-id="4ab46-125">Make the ribbon customization XML available</span></span>

### <a name="store-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="4ab46-126">Stocker l’extensibilité du ruban XML dans une table</span><span class="sxs-lookup"><span data-stu-id="4ab46-126">Store ribbon extensibility XML in a table</span></span>

<span data-ttu-id="4ab46-127">Une des méthodes que vous pouvez utiliser pour rendre disponibles des personnalisations de ruban consiste à stocker dans une table.</span><span class="sxs-lookup"><span data-stu-id="4ab46-127">One method that you can use to make ribbon customizations available is to store them in a table.</span></span> <span data-ttu-id="4ab46-128">Si vous stockez les personnalisations dans une table dénommée **RubansSysU**, les personnalisations peuvent être implémentées sans utiliser de macros ou du code VBA.</span><span class="sxs-lookup"><span data-stu-id="4ab46-128">If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="4ab46-129">**RubansSysU** est une table système créée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4ab46-129">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="4ab46-130">Le tableau doit être créé en utilisant des noms de colonne spécifiques pour les personnalisations du ruban à mettre en œuvre.</span><span class="sxs-lookup"><span data-stu-id="4ab46-130">The table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="4ab46-131">La table ci-dessous contient les paramètres à utiliser lors de la création de la table **RubansSysU**.</span><span class="sxs-lookup"><span data-stu-id="4ab46-131">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
>>>>>>> <span data-ttu-id="4ab46-132">master</span><span class="sxs-lookup"><span data-stu-id="4ab46-132">master</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<span data-ttu-id="4ab46-133"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="4ab46-133"><<<<<<< HEAD</span></span>
<th><p><span data-ttu-id="4ab46-134">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="4ab46-134">Column Name</span></span></p></th>
<th><p><span data-ttu-id="4ab46-135">Type de données</span><span class="sxs-lookup"><span data-stu-id="4ab46-135">Data Type</span></span></p></th>
=======
<th><p><span data-ttu-id="4ab46-136">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="4ab46-136">Column name</span></span></p></th>
<th><p><span data-ttu-id="4ab46-137">Type de données</span><span class="sxs-lookup"><span data-stu-id="4ab46-137">Data type</span></span></p></th><span data-ttu-id="4ab46-138">
>>>>>>>forme de base</span><span class="sxs-lookup"><span data-stu-id="4ab46-138">
>>>>>>> master</span></span>
<th><p><span data-ttu-id="4ab46-139">Description</span><span class="sxs-lookup"><span data-stu-id="4ab46-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ab46-140"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="4ab46-140"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="4ab46-141">Texte</span><span class="sxs-lookup"><span data-stu-id="4ab46-141">Text</span></span></p></td>
<span data-ttu-id="4ab46-142"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="4ab46-142"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="4ab46-143">Contient le nom du ruban personnalisé à associer à cette personnalisation</span><span class="sxs-lookup"><span data-stu-id="4ab46-143">Contains the name of the custom ribbon to be associated with this customization</span></span></p></td>
=======
<td><p><span data-ttu-id="4ab46-144">Contient le nom du ruban personnalisé devant être associé à cette personnalisation.</span><span class="sxs-lookup"><span data-stu-id="4ab46-144">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td><span data-ttu-id="4ab46-145">
>>>>>>>forme de base</span><span class="sxs-lookup"><span data-stu-id="4ab46-145">
>>>>>>> master</span></span>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ab46-146"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="4ab46-146"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="4ab46-147">Mémo</span><span class="sxs-lookup"><span data-stu-id="4ab46-147">Memo</span></span></p></td>
<span data-ttu-id="4ab46-148"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="4ab46-148"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="4ab46-149">Contient le XML d’extensibilité (RibbonX) qui définit la personnalisation du ruban du ruban</span><span class="sxs-lookup"><span data-stu-id="4ab46-149">Contains the ribbon Extensibility XML (RibbonX) that defines the ribbon customization</span></span></p></td>
=======
<td><p><span data-ttu-id="4ab46-150">Contient l’extensibilité du ruban (RibbonX) XML qui définit la personnalisation du ruban.</span><span class="sxs-lookup"><span data-stu-id="4ab46-150">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td><span data-ttu-id="4ab46-151">
>>>>>>>forme de base</span><span class="sxs-lookup"><span data-stu-id="4ab46-151">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>


<span data-ttu-id="4ab46-152"><<<<<<< Tête de **chargement de l’extensibilité du ruban XML par programmation**</span><span class="sxs-lookup"><span data-stu-id="4ab46-152"><<<<<<< HEAD **Loading Ribbon Extensibility XML Programmatically**</span></span>

<a name="you-can-use-the-loadcustomuihttpsmsdnmicrosoftcomlibraryff194416voffice15-method-to-load-ribbon-customizations-programmatically-typically-to-create-and-make-the-ribbon-available-to-the-application-you-first-create-a-module-in-the-database-with-a-procedure-that-calls-the-loadcustomui-method-passing-in-the-name-of-the-ribbon-and-the-xml-customization-markup"></a><span data-ttu-id="4ab46-153">Vous pouvez utiliser la méthode **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** pour charger les personnalisations du ruban par programme.</span><span class="sxs-lookup"><span data-stu-id="4ab46-153">You can use the **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** method to load ribbon customizations programmatically.</span></span> <span data-ttu-id="4ab46-154">En règle générale, pour créer le ruban et disponibles pour l’application, vous créez tout d’abord un module dans la base de données avec une procédure qui appelle la méthode **LoadCustomUI** , en passant le nom du ruban et le balisage de personnalisation XML.</span><span class="sxs-lookup"><span data-stu-id="4ab46-154">Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>
=======
### <a name="load-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="4ab46-155">Charger le code XML d’extensibilité du ruban par programme</span><span class="sxs-lookup"><span data-stu-id="4ab46-155">Load ribbon extensibility XML programmatically</span></span>

<span data-ttu-id="4ab46-156">Vous pouvez utiliser la méthode **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** pour charger les personnalisations du ruban par programme.</span><span class="sxs-lookup"><span data-stu-id="4ab46-156">You can use the **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** method to load ribbon customizations programmatically.</span></span> <span data-ttu-id="4ab46-157">En règle générale, pour créer le ruban et disponibles pour l’application, vous créez tout d’abord un module dans la base de données avec une procédure qui appelle la méthode **LoadCustomUI** , en passant le nom du ruban et le balisage de personnalisation XML.</span><span class="sxs-lookup"><span data-stu-id="4ab46-157">Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>
>>>>>>> <span data-ttu-id="4ab46-158">master</span><span class="sxs-lookup"><span data-stu-id="4ab46-158">master</span></span>

<span data-ttu-id="4ab46-159">Le balisage XML peut provenir d’un objet **Recordset** créé à partir d’une table, d’une source externe à la base de données, tel qu’un fichier XML que vous analysez dans une chaîne ou d’un balisage XML incorporé directement dans la procédure.</span><span class="sxs-lookup"><span data-stu-id="4ab46-159">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure.</span></span> <span data-ttu-id="4ab46-160">Vous pouvez créer différents rubans en utilisant plusieurs appels de la méthode **LoadCustomUI** , en passant un balisage XML différent dans la mesure où le nom de chaque ruban et l’attribut **id** des onglets constituant le ruban sont uniques.</span><span class="sxs-lookup"><span data-stu-id="4ab46-160">You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="4ab46-161">Une fois la procédure terminée, vous créez ensuite une macro AutoExec qui appelle la procédure à l'aide de l'action ExécuterCode.</span><span class="sxs-lookup"><span data-stu-id="4ab46-161">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action.</span></span> <span data-ttu-id="4ab46-162">Ainsi, lorsque l’application est démarrée, la méthode **LoadCustomUI** s’exécute automatiquement et tous les rubans personnalisés sont accessibles à l’application.</span><span class="sxs-lookup"><span data-stu-id="4ab46-162">That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

<span data-ttu-id="4ab46-163"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="4ab46-163"><<<<<<< HEAD</span></span>
## <a name="assigning-custom-ribbons-to-forms-or-reports"></a><span data-ttu-id="4ab46-164">Affectation de rubans personnalisés à des formulaires ou des États</span><span class="sxs-lookup"><span data-stu-id="4ab46-164">Assigning Custom Ribbons to Forms or Reports</span></span>
=======
## <a name="assign-custom-ribbons-to-forms-or-reports"></a><span data-ttu-id="4ab46-165">Affecter des rubans personnalisés à des formulaires ou des États</span><span class="sxs-lookup"><span data-stu-id="4ab46-165">Assign custom ribbons to forms or reports</span></span>
>>>>>>> <span data-ttu-id="4ab46-166">master</span><span class="sxs-lookup"><span data-stu-id="4ab46-166">master</span></span>

1.  <span data-ttu-id="4ab46-167">Suivez le processus décrit précédemment pour rendre le ruban personnalisé disponible pour cette application.</span><span class="sxs-lookup"><span data-stu-id="4ab46-167">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="4ab46-168">Ouvrez le formulaire ou l'état en mode Création.</span><span class="sxs-lookup"><span data-stu-id="4ab46-168">Open the form or report in Design view.</span></span>

<span data-ttu-id="4ab46-169"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="4ab46-169"><<<<<<< HEAD</span></span>
3.  <span data-ttu-id="4ab46-170">Sous l’onglet Création, cliquez sur **Feuille de propriétés**.</span><span class="sxs-lookup"><span data-stu-id="4ab46-170">On the Design tab, click **Property Sheet**.</span></span>

4.  <span data-ttu-id="4ab46-171">Sous l’onglet **Tout** de la fenêtre Propriétés, cliquez dans la liste **Nom du ruban**, puis sélectionnez un Ruban.</span><span class="sxs-lookup"><span data-stu-id="4ab46-171">On the **All** tab of the Property window, click the **Ribbon Name** list and then select a ribbon.</span></span>
=======
3.  <span data-ttu-id="4ab46-172">Sous l’onglet Création, cliquez sur **Feuille de propriétés**.</span><span class="sxs-lookup"><span data-stu-id="4ab46-172">On the Design tab, choose **Property Sheet**.</span></span>

4.  <span data-ttu-id="4ab46-173">Sous l’onglet **tous** de la fenêtre Propriétés, sélectionnez la liste **Nom du ruban** , puis sélectionnez un ruban.</span><span class="sxs-lookup"><span data-stu-id="4ab46-173">On the **All** tab of the Property window, choose the **Ribbon Name** list and then select a ribbon.</span></span>
>>>>>>> <span data-ttu-id="4ab46-174">master</span><span class="sxs-lookup"><span data-stu-id="4ab46-174">master</span></span>

5.  <span data-ttu-id="4ab46-175">Enregistrer, fermez et rouvrez le formulaire ou état.</span><span class="sxs-lookup"><span data-stu-id="4ab46-175">Save, close, and then reopen the form or report.</span></span> <span data-ttu-id="4ab46-176">Le ruban de l’interface utilisateur que vous avez sélectionné est affiché.</span><span class="sxs-lookup"><span data-stu-id="4ab46-176">The ribbon UI you selected is displayed.</span></span>


> [!NOTE]
> <span data-ttu-id="4ab46-177">Les onglets affichés dans l’interface utilisateur du ruban sont additive.</span><span class="sxs-lookup"><span data-stu-id="4ab46-177">The tabs displayed in the ribbon UI are additive.</span></span> <span data-ttu-id="4ab46-178">Autrement dit, sauf si vous spécifiquement masquez les onglets ou définissez l’attribut *Démarrer à partir de zéro* à **la valeur True**, les onglets affichés dans un formulaire ou interface utilisateur de ruban de l’état s’ajoutent aux onglets existants.</span><span class="sxs-lookup"><span data-stu-id="4ab46-178">That is, unless you specifically hide the tabs or set the *Start from Scratch* attribute to **True**, the tabs displayed in a form's or report's ribbon user interface are in addition to the existing tabs.</span></span>

> [!NOTE]
> <span data-ttu-id="4ab46-179">[!REMARQUE] Pour plus d'informations sur l'interface du ruban dans d'autres applications Office, consultez l'article [Vue d'ensemble du ruban Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="4ab46-179">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


