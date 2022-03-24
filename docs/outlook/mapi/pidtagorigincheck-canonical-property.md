---
title: Propriété canonique PidTagOriginCheck
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginCheck
api_type:
- COM
ms.assetid: 27e0ab2f-b373-41ae-b922-2f45f9671ac6
description: Contient une valeur de vérification binaire qui permet à un destinataire de rapport de remise de vérifier l’origine du message d’origine.
ms.openlocfilehash: 258ec4a0b72badd7fc91995bbdcaa431d3b0a589
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63762675"
---
# <a name="pidtagorigincheck-canonical-property"></a>Propriété canonique PidTagOriginCheck

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur de vérification binaire qui permet à un destinataire de rapport de remise de vérifier l’origine du message d’origine.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGIN_CHECK  <br/> |
|Identificateur :  <br/> |0x0027  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété permet à un tiers, tel qu’un agent de transfert de messages (MTA) ou un utilisateur de messagerie recevant un rapport de remise, de vérifier l’origine du message envoyé. Si elle est présente sur un message reçu, cette propriété doit être copiée dans n’importe quel rapport de remise généré en réponse au message.
  
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

