---
title: Reconfiguration d’un fournisseur de Transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: ec5a431d04799e3f19c23dd0437aeac13fbf0968
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786974"
---
# <a name="reconfiguring-a-transport-provider"></a>Reconfiguration d’un fournisseur de Transport

  
  
**S’applique à**: Outlook 
  
Vous pouvez utiliser l’objet d’état d’un fournisseur de transport pour modifier certaines des propriétés du fournisseur. La plage de propriétés qui peuvent être modifiées dépend des propriétés qui sont incluses dans la feuille des propriétés du fournisseur et la façon dont ces propriétés sont définies. 
  
 **Pour reconfigurer un fournisseur de transport actif**
  
1. Appelez [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d’état. 
    
2. Recherchez la ligne pour le fournisseur de transport pour être reconfigurée en créant une restriction de propriété qui correspond à **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) avec le nom du fournisseur cible. 
    
3. Appel [IMAPITable::FindRow](imapitable-findrow.md) pour récupérer la ligne adéquate. 
    
4. Vérifiez que les indicateurs STATUS_SETTINGS_DIALOG et STATUS_VALIDATE_STATE sont définis dans la propriété de **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) du fournisseur de transport cible. Si STATUS_SETTINGS_DIALOG n’est pas défini, le fournisseur de transport n’affiche pas une feuille de propriétés de configuration. Si STATUS_VALIDATE_STATE n’est pas définie, vous ne pouvez pas effectuer de reconfiguration dynamique.
    
5. Si STATUS_SETTINGS_DIALOG est défini, appelez [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) pour afficher la feuille des propriétés du fournisseur de transport et autoriser l’utilisateur à modifier. 
    
6. Une fois que l’utilisateur a terminé la reconfiguration, appelez [IMAPIStatus::ValidateState](imapistatus-validatestate.md) si STATUS_VALIDATE_STATE est défini, en transmettant CONFIG_CHANGED. 
    

