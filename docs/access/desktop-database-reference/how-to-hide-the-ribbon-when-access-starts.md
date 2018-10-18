---
<span data-ttu-id="c814c-101">titre : masquer le ruban au démarrage d’Access TOCTitle : masquer le ruban au démarrage d’Access <<<<<<< ms:assetid tête : f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl : https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID : ms.date 48548817 : 18/09/2015 === Description : comment charger un ruban personnalisé qui masque tous les onglets intégrés dans Access 2013.</span><span class="sxs-lookup"><span data-stu-id="c814c-101">title: Hide the ribbon when Access starts TOCTitle: Hide the ribbon when Access starts <<<<<<< HEAD ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: 48548817 ms.date: 09/18/2015 ======= description: How to load a customized ribbon that hides all of the built-in tabs in Access 2013.</span></span>
<span data-ttu-id="c814c-102">MS:AssetId : f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl : https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID : ms.date 48548817 : 10/16/2018</span><span class="sxs-lookup"><span data-stu-id="c814c-102">ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: 48548817 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="c814c-103">maître mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="c814c-103">master mtps_version: v=office.15</span></span>
---

# <a name="hide-the-ribbon-when-access-starts"></a><span data-ttu-id="c814c-104">Masquer le ruban au démarrage d’Access</span><span class="sxs-lookup"><span data-stu-id="c814c-104">Hide the ribbon when Access starts</span></span>

<span data-ttu-id="c814c-105">**S’applique à :** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c814c-105">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="c814c-p102">Par défaut, Microsoft Access ne fournit pas de méthode pour masquer le ruban. Cette rubrique décrit comment charger un ruban personnalisé qui masque tous les onglets prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="c814c-p102">By default, Microsoft Access does not provide a method for hiding the ribbon. This topic describes how to load a customized ribbon that hides all of the built-in tabs.</span></span>

<span data-ttu-id="c814c-108">Pour charger le ruban personnalisé au démarrage d'Access, vous devez stocker ses paramètres dans une table dénommée **RubansSysU**.</span><span class="sxs-lookup"><span data-stu-id="c814c-108">To load the customized ribbon when Access starts, you should store its settings in a table named **USysRibbons**.</span></span>

<span data-ttu-id="c814c-109"><<<<<<< Tête la table **RubansSysU** doit être créée à l’aide des noms de colonne spécifique afin que les personnalisations du ruban à mettre en œuvre.</span><span class="sxs-lookup"><span data-stu-id="c814c-109"><<<<<<< HEAD The **USysRibbons** table must be created using specific column names in order for the ribbon customizations to be implemented.</span></span> <span data-ttu-id="c814c-110">La table ci-dessous contient les paramètres à utiliser lors de la création de la table **RubansSysU**.</span><span class="sxs-lookup"><span data-stu-id="c814c-110">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
<span data-ttu-id="c814c-111">=== La table **RubansSysU** doit être créée en utilisant des noms de colonne spécifiques pour les personnalisations du ruban à mettre en œuvre.</span><span class="sxs-lookup"><span data-stu-id="c814c-111">======= The **USysRibbons** table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="c814c-112">La table ci-dessous contient les paramètres à utiliser lors de la création de la table **RubansSysU**.</span><span class="sxs-lookup"><span data-stu-id="c814c-112">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
>>>>>>> <span data-ttu-id="c814c-113">master</span><span class="sxs-lookup"><span data-stu-id="c814c-113">master</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<span data-ttu-id="c814c-114"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="c814c-114"><<<<<<< HEAD</span></span>
<th><p><span data-ttu-id="c814c-115">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c814c-115">Column Name</span></span></p></th>
<th><p><span data-ttu-id="c814c-116">Type de données</span><span class="sxs-lookup"><span data-stu-id="c814c-116">Data Type</span></span></p></th>
=======
<th><p><span data-ttu-id="c814c-117">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c814c-117">Column name</span></span></p></th>
<th><p><span data-ttu-id="c814c-118">Type de données</span><span class="sxs-lookup"><span data-stu-id="c814c-118">Data type</span></span></p></th><span data-ttu-id="c814c-119">
>>>>>>>forme de base</span><span class="sxs-lookup"><span data-stu-id="c814c-119">
>>>>>>> master</span></span>
<th><p><span data-ttu-id="c814c-120">Description</span><span class="sxs-lookup"><span data-stu-id="c814c-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c814c-121"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="c814c-121"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="c814c-122">Texte</span><span class="sxs-lookup"><span data-stu-id="c814c-122">Text</span></span></p></td>
<td><p><span data-ttu-id="c814c-123">Contient le nom du ruban personnalisé devant être associé à cette personnalisation.</span><span class="sxs-lookup"><span data-stu-id="c814c-123">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c814c-124"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="c814c-124"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="c814c-125">Mémo</span><span class="sxs-lookup"><span data-stu-id="c814c-125">Memo</span></span></p></td>
<span data-ttu-id="c814c-126"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="c814c-126"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="c814c-127">Contient le XML d'extensibilité du ruban (RibbonX) qui définit la personnalisation du ruban.</span><span class="sxs-lookup"><span data-stu-id="c814c-127">Contains the Ribbon Extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
=======
<td><p><span data-ttu-id="c814c-128">Contient l’extensibilité du ruban (RibbonX) XML qui définit la personnalisation du ruban.</span><span class="sxs-lookup"><span data-stu-id="c814c-128">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td><span data-ttu-id="c814c-129">
>>>>>>>forme de base</span><span class="sxs-lookup"><span data-stu-id="c814c-129">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>

<span data-ttu-id="c814c-130"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="c814c-130"><<<<<<< HEAD</span></span>

<span data-ttu-id="c814c-131">La table contient les paramètres de personnalisation du ruban à stocker dans la table **RubansSysU**.</span><span class="sxs-lookup"><span data-stu-id="c814c-131">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c814c-132">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c814c-132">Column Name</span></span></p></th>
<th><p><span data-ttu-id="c814c-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="c814c-133">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c814c-134"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="c814c-134"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="c814c-135">HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="c814c-135">HideTheRibbon</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c814c-136"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="c814c-136"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="c814c-137">&lt;CustomUI xmlns =&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot; &gt; &lt;ruban startFromScratch =&quot;true&quot;/&gt;&lt;/CustomUI&gt;</span><span class="sxs-lookup"><span data-stu-id="c814c-137">&lt;CustomUI xmlns=&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot;&gt; &lt;ribbon startFromScratch=&quot;true&quot;/&gt;&lt;/CustomUI&gt;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="applying-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="c814c-138">Appliquer le ruban personnalisé au démarrage d'Access</span><span class="sxs-lookup"><span data-stu-id="c814c-138">Applying a Custom Ribbon When Access Starts</span></span>
=======
<br/>

<span data-ttu-id="c814c-139">La table contient les paramètres de personnalisation du ruban à stocker dans la table **RubansSysU**.</span><span class="sxs-lookup"><span data-stu-id="c814c-139">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

|<span data-ttu-id="c814c-140">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c814c-140">Column name</span></span>|<span data-ttu-id="c814c-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="c814c-141">Value</span></span>|
|:----------|:----|
|<span data-ttu-id="c814c-142">**RibbonName**</span><span class="sxs-lookup"><span data-stu-id="c814c-142">**RibbonName**</span></span>|<span data-ttu-id="c814c-143">HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="c814c-143">HideTheRibbon</span></span>|
|<span data-ttu-id="c814c-144">**RibbonXML**</span><span class="sxs-lookup"><span data-stu-id="c814c-144">**RibbonXML**</span></span>|`<CustomUI xmlns="https://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="c814c-145">Appliquer un ruban personnalisé au démarrage d’Access</span><span class="sxs-lookup"><span data-stu-id="c814c-145">Apply a custom ribbon when Access starts</span></span>
>>>>>>> <span data-ttu-id="c814c-146">master</span><span class="sxs-lookup"><span data-stu-id="c814c-146">master</span></span>

<span data-ttu-id="c814c-147">Pour appliquer un ruban personnalisé disponible au démarrage de l'application, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="c814c-147">To apply a custom ribbon so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="c814c-148">Suivez le processus décrit précédemment pour rendre le ruban personnalisé disponible pour cette application.</span><span class="sxs-lookup"><span data-stu-id="c814c-148">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="c814c-149">Redémarrez l'application.</span><span class="sxs-lookup"><span data-stu-id="c814c-149">Close and then restart the application.</span></span>

<span data-ttu-id="c814c-150"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="c814c-150"><<<<<<< HEAD</span></span>
3.  <span data-ttu-id="c814c-151">Cliquez sur le **Bouton Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") , puis sur **Options Access**.</span><span class="sxs-lookup"><span data-stu-id="c814c-151">Click the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then click **Access Options**.</span></span>

4.  <span data-ttu-id="c814c-152">Cliquez sur l'option **Base de données active**, dans la section **Options de la barre d'outils et du ruban**, puis sur la liste **Nom du ruban** et sélectionnez **HideTheRibbon**.</span><span class="sxs-lookup"><span data-stu-id="c814c-152">Click the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, click the **Ribbon Name** list and select **HideTheRibbon**.</span></span>
=======
3.  <span data-ttu-id="c814c-153">Cliquez sur le **Bouton Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), puis cliquez sur **Options Access**.</span><span class="sxs-lookup"><span data-stu-id="c814c-153">Choose the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), and then choose **Access Options**.</span></span>

4.  <span data-ttu-id="c814c-154">Choisissez l’option de **Base de données actuelle** puis, dans la section **Options de la barre d’outils et du ruban** , cliquez sur la liste **Nom du ruban** et sélectionnez **HideTheRibbon**.</span><span class="sxs-lookup"><span data-stu-id="c814c-154">Choose the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, choose the **Ribbon Name** list and select **HideTheRibbon**.</span></span>
>>>>>>> <span data-ttu-id="c814c-155">master</span><span class="sxs-lookup"><span data-stu-id="c814c-155">master</span></span>

5.  <span data-ttu-id="c814c-156">Fermez er redémarrez l'application.</span><span class="sxs-lookup"><span data-stu-id="c814c-156">Close and then restart the application.</span></span>

> [!NOTE]
> <span data-ttu-id="c814c-157">[!REMARQUE] Pour plus d'informations sur l'interface du ruban dans d'autres applications Office, consultez l'article [Vue d'ensemble du ruban Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="c814c-157">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


