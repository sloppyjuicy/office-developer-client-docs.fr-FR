---
title: Propriété canonique PidTagProviderOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagProviderOrdinal
api_type:
- COM
ms.assetid: d062b54d-7c32-4369-ab69-f7193773a1c0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f7bb9fd61e7df9aa8398bfd7c43890762c5fd954
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599690"
---
# <a name="pidtagproviderordinal-canonical-property"></a>Propriété canonique PidTagProviderOrdinal

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’index de base 0 de la position d’un fournisseur de services dans la table fournisseur.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROVIDER_ORDINAL  <br/> |
|Identificateur :  <br/> |0x300D  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |MAPI courant  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est calculée par MAPI.
  
Obtenez la table fournisseur en appelant la [méthode IMsgServiceAdmin::GetProviderTable.](imsgserviceadmin-getprovidertable.md) Tez la table des fournisseurs sur cette propriété pour afficher l’ordre de transport. 
  
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

