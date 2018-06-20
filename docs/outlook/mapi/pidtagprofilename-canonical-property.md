---
title: Propriété canonique PidTagProfileName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProfileName
api_type:
- COM
ms.assetid: 13ca726d-ae7a-4da9-9c8e-3db3c479f839
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6ecd84e4ffa0959a037574998b5ff12d8f539c95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786443"
---
# <a name="pidtagprofilename-canonical-property"></a>Propriété canonique PidTagProfileName

  
  
**S’applique à**: Outlook 
  
Contient le nom du profil.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W  <br/> |
|Identificateur :  <br/> |0x3D12  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Zone :  <br/> |Configuration d’un profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont calculées par les fournisseurs de services. Implémentation d’un fournisseur de la fonction **ServiceEntry** peut utiliser ces propriétés pour découvrir le nom du profil. 
  
Applications clientes peuvent utiliser ces propriétés comme une alternative pratique pour obtenir le nom du profil en examinant la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) dans la ligne table d’état du sous-système MAPI.
  
Ces propriétés ne peuvent pas être uniques au fil du temps, par exemple où un profil est supprimé et recréé ultérieurement portant le même nom. MAPI apporte une propriété **clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) unique dans une section de profil codé en dur appelée **MUID_PROFILE_INSTANCE.**
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

