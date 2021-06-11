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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2c771f1d97305271b70102c148e62f30512974fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432470"
---
# <a name="pidtagserviceentryname-canonical-property"></a>Propriété canonique PidTagServiceEntryName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom de la fonction de point d’entrée pour la configuration d’un service de message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SERVICE_ENTRY_NAME  <br/> |
|Identificateur :  <br/> |0x3D0B  <br/> |
|Type de données :  <br/> |PT_STRING8  <br/> |
|Domaine :  <br/> |Profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Il est recommandé que les implémenteurs de service de message fournissent un point d’entrée de service de message, mais le point d’entrée n’est pas obligatoire. Toutefois, le point d’entrée doit être fourni uniquement si les propriétés de configuration associées existent. Si ces propriétés n’existent pas, MAPI suppose qu’aucun point d’entrée n’est fourni.
  
La bibliothèque de liens dynamiques (DLL) dans laquelle la fonction de point d’entrée apparaît est nommée par la **propriété PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)).
  
Pour plus d’informations sur les points d’entrée de service de message, voir [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).
  
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

