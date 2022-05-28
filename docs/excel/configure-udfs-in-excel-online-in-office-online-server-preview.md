---
title: Configurer des fonctions définies par l’utilisateur dans Excel Online dans Office Online Server
manager: lindalu
ms.date: 12/03/2019
ms.audience: ITPro
ms.localizationpriority: medium
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Utilisez des fonctions définies par l’utilisateur dans Excel Online dans Office Online Server pour appeler des fonctions personnalisées.
ms.openlocfilehash: 746a7194defdf25c3e401c1056b5f118c96f2323
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65769577"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a>Configurer des fonctions définies par l’utilisateur dans Excel Online dans Office Online Server

Utilisez des fonctions définies par l’utilisateur dans Excel Online dans Office Online Server pour appeler des fonctions personnalisées. 
  
Les fonctions définies par l’utilisateur dans Excel Online vous permettent d’appeler des fonctions personnalisées écrites en code managé à l’aide de formules dans des cellules. Vous pouvez utiliser des fonctions définies par l’utilisateur pour :
  
- Call custom mathematical functions.
    
- Get data from custom data sources into worksheets.
    
- Appeler des services web.
    
Vous pouvez installer des fichiers binaires UDF dans l’un des deux emplacements suivants :
  
- Répertoire local. Par exemple : 
    
    C:\UDFs\MySampleUdf.dll
    
- Cache d’assembly global. Par exemple : 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
Référencez l’emplacement lorsque vous **créez une définition New-OfficeWebAppsExcelUserDefinedFunction** sur le Office Online Server. 
  
> [!NOTE]
> Office Online Server ne prend pas en charge les fonctions définies par l’utilisateur situées sur des partages réseau. 
  
## <a name="enable-udfs-on-office-online-server"></a>Activer les fonctions définies par l’utilisateur sur Office Online Server 

Lorsqu’un administrateur crée une batterie de serveurs Office Web Apps à l’aide de l’applet de commande [New-OfficeWebAppsFarm](/powershell/module/officewebapps/new-officewebappsfarm) Windows PowerShell, les assemblys UDF sont désactivés par défaut. La valeur par défaut de l’indicateur **ExcelUdfsAllowed** est false. 
  
Pour activer les fonctions définies par l’utilisateur, exécutez la commande Windows PowerShell suivante sur le Office Online Server, une fois la batterie de serveurs Office Web Apps créée.
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a>Créer des définitions UDF sur Office Online Server

Une fois que vous avez activé les fonctions définies par l’utilisateur, vous devez créer une définition pour le binaire qui contient les fonctions définies par l’utilisateur. Pour créer une définition pour votre fichier binaire UDF sur le Office Online Server, utilisez l’applet de commande **New-OfficeWebAppsExcelUserDefinedFunction**. Cette applet de commande inclut les paramètres suivants : 
  
- **Assembly**
    
- **AssemblyLocation**
    
- **Activer** (défini sur False par défaut) 
    
- **Description**
    
Les exemples suivants montrent comment créer les définitions UDF.
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
Après avoir créé la référence UDF, exécutez **iisreset** sur le serveur pour récupérer la référence immédiatement. 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a>Commandes de Windows PowerShell UDF Office Online Server supplémentaires

Utilisez les applets de commande Windows PowerShell suivantes pour utiliser des fonctions définies par l’utilisateur :
  
- **Get-OfficeWebAppsExcelUserDefinedFunction** (aucun paramètre obligatoire) : retourne une liste de définitions UDF configurées sur le Office Online Server. 
    
- **Set- OfficeWebAppsExcelUserDefinedFunction** (paramètre d’identité requis) : définit des propriétés sur les définitions UDF existantes. 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (paramètre d’identité requis) : supprime les définitions UDF existantes. 
    
## <a name="udf-sample"></a>Exemple de fonction définie par l’utilisateur

L’exemple de fichier suivant fournit un exemple de classeur qui utilise une fonction UDF et le fichier binaire UDF :
  
- [BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): exemple de classeur qui utilise une fonction UDF  
    
## <a name="see-also"></a>Voir aussi

- [Configurer les paramètres d’administration d’Excel Online](/officeonlineserver/configure-excel-online-administrative-settings)  
- [Office Online Server](/officeonlineserver/office-online-server)
    

