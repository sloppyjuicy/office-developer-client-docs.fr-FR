---
title: Propriété canonique PidLidDistributionListOneOffMembers
description: Décrit la propriété canonique PidLidDistributionListOneOffMembers, qui spécifie une liste d’EntryIds uniques.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidDistributionListOneOffMembers
api_type:
- COM
ms.assetid: 0b92e654-9e2d-4c2e-9a63-d5fac603b0c0
ms.openlocfilehash: 45010d5d66e7d0048b86563a4e01fdd7fb019da3
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65853523"
---
# <a name="pidliddistributionlistoneoffmembers-canonical-property"></a>Propriété canonique PidLidDistributionListOneOffMembers

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie la liste des EntryIds uniques qui correspondent aux membres de la liste de distribution personnelle.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidDLOneOffMembers  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Address  <br/> |
|ID long (LID) :  <br/> |0x00008054  <br/> |
|Type de données :  <br/> |PT_MV_BINARY  <br/> |
|Domaine :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

Ces EntryIds uniques encapsulent les noms d’affichage et les adresses e-mail des membres de la liste de distribution personnelle.
  
Si le client ou le serveur définit cette propriété, elle doit être synchronisée avec la propriété **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) : pour chaque entrée de la propriété **dispidDLOneOffMembers** , il doit y avoir une entrée dans la même position dans la propriété **dispidDLMembers** . 
  
Lorsque vous définissez **dispidDLOneOffMembers**, le client ou le serveur doit s’assurer que sa taille totale est inférieure à 15 000 octets.
  
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

