---
title: PidTagStatus Canonical, propriété
description: Décrit la propriété canonique PidTagStatus, qui contient un masque de bits 32 bits d’indicateurs qui définissent l’état du dossier.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagStatus
api_type:
- COM
ms.assetid: 8b947660-eafe-47e1-9595-bd3ab7d455bf
ms.openlocfilehash: fc67aa7d7186e0cdcba452bbbeb44599fe52f035
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752539"
---
# <a name="pidtagstatus-canonical-property"></a>PidTagStatus Canonical, propriété

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de bits 32 bits d’indicateurs qui définissent l’état du dossier.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_STATUS  <br/> |
|Identificateur :  <br/> |0x360B  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Conteneur MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété pour les dossiers est analogue à la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) pour les messages. Ses indicateurs sont fournis uniquement pour l’application cliente et n’affectent pas le magasin de messages. Les clients peuvent utiliser ou ignorer ces paramètres. Le client peut également définir ses propres valeurs pour les bits définissables par le client de cette propriété.
  
Un ou plusieurs des indicateurs suivants peuvent être définis pour le masque de bits :
  
FLDSTATUS_DELMARKED 
  
> Le dossier est marqué pour suppression. L’application cliente définit cet indicateur.
    
FLDSTATUS_HIDDEN 
  
> Le dossier est masqué.
    
FLDSTATUS_HIGHLIGHTED 
  
> Le dossier est mis en surbrillance, par exemple, dans la vidéo inversée.
    
FLDSTATUS_TAGGED 
  
> Le dossier est balisé.
    
Les fournisseurs de magasins de messages définissent cette propriété sur un dossier sur une ou plusieurs de ces valeurs et les clients interprètent l’état comme approprié pour leurs applications. Par exemple, un client peut utiliser l’état du dossier pour différencier visuellement les dossiers d’une table de hiérarchie, en affichant les dossiers avec le même état de la même façon. Les dossiers mis en surbrillance peuvent être affichés dans une vidéo inversée, les dossiers marqués et les dossiers marqués pour suppression peuvent être affichés avec une icône explicite, et les dossiers masqués peuvent être masqués.
  
Les bits 16 à 31 (« 0x10000 » à « 0x80000000 ») de cette propriété sont disponibles pour être utilisés par l’application cliente IPM. Tous les autres bits sont réservés à l’utilisation par MAPI ; celles qui ne sont pas définies dans la liste précédente doivent être initialement définies sur zéro et ne pas être modifiées.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

