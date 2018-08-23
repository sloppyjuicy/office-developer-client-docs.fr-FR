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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b79b40a59a2bf7b68c58bffbccca04034b853a15
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570204"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a>Propriété canonique PidTagPstConfigurationFlags
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Spécifie les indicateurs de configuration pour une table de stockage personnel (fichier .pst).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PST_CONFIG_FLAGS  <br/> |
|Identificateur :  <br/> |0x6770  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Tableau de stockage personnel (.pst) interne  <br/> |
   
## <a name="remarks"></a>Remarques

Les valeurs valides pour cette propriété sont les suivantes :
  
PST_CONFIG_UNICODE
  
> Indique un fichier .pst Unicode. 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
PST_CONFIG_CREATE_NOWARN
  
> Lorsque set à partir du client indicateurs à la méthode [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) , **ConfigureMsgService** la traite comme un appel [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) et ignore la « ce service d’informations n'a pas été configuré » avertissement. 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
PST_CONFIG_PRESERVE_DISPLAY_NAME
  
> Indique à **ConfigureMsgService** de ne pas modifier la valeur de la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), même si elle a été fournie. Dans ce cas, il a été fourni uniquement pour les nouveaux fichiers .pst.
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
OST_CONFIG_POLICY_DELAY_IGNORE_OST
  
> Indique le code de configuration pour la première afficher une boîte de dialogue pour vérifier si un fichier de dossier hors connexion (.ost) a été trouvé et, en fonction de la réponse de l’utilisateur, utiliser le dossier en mode hors connexion trouvé ou permettre à l’utilisateur rechercher un autre dossier en mode hors connexion.
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
OST_CONFIG_CREATE_NEW_DEFAULT
  
> Copie du fichier .ost avec un nouveau nom unique et ignore le nom actuel. Le fichier .ost existant reste sur l’ordinateur, mais n’est plus utilisé dans ce profil. Cela se produit généralement lorsque Microsoft Outlook ne sont plus permet à un fichier .ost particulier et stratégies de Registre ne pas autorisent l’utilisateur à renommer le fichier. 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]] 
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

