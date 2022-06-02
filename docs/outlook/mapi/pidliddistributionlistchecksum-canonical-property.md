---
title: Propriété canonique PidLidDistributionListChecksum
description: Décrit la propriété canonique PidLidDistributionListChecksum, qui spécifie la somme de contrôle polynomiale CRC-32 pour une liste de distribution personnelle.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidLidDistributionListChecksum
api_type:
- COM
ms.assetid: bd50ab34-caae-4258-8afc-769e3cbc5220
ms.openlocfilehash: 9bd916c714db3b8d469354929a1a5f35162ddc39
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65854216"
---
# <a name="pidliddistributionlistchecksum-canonical-property"></a>Propriété canonique PidLidDistributionListChecksum

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie la somme de contrôle polynomiale de vérification de la redondance cyclique 32 bits (CRC-32) pour une liste de distribution personnelle.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |dispidDLChecksum  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Address  <br/> |
|ID long (LID) :  <br/> |0x0000804C  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de cette propriété peut être utilisée pour détecter quand la propriété **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) a été mise à jour sans mettre à jour les autres propriétés membres de liste de distribution personnelles en calculant la CRC-32 sur la valeur existante de **dispidDLMembers et en** la comparant à la valeur de la propriété **dispidDLChecksum** . 
  
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

