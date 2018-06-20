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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bbf09cb841c633b6f13ae12ec20e120ea3fd7ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786368"
---
# <a name="pidtagorigincheck-canonical-property"></a>Propriété canonique PidTagOriginCheck

  
  
**S’applique à**: Outlook 
  
Contient une valeur binaire de vérification qui permet à un destinataire de rapport de remise vérifier l’origine du message d’origine.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGIN_CHECK  <br/> |
|Identificateur :  <br/> |forme0x0027  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété fournit un moyen d’un fournisseur tiers, comme un message transfert agent d’ou recevoir un rapport de remise d’un utilisateur de messagerie pour vérifier l’origine du message envoyé. S’il est présent sur un message reçu, cette propriété doit être copiée sur un rapport de remise généré en réponse au message.
  
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

