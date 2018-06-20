---
title: Propriété canonique PidTagRecipientNumberForAdvice
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientNumberForAdvice
api_type:
- COM
ms.assetid: 636c1e75-3024-43ca-a7dd-1bb480dfbb5b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ac4da2d4082cac632548594411528b7bf1d6dc64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786523"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a>Propriété canonique PidTagRecipientNumberForAdvice

  
  
**S’applique à**: Outlook 
  
Cette propriété contient le numéro de téléphone du destinataire du message à appeler pour signaler la remise physique d’un message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W  <br/> |
|Identificateur :  <br/> |0x0C14  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Zone :  <br/> |Destinataire MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont destinées à être utilisées conjointement avec la remise vers une destination physique, plutôt qu’une boîte aux lettres électronique, lorsque le destinataire humain n’est pas censé être présent à la remise. Le numéro de téléphone sur une page de garde est un exemple.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

