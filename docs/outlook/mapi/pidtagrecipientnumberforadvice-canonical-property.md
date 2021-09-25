---
title: Propriété canonique PidTagRecipientNumberForAdvice
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRecipientNumberForAdvice
api_type:
- COM
ms.assetid: 636c1e75-3024-43ca-a7dd-1bb480dfbb5b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 402ef59d4645dd5abaf959188c155902e5bd8eee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594992"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a>Propriété canonique PidTagRecipientNumberForAdvice

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette propriété contient le numéro de téléphone d’un destinataire du message à appeler pour informer de la remise physique d’un message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W  <br/> |
|Identificateur :  <br/> |0x0C14  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Destinataire MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont destinées à être utilisées conjointement avec la remise à une destination physique, plutôt qu’à une boîte aux lettres électronique, lorsque le destinataire humain n’est pas censé être présent lors de la remise. Par exemple, le numéro de téléphone d’une feuille de couverture de télécopie.
  
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

