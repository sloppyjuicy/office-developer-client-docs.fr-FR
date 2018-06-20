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
ms.openlocfilehash: f346baf303db9da765eec183d168b370547ec2de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786588"
---
# <a name="pidtagresourcemethods-canonical-property"></a>Propriété canonique PidTagResourceMethods

  
  
**S’applique à**: Outlook 
  
Contient un masque binaire composé des indicateurs qui influencent les méthodes de l’interface **IMAPIStatus** qui sont prises en charge par l’objet d’état. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RESOURCE_METHODS  <br/> |
|Identificateur :  <br/> |0x3E02  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |État MAPI  <br/> |
   
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
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

