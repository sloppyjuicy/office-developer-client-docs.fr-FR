---
title: Propriété canonique PidTagStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatus
api_type:
- COM
ms.assetid: 8b947660-eafe-47e1-9595-bd3ab7d455bf
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 01a65306e5e0d34ed6f1ce7231227224868ff5cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786831"
---
# <a name="pidtagstatus-canonical-property"></a>Propriété canonique PidTagStatus

  
  
**S’applique à**: Outlook 
  
Contient un masque de bits 32 bits d’indicateurs qui définissent l’état du dossier.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_STATUS  <br/> |
|Identificateur :  <br/> |0x360B  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Conteneur MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété pour les dossiers est similaire à la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) pour les messages. Ses indicateurs sont fournis pour l’application cliente uniquement et n’affectent pas la banque de messages. Les clients peuvent utiliser ou ignorer ces paramètres. Le client peut également définir ses propres valeurs pour les fichiers binaires client définissables de cette propriété.
  
Un ou plusieurs des indicateurs suivants peuvent être définies pour le masque de bits :
  
FLDSTATUS_DELMARKED 
  
> Le dossier est marqué pour suppression. L’application cliente définit cet indicateur.
    
FLDSTATUS_HIDDEN 
  
> Le dossier est masqué.
    
FLDSTATUS_HIGHLIGHTED 
  
> Le dossier est mis en surbrillance, par exemple, présentée dans l’ordre inverse vidéo.
    
FLDSTATUS_TAGGED 
  
> Le dossier est marqué.
    
Fournisseurs de magasins message définir cette propriété sur un dossier pour une ou plusieurs de ces valeurs et les clients interprètent le statut en fonction de leurs applications. Par exemple, un client peut utiliser l’état des dossiers pour différencier visuellement les dossiers dans une table de hiérarchie, en affichant les dossiers avec le même état de la même manière. Dossiers en surbrillance puissent être affichés dans des dossiers vidéos, avec balise inverses dossiers marquées pour suppression peuvent être affichés avec une icône significative, et les dossiers cachés peuvent être masqués.
  
Bits 16 à 31 (« 0 x 10000 » par « 0 x 80000000 ») de cette propriété sont disponibles pour une utilisation par l’application cliente IPM. Tous les autres bits sont réservés pour une utilisation par MAPI ; les paramètres non définis dans la liste précédente doivent initialement la valeur zéro et n’a pas été modifiés.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

