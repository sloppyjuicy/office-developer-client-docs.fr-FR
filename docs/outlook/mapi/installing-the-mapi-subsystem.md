---
title: Installation du sous-système MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c2e135fc031dd3faf5a4e08c50147dfcf7787b5e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784316"
---
# <a name="installing-the-mapi-subsystem"></a>Installation du sous-système MAPI

  
  
**S’applique à**: Outlook 
  
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

