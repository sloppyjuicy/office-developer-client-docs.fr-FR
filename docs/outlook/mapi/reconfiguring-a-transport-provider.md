---
title: Reconfiguration d’un fournisseur de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
ms.openlocfilehash: 897d05980fc55c2777176328bc0774faccba4609
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63377672"
---
# <a name="reconfiguring-a-transport-provider"></a>Reconfiguration d’un fournisseur de transport

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Vous pouvez utiliser l’objet d’état d’un fournisseur de transport pour modifier certaines propriétés du fournisseur. La plage de propriétés qui peut être modifiée dépend des propriétés incluses dans la feuille des propriétés du fournisseur et de la façon dont ces propriétés sont définies. 
  
 **Pour reconfigurer un fournisseur de transport actif**
  
1. [Appelez IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d’état. 
    
2. Recherchez la ligne du fournisseur de transport à reconfigurer en créant une restriction de propriété qui correspond à **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) avec le nom du fournisseur cible. 
    
3. [Appelez IMAPITable::FindRow](imapitable-findrow.md) pour récupérer la ligne appropriée. 
    
4. Vérifiez que les indicateurs STATUS_SETTINGS_DIALOG et STATUS_VALIDATE_STATE sont définies dans la propriété **PR_RESOURCE_METHODS (**[PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) du fournisseur de transport cible. Si STATUS_SETTINGS_DIALOG n’est pas définie, le fournisseur de transport n’affiche pas de feuille des propriétés de configuration. Si STATUS_VALIDATE_STATE n’est pas définie, vous ne pouvez pas effectuer de reconfiguration dynamique.
    
5. Si STATUS_SETTINGS_DIALOG est définie, appelez [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) pour afficher la feuille des propriétés du fournisseur de transport et permettre à l’utilisateur d’apporter des modifications. 
    
6. Une fois que l’utilisateur a terminé la reconfiguration, appelez [IMAPIStatus::ValidateState](imapistatus-validatestate.md) si STATUS_VALIDATE_STATE est définie, en passant CONFIG_CHANGED. 
    

