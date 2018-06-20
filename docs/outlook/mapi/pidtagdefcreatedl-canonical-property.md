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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3fb86fba3b0ff8a79858fad59dca61069aff6db9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785920"
---
# <a name="pidtagdefcreatedl-canonical-property"></a>Propriété canonique PidTagDefCreateDl

  
  
**S’applique à**: Outlook 
  
Contient l’identificateur d’entrée de modèle pour une liste de distribution par défaut. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DEF_CREATE_DL  <br/> |
|Identificateur :  <br/> |0x3611  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Applications clientes utilisent cette propriété pour créer une liste de distribution dans un conteneur. Prise en charge de la création de l’entrée est facultatif pour les conteneurs de carnet d’adresses ; ceux qui ne prennent pas en charge qu’il ne sont pas nécessaire d’exposer cette propriété. 
  
Cette propriété spécifie une entrée qui peut s’afficher dans la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) pour les listes de distribution. Après avoir obtenu l’identificateur, le client utilise un appel à la méthode [IABContainer::CreateEntry](iabcontainer-createentry.md) . L’entrée représente le modèle pour la liste de distribution par défaut. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[IABLogon::CompareEntryIDs](iablogon-compareentryids.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

