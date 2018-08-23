---
title: Installation du sous-système MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: adb4d09ccce95683ac46e7b271fafa328b1a9f97
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575349"
---
# <a name="installing-the-mapi-subsystem"></a>Installation du sous-système MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Versions prises en charge de Windows installent la bibliothèque stub MAPI, Mapi32.dll, dans le _ \<lecteur\>_ dossier \Windows\System32. 
  
Les versions de Windows prises en charge sont les suivantes :
  
- Windows 7.
    
- Windows Vista.
    
- Windows Server 2008.
    
- Windows Server 2003.
    
- Windows XP.
    
Pour installer correctement le sous-système MAPI, installer une application qui contient un sous-système basées sur MAPI, tel que Microsoft Outlook.
  
Vous trouverez plus d’informations sur l’installation du sous-système MAPI d’un ordinateur dans le Registre système. Toutes les valeurs dans les entrées de Registre sont des chaînes de caractères. 
  
Programmes d’installation de service de message sont chargés de créer les informations d’installation dans la clé de Registre système suivantes : 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
Services de messagerie doivent ajouter des entrées dans le Registre système. 
  
Le tableau suivant résume comment les clients récupèrent les informations de version pour le sous-système MAPI sur leur ordinateur.
  
|**Pour vérifier**|**Dans le Registre**|
|:-----|:-----|
|Disponibilité de MAPI  <br/> |Recherchez `MAPIX=1`.  <br/> |
|Version de MAPI  <br/> |Rechercher une chaîne MAPIXVER sous la forme « _x.x.x_».  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Vue d'ensemble de la programmation MAPI](mapi-programming-overview.md)

