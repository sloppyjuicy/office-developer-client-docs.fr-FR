---
title: Configurer des fichiers UDF dans Excel Online dans Office Online Server
manager: lindalu
ms.date: 12/03/2019
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Utilisez des fonctions définies par l’utilisateur dans Excel Online dans Office Online Server pour appeler des fonctions personnalisées.
ms.openlocfilehash: e1b005079c03ae3028ba6bf9ee1156c6ae2eae80
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2020
ms.locfileid: "43102932"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a><span data-ttu-id="6bd12-103">Configurer des fichiers UDF dans Excel Online dans Office Online Server</span><span class="sxs-lookup"><span data-stu-id="6bd12-103">Configure UDFs in Excel Online in Office Online Server</span></span>

<span data-ttu-id="6bd12-104">Utilisez des fonctions définies par l’utilisateur dans Excel Online dans Office Online Server pour appeler des fonctions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="6bd12-104">Use user-defined functions (UDFs) in Excel Online in Office Online Server to call custom functions.</span></span> 
  
<span data-ttu-id="6bd12-105">Les fonctions définies par l’utilisateur dans Excel Online vous permettent d’appeler des fonctions personnalisées écrites en code managé à l’aide de formules dans les cellules.</span><span class="sxs-lookup"><span data-stu-id="6bd12-105">User-defined functions (UDFs) in Excel Online enable you to call custom functions written in managed code by using formulas in cells.</span></span> <span data-ttu-id="6bd12-106">Vous pouvez utiliser des FDU pour :</span><span class="sxs-lookup"><span data-stu-id="6bd12-106">You can use UDFs to:</span></span>
  
- <span data-ttu-id="6bd12-107">Call custom mathematical functions.</span><span class="sxs-lookup"><span data-stu-id="6bd12-107">Call custom mathematical functions.</span></span>
    
- <span data-ttu-id="6bd12-108">Get data from custom data sources into worksheets.</span><span class="sxs-lookup"><span data-stu-id="6bd12-108">Get data from custom data sources into worksheets.</span></span>
    
- <span data-ttu-id="6bd12-109">Appeler des services Web.</span><span class="sxs-lookup"><span data-stu-id="6bd12-109">Call web services.</span></span>
    
<span data-ttu-id="6bd12-110">Vous pouvez installer les fichiers binaires UDF à l’un des deux emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="6bd12-110">You can install UDF binaries in one of two locations:</span></span>
  
- <span data-ttu-id="6bd12-111">Un répertoire local.</span><span class="sxs-lookup"><span data-stu-id="6bd12-111">A local directory.</span></span> <span data-ttu-id="6bd12-112">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="6bd12-112">For example:</span></span> 
    
    <span data-ttu-id="6bd12-113">C:\UDFs\MySampleUdf.dll</span><span class="sxs-lookup"><span data-stu-id="6bd12-113">C:\UDFs\MySampleUdf.dll</span></span>
    
- <span data-ttu-id="6bd12-114">Le global assembly cache.</span><span class="sxs-lookup"><span data-stu-id="6bd12-114">The global assembly cache.</span></span> <span data-ttu-id="6bd12-115">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="6bd12-115">For example:</span></span> 
    
    <span data-ttu-id="6bd12-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span><span class="sxs-lookup"><span data-stu-id="6bd12-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span></span>
    
<span data-ttu-id="6bd12-117">Référencez l’emplacement lorsque vous créez une définition **OfficeWebAppsExcelUserDefinedFunction** sur le serveur Office Online.</span><span class="sxs-lookup"><span data-stu-id="6bd12-117">Reference the location when you create a **New-OfficeWebAppsExcelUserDefinedFunction** definition on the Office Online Server.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6bd12-118">Office Online Server ne prend pas en charge les fonctions définies par l’utilisateur sur les partages réseau.</span><span class="sxs-lookup"><span data-stu-id="6bd12-118">Office Online Server does not support UDFs located on network shares.</span></span> 
  
## <a name="enable-udfs-on-office-online-server"></a><span data-ttu-id="6bd12-119">Activer les fonctions UDF sur Office Online Server</span><span class="sxs-lookup"><span data-stu-id="6bd12-119">Enable UDFs on Office Online Server</span></span> 

<span data-ttu-id="6bd12-120">Lorsqu’un administrateur crée une batterie Office Web Apps Server à l’aide de la cmdlet Windows PowerShell [New-OfficeWebAppsFarm](https://docs.microsoft.com/powershell/module/officewebapps/new-officewebappsfarm?view=officewebapps-ps) , les assemblys UDF sont désactivés par défaut.</span><span class="sxs-lookup"><span data-stu-id="6bd12-120">When an administrator creates a new Office Web Apps Server farm by using the [New-OfficeWebAppsFarm](https://docs.microsoft.com/powershell/module/officewebapps/new-officewebappsfarm?view=officewebapps-ps) Windows PowerShell cmdlet, UDF assemblies are disabled by default.</span></span> <span data-ttu-id="6bd12-121">La valeur par défaut de l’indicateur **ExcelUdfsAllowed** est false.</span><span class="sxs-lookup"><span data-stu-id="6bd12-121">The default value of the **ExcelUdfsAllowed** flag is false.</span></span> 
  
<span data-ttu-id="6bd12-122">Pour activer les fonctions définies par l’utilisateur, exécutez la commande Windows PowerShell suivante sur le serveur Office Online, une fois la batterie de serveurs Office Web Apps Server créée.</span><span class="sxs-lookup"><span data-stu-id="6bd12-122">To enable UDFs, run the following Windows PowerShell command on the Office Online Server, after the Office Web Apps Server farm has been created.</span></span>
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a><span data-ttu-id="6bd12-123">Créer des définitions de FDU sur Office Online Server</span><span class="sxs-lookup"><span data-stu-id="6bd12-123">Create UDF definitions on Office Online Server</span></span>

<span data-ttu-id="6bd12-124">Une fois que vous avez activé les FDU, vous devez créer une définition pour le fichier binaire contenant les FDU.</span><span class="sxs-lookup"><span data-stu-id="6bd12-124">After you enable UDFs, you need to create a definition for the binary that contains the UDFs.</span></span> <span data-ttu-id="6bd12-125">Pour créer une définition pour votre fichier binaire UDF sur le serveur Office Online, utilisez la cmdlet **New-OfficeWebAppsExcelUserDefinedFunction** .</span><span class="sxs-lookup"><span data-stu-id="6bd12-125">To create a definition for your UDF binary on the Office Online Server, use the **New-OfficeWebAppsExcelUserDefinedFunction** cmdlet.</span></span> <span data-ttu-id="6bd12-126">Cette applet de commande inclut les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="6bd12-126">This cmdlet includes the following parameters:</span></span> 
  
- <span data-ttu-id="6bd12-127">**Assembly**</span><span class="sxs-lookup"><span data-stu-id="6bd12-127">**Assembly**</span></span>
    
- <span data-ttu-id="6bd12-128">**AssemblyLocation**</span><span class="sxs-lookup"><span data-stu-id="6bd12-128">**AssemblyLocation**</span></span>
    
- <span data-ttu-id="6bd12-129">**Enable** (défini sur false par défaut)</span><span class="sxs-lookup"><span data-stu-id="6bd12-129">**Enable** (set to False by default)</span></span> 
    
- <span data-ttu-id="6bd12-130">**Description**</span><span class="sxs-lookup"><span data-stu-id="6bd12-130">**Description**</span></span>
    
<span data-ttu-id="6bd12-131">Les exemples suivants montrent comment créer des définitions de FDU.</span><span class="sxs-lookup"><span data-stu-id="6bd12-131">The following examples show how create the UDF definitions.</span></span>
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
<span data-ttu-id="6bd12-132">Après avoir créé la nouvelle référence UDF, exécutez **IISReset** sur le serveur pour extraire immédiatement la référence.</span><span class="sxs-lookup"><span data-stu-id="6bd12-132">After you create the new UDF reference, run **iisreset** on the server to pick up the reference immediately.</span></span> 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a><span data-ttu-id="6bd12-133">Commandes supplémentaires de Windows PowerShell Office Online Server UDF</span><span class="sxs-lookup"><span data-stu-id="6bd12-133">Additional Office Online Server UDF Windows PowerShell commands</span></span>

<span data-ttu-id="6bd12-134">Utilisez les applets de commande Windows PowerShell suivantes pour utiliser les fonctions définies par l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="6bd12-134">Use the following Windows PowerShell cmdlets to work with UDFs:</span></span>
  
- <span data-ttu-id="6bd12-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (pas de paramètres obligatoires) : renvoie la liste des définitions UDF qui sont configurées sur le serveur Office Online.</span><span class="sxs-lookup"><span data-stu-id="6bd12-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (no required parameters) - Returns a list of UDF definitions that are configured on the Office Online Server.</span></span> 
    
- <span data-ttu-id="6bd12-136">**Set-OfficeWebAppsExcelUserDefinedFunction** (paramètre Identity requis)-définit les propriétés sur les définitions UDF existantes.</span><span class="sxs-lookup"><span data-stu-id="6bd12-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Sets properties on existing UDF definitions.</span></span> 
    
- <span data-ttu-id="6bd12-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (paramètre Identity requis)-supprime les définitions UDF existantes.</span><span class="sxs-lookup"><span data-stu-id="6bd12-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Removes existing UDF definitions.</span></span> 
    
## <a name="udf-sample"></a><span data-ttu-id="6bd12-138">Exemple de FDU</span><span class="sxs-lookup"><span data-stu-id="6bd12-138">UDF sample</span></span>

<span data-ttu-id="6bd12-139">L’exemple de fichier suivant fournit un exemple de classeur qui utilise une FDU et la FDU binaire :</span><span class="sxs-lookup"><span data-stu-id="6bd12-139">The following sample file provide a sample workbook that uses a UDF and the UDF binary:</span></span>
  
- <span data-ttu-id="6bd12-140">[BooleanDataType. xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): exemple de classeur qui utilise une FDU</span><span class="sxs-lookup"><span data-stu-id="6bd12-140">[BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): a sample workbook that uses a UDF</span></span>  
    
## <a name="see-also"></a><span data-ttu-id="6bd12-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bd12-141">See also</span></span>

- [<span data-ttu-id="6bd12-142">Configurer les paramètres d’administration d’Excel Online</span><span class="sxs-lookup"><span data-stu-id="6bd12-142">Configure Excel Online administrative settings</span></span>](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [<span data-ttu-id="6bd12-143">Office Online Server</span><span class="sxs-lookup"><span data-stu-id="6bd12-143">Office Online Server</span></span>](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

