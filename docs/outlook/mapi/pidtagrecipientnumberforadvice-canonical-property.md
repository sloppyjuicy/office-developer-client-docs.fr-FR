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
description: Cette propriété contient le numéro de téléphone d’un destinataire du message à appeler pour informer de la remise physique d’un message.
ms.openlocfilehash: 7d785296cb0501e4075847a3da9043a9a9ff5b9e
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523459"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a>Propriété canonique PidTagRecipientNumberForAdvice

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette propriété contient le numéro de téléphone d’un destinataire du message à appeler pour informer de la remise physique d’un message.
  
|Propriété |Valeur |
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

