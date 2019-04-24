---
title: Configurer des fichiers UDF dans Excel Online dans Office Online Server
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Utilisez des fonctions définies par l'utilisateur dans Excel Online dans Office Online Server pour appeler des fonctions personnalisées.
ms.openlocfilehash: dbba60a62a1a4783b47c3f1fe40a118dd8ed0d6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311059"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a>Configurer des fichiers UDF dans Excel Online dans Office Online Server

Utilisez des fonctions définies par l'utilisateur dans Excel Online dans Office Online Server pour appeler des fonctions personnalisées. 
  
Les fonctions définies par l'utilisateur dans Excel Online vous permettent d'appeler des fonctions personnalisées écrites en code managé à l'aide de formules dans les cellules. Vous pouvez utiliser des FDU pour:
  
- Call custom mathematical functions.
    
- Get data from custom data sources into worksheets.
    
- Appeler des services Web.
    
Vous pouvez installer les fichiers binaires UDF à l'un des deux emplacements suivants:
  
- Un répertoire local. Par exemple : 
    
    C:\UDFs\MySampleUdf.dll
    
- Le global assembly cache. Par exemple : 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
Référencez l'emplacement lorsque vous créez une définition **OfficeWebAppsExcelUserDefinedFunction** sur le serveur Office Online. 
  
> [!NOTE]
> Office Online Server ne prend pas en charge les fonctions définies par l'utilisateur sur les partages réseau. 
  
## <a name="enable-udfs-on-office-online-server"></a>Activer les fonctions UDF sur Office Online Server 

Lorsqu'un administrateur crée une batterie Office Web Apps Server à l'aide de la cmdlet Windows PowerShell [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) , les assemblys UDF sont désactivés par défaut. La valeur par défaut de l'indicateur **ExcelUdfsAllowed** est false. 
  
Pour activer les fonctions définies par l'utilisateur, exécutez la commande Windows PowerShell suivante sur le serveur Office Online, une fois la batterie de serveurs Office Web Apps Server créée.
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a>Créer des définitions de FDU sur Office Online Server

Une fois que vous avez activé les FDU, vous devez créer une définition pour le fichier binaire contenant les FDU. Pour créer une définition pour votre fichier binaire UDF sur le serveur Office Online, utilisez la cmdlet **New-OfficeWebAppsExcelUserDefinedFunction** . Cette applet de commande inclut les paramètres suivants: 
  
- **Assembly**
    
- **AssemblyLocation**
    
- **Activer** (défini sur false par défaut) 
    
- **Description**
    
Les exemples suivants montrent comment créer des définitions de FDU.
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
Après avoir créé la nouvelle référence UDF, exécutez **IISReset** sur le serveur pour extraire immédiatement la référence. 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a>Commandes supplémentaires de Windows PowerShell Office Online Server UDF

Utilisez les applets de commande Windows PowerShell suivantes pour utiliser les fonctions définies par l'utilisateur:
  
- **Get-OfficeWebAppsExcelUserDefinedFunction** (aucun paramètre obligatoire): renvoie la liste des définitions UDF qui sont configurées sur le serveur Office Online. 
    
- **Set-OfficeWebAppsExcelUserDefinedFunction** (Paramètre Identity requis): définit les propriétés sur les définitions UDF existantes. 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (Paramètre Identity requis): supprime les définitions UDF existantes. 
    
## <a name="udf-sample"></a>Exemple de FDU

Les fichiers suivants fournissent un exemple de classeur qui utilise une FDU et la FDU binaire:
  
- [BooleanDataType. xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): exemple de classeur qui utilise une FDU  
- [EcsUdfsCommonSet. dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): fichier binaire UDF 
    
## <a name="see-also"></a>Voir aussi

- [Configurer les paramètres d’administration d’Excel Online](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [Office Online Server](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

