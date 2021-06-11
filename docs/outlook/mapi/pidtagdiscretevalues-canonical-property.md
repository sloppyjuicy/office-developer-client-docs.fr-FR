---
title: Propriété canonique PidTagDiscreteValues
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDiscreteValues
api_type:
- HeaderDef
ms.assetid: 958f3cf7-953a-43f4-9102-ad35edf5e813
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6d6974302e3413db3590abbbd3e6567976c6ac72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404840"
---
# <a name="pidtagdiscretevalues-canonical-property"></a>Propriété canonique PidTagDiscreteValues

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si un rapport non distribué s’applique uniquement aux membres discrets d’une liste de distribution plutôt qu’à la liste entière. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DISCRETE_VALUES  <br/> |
|Identificateur :  <br/> |0x0E0E  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |MAPI non transmetteable  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée dans un rapport non remis lorsque le message n’a pas pu être remis à un ou plusieurs membres d’une liste de distribution. Son objectif est de limiter les tentatives de retransmission à ces membres individuels et non à la liste de distribution dans son ensemble. 
  
La table des destinataires d’un rapport non remis contient des entrées pour tous les destinataires auxquels le message n’a pas pu être remis, ainsi que pour les listes de distribution, le cas contraire, à laquelle ils appartiennent. Le fournisseur de transport doit définir cette propriété sur TRUE pour chaque entrée de liste de distribution. elle doit copier les propriétés **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) et **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) de la liste de distribution vers les propriétés **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) et **PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) pour chaque membre de cette liste de distribution. 
  
 **PR_DISCRETE_VALUES** ne doivent pas être définies pour toute entrée de destinataire de rapport autre qu’une liste de distribution. 
  
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

