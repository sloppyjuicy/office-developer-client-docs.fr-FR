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
ms.openlocfilehash: de2342ef4d3e9d06f198e06dc19c65b7b144624f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278791"
---
# <a name="pidtagstatus-canonical-property"></a>Propriété canonique PidTagStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de bits 32 bits des indicateurs qui définissent l'état du dossier.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_STATUS  <br/> |
|Identificateur :  <br/> |0x360B  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Conteneur MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété pour les dossiers est analogue à la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) pour les messages. Ses indicateurs sont fournis uniquement pour l'application cliente et n'affectent pas la Banque de messages. Les clients peuvent utiliser ou ignorer ces paramètres. Le client peut également définir ses propres valeurs pour les bits définissables par le client de cette propriété.
  
Un ou plusieurs des indicateurs suivants peuvent être définis pour le masque de masques:
  
FLDSTATUS_DELMARKED 
  
> Le dossier est marqué pour suppression. L'application cliente définit cet indicateur.
    
FLDSTATUS_HIDDEN 
  
> Le dossier est masqué.
    
FLDSTATUS_HIGHLIGHTED 
  
> Le dossier est mis en surbrillance, par exemple, affiché dans la vidéo inversée.
    
FLDSTATUS_TAGGED 
  
> Le dossier est balisé.
    
Les fournisseurs de banque de messages définissent cette propriété d'un dossier sur une ou plusieurs de ces valeurs et les clients interprètent l'État comme approprié pour leurs applications. Par exemple, un client peut utiliser l'état du dossier pour faire la distinction visuelle entre les dossiers d'une table de hiérarchie, en affichant les dossiers présentant le même état de la même façon. Les dossiers en surBrillance peuvent être affichés dans la vidéo inversée, les dossiers et les dossiers balisés marqués pour suppression peuvent être affichés avec une icône significative, et les dossiers masqués peuvent être masqués.
  
Les bits 16 à 31 («0x10000» à «0x80000000») de cette propriété peuvent être utilisés par l'application cliente IPM. Tous les autres bits sont réservés à l'usage de MAPI; ceux qui ne sont pas définis dans la liste précédente doivent être initialement définis sur zéro et ne sont pas modifiés.
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et Attachment.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

