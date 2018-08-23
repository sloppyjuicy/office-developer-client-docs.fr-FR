---
title: Propriété canonique PidTagServiceEntryName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceEntryName
api_type:
- COM
ms.assetid: 783f08aa-fb5a-432d-b8bd-48d69f0e5c38
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3988596cc0b9c01d526354dabef3a6e7fdefc3b6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583224"
---
# <a name="pidtagserviceentryname-canonical-property"></a>Propriété canonique PidTagServiceEntryName

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient le nom de la fonction de point d’entrée pour la configuration d’un service de message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SERVICE_ENTRY_NAME  <br/> |
|Identificateur :  <br/> |0x3D0B  <br/> |
|Type de données :  <br/> |PT_STRING8  <br/> |
|Domaine :  <br/> |Profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Il est recommandé que l’implémentation de service de message fournit un point d’entrée de service message, mais le point d’entrée n’est pas obligatoire. Toutefois, le point d’entrée doit être fourni uniquement si les propriétés de configuration associées existent. Si ces propriétés n’existent pas, MAPI suppose qu’aucun point d’entrée n’est fournie.
  
La bibliothèque de liens dynamiques (DLL) dans lequel la fonction de point d’entrée apparaît est nommée par la propriété **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)).
  
Pour plus d’informations sur les points d’entrée de service de message, voir [mise en œuvre de la fonction de Point d’entrée un fournisseur de Service](implementing-a-service-provider-entry-point-function.md).
  
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

