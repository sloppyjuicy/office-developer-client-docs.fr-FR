---
title: Propriété canonique PidTagCorrelateMtsid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelateMtsid
api_type:
- HeaderDef
ms.assetid: d0fc4e91-ed90-4d27-bd23-f01e99728e2d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 96bfc184752b6a3e15434ad67ac8c2b4b26cac4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426834"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a>Propriété canonique PidTagCorrelateMtsid

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l'identificateur MTS (Message Transfer System) utilisé pour la corrélation des rapports avec des messages envoyés.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CORRELATE_MTSID  <br/> |
|Identificateur :  <br/> |0x0E0D  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsqu'un fournisseur de transport rencontre un message envoyé lorsque cette propriété a la valeur TRUE, il définit cette propriété sur l'identificateur MTS pour ce message. Après la transmission, cette propriété est stockée avec le message dans le dossier éléments envoyés de message.
  
Les systèmes de messagerie qui prennent en charge la corrélation par l'identificateur MTS, tel que X. 400, conservent l'identificateur dans le cadre de l'enveloppe de transport du message d'origine et des rapports éventuellement générés en réponse à ce dernier. Lorsqu'un rapport est remis à partir d'un tel système de messagerie, le fournisseur de transport affecte à cette propriété l'identificateur MTS d'origine à partir de l'enveloppe de transport de l'État. Cette propriété est ensuite stockée avec le rapport.
  
Une application cliente peut gérer un dossier de résultats de recherche de tous les messages ayant cette propriété. Lorsqu'un rapport est fourni pour un tel message, le client peut appliquer des restrictions au dossier de résultats de recherche, trouver la version d'origine du message et corréler les informations du message d'origine avec les nouvelles informations.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés indiquées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

