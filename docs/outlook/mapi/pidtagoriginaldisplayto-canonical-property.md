---
title: Propriété canonique PidTagOriginalDisplayTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginalDisplayTo
api_type:
- COM
ms.assetid: 8c1cf14c-0339-4ced-8f68-4bfaa1e4d3e9
description: Contient les noms d’affichage des destinataires principaux (À) du message d’origine. Il est fourni par MAPI et est copié directement à partir PR_DISPLAY_TO.
ms.openlocfilehash: 281f8ddd6a4176d0d66de90301d79b5f7e31ea21
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524039"
---
# <a name="pidtagoriginaldisplayto-canonical-property"></a>Propriété canonique PidTagOriginalDisplayTo

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient les noms d’affichage des destinataires principaux (À) du message d’origine.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A, PR_ORIGINAL_DISPLAY_TO_W  <br/> |
|Identificateur :  <br/> |0x0074  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés contiennent une liste ASCII séparée par des points-virgules. Il est fourni par MAPI et copié directement à partir de **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) lorsqu’un rapport de remise ou non remise ou un rapport lu ou non lu est généré. Cette propriété peut être présente sur d’autres messages tels que définis par leurs classes de messages.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées sur les objets de message électronique.
    
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

