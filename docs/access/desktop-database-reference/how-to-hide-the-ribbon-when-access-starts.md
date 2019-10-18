---
title: Masquer le ruban au démarrage d’Access
TOCTitle: Hide the ribbon when Access starts
description: Comment charger un ruban personnalisé qui masque tous les onglets prédéfinis dans Access 2013.
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15)
ms:contentKeyID: 48548817
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 384a575ae5e15b75ba7b0b891529c695cc3de599
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537828"
---
# <a name="hide-the-ribbon-when-access-starts"></a><span data-ttu-id="c4aa9-103">Masquer le ruban au démarrage d’Access</span><span class="sxs-lookup"><span data-stu-id="c4aa9-103">Hide the ribbon when Access starts</span></span>

<span data-ttu-id="c4aa9-104">**S’applique à** : Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4aa9-104">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="c4aa9-p101">Par défaut, Microsoft Access ne fournit pas de méthode pour masquer le ruban. Cette rubrique décrit comment charger un ruban personnalisé qui masque tous les onglets prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-p101">By default, Microsoft Access does not provide a method for hiding the ribbon. This topic describes how to load a customized ribbon that hides all of the built-in tabs.</span></span>

<span data-ttu-id="c4aa9-107">Pour charger le ruban personnalisé au démarrage d'Access, vous devez stocker ses paramètres dans une table dénommée **RubansSysU**.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-107">To load the customized ribbon when Access starts, you should store its settings in a table named **USysRibbons**.</span></span>

<span data-ttu-id="c4aa9-108">Cette **table** doit être créée en utilisant des noms de colonnes spécifiques afin que les personnalisations du ruban soient implémentées.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-108">The **USysRibbons** table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="c4aa9-109">Le tableau suivant répertorie les paramètres à utiliser lors de la création du tableau**USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-109">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c4aa9-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c4aa9-110">Column name</span></span></p></th>
<th><p><span data-ttu-id="c4aa9-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="c4aa9-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="c4aa9-112">Description</span><span class="sxs-lookup"><span data-stu-id="c4aa9-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4aa9-113"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="c4aa9-113"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="c4aa9-114">Text</span><span class="sxs-lookup"><span data-stu-id="c4aa9-114">Text</span></span></p></td>
<td><p><span data-ttu-id="c4aa9-115">Contient le nom du ruban personnalisé devant être associé à cette personnalisation.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-115">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4aa9-116"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="c4aa9-116"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="c4aa9-117">Mémo</span><span class="sxs-lookup"><span data-stu-id="c4aa9-117">Memo</span></span></p></td>
<td><p><span data-ttu-id="c4aa9-118">Contient le XML d'extensibilité du ruban (RibbonX) qui définit la personnalisation du ruban.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-118">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="c4aa9-119">Le tableau suivant répertorie les paramètres de personnalisation du ruban pour les stocker dans le tableau **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-119">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

|<span data-ttu-id="c4aa9-120">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c4aa9-120">Column name</span></span>|<span data-ttu-id="c4aa9-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4aa9-121">Value</span></span>|
|:----------|:----|
|<span data-ttu-id="c4aa9-122">**RibbonName**</span><span class="sxs-lookup"><span data-stu-id="c4aa9-122">**RibbonName**</span></span>|<span data-ttu-id="c4aa9-123">HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="c4aa9-123">HideTheRibbon</span></span>|
|<span data-ttu-id="c4aa9-124">**RibbonXML**</span><span class="sxs-lookup"><span data-stu-id="c4aa9-124">**RibbonXML**</span></span>|`<CustomUI xmlns="http://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="c4aa9-125">Appliquer un ruban personnalisé au démarrage d’Access</span><span class="sxs-lookup"><span data-stu-id="c4aa9-125">Apply a custom ribbon when Access starts</span></span>

<span data-ttu-id="c4aa9-126">Pour appliquer un ruban personnalisé disponible au démarrage de l'application, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="c4aa9-126">To apply a custom ribbon so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="c4aa9-127">Suivez le processus décrit précédemment pour rendre le ruban personnalisé disponible pour cette application.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-127">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="c4aa9-128">Redémarrez l'application.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-128">Close and then restart the application.</span></span>

3.  <span data-ttu-id="c4aa9-129">Sélectionnez le **bouton Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") , puis **Access Options**.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-129">Choose the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), and then choose **Access Options**.</span></span>

4.  <span data-ttu-id="c4aa9-130">Cliquez sur l'option **Base de données active**, dans la section **Options de la barre d'outils et du ruban**, puis sur la liste **Nom du ruban** et sélectionnez **MasquerLeRuban**.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-130">Choose the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, choose the **Ribbon Name** list and select **HideTheRibbon**.</span></span>

5.  <span data-ttu-id="c4aa9-131">Fermez er redémarrez l'application.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-131">Close and then restart the application.</span></span>

> [!NOTE]
> <span data-ttu-id="c4aa9-132">Pour plus d'informations sur l'interface du ruban dans d'autres applications Office, consultez l'article [Vue d'ensemble du ruban Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="c4aa9-132">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


