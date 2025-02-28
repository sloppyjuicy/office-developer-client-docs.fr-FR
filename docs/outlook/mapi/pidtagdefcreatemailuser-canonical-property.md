---
title: Propriété canonique PidTagDefCreateMailuser
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDefCreateMailuser
api_type:
- HeaderDef
ms.assetid: e8293dc9-f2f1-4065-89f4-e734a8db63df
description: Contient l’identificateur d’entrée de modèle pour un objet utilisateur de messagerie par défaut. Les applications clientes utilisent cette propriété pour créer un objet utilisateur de messagerie dans un conteneur.
ms.openlocfilehash: 75e9d0249479ed1c6849c7408f442ae99b03c05b
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63762857"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a>Propriété canonique PidTagDefCreateMailuser

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’identificateur d’entrée de modèle pour un objet utilisateur de messagerie par défaut. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DEF_CREATE_MAILUSER  <br/> |
|Identificateur :  <br/> |0x3612  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Les applications clientes utilisent cette propriété pour créer un objet utilisateur de messagerie dans un conteneur. La prise en charge de la création d’entrées est facultative pour les conteneurs de carnet d’adresses . ceux qui ne la prisent pas en charge ne sont pas obligés d’exposer cette propriété. 
  
Cette propriété spécifie une entrée qui peut apparaître dans la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) pour les utilisateurs de messagerie. Une fois l’identificateur obtenu, le client l’utilise dans un appel à la méthode [IABContainer::CreateEntry](iabcontainer-createentry.md) . L’entrée représente le modèle de l’utilisateur de messagerie par défaut. 
  
## <a name="related-resources"></a>Ressources connexes

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

