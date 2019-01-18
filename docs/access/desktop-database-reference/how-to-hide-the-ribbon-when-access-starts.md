---
title: Masquer le ruban au démarrage d’Access
TOCTitle: Hide the ribbon when Access starts
description: Comment charger un ruban personnalisé qui masque tous les onglets intégrés dans Access 2013.
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15)
ms:contentKeyID: 48548817
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 4ce9327790f620ba9163f5cdbe7b5c8900de4341
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704104"
---
# <a name="hide-the-ribbon-when-access-starts"></a><span data-ttu-id="c6a9e-103">Masquer le ruban au démarrage d’Access</span><span class="sxs-lookup"><span data-stu-id="c6a9e-103">Hide the ribbon when Access starts</span></span>

<span data-ttu-id="c6a9e-104">**S’applique à :** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c6a9e-104">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="c6a9e-p101">Par défaut, Microsoft Access ne fournit pas de méthode pour masquer le ruban. Cette rubrique décrit comment charger un ruban personnalisé qui masque tous les onglets prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="c6a9e-p101">By default, Microsoft Access does not provide a method for hiding the ribbon. This topic describes how to load a customized ribbon that hides all of the built-in tabs.</span></span>

<span data-ttu-id="c6a9e-107">Pour charger le ruban personnalisé au démarrage d'Access, vous devez stocker ses paramètres dans une table dénommée **RubansSysU**.</span><span class="sxs-lookup"><span data-stu-id="c6a9e-107">To load the customized ribbon when Access starts, you should store its settings in a table named **USysRibbons**.</span></span>

<span data-ttu-id="c6a9e-108">La table **RubansSysU** doit être créée en utilisant des noms de colonne spécifiques pour les personnalisations du ruban à mettre en œuvre.</span><span class="sxs-lookup"><span data-stu-id="c6a9e-108">The **USysRibbons** table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="c6a9e-109">La table ci-dessous contient les paramètres à utiliser lors de la création de la table **RubansSysU**.</span><span class="sxs-lookup"><span data-stu-id="c6a9e-109">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c6a9e-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c6a9e-110">Column name</span></span></p></th>
<th><p><span data-ttu-id="c6a9e-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="c6a9e-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="c6a9e-112">Description</span><span class="sxs-lookup"><span data-stu-id="c6a9e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6a9e-113"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="c6a9e-113"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="c6a9e-114">Texte</span><span class="sxs-lookup"><span data-stu-id="c6a9e-114">Text</span></span></p></td>
<td><p><span data-ttu-id="c6a9e-115">Contient le nom du ruban personnalisé devant être associé à cette personnalisation.</span><span class="sxs-lookup"><span data-stu-id="c6a9e-115">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6a9e-116"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="c6a9e-116"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="c6a9e-117">Mémo</span><span class="sxs-lookup"><span data-stu-id="c6a9e-117">Memo</span></span></p></td>
<td><p><span data-ttu-id="c6a9e-118">Contient l’extensibilité du ruban (RibbonX) XML qui définit la personnalisation du ruban.</span><span class="sxs-lookup"><span data-stu-id="c6a9e-118">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="c6a9e-119">La table contient les paramètres de personnalisation du ruban à stocker dans la table **RubansSysU**.</span><span class="sxs-lookup"><span data-stu-id="c6a9e-119">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

|<span data-ttu-id="c6a9e-120">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c6a9e-120">Column name</span></span>|<span data-ttu-id="c6a9e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6a9e-121">Value</span></span>|
|:----------|:----|
|<span data-ttu-id="c6a9e-122">**RibbonName**</span><span class="sxs-lookup"><span data-stu-id="c6a9e-122">**RibbonName**</span></span>|<span data-ttu-id="c6a9e-123">HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="c6a9e-123">HideTheRibbon</span></span>|
|<span data-ttu-id="c6a9e-124">**RibbonXML**</span><span class="sxs-lookup"><span data-stu-id="c6a9e-124">**RibbonXML**</span></span>|`<CustomUI xmlns="https://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="c6a9e-125">Appliquer un ruban personnalisé au démarrage d’Access</span><span class="sxs-lookup"><span data-stu-id="c6a9e-125">Apply a custom ribbon when Access starts</span></span>

<span data-ttu-id="c6a9e-126">Pour appliquer un ruban personnalisé disponible au démarrage de l'application, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="c6a9e-126">To apply a custom ribbon so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="c6a9e-127">Suivez le processus décrit précédemment pour rendre le ruban personnalisé disponible pour cette application.</span><span class="sxs-lookup"><span data-stu-id="c6a9e-127">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="c6a9e-128">Redémarrez l'application.</span><span class="sxs-lookup"><span data-stu-id="c6a9e-128">Close and then restart the application.</span></span>

3.  <span data-ttu-id="c6a9e-129">Cliquez sur le **Bouton Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), puis cliquez sur **Options Access**.</span><span class="sxs-lookup"><span data-stu-id="c6a9e-129">Choose the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), and then choose **Access Options**.</span></span>

4.  <span data-ttu-id="c6a9e-130">Choisissez l’option de **Base de données actuelle** puis, dans la section **Options de la barre d’outils et du ruban** , cliquez sur la liste **Nom du ruban** et sélectionnez **HideTheRibbon**.</span><span class="sxs-lookup"><span data-stu-id="c6a9e-130">Choose the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, choose the **Ribbon Name** list and select **HideTheRibbon**.</span></span>

5.  <span data-ttu-id="c6a9e-131">Fermez er redémarrez l'application.</span><span class="sxs-lookup"><span data-stu-id="c6a9e-131">Close and then restart the application.</span></span>

> [!NOTE]
> <span data-ttu-id="c6a9e-132">[!REMARQUE] Pour plus d'informations sur l'interface du ruban dans d'autres applications Office, consultez l'article [Vue d'ensemble du ruban Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="c6a9e-132">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


