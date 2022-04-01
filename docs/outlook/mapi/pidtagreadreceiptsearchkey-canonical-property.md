---
title: Propriété canonique PidTagReadReceiptSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagReadReceiptSearchKey
api_type:
- COM
ms.assetid: a0ea5628-1393-4ab8-bc34-a58cf130db51
description: Contient une clé de recherche pour l’utilisateur de messagerie vers lequel le système de messagerie doit diriger un rapport de lecture pour un message.
ms.openlocfilehash: 7137af24aa28ba27a1ef42ee012f51a77757fd4d
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523465"
---
# <a name="pidtagreadreceiptsearchkey-canonical-property"></a>Propriété canonique PidTagReadReceiptSearchKey

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une clé de recherche pour l’utilisateur de messagerie vers lequel le système de messagerie doit diriger un rapport de lecture pour un message.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_READ_RECEIPT_SEARCH_KEY  <br/> |
|Identificateur :  <br/> |0x0053  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est ignorée, sauf si la **propriété PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) est définie sur TRUE.
  
Si une application cliente souhaite recevoir elle-même des rapports de lecture, elle peut laisser cette propriété non définie ou la définir sur la clé de recherche contenue dans la propriété **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) au moment de l’envoi du message.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées sur les messages électroniques.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidef.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

