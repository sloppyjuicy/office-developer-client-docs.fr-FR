---
title: Propriété canonique PidTagCorrelateMtsid
description: Décrit la propriété canonique PidTagCorrelateMtsid, qui contient l’identificateur MTS utilisé pour mettre en corrélation des rapports avec des messages envoyés.
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
ms.openlocfilehash: 957aef9c2e3b218bdd7df3b3bb066a2a95ff79da
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65769990"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a>Propriété canonique PidTagCorrelateMtsid

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’identificateur du système de transfert de messages (MTS) utilisé pour mettre en corrélation les rapports avec les messages envoyés.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CORRELATE_MTSID  <br/> |
|Identificateur :  <br/> |0x0E0D  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsqu’un fournisseur de transport rencontre un message envoyé avec cette propriété définie sur TRUE, il définit cette propriété sur l’identificateur MTS pour ce message. Après la transmission, cette propriété est stockée avec le message dans le dossier Messages interpersonnels (IPM) Éléments envoyés.
  
Les systèmes de messagerie qui prennent en charge la corrélation par l’identificateur MTS, comme X.400, conservent l’identificateur dans l’enveloppe de transport du message d’origine et des rapports générés en réponse à celui-ci. Lorsqu’un rapport est remis à partir d’un tel système de messagerie, le fournisseur de transport définit cette propriété sur l’identificateur MTS d’origine à partir de l’enveloppe de transport du rapport. Cette propriété est ensuite stockée avec le rapport.
  
Une application cliente peut conserver un dossier de résultats de recherche de tous les messages ayant cette propriété. Lorsqu’un rapport est fourni pour un tel message, le client peut appliquer des restrictions au dossier de résultats de recherche, rechercher la version d’origine du message et mettre en corrélation les informations du message d’origine avec les nouvelles informations.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

