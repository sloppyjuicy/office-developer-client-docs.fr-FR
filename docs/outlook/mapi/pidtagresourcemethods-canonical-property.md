---
title: Propriété canonique PidTagResourceMethods
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceMethods
api_type:
- COM
ms.assetid: 60ebbcd5-b758-4c96-b8ec-089e0aae1a5f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e9aee3280edbed60e97ef6e00e61f3086f6f07ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330141"
---
# <a name="pidtagresourcemethods-canonical-property"></a>Propriété canonique PidTagResourceMethods

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de réindicateur des indicateurs qui indiquent les méthodes de l'interface **IMAPIStatus** qui sont prises en charge par l'objet Status. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RESOURCE_METHODS  <br/> |
|Identificateur :  <br/> |0x3E02  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété indique quelles méthodes de l'implémentation d'un objet d'état de **IMAPIStatus** sont prises en charge. Les objets d'État sont autorisés à renvoyer MAPI_E_NO_SUPPORT à partir de méthodes non prises en charge. 
  
Les clients utilisent la propriété **PR_RESOURCE_METHODS** d'un objet Status pour éviter d'appeler des méthodes non prises en charge. Si l'indicateur correspondant à une méthode particulière est défini, la méthode existe et peut être appelée. Si cet indicateur est clair, la méthode ne doit pas être appelée. 
  
Les objets d'État implémentés par MAPI prennent en charge les méthodes suivantes:
  
|**Objet Status**|**Méthodes prises en charge**|
|:-----|:-----|
|Sous-système MAPI  <br/> |**ValidateState** uniquement  <br/> |
|Carnet d'adresses MAPI  <br/> |**ValidateState** uniquement  <br/> |
|Spouleur MAPI  <br/> |**ValidateState** et **FlushQueues** <br/> |
   
Un ou plusieurs des indicateurs suivants peuvent être définis dans **PR_RESOURCE_METHODS**:
  
STATUS_CHANGE_PASSWORD 
  
> Indique que la méthode [IMAPIStatus:: ChangePassword](imapistatus-changepassword.md) est prise en charge. 
    
STATUS_FLUSH_QUEUES 
  
> Indique que la méthode [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) est prise en charge. 
    
STATUS_SETTINGS_DIALOG 
  
> Indique que la méthode [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) est prise en charge. 
    
STATUS_VALIDATE_STATE 
  
> Indique que la méthode [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) est prise en charge. 
    
## <a name="related-resources"></a>Ressources associées

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

