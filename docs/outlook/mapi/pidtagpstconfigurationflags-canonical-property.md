---
title: Propriété canonique PidTagPstConfigurationFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: e4234ddf-d9dc-4dc9-8eda-dbbee151b5d7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e881c8eeffa29706591e07113d70a3670606f2be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408942"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a>Propriété canonique PidTagPstConfigurationFlags
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifications des indicateurs de configuration pour une table de stockage personnel (fichier .pst).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PST_CONFIG_FLAGS  <br/> |
|Identificateur :  <br/> |0x6770  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Table de stockage personnel (.pst) interne  <br/> |
   
## <a name="remarks"></a>Remarques

Les valeurs valides pour cette propriété sont les suivantes :
  
PST_CONFIG_UNICODE
  
> Indique un fichier .pst Unicode. 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
PST_CONFIG_CREATE_NOWARN
  
> Lorsqu’il est configuré à partir des indicateurs clients vers la méthode [IMsgServiceAdmin::ConfigureMsgService,](imsgserviceadmin-configuremsgservice.md) **configureMsgService** est traité comme un appel [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) et ignore l’avertissement « Ce service d’information n’a pas été configuré ». 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
PST_CONFIG_PRESERVE_DISPLAY_NAME
  
> Indique **à ConfigureMsgService** de ne pas modifier la valeur de la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), même si elle a été fournie. Dans ce cas, il a été fourni uniquement pour les nouveaux fichiers .pst.
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
OST_CONFIG_POLICY_DELAY_IGNORE_OST
  
> Indique au code de configuration d’afficher d’abord une boîte de dialogue pour confirmer si un fichier de dossier hors connexion (.ost) a été trouvé et, selon la réponse de l’utilisateur, utiliser le dossier hors connexion trouvé ou permettre à l’utilisateur de rechercher un autre dossier hors connexion.
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
OST_CONFIG_CREATE_NEW_DEFAULT
  
> Copie le fichier .ost avec un nouveau nom unique et rejette le nom actuel. Le fichier .ost existant reste sur l’ordinateur, mais n’est plus utilisé dans ce profil. Cela se produit généralement lorsque Microsoft Outlook n’autorise plus un fichier .ost particulier et que les stratégies de Registre n’autorisent pas l’utilisateur à renommer le fichier. 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]] 
  
> Fournit des références aux spécifications Exchange Server protocole.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

