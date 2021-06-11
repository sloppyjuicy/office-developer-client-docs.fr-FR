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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2dac2cb1d40fadbe0cad67b144891b0ece54aae9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341110"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a>Propriété canonique PidTagRecipientReassignmentProhibited

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie si l’ajout de destinataires supplémentaires, lors du forwarding du message, est interdit pour le message électronique.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECIPIENT_REASSIGNMENT_PROHIBITED  <br/> |
|Identificateur :  <br/> |0x002B  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est définie en fonction  de la valeur PR_SENSITIVITY[(PidTagSensitivity)](pidtagsensitivity-canonical-property.md)du message électronique. Si **PR_SENSITIVITY** est définie sur « 0x00000000 » (normal) ou « 0x00000003 » (confidentiel), cette propriété doit être définie sur « 0x00 » ou ne signifie pas que l’ajout de destinataires supplémentaires ou différents au message électronique est autorisé. Si **l’PR_SENSITIVITY** de l’objet de messagerie est définie sur « 0x00000001 » (personnel) ou « 0x00000002 » (privé), cette propriété doit être définie sur « 0x01 » pour empêcher l’ajout de destinataires supplémentaires ou différents de ce message électronique par le biais du forwarding. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées sur les messages électroniques.
    
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

