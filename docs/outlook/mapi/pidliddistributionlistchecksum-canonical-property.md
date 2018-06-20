---
title: Propriété canonique PidLidDistributionListChecksum
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidLidDistributionListChecksum
api_type:
- COM
ms.assetid: bd50ab34-caae-4258-8afc-769e3cbc5220
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bba1e78d79800b1c8e56ad50ce1abb144d4c9aae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785119"
---
# <a name="pidliddistributionlistchecksum-canonical-property"></a>Propriété canonique PidLidDistributionListChecksum

  
  
**S’applique à**: Outlook 
  
Spécifie la redondance cyclique de 32 bits à cocher (CRC-32) polynomiale somme de contrôle pour obtenir une liste de distribution personnelle.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidDLChecksum  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Address  <br/> |
|ID de type long (capot) :  <br/> |0x0000804C  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de cette propriété peut être utilisée pour détecter le moment où la propriété **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) a été mis à jour sans mettre à jour les autres propriétés de membre de liste distribution personnelle en calculant le CRC-32 sur le serveur existant valeur de **dispidDLMembers** et en les comparant avec la valeur de la propriété **dispidDLChecksum** . 
  
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

