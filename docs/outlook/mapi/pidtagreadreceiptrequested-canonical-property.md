---
title: Propriété canonique PidTagReadReceiptRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagReadReceiptRequested
api_type:
- COM
ms.assetid: 7db0645b-f3ab-4fc4-b865-68c952aeb359
description: Contient TRUE si un expéditeur de message souhaite que le système de messagerie génère un rapport de lecture lorsque le destinataire a lu un message.
ms.openlocfilehash: 51d7cfc25b0e83e4c44d9234c988a98937b14649
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523897"
---
# <a name="pidtagreadreceiptrequested-canonical-property"></a>Propriété canonique PidTagReadReceiptRequested

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si un expéditeur de message souhaite que le système de messagerie génère un rapport de lecture lorsque le destinataire a lu un message.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_READ_RECEIPT_REQUESTED  <br/> |
|Identificateur :  <br/> |0x0029  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |E-mail  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété doit être définie sur TRUE pour valider les valeurs des propriétés **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)) et **PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)).
  
Si un message avec **PR_READ_RECEIPT_REQUESTED** est supprimé ou expire avant que le système de messagerie puisse générer un rapport de lecture, un rapport non lu est généré. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour les objets de message électronique.
    
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

