---
title: Configurer des UDF dans Excel Online dans Office Server Online Preview
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Utilisez les fonctions définies par l’utilisateur (UDF) dans Excel Online dans Office Online Server Preview pour appeler des fonctions personnalisées.
ms.openlocfilehash: ae2d668ebd4a4df278a5c19e702de248b1749b84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782005"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server-preview"></a><span data-ttu-id="60fa3-103">Configurer des UDF dans Excel Online dans Office Server Online Preview</span><span class="sxs-lookup"><span data-stu-id="60fa3-103">Configure UDFs in Excel Online in Office Online Server Preview</span></span>

<span data-ttu-id="60fa3-104">[Cette rubrique est une documentation préliminaire et sujette à modification dans les versions futures.] Utilisez les fonctions définies par l’utilisateur (UDF) dans Excel Online dans Office Online Server Preview pour appeler des fonctions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="60fa3-104">[This topic is pre-release documentation and is subject to change in future releases.] Use user-defined functions (UDFs) in Excel Online in Office Online Server Preview to call custom functions.</span></span> 
  
<span data-ttu-id="60fa3-105">Fonctions définies par l’utilisateur (UDF) dans Excel Online permettent d’appeler des fonctions personnalisées écrites en code managé à l’aide de formules dans les cellules.</span><span class="sxs-lookup"><span data-stu-id="60fa3-105">User-defined functions (UDFs) in Excel Online enable you to call custom functions written in managed code by using formulas in cells.</span></span> <span data-ttu-id="60fa3-106">Vous pouvez utiliser l’appel des UDF :</span><span class="sxs-lookup"><span data-stu-id="60fa3-106">You can use UDFs to:</span></span>
  
- <span data-ttu-id="60fa3-107">Call custom mathematical functions.</span><span class="sxs-lookup"><span data-stu-id="60fa3-107">Call custom mathematical functions.</span></span>
    
- <span data-ttu-id="60fa3-108">Get data from custom data sources into worksheets.</span><span class="sxs-lookup"><span data-stu-id="60fa3-108">Get data from custom data sources into worksheets.</span></span>
    
- <span data-ttu-id="60fa3-109">Appeler des services web.</span><span class="sxs-lookup"><span data-stu-id="60fa3-109">Call web services.</span></span>
    
<span data-ttu-id="60fa3-110">Vous pouvez installer les fichiers binaires UDF dans un des deux emplacements :</span><span class="sxs-lookup"><span data-stu-id="60fa3-110">You can install UDF binaries in one of two locations:</span></span>
  
- <span data-ttu-id="60fa3-111">Un répertoire local.</span><span class="sxs-lookup"><span data-stu-id="60fa3-111">A local directory.</span></span> <span data-ttu-id="60fa3-112">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="60fa3-112">For example:</span></span> 
    
    <span data-ttu-id="60fa3-113">C:\UDFs\MySampleUdf.dll </span><span class="sxs-lookup"><span data-stu-id="60fa3-113">C:\UDFs\MySampleUdf.dll</span></span>
    
- <span data-ttu-id="60fa3-114">Le global assembly cache.</span><span class="sxs-lookup"><span data-stu-id="60fa3-114">The global assembly cache.</span></span> <span data-ttu-id="60fa3-115">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="60fa3-115">For example:</span></span> 
    
    <span data-ttu-id="60fa3-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span><span class="sxs-lookup"><span data-stu-id="60fa3-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span></span>
    
<span data-ttu-id="60fa3-117">Référence de l’emplacement lorsque vous créez une définition de **New-OfficeWebAppsExcelUserDefinedFunction** sur Office Online Server Preview.</span><span class="sxs-lookup"><span data-stu-id="60fa3-117">Reference the location when you create a **New-OfficeWebAppsExcelUserDefinedFunction** definition on the Office Online Server Preview.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="60fa3-118">Office Online Server Preview ne gère pas les UDF situés sur des partages réseau.</span><span class="sxs-lookup"><span data-stu-id="60fa3-118">Office Online Server Preview does not support UDFs located on network shares.</span></span> 
  
## <a name="enable-udfs-on-office-online-server-preview"></a><span data-ttu-id="60fa3-119">Activer les UDF sur Office Online Server Preview</span><span class="sxs-lookup"><span data-stu-id="60fa3-119">Enable UDFs on Office Online Server Preview</span></span>

<span data-ttu-id="60fa3-120">Lorsqu’un administrateur crée une nouvelle batterie de serveurs Office Web Apps Server à l’aide de l’applet de commande [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell, les assemblys UDF sont désactivés par défaut.</span><span class="sxs-lookup"><span data-stu-id="60fa3-120">When an adminstrator creates a new Office Web Apps Server farm by using the [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell cmdlet, UDF assemblies are disabled by default.</span></span> <span data-ttu-id="60fa3-121">La valeur par défaut de l’indicateur **ExcelUdfsAllowed** a la valeur false.</span><span class="sxs-lookup"><span data-stu-id="60fa3-121">The default value of the **ExcelUdfsAllowed** flag is false.</span></span> 
  
<span data-ttu-id="60fa3-122">Pour activer les UDF, exécutez la commande Windows PowerShell suivante sur Office Online Server Preview, une fois que la batterie de serveurs Office Web Apps Server a été créé.</span><span class="sxs-lookup"><span data-stu-id="60fa3-122">To enable UDFs, run the following Windows PowerShell command on the Office Online Server Preview, after the Office Web Apps Server farm has been created.</span></span>
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server-preview"></a><span data-ttu-id="60fa3-123">Créer des définitions de fonctions UDF sur Office Online Server Preview</span><span class="sxs-lookup"><span data-stu-id="60fa3-123">Create UDF definitions on Office Online Server Preview</span></span>

<span data-ttu-id="60fa3-124">Une fois que vous activez UDF, vous devez créer une définition pour le fichier binaire qui contient l’UDF.</span><span class="sxs-lookup"><span data-stu-id="60fa3-124">After you enable UDFs, you need to create a definition for the binary that contains the UDFs.</span></span> <span data-ttu-id="60fa3-125">Pour créer une définition pour votre UDF binaire sur Office Online Server Preview, utilisez l’applet de commande **New-OfficeWebAppsExcelUserDefinedFunction** .</span><span class="sxs-lookup"><span data-stu-id="60fa3-125">To create a definition for your UDF binary on the Office Online Server Preview, use the **New-OfficeWebAppsExcelUserDefinedFunction** cmdlet.</span></span> <span data-ttu-id="60fa3-126">Cette applet de commande inclut les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="60fa3-126">This cmdlet includes the following parameters:</span></span> 
  
- <span data-ttu-id="60fa3-127">**Assembly**</span><span class="sxs-lookup"><span data-stu-id="60fa3-127">**Assembly**</span></span>
    
- <span data-ttu-id="60fa3-128">**AssemblyLocation**</span><span class="sxs-lookup"><span data-stu-id="60fa3-128">**AssemblyLocation**</span></span>
    
- <span data-ttu-id="60fa3-129">**Activer** (la valeur False par défaut)</span><span class="sxs-lookup"><span data-stu-id="60fa3-129">**Enable** (set to False by default)</span></span> 
    
- <span data-ttu-id="60fa3-130">**Description**</span><span class="sxs-lookup"><span data-stu-id="60fa3-130">**Description**</span></span>
    
<span data-ttu-id="60fa3-131">Les exemples suivants montrent comment créer les définitions de fonctions UDF.</span><span class="sxs-lookup"><span data-stu-id="60fa3-131">The following examples show how create the UDF definitions.</span></span>
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
<span data-ttu-id="60fa3-132">Après avoir créé la nouvelle référence UDF, exécutez **iisreset** sur le serveur pour identifier les immédiatement la référence.</span><span class="sxs-lookup"><span data-stu-id="60fa3-132">After you create the new UDF reference, run **iisreset** on the server to pick up the reference immediately.</span></span> 
  
## <a name="additional-office-online-server-preview-udf-windows-powershell-commands"></a><span data-ttu-id="60fa3-133">Commandes Office Online Server Preview UDF Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="60fa3-133">Additional Office Online Server Preview UDF Windows PowerShell commands</span></span>

<span data-ttu-id="60fa3-134">Utiliser les applets de commande Windows PowerShell suivante pour travailler avec UDF :</span><span class="sxs-lookup"><span data-stu-id="60fa3-134">Use the following Windows PowerShell cmdlets to work with UDFs:</span></span>
  
- <span data-ttu-id="60fa3-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (aucun paramètre requis -) renvoie une liste de définitions de fonctions UDF sont configurés sur Office Online Server Preview.</span><span class="sxs-lookup"><span data-stu-id="60fa3-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (no required parameters) - Returns a list of UDF definitions that are configured on the Office Online Server Preview.</span></span> 
    
- <span data-ttu-id="60fa3-136">**Set-OfficeWebAppsExcelUserDefinedFunction** (Paramètre identity requis) - définit les propriétés de définitions de fonctions UDF existantes.</span><span class="sxs-lookup"><span data-stu-id="60fa3-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Sets properties on existing UDF definitions.</span></span> 
    
- <span data-ttu-id="60fa3-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Paramètre identity requis) - supprime les définitions de fonctions UDF existantes.</span><span class="sxs-lookup"><span data-stu-id="60fa3-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Removes existing UDF definitions.</span></span> 
    
## <a name="udf-sample"></a><span data-ttu-id="60fa3-138">Exemple de fichier UDF</span><span class="sxs-lookup"><span data-stu-id="60fa3-138">UDF sample</span></span>

<span data-ttu-id="60fa3-139">Les fichiers suivants fournissent un exemple de classeur qui utilise un fichier UDF et le fichier UDF binaires :</span><span class="sxs-lookup"><span data-stu-id="60fa3-139">The following files provide a sample workbook that uses a UDF and the UDF binary:</span></span>
  
- <span data-ttu-id="60fa3-140">[BooleanDataType.xlsx](http://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx) --un exemple de classeur qui utilise un fichier UDF</span><span class="sxs-lookup"><span data-stu-id="60fa3-140">[BooleanDataType.xlsx](http://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx) -- a sample workbook that uses a UDF</span></span>  
- <span data-ttu-id="60fa3-141">[EcsUdfsCommonSet.dll](http://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/EcsUdfsCommonSet.dll) --le fichier binaire UDF</span><span class="sxs-lookup"><span data-stu-id="60fa3-141">[EcsUdfsCommonSet.dll](http://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/EcsUdfsCommonSet.dll) -- the UDF binary</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="60fa3-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60fa3-142">See also</span></span>

- [<span data-ttu-id="60fa3-143">Configurer les paramètres d’administration Excel Online</span><span class="sxs-lookup"><span data-stu-id="60fa3-143">Configure Excel Online administrative settings</span></span>](https://technet.microsoft.com/en-us/library/jj219698%28v=office.16%29.aspx)  
- [<span data-ttu-id="60fa3-144">Office Online Server Preview</span><span class="sxs-lookup"><span data-stu-id="60fa3-144">Office Online Server Preview</span></span>](https://technet.microsoft.com/en-us/library/jj219456%28v=office.16%29.aspx)
    

