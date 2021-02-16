---
title: Propriété canonique PidTagDefCreateDl
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateDl
api_type:
- HeaderDef
ms.assetid: 172dc15b-7bda-403f-a93a-446b2f9ff1d3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ff5d35104e9effc27c405b716cb61cf4643677b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417790"
---
# <a name="pidtagdefcreatedl-canonical-property"></a>Propriété canonique PidTagDefCreateDl

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’identificateur d’entrée de modèle pour une liste de distribution par défaut. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DEF_CREATE_DL  <br/> |
|Identificateur :  <br/> |0x3611  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Les applications clientes utilisent cette propriété pour créer une liste de distribution dans un conteneur. La prise en charge de la création d’entrées est facultative pour les conteneurs de carnet d’adresses . ceux qui ne la prisent pas en charge ne sont pas obligés d’exposer cette propriété. 
  
Cette propriété spécifie une entrée qui peut apparaître dans la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) pour les listes de distribution. Une fois l’identificateur obtenu, le client l’utilise dans un appel à la méthode [IABContainer::CreateEntry.](iabcontainer-createentry.md) L’entrée représente le modèle de la liste de distribution par défaut. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[IABLogon::CompareEntryIDs](iablogon-compareentryids.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

