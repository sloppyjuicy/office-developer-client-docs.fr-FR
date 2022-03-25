---
title: Propriété canonique PidTagOwnStoreEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOwnStoreEntryId
api_type:
- COM
ms.assetid: 6a82ee90-10a1-49e0-8f3a-a2cd9f490f99
description: Contient l’identificateur d’entrée de la boutique de messages fortement couplée d’un transport pour Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: 6c7627cebdaab923d524af78cd09eb61c9878db4
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64405249"
---
# <a name="pidtagownstoreentryid-canonical-property"></a>Propriété canonique PidTagOwnStoreEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’identificateur d’entrée de la magasin de messages fortement couplé d’un transport.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_OWN_STORE_ENTRYID  <br/> |
|Identificateur :  <br/> |0x3E06  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Propriétés de la boutique de messages  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété spécifie l’identificateur d’entrée pour le magasin étroitement couplé, s’il en existe un. Par exemple, un fournisseur de transport peut spécifier l’identificateur d’entrée du magasin de dossiers privés afin que lepooler MAPI puisse connecter le fournisseur de transport à la banque.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

