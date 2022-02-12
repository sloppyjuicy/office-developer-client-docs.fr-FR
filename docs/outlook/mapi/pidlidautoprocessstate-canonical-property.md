---
title: Propriété canonique PidLidAutoProcessState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAutoProcessState
api_type:
- COM
ms.assetid: 9e724af6-5b56-4eb3-a94c-1015ebce197c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 79b22c642007b7ea27792231b3b85109b47f79ba
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62778768"
---
# <a name="pidlidautoprocessstate-canonical-property"></a>Propriété canonique PidLidAutoProcessState

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie les options utilisées dans le traitement automatique des messages électroniques.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidSniffState  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x0000851A  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

La propriété peut être absente, auquel cas la valeur par défaut de « 0x00000000 » est utilisée. Si elle est définie, cette propriété doit être définie sur l’une des valeurs du tableau suivant.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0x00000000  <br/> |Ne pas traiter automatiquement le message. |
|0x00000001  <br/> |Traiter le message automatiquement ou lorsque le message est ouvert. |
|0x00000002  <br/> |Traiter le message uniquement lorsque le message est ouvert. |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour les objets de message électronique.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

