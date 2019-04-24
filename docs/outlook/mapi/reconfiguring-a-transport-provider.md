---
title: Reconfiguration d'un fournisseur de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: b35ca2bb52439cf2ba1750c6fad2883730c4c3f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328412"
---
# <a name="reconfiguring-a-transport-provider"></a>Reconfiguration d'un fournisseur de transport

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Vous pouvez utiliser l'objet d'état d'un fournisseur de transport pour modifier certaines des propriétés du fournisseur. La plage de propriétés qui peut être modifiée dépend des propriétés incluses dans la feuille des propriétés du fournisseur et de la façon dont ces propriétés sont définies. 
  
 **Pour reconfigurer un fournisseur de transport actif**
  
1. Appelez [IMAPISession:: GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d'État. 
    
2. Localisez la ligne du fournisseur de transport qui doit être reconfigurée en créant une restriction de propriété qui correspond à **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) avec le nom du fournisseur cible. 
    
3. Appelez [IMAPITable:: FindRow](imapitable-findrow.md) pour récupérer la ligne appropriée. 
    
4. Vérifiez que les indicateurs STATUS_SETTINGS_DIALOG et STATUS_VALIDATE_STATE sont définis dans la propriété **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) du fournisseur de transport cible. Si STATUS_SETTINGS_DIALOG n'est pas défini, le fournisseur de transport n'affiche pas de feuille de propriétés de configuration. Si STATUS_VALIDATE_STATE n'est pas défini, vous ne pouvez pas effectuer une reconfiguration dynamique.
    
5. Si STATUS_SETTINGS_DIALOG est défini, appelez [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) pour afficher la feuille de propriétés du fournisseur de transport et permettre à l'utilisateur d'effectuer des modifications. 
    
6. Une fois que l'utilisateur a terminé la reconfiguration, appelez [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) si STATUS_VALIDATE_STATE est défini, en passant CONFIG_CHANGED. 
    

