---
title: Propriété canonique PidTagPstConfigurationFlags
description: Décrit la propriété canonique PidTagPstConfigurationFlags, qui spécifie les indicateurs de configuration pour une table de stockage personnelle (fichier .pst).
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e4234ddf-d9dc-4dc9-8eda-dbbee151b5d7
ms.openlocfilehash: 4ef8c9d6ada170b906654d93a8d213384edc70be
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752553"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a>Propriété canonique PidTagPstConfigurationFlags
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie les indicateurs de configuration pour une table de stockage personnelle (fichier .pst).
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PST_CONFIG_FLAGS  <br/> |
|Identificateur :  <br/> |0x6770  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Table de stockage personnelle (.pst) interne  <br/> |
   
## <a name="remarks"></a>Remarques

Les valeurs suivantes sont valides pour cette propriété :
  
PST_CONFIG_UNICODE
  
> Indique un fichier .pst Unicode. 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
PST_CONFIG_CREATE_NOWARN
  
> Lorsqu’il est défini à partir des indicateurs client sur la méthode [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) , traite **ConfigureMsgService** comme un appel [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) et ignore l’avertissement « Ce service d’informations n’a pas été configuré ». 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
PST_CONFIG_PRESERVE_DISPLAY_NAME
  
> Indique à **ConfigureMsgService** de ne pas modifier la valeur de la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), même si elle a été fournie. Dans ce cas, il a été fourni uniquement pour les nouveaux fichiers .pst.
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
OST_CONFIG_POLICY_DELAY_IGNORE_OST
  
> Indique au code de configuration d’afficher d’abord une boîte de dialogue pour confirmer si un fichier dossier hors connexion (.ost) a été trouvé et, selon la réponse de l’utilisateur, utilisez le dossier hors connexion trouvé ou autorisez l’utilisateur à rechercher un autre dossier hors connexion.
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
OST_CONFIG_CREATE_NEW_DEFAULT
  
> Copie le fichier .ost avec un nouveau nom unique et ignore le nom actuel. Le fichier .ost existant reste sur l’ordinateur, mais n’est plus utilisé dans ce profil. Cela se produit généralement lorsque Microsoft Outlook n’autorise plus un fichier .ost particulier et que les stratégies de Registre n’autorisent pas l’utilisateur à renommer le fichier. 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]] 
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

