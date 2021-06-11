---
title: Propri t canonique PidLidDistributionListMembers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListMembers
api_type:
- COM
ms.assetid: 029767ab-de72-4402-9cc3-31b006591042
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f04d1593e2a13a2bfc23412340d7eb9f38f5d9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335069"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a>Propri t canonique PidLidDistributionListMembers

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie la liste des EntryIds des objets qui correspondent aux membres de la liste de distribution personnelle.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidDLMembers  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Address  <br/> |
|ID long (LID) :  <br/> |0x00008055  <br/> |
|Type de données :  <br/> |PT_MV_BINARY  <br/> |
|Domaine :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

Les membres de la liste de distribution personnelle peuvent être d’autres listes de distribution personnelles, des adresses électroniques contenues dans un contact, des utilisateurs de listes d’adresses globales ou des listes de distribution, ou des adresses de messagerie one-off. Le format de chaque EntryId doit être un EntryId one-off, comme spécifié dans [[MS-OXCDATA],](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) ou un EntryId wrapped. 
  
Lors de la définition de cette propriété, le client ou le serveur doit s’assurer que sa taille totale est inférieure à 15 000 octets.
  
Cette propriété spécifie la liste des EntryIds one-off qui correspondent aux membres de la liste de distribution personnelle. Ces EntryIds encapsulent les noms d’affichage et les adresses e-mail des membres de la liste de distribution personnelle.
  
Si le client ou le serveur définisse cette propriété, elle doit être synchronisée avec cette propriété **dispidDLMembers** pour chaque entrée dans la propriété **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)), il doit y avoir une entrée à la même position dans la **dispidDLOneOffMembers**.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour les contacts et les listes de distribution personnelles.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

