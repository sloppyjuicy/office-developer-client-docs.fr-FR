---
title: Propriété canonique PidTagProviderDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDisplay
api_type:
- COM
ms.assetid: 62e96db8-4c3e-4f73-b695-99eb4b2396fd
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 58db944720817491420f2bcb1774e51e3842b4a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421591"
---
# <a name="pidtagproviderdisplay-canonical-property"></a>Propriété canonique PidTagProviderDisplay

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom d'affichage défini par le fournisseur pour un fournisseur de services.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W  <br/> |
|Identificateur :  <br/> |0x3006  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |MAPI commun  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés et **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) sont définis uniquement sur les sections de profil appartenant aux fournisseurs de services. Ils doivent être présents dans MAPISVC. INF.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

