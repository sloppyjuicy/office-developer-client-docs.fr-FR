---
title: Propriété canonique PidTagContainerFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerFlags
api_type:
- HeaderDef
ms.assetid: 66b8d333-227e-464d-8cf9-cd8a5ff15efb
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b62fc62bb9232b7106019fca82f502221e50bad0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583560"
---
# <a name="pidtagcontainerflags-canonical-property"></a>Propriété canonique PidTagContainerFlags

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un masque binaire composé des indicateurs décrivant les fonctionnalités d’un conteneur de carnet d’adresses. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTAINER_FLAGS  <br/> |
|Identificateur :  <br/> |0x3600  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Un ou plusieurs des indicateurs suivants peuvent être définies pour le masque de bits :
  
AB_FIND_ON_OPEN 
  
> Affiche une boîte de dialogue pour demander une restriction avant d’afficher le contenu du conteneur. 
    
AB_MODIFIABLE 
  
> Entrées peuvent être ajoutées à et supprimées du conteneur. Cet indicateur n’indique pas si les entrées dans le conteneur peuvent être modifiées.
    
AB_RECIPIENTS 
  
> Le conteneur peut contenir des destinataires. Cet indicateur n’indique pas si les destinataires sont présents dans le conteneur, ou si elles peuvent être ajoutés ou supprimés. 
    
AB_SUBCONTAINERS 
  
> Le conteneur peut contenir les conteneurs enfants. Cet indicateur n’indique pas si les sous-conteneurs sont présents dans le conteneur, ni si elles peuvent être ajoutés ou supprimés. AB_SUBCONTAINERS doit être définie pour le conteneur prendre en charge [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md). 
    
AB_UNMODIFIABLE 
  
> Les entrées ne peut pas être ajoutées à ou supprimées du conteneur. Cet indicateur n’indique pas si les entrées dans le conteneur peuvent être modifiées. 
    
L’indicateur AB_FIND_ON_OPEN est vivement recommandé pour les conteneurs utilisés avec les services en ligne ou les connexions lentes aux serveurs. Ouverture d’un conteneur qui a la valeur AB_FIND_ON_OPEN, une boîte de dialogue **Rechercher** est présentée à l’utilisateur pour limiter les utilisateurs de messagerie affichées. Même une spécification partielle limitant les utilisateurs de messagerie peut considérablement accélérer un affichage du contenu. 
  
Indicateur AB_UNMODIFIABLE ou AB_MODIFIABLE doit être défini. Les deux indicateurs peuvent être définis pour indiquer que le conteneur ne sait pas si elle peut être modifiée ou non, par exemple si modification dépend des droits d’accès de l’utilisateur. Dans ce cas, une application cliente doit essayer un appel et examinez le code de retour pour déterminer les fonctionnalités du conteneur. Un client commence généralement en examinant AB_MODIFIABLE. Si elle est définie, le client effectue un appel qui tente de modifier le conteneur et vérifie la valeur de retour. 
  
L’indicateur AB_MODIFIABLE n’indique pas les types d’entrées peuvent être ajoutés au conteneur. Pour cela, le client doit utiliser la méthode [OpenProperty](imapiprop-openproperty.md) appropriée pour ouvrir la propriété du conteneur **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Ouverture **PR_CREATE_TEMPLATES** causes unique du conteneur de table pour être retournés, les types d’entrées qui peuvent être créées dans le conteneur de liste. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.
    
[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Gère les communications d’un client avec un serveur NSPI Name Service Provider Interface ().
    
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

