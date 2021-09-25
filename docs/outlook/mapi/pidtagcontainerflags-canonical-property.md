---
title: Propriété canonique PidTagContainerFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContainerFlags
api_type:
- HeaderDef
ms.assetid: 66b8d333-227e-464d-8cf9-cd8a5ff15efb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8816d3cbb4c34330cdc970f1d197aeda415f9ed2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600371"
---
# <a name="pidtagcontainerflags-canonical-property"></a>Propriété canonique PidTagContainerFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de bits d’indicateurs décrivant les fonctionnalités d’un conteneur de carnet d’adresses. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTAINER_FLAGS  <br/> |
|Identificateur :  <br/> |0x3600  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Un ou plusieurs des indicateurs suivants peuvent être définies pour le masque de bits :
  
AB_FIND_ON_OPEN 
  
> Affiche une boîte de dialogue pour demander une restriction avant d’afficher le contenu du conteneur. 
    
AB_MODIFIABLE 
  
> Les entrées peuvent être ajoutées au conteneur et supprimées. Cet indicateur n’indique pas si des entrées dans le conteneur peuvent être modifiées.
    
AB_RECIPIENTS 
  
> Le conteneur peut contenir des destinataires. Cet indicateur n’indique pas si des destinataires sont réellement présents dans le conteneur, ou s’ils peuvent être ajoutés ou supprimés. 
    
AB_SUBCONTAINERS 
  
> Le conteneur peut contenir des conteneurs enfants. Cet indicateur n’indique pas si des sous-locataires sont réellement présents dans le conteneur, ni s’ils peuvent être ajoutés ou supprimés. AB_SUBCONTAINERS être définie pour que le conteneur soit en charge [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md). 
    
AB_UNMODIFIABLE 
  
> Les entrées ne peuvent pas être ajoutées ou supprimées du conteneur. Cet indicateur n’indique pas si des entrées dans le conteneur peuvent être modifiées. 
    
L AB_FIND_ON_OPEN est vivement recommandé pour les conteneurs utilisés avec des services en ligne ou avec des connexions lentes aux serveurs. Lorsqu’un conteneur est ouvert et AB_FIND_ON_OPEN,  une boîte de dialogue Rechercher est présentée à l’utilisateur pour restreindre les utilisateurs de messagerie affichés. Même une spécification partielle limitant les utilisateurs de messagerie peut accélérer considérablement l’affichage du contenu. 
  
L’AB_MODIFIABLE ou AB_UNMODIFIABLE’indicateur doit être définie. Les deux indicateurs peuvent être définies pour indiquer que le conteneur ne sait pas s’il peut être modifié ou non, par exemple si la modification dépend des droits d’accès de l’utilisateur. Dans ce cas, une application cliente doit tenter un appel et examiner le code de retour pour déterminer les fonctionnalités du conteneur. Un client commence généralement par examiner AB_MODIFIABLE. Si elle est définie, le client effectue un appel qui tente de modifier le conteneur et vérifie la valeur de retour. 
  
L AB_MODIFIABLE n’indique pas les types d’entrées qui peuvent être ajoutés au conteneur. Pour le déterminer, le client doit utiliser la méthode [OpenProperty](imapiprop-openproperty.md) appropriée pour ouvrir la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). **L PR_CREATE_TEMPLATES** entraîne le retour de la table unas du conteneur, répertoriant les types d’entrées qui peuvent être créées dans le conteneur. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.
    
[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Gère les communications d’un client avec un serveur NSPI (Name Service Provider Interface).
    
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

