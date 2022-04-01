---
title: Propriété canonique PidTagResourceType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagResourceType
api_type:
- COM
ms.assetid: 48b634d7-deea-422b-8944-a8d929d83838
description: Contient une valeur qui indique le type de fournisseur de services pour Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: c22bdc88fd7d69c6e24afa5e0d64c1ee2a5976e8
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524029"
---
# <a name="pidtagresourcetype-canonical-property"></a>Propriété canonique PidTagResourceType

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur qui indique le type de fournisseur de services.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RESOURCE_TYPE  <br/> |
|Identificateur :  <br/> |0x3E03  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut avoir exactement l’une des valeurs suivantes :
  
MAPI_AB 
  
> Carnet d’adresses
    
MAPI_AB_PROVIDER 
  
> Fournisseur de carnet d’adresses
    
MAPI_HOOK_PROVIDER 
  
> Fournisseur de crochets Spooler
    
MAPI_PROFILE_PROVIDER 
  
> Fournisseur de profils
    
MAPI_SPOOLER 
  
> Spooler de message
    
MAPI_STORE_PROVIDER 
  
> Fournisseur de magasin de messages
    
MAPI_SUBSYSTEM 
  
> Sous-système MAPI interne
    
MAPI_TRANSPORT_PROVIDER 
  
> Fournisseur de transport
    
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

