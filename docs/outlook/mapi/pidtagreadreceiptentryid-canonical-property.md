---
title: Propriété canonique PidTagReadReceiptEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagReadReceiptEntryId
api_type:
- COM
ms.assetid: 141d49c8-87cf-4d80-a33b-ccbf3eeae19e
description: Contient un identificateur d’entrée pour l’utilisateur de messagerie où le système de messagerie doit diriger un rapport de lecture pour ce message.
ms.openlocfilehash: 55f883df1d7d5100bf6c5afdae2d906ebc19cb06
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524143"
---
# <a name="pidtagreadreceiptentryid-canonical-property"></a>Propriété canonique PidTagReadReceiptEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un identificateur d’entrée pour l’utilisateur de messagerie où le système de messagerie doit diriger un rapport de lecture pour ce message.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_READ_RECEIPT_ENTRYID  <br/> |
|Identificateur :  <br/> |0x0046  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est ignorée, sauf si la **propriété PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) est définie sur TRUE.
  
Si une application cliente souhaite recevoir elle-même des rapports de lecture, elle peut laisser cette propriété non définie ou la définir sur l’identificateur d’entrée contenu dans la propriété **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) au moment de l’envoi du message.
  
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

