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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 992b3a6a30e15d267ffeda11ec98c7b4aeacb2c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435648"
---
# <a name="pidtagprofilename-canonical-property"></a>Propriété canonique PidTagProfileName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom du profil.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W  <br/> |
|Identificateur :  <br/> |0x3D12  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Configuration de profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont calculées par les fournisseurs de services. L’implémentation d’un fournisseur de **la fonction ServiceEntry** peut utiliser ces propriétés pour découvrir le nom du profil. 
  
Les applications clientes peuvent utiliser ces propriétés comme alternative pratique à l’obtention du nom du profil en examinant la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) dans la ligne de table d’état du sous-système MAPI.
  
Ces propriétés peuvent ne pas être uniques dans le temps, par exemple lorsqu’un profil est supprimé et recréé ultérieurement avec le même nom. MAPI fournit une propriété PR_SEARCH_KEY **unique** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) dans une section de profil codée en dur appelée **MUID_PROFILE_INSTANCE.**
  
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

