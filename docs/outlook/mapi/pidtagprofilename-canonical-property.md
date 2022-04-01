---
title: Propriété canonique PidTagProfileName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagProfileName
api_type:
- COM
ms.assetid: 13ca726d-ae7a-4da9-9c8e-3db3c479f839
description: Contient le nom du profil. Les fournisseurs de services calculent ces propriétés. La fonction ServiceEntry peut utiliser ces propriétés pour découvrir le nom du profil.
ms.openlocfilehash: ed4af94faeb059fb9a514ac7c07ac587654def49
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524144"
---
# <a name="pidtagprofilename-canonical-property"></a>Propriété canonique PidTagProfileName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom du profil.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W  <br/> |
|Identificateur :  <br/> |0x3D12  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Configuration de profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont calculées par les fournisseurs de services. L’implémentation d’un fournisseur de **la fonction ServiceEntry** peut utiliser ces propriétés pour découvrir le nom du profil. 
  
Les applications clientes peuvent utiliser ces propriétés comme alternative pratique à l’obtention du nom du profil en examinant la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) dans la ligne de table d’état du sous-système MAPI.
  
Ces propriétés peuvent ne pas être uniques dans le temps, par exemple lorsqu’un profil est supprimé et recréé ultérieurement avec le même nom. MAPI fournit une propriété **PR_SEARCH_KEY unique (**[PidTagSearchKey](pidtagsearchkey-canonical-property.md)) dans une section de profil codée en dur appelée **MUID_PROFILE_INSTANCE.**
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

