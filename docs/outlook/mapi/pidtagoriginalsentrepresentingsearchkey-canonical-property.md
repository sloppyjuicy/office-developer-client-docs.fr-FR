---
title: Propriété canonique PidTagOriginalSentRepresentingSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginalSentRepresentingSearchKey
api_type:
- COM
ms.assetid: 0fb1b803-f8b4-4d6d-8e2a-836daa98ac63
description: Contient la clé de recherche de l’utilisateur de messagerie au nom de qui le message d’origine a été envoyé. Il est utilisé dans un thread de conversation.
ms.openlocfilehash: 3327384543e2e89dbf9aad1c855aa651a8238cd4
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524218"
---
# <a name="pidtagoriginalsentrepresentingsearchkey-canonical-property"></a>Propriété canonique PidTagOriginalSentRepresentingSearchKey

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la clé de recherche de l’utilisateur de messagerie au nom de qui le message d’origine a été envoyé.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINAL_SENT_REPRESENTING_SEARCH_KEY  <br/> |
|Identificateur :  <br/> |0x005F  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est l’une des propriétés d’adresse de l’expéditeur représenté d’origine d’un message. Il est utilisé dans un thread de conversation.
  
Une application cliente envoyant un message pour le compte d’un autre client doit définir cette propriété sur la valeur de la propriété **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) lors de la première soumission du message. Une fois définie, elle ne doit jamais être modifiée.
  
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

