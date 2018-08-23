---
title: Configurer des UDF dans Excel Online dans Office Server Online Preview
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Utilisez les fonctions définies par l’utilisateur (UDF) dans Excel Online dans Office Online Server Preview pour appeler des fonctions personnalisées.
ms.openlocfilehash: 12f452241754be1b4b1e545c69225aed055f4965
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590181"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server-preview"></a>Configurer des UDF dans Excel Online dans Office Server Online Preview

[Cette rubrique est une documentation préliminaire et sujette à modification dans les versions futures.] Utilisez les fonctions définies par l’utilisateur (UDF) dans Excel Online dans Office Online Server Preview pour appeler des fonctions personnalisées. 
  
Fonctions définies par l’utilisateur (UDF) dans Excel Online permettent d’appeler des fonctions personnalisées écrites en code managé à l’aide de formules dans les cellules. Vous pouvez utiliser l’appel des UDF :
  
- Call custom mathematical functions.
    
- Get data from custom data sources into worksheets.
    
- Appeler des services web.
    
Vous pouvez installer les fichiers binaires UDF dans un des deux emplacements :
  
- Un répertoire local. Par exemple : 
    
    C:\UDFs\MySampleUdf.dll 
    
- Le global assembly cache. Par exemple : 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
Référence de l’emplacement lorsque vous créez une définition de **New-OfficeWebAppsExcelUserDefinedFunction** sur Office Online Server Preview. 
  
> [!NOTE]
> Office Online Server Preview ne gère pas les UDF situés sur des partages réseau. 
  
## <a name="enable-udfs-on-office-online-server-preview"></a>Activer les UDF sur Office Online Server Preview

Lorsqu’un administrateur crée une nouvelle batterie de serveurs Office Web Apps Server à l’aide de l’applet de commande [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell, les assemblys UDF sont désactivés par défaut. La valeur par défaut de l’indicateur **ExcelUdfsAllowed** a la valeur false. 
  
Pour activer les UDF, exécutez la commande Windows PowerShell suivante sur Office Online Server Preview, une fois que la batterie de serveurs Office Web Apps Server a été créé.
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server-preview"></a>Créer des définitions de fonctions UDF sur Office Online Server Preview

Une fois que vous activez UDF, vous devez créer une définition pour le fichier binaire qui contient l’UDF. Pour créer une définition pour votre UDF binaire sur Office Online Server Preview, utilisez l’applet de commande **New-OfficeWebAppsExcelUserDefinedFunction** . Cette applet de commande inclut les paramètres suivants : 
  
- **Assembly**
    
- **AssemblyLocation**
    
- **Activer** (la valeur False par défaut) 
    
- **Description**
    
Les exemples suivants montrent comment créer les définitions de fonctions UDF.
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
Après avoir créé la nouvelle référence UDF, exécutez **iisreset** sur le serveur pour identifier les immédiatement la référence. 
  
## <a name="additional-office-online-server-preview-udf-windows-powershell-commands"></a>Commandes Office Online Server Preview UDF Windows PowerShell

Utiliser les applets de commande Windows PowerShell suivante pour travailler avec UDF :
  
- **Get-OfficeWebAppsExcelUserDefinedFunction** (aucun paramètre requis -) renvoie une liste de définitions de fonctions UDF sont configurés sur Office Online Server Preview. 
    
- **Set-OfficeWebAppsExcelUserDefinedFunction** (Paramètre identity requis) - définit les propriétés de définitions de fonctions UDF existantes. 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (Paramètre identity requis) - supprime les définitions de fonctions UDF existantes. 
    
## <a name="udf-sample"></a>Exemple de fichier UDF

Les fichiers suivants fournissent un exemple de classeur qui utilise un fichier UDF et le fichier UDF binaires :
  
- [BooleanDataType.xlsx](http://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx) --un exemple de classeur qui utilise un fichier UDF  
- [EcsUdfsCommonSet.dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll) --le fichier binaire UDF 
    
## <a name="see-also"></a>Voir aussi

- [Configurer les paramètres d’administration Excel Online](https://docs.microsoft.com/en-us/officeonlineserver/configure-excel-online-administrative-settings)  
- [Office Online Server](https://docs.microsoft.com/en-us/officeonlineserver/office-online-server)
    

