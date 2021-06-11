---
title: Configurer des UDF dans Excel Online dans Office Online Server
manager: lindalu
ms.date: 12/03/2019
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Utilisez des fonctions définies par l’utilisateur (UDF) dans Excel Online Office Online Server pour appeler des fonctions personnalisées.
ms.openlocfilehash: e1b005079c03ae3028ba6bf9ee1156c6ae2eae80
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2020
ms.locfileid: "43102932"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a>Configurer des UDF dans Excel Online dans Office Online Server

Utilisez des fonctions définies par l’utilisateur (UDF) dans Excel Online Office Online Server pour appeler des fonctions personnalisées. 
  
Les fonctions définies par l’utilisateur dans Excel Online vous permettent d’appeler des fonctions personnalisées écrites en code géré à l’aide de formules dans les cellules. Vous pouvez utiliser des UDF pour :
  
- Call custom mathematical functions.
    
- Get data from custom data sources into worksheets.
    
- Appeler des services web.
    
Vous pouvez installer des binaires UDF dans l’un des deux emplacements :
  
- Répertoire local. Par exemple : 
    
    C:\UDFs\MySampleUdf.dll
    
- Global Assembly Cache. Par exemple : 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
Référencez l’emplacement lorsque vous créez une **définition New-OfficeWebAppsExcelUserDefinedFunction** sur le Office Online Server. 
  
> [!NOTE]
> Office Online Server ne prend pas en charge les UDF situées sur des partages réseau. 
  
## <a name="enable-udfs-on-office-online-server"></a>Activer les UDF sur Office Online Server 

Lorsqu’un administrateur crée une batterie Office Web Apps Server à l’aide de la cmdlet [New-OfficeWebAppsFarm](https://docs.microsoft.com/powershell/module/officewebapps/new-officewebappsfarm?view=officewebapps-ps) Windows PowerShell, les assemblys UDF sont désactivés par défaut. La valeur par défaut de **l’indicateur ExcelUdfsAllowed** est false. 
  
Pour activer les UDF, exécutez la commande Windows PowerShell suivante sur la Office Online Server, une fois la batterie Office Web Apps Server créée.
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a>Créer des définitions UDF sur Office Online Server

Après avoir activé les UDF, vous devez créer une définition pour le fichier binaire qui contient les UDF. Pour créer une définition pour votre fichier binaire UDF sur le Office Online Server, utilisez la cmdlet **New-OfficeWebAppsExcelUserDefinedFunction.** Cette cmdlet inclut les paramètres suivants : 
  
- **Assembly**
    
- **AssemblyLocation**
    
- **Activer** (définie sur False par défaut) 
    
- **Description**
    
Les exemples suivants montrent comment créer les définitions UDF.
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
Après avoir créé la référence UDF, exécutez **iisreset** sur le serveur pour récupérer la référence immédiatement. 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a>Autres Office Online Server commandes de Windows PowerShell UDF

Utilisez les cmdlets Windows PowerShell suivantes pour utiliser les UDF :
  
- **Get-OfficeWebAppsExcelUserDefinedFunction** (aucun paramètre requis) : renvoie la liste des définitions UDF configurées sur le Office Online Server. 
    
- **Set- OfficeWebAppsExcelUserDefinedFunction** (paramètre d’identité obligatoire) : définit les propriétés sur les définitions UDF existantes. 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (paramètre d’identité obligatoire) : supprime les définitions UDF existantes. 
    
## <a name="udf-sample"></a>Exemple UDF

L’exemple de fichier suivant fournit un exemple de classer qui utilise une UDF et le fichier binaire UDF :
  
- [BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): exemple de workbook qui utilise une UDF  
    
## <a name="see-also"></a>Voir aussi

- [Configurer les paramètres d’administration d’Excel Online](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [Office Online Server](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

