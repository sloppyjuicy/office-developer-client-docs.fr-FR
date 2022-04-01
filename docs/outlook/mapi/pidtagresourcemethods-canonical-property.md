---
title: Propriété canonique PidTagResourceMethods
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagResourceMethods
api_type:
- COM
ms.assetid: 60ebbcd5-b758-4c96-b8ec-089e0aae1a5f
description: Contient un masque de bits d’indicateurs qui indiquent les méthodes dans l’interface IMAPIStatus qui sont pris en charge par l’objet d’état.
ms.openlocfilehash: aac27ed6a6569c79110efde04f299ecd176b455d
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524497"
---
# <a name="pidtagresourcemethods-canonical-property"></a>Propriété canonique PidTagResourceMethods

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de bits d’indicateurs qui indiquent les méthodes dans l’interface **IMAPIStatus** qui sont pris en charge par l’objet d’état. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RESOURCE_METHODS  <br/> |
|Identificateur :  <br/> |0x3E02  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété indique quelles méthodes de l’implémentation **d’IMAPIStatus** d’un objet d’état sont pris en charge. Les objets d’état sont autorisés à renvoyer MAPI_E_NO_SUPPORT des méthodes non pris en MAPI_E_NO_SUPPORT' 
  
Les clients utilisent la propriété **PR_RESOURCE_METHODS d’un** objet d’état pour éviter d’effectuer des appels à des méthodes non pris en compte. Si l’indicateur qui correspond à une méthode particulière est définie, la méthode existe et peut être appelée. Si cet indicateur est clair, la méthode ne doit pas être appelée. 
  
Les objets d’état implémentés par MAPI prise en charge les méthodes suivantes :
  
|**Objet Status**|**Méthodes prise en charge**|
|:-----|:-----|
|Sous-système MAPI  <br/> |**ValidateState** uniquement  <br/> |
|Carnet d’adresses MAPI  <br/> |**ValidateState** uniquement  <br/> |
|Pooler MAPI  <br/> |**ValidateState** et **FlushQueues** <br/> |
   
Un ou plusieurs des indicateurs suivants peuvent être **PR_RESOURCE_METHODS :**
  
STATUS_CHANGE_PASSWORD 
  
> Indique que la [méthode IMAPIStatus::ChangePassword](imapistatus-changepassword.md) est prise en charge. 
    
STATUS_FLUSH_QUEUES 
  
> Indique que la [méthode IMAPIStatus::FlushQueues est](imapistatus-flushqueues.md) prise en charge. 
    
STATUS_SETTINGS_DIALOG 
  
> Indique que la [méthode IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) est prise en charge. 
    
STATUS_VALIDATE_STATE 
  
> Indique que la [méthode IMAPIStatus::ValidateState](imapistatus-validatestate.md) est prise en charge. 
    
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

