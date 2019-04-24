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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c9c446097213e5b743a47ec32db17ec0afe63b78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357546"
---
# <a name="pidtagcontainerflags-canonical-property"></a>Propriété canonique PidTagContainerFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de masque des indicateurs décrivant les capacités d'un conteneur de carnet d'adresses. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTAINER_FLAGS  <br/> |
|Identificateur :  <br/> |0x3600  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Un ou plusieurs des indicateurs suivants peuvent être définis pour le masque de masques:
  
AB_FIND_ON_OPEN 
  
> Affiche une boîte de dialogue pour demander une restriction avant d'afficher le contenu du conteneur. 
    
AB_MODIFIABLE 
  
> Les entrées peuvent être ajoutées et supprimées du conteneur. Cet indicateur n'indique pas si les entrées du conteneur peuvent être modifiées.
    
AB_RECIPIENTS 
  
> Le conteneur peut contenir des destinataires. Cet indicateur n'indique pas si les destinataires sont réellement présents dans le conteneur, ou s'ils peuvent être ajoutés ou supprimés. 
    
AB_SUBCONTAINERS 
  
> Le conteneur peut contenir des conteneurs enfants. Cet indicateur n'indique pas si des sous-conteneurs sont réellement présents dans le conteneur, ni s'ils peuvent être ajoutés ou supprimés. AB_SUBCONTAINERS doit être défini pour que le conteneur prenne en charge [IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md). 
    
AB_UNMODIFIABLE 
  
> Les entrées ne peuvent pas être ajoutées ou supprimées du conteneur. Cet indicateur n'indique pas si les entrées du conteneur peuvent être modifiées. 
    
L'indicateur AB_FIND_ON_OPEN est fortement recommandé pour les conteneurs utilisés avec les services en ligne ou avec des connexions lentes aux serveurs. Lorsqu'un conteneur est ouvert et qu'il a AB_FIND_ON_OPEN défini, une boîte de dialogue **Rechercher** est présentée à l'utilisateur pour limiter les utilisateurs de messagerie affichés. Même une spécification partielle limitation les utilisateurs de messagerie peuvent considérablement accélérer l'affichage du contenu. 
  
L'indicateur AB_MODIFIABLE ou AB_UNMODIFIABLE doit être défini. Les deux indicateurs peuvent être définis pour indiquer que le conteneur ne sait pas s'il peut être modifié, par exemple si la modification dépend des droits d'accès de l'utilisateur. Dans ce cas, une application cliente doit essayer un appel et examiner le code de retour pour déterminer les fonctionnalités du conteneur. Un client commence généralement par examiner AB_MODIFIABLE. Si elle est définie, le client effectue un appel qui tente de modifier le conteneur et vérifie la valeur renvoyée. 
  
L'indicateur AB_MODIFIABLE n'indique pas les types d'entrées pouvant être ajoutés au conteneur. Pour déterminer cela, le client doit utiliser la méthode [OpenProperty](imapiprop-openproperty.md) appropriée pour ouvrir la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) du conteneur. L'ouverture de **PR_CREATE_TEMPLATES** entraîne le renvoi de la table ponctuelle du conteneur, qui répertorie les types d'entrées pouvant être créés dans le conteneur. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les listes d'utilisateurs, de contacts, de groupes et de ressources.
    
[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Gère les communications d'un client avec un serveur NSPI (Name Service Provider Interface).
    
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

