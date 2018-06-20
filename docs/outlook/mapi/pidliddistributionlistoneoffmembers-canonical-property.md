---
title: Propriété canonique PidLidDistributionListOneOffMembers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListOneOffMembers
api_type:
- COM
ms.assetid: 0b92e654-9e2d-4c2e-9a63-d5fac603b0c0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ae6202a1fdf7ec43bf2269236aa8120aa67e3c50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785126"
---
# <a name="pidliddistributionlistoneoffmembers-canonical-property"></a>Propriété canonique PidLidDistributionListOneOffMembers

  
  
**S’applique à**: Outlook 
  
Spécifie la liste des ID d’entrée uniques qui correspondre aux membres de la liste de distribution personnelle.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidDLOneOffMembers  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Address  <br/> |
|ID de type long (capot) :  <br/> |0x00008054  <br/> |
|Type de données :  <br/> |PT_MV_BINARY  <br/> |
|Zone :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

Ces ID d’entrée uniques encapsulent les noms complets et les adresses de messagerie des membres de liste de distribution personnelle.
  
Si le client ou le serveur de définie cette propriété, il doit être synchronisé avec la propriété **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) : pour chaque entrée dans la propriété **dispidDLOneOffMembers** , doit être une entrée dans la même position dans la propriété **dispidDLMembers** . 
  
Lors de la définition de **dispidDLOneOffMembers**, le client ou le serveur doit vérifier que sa taille est inférieure à 15 000 octets.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

