---
title: Propriété canonique PidTagDefCreateMailuser
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateMailuser
api_type:
- HeaderDef
ms.assetid: e8293dc9-f2f1-4065-89f4-e734a8db63df
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: cd09c85e4f44bbea29807d72a273ccf6980ca6df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407479"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a>Propriété canonique PidTagDefCreateMailuser

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l'identificateur d'entrée de modèle pour un objet utilisateur de messagerie par défaut. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DEF_CREATE_MAILUSER  <br/> |
|Identificateur :  <br/> |0x3612  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Les applications clientes utilisent cette propriété pour créer un objet utilisateur de messagerie dans un conteneur. La prise en charge de la création d'entrées est facultative pour les conteneurs du carnet d'adresses; les personnes qui ne le prennent pas en charge n'ont pas besoin d'exposer cette propriété. 
  
Cette propriété spécifie une entrée pouvant apparaître dans la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) pour les utilisateurs de messagerie. Après avoir obtenu l'identificateur, le client l'utilise dans un appel à la méthode [IABContainer:: CreateEntry](iabcontainer-createentry.md) . L'entrée représente le modèle pour l'utilisateur de messagerie par défaut. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés indiquées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

