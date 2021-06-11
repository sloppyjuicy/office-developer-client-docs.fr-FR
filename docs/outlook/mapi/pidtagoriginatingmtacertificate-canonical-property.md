---
title: Propriété canonique PidTagOriginatingMtaCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatingMtaCertificate
api_type:
- COM
ms.assetid: f6b7ff0c-19a0-4cad-8868-c05397fcebf4
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6f78609537b85a89617e7b2fa8f30a4ba952805b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414808"
---
# <a name="pidtagoriginatingmtacertificate-canonical-property"></a>Propriété canonique PidTagOriginatingMtaCertificate

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un identificateur pour l’agent de transfert de messages (MTA) à l’origine du message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINATING_MTA_CERTIFICATE  <br/> |
|Identificateur :  <br/> |0x0E25  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Server  <br/> |
   
## <a name="remarks"></a>Remarques

Si elle est définie, cette propriété est disponible pour les messages envoyés dans le dossier Éléments envoyés.
  
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

