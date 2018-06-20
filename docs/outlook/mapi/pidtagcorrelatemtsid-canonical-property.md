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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 57da2d4c78914323b5dafa4f5ba5b7628d0e2f2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785899"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a>Propriété canonique PidTagCorrelateMtsid

  
  
**S’applique à**: Outlook 
  
Contient l’identificateur de système (MTS) de transfert de message utilisé en corrélation des rapports avec les messages envoyés.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CORRELATE_MTSID  <br/> |
|Identificateur :  <br/> |0x0E0D  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsqu’un fournisseur de transport rencontre un message envoyé à cette propriété la valeur True, elle définit cette propriété sur l’identificateur MTS pour ce message. Après transmission, cette propriété est stockée avec le message dans le dossier éléments envoyés de message interpersonnel (IPM).
  
Systèmes de messagerie qui prennent en charge la corrélation par identificateur MTS, tels que X.400, conservent l’identificateur dans le cadre de l’enveloppe de transport du message d’origine et de tous les rapports générés en réponse à celui-ci. Lorsqu’un rapport est remis à partir d’un tel système de messagerie, le fournisseur de transport définit cette propriété sur l’identificateur MTS d’origine à partir de l’enveloppe de transport de l’état. Cette propriété est ensuite stockée avec le rapport.
  
Une application cliente peut maintenir un dossier de résultats de recherche de tous les messages ayant cette propriété. Lorsqu’un rapport entre pour ce type de message, le client peut appliquer des restrictions dans le dossier de résultats de recherche, recherchez la version d’origine du message et corréler les informations du message d’origine avec les nouvelles informations.
  
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

