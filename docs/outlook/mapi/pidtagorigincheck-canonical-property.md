---
title: Propriété canonique PidTagOriginCheck
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginCheck
api_type:
- COM
ms.assetid: 27e0ab2f-b373-41ae-b922-2f45f9671ac6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a82b1351c9d2d19c32e34b03a537a12bf93deb8a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435760"
---
# <a name="pidtagorigincheck-canonical-property"></a>Propriété canonique PidTagOriginCheck

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur de vérification binaire qui permet à un destinataire de rapport de remise de vérifier l’origine du message d’origine.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGIN_CHECK  <br/> |
|Identificateur :  <br/> |0x0027  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Server  <br/> |
   
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

