---
title: Propriété canonique PidTagCorrelateMtsid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagCorrelateMtsid
api_type:
- HeaderDef
ms.assetid: d0fc4e91-ed90-4d27-bd23-f01e99728e2d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a7b08f57c0c968bf538f310b9c7b2026efff4628
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455313"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a>Propriété canonique PidTagCorrelateMtsid

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’identificateur du système de transfert de messages (MTS) utilisé dans la corrélation de rapports avec des messages envoyés.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CORRELATE_MTSID  <br/> |
|Identificateur :  <br/> |0x0E0D  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsqu’un fournisseur de transport rencontre un message envoyé avec cette propriété définie sur TRUE, il définit cette propriété sur l’identificateur MTS pour ce message. Après la transmission, cette propriété est stockée avec le message dans le dossier Éléments envoyés du message interpersonnel (IPM).
  
Les systèmes de messagerie qui supportent la corrélation par l’identificateur MTS, comme X.400, conservent l’identificateur dans l’enveloppe de transport du message d’origine, ainsi que dans tous les rapports générés en réponse à celui-ci. Lorsqu’un état est remis à partir d’un tel système de messagerie, le fournisseur de transport définit cette propriété sur l’identificateur MTS d’origine à partir de l’enveloppe de transport de l’état. Cette propriété est ensuite stockée avec l’état.
  
Une application cliente peut gérer un dossier de résultats de recherche de tous les messages ayant cette propriété. Lorsqu’un rapport intervient pour un tel message, le client peut appliquer des restrictions au dossier de résultats de recherche, trouver la version d’origine du message et mettre en corrélation les informations du message d’origine avec les nouvelles informations.
  
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

