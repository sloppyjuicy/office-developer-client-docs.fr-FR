---
title: Propriété canonique PidTagOriginatingMtaCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginatingMtaCertificate
api_type:
- COM
ms.assetid: f6b7ff0c-19a0-4cad-8868-c05397fcebf4
description: Contient un identificateur pour l’agent de transfert de messages (MTA) à l’origine du message. Cette propriété est disponible pour les messages envoyés dans le dossier Éléments envoyés.
ms.openlocfilehash: 66f242a41db71fcb1b4417e5f49e7917367e3330
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63783300"
---
# <a name="pidtagoriginatingmtacertificate-canonical-property"></a>Propriété canonique PidTagOriginatingMtaCertificate

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un identificateur pour l’agent de transfert de messages (MTA) à l’origine du message.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINATING_MTA_CERTIFICATE  <br/> |
|Identificateur :  <br/> |0x0E25  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété, si elle est définie, est disponible pour les messages envoyés dans le dossier Éléments envoyés.
  
Cette propriété correspond à l’attribut de rapport X.400 par message.
  
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

