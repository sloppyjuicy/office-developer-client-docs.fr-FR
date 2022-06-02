---
title: Propriété canonique PidLidDistributionListMembers
description: Décrit la propriété canonique PidLidDistributionListMembers, qui spécifie une liste d’EntryIds et s’applique à Outlook 2013 et Outlook 2016.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidDistributionListMembers
api_type:
- COM
ms.assetid: 029767ab-de72-4402-9cc3-31b006591042
ms.openlocfilehash: 18c34438ecccc15f202989a449e509961c39495c
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852844"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a>Propriété canonique PidLidDistributionListMembers

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie la liste des EntryIds des objets qui correspondent aux membres de la liste de distribution personnelle.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidDLMembers  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Address  <br/> |
|ID long (LID) :  <br/> |0x00008055  <br/> |
|Type de données :  <br/> |PT_MV_BINARY  <br/> |
|Domaine :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

Les membres de la liste de distribution personnelle peuvent être d’autres listes de distribution personnelles, des adresses électroniques contenues dans un contact, des utilisateurs de liste d’adresses globales ou des listes de distribution, ou des adresses e-mail ponctuelles. Le format de chaque EntryId doit être un EntryId unique, comme spécifié dans [[MS-OXCDATA],](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) ou un EntryId encapsulé. 
  
Lors de la définition de cette propriété, le client ou le serveur doit s’assurer que sa taille totale est inférieure à 15 000 octets.
  
Cette propriété spécifie la liste des EntryIds uniques qui correspondent aux membres de la liste de distribution personnelle. Ces EntryIds uniques encapsulent les noms d’affichage et les adresses e-mail des membres de la liste de distribution personnelle.
  
Si le client ou le serveur définit cette propriété, elle doit être synchronisée avec cette propriété **dispidDLMembers** pour chaque entrée de la propriété **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)), il doit y avoir une entrée dans la même position dans **le dispidDDLOneOffMembers**.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées pour les contacts et les listes de distribution personnelles.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

