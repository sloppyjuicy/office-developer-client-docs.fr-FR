---
title: Propriété canonique PidTagRecipientReassignmentProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 8636774b-1fff-4b29-bc12-4d0bd63fcba2
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0176485ca9b84260176e3be8ec9c8f42cf755cba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786537"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a>Propriété canonique PidTagRecipientReassignmentProhibited

  
  
**S’applique à**: Outlook 
  
Spécifie si l’ajout de destinataires supplémentaires, lors de la transmission du message, est interdite pour le message électronique.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECIPIENT_REASSIGNMENT_PROHIBITED  <br/> |
|Identificateur :  <br/> |0x002B  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Zone :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est définie en fonction de valeur de **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) du message électronique. Si **PR_SENSITIVITY** est défini sur « 0 x 00000000 » (normal) ou « 0 x 00000003 » (confidentiel), cette propriété doit être définie sur 0 x « 00 » ou absent ce qui signifie que l’ajout des destinataires supplémentaires ou différentes pour le message électronique est autorisé. Si le message électronique de l’objet **PR_SENSITIVITY** est défini sur « 0 x 00000001 » (personnelles) ou « 0 x 00000002 » (privé), cette propriété doit être définie à « 0 x 01 » pour empêcher l’ajout de destinataires supplémentaires ou différentes de ce message électronique par le biais de transfert. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les messages électroniques.
    
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

