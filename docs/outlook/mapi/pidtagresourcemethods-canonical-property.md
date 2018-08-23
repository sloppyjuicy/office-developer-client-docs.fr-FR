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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 2e1cff8148815c3e03b92e4d57d1c6a303943c9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578163"
---
# <a name="pidtagresourcemethods-canonical-property"></a>Propriété canonique PidTagResourceMethods

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un masque binaire composé des indicateurs qui influencent les méthodes de l’interface **IMAPIStatus** qui sont prises en charge par l’objet d’état. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RESOURCE_METHODS  <br/> |
|Identificateur :  <br/> |0x3E02  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété indique parmi les méthodes de mise en œuvre d’un objet d’état de **IMAPIStatus** sont pris en charge. Objets d’état sont autorisés à renvoyer MAPI_E_NO_SUPPORT à partir de méthodes non prises en charge. 
  
Clients utilisent état **PR_RESOURCE_METHODS** propriété d’un objet pour éviter d’effectuer des appels aux méthodes non prises en charge. Si l’indicateur qui correspond à une méthode particulière est défini, la méthode existe et peut être appelée. Si cet indicateur est désactivée, la méthode ne doit pas être appelée. 
  
Les objets état implémentée par prise en charge MAPI les méthodes suivantes :
  
|**Objet d’état**|**Méthodes prises en charge**|
|:-----|:-----|
|Sous-système MAPI  <br/> |**ValidateState**  <br/> |
|Carnet d’adresses MAPI  <br/> |**ValidateState**  <br/> |
|Spouleur MAPI  <br/> |**ValidateState** et **FlushQueues** <br/> |
   
Un ou plusieurs des indicateurs suivants peuvent être définie dans **PR_RESOURCE_METHODS**:
  
STATUS_CHANGE_PASSWORD 
  
> Indique que la méthode [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) est pris en charge. 
    
STATUS_FLUSH_QUEUES 
  
> Indique que la méthode [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) est pris en charge. 
    
STATUS_SETTINGS_DIALOG 
  
> Indique que la méthode [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) est pris en charge. 
    
STATUS_VALIDATE_STATE 
  
> Indique que la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) est pris en charge. 
    
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

