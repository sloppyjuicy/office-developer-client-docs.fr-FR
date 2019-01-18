---
title: Configurer des UDF dans Excel Online dans Office Server en ligne
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Utilisez les fonctions définies par l’utilisateur (UDF) dans Excel Online dans Office Online Server pour appeler des fonctions personnalisées.
ms.openlocfilehash: dbba60a62a1a4783b47c3f1fe40a118dd8ed0d6d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722787"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a>Configurer des UDF dans Excel Online dans Office Server en ligne

Utilisez les fonctions définies par l’utilisateur (UDF) dans Excel Online dans Office Online Server pour appeler des fonctions personnalisées. 
  
Fonctions définies par l’utilisateur (UDF) dans Excel Online permettent d’appeler des fonctions personnalisées écrites en code managé à l’aide de formules dans les cellules. Vous pouvez utiliser l’appel des UDF :
  
- Call custom mathematical functions.
    
- Get data from custom data sources into worksheets.
    
- Appeler des services web.
    
Vous pouvez installer les fichiers binaires UDF dans un des deux emplacements :
  
- Un répertoire local. Par exemple: 
    
    C:\UDFs\MySampleUdf.dll 
    
- Le global assembly cache. Par exemple: 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
Référence de l’emplacement lorsque vous créez une définition de **New-OfficeWebAppsExcelUserDefinedFunction** sur le serveur en ligne. 
  
> [!NOTE]
> Office Online Server ne gère pas les UDF situés sur des partages réseau. 
  
## <a name="enable-udfs-on-office-online-server"></a>Activer les UDF sur Office Online serveur 

Lorsqu’un administrateur crée une nouvelle batterie de serveurs Office Web Apps Server à l’aide de l’applet de commande [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell, les assemblys UDF sont désactivés par défaut. La valeur par défaut de l’indicateur **ExcelUdfsAllowed** a la valeur false. 
  
Pour activer les UDF, exécutez la commande Windows PowerShell suivante sur le serveur en ligne Office, une fois que la batterie de serveurs Office Web Apps Server a été créé.
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a>Créer des définitions de fonctions UDF sur Office Online Server

Une fois que vous activez UDF, vous devez créer une définition pour le fichier binaire qui contient l’UDF. Pour créer une définition pour votre UDF binaires sur le serveur en ligne, utilisez l’applet de commande **New-OfficeWebAppsExcelUserDefinedFunction** . Cette applet de commande inclut les paramètres suivants : 
  
- **Assembly**
    
- **AssemblyLocation**
    
- **Activer** (la valeur False par défaut) 
    
- **Description**
    
Les exemples suivants montrent comment créer les définitions de fonctions UDF.
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
Après avoir créé la nouvelle référence UDF, exécutez **iisreset** sur le serveur pour identifier les immédiatement la référence. 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a>Commandes Office Online Server UDF Windows PowerShell

Utiliser les applets de commande Windows PowerShell suivante pour travailler avec UDF :
  
- **Get-OfficeWebAppsExcelUserDefinedFunction** (aucun paramètre requis -) renvoie une liste de définitions de fonctions UDF sont configurés sur le serveur en ligne. 
    
- **Set-OfficeWebAppsExcelUserDefinedFunction** (Paramètre identity requis) - définit les propriétés de définitions de fonctions UDF existantes. 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (Paramètre identity requis) - supprime les définitions de fonctions UDF existantes. 
    
## <a name="udf-sample"></a>Exemple de fichier UDF

Les fichiers suivants fournissent un exemple de classeur qui utilise un fichier UDF et le fichier UDF binaires :
  
- [BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): un exemple de classeur qui utilise un fichier UDF  
- [EcsUdfsCommonSet.dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): le fichier binaire UDF 
    
## <a name="see-also"></a>Voir aussi

- [Configurer les paramètres d’administration Excel Online](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [Office Online Server](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

