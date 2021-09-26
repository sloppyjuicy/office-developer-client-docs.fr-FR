---
title: Propriété canonique PidTagStatus
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 68ab44134fd26f4a29b3048126bae73bf4dd0c82
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599409"
---
# <a name="pidtagstatus-canonical-property"></a>Propriété canonique PidTagStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de bits 32 bits d’indicateurs qui définissent l’état du dossier.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_STATUS  <br/> |
|Identificateur :  <br/> |0x360B  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Conteneur MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété pour les dossiers est analogue à la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) pour les messages. Ses indicateurs sont fournis pour l’application cliente uniquement et n’affectent pas la magasin de messages. Les clients peuvent utiliser ou ignorer ces paramètres. Le client peut également définir ses propres valeurs pour les bits définissables par le client de cette propriété.
  
Un ou plusieurs des indicateurs suivants peuvent être définies pour le masque de bits :
  
FLDSTATUS_DELMARKED 
  
> Le dossier est marqué pour suppression. L’application cliente définit cet indicateur.
    
FLDSTATUS_HIDDEN 
  
> Le dossier est masqué.
    
FLDSTATUS_HIGHLIGHTED 
  
> Le dossier est mis en surbrillant, par exemple, affiché dans la vidéo inversée.
    
FLDSTATUS_TAGGED 
  
> Le dossier est balisé.
    
Les fournisseurs de magasins de messages définissent cette propriété sur un dossier sur une ou plusieurs de ces valeurs et les clients interprètent l’état comme approprié pour leurs applications. Par exemple, un client peut utiliser l’état du dossier pour différencier visuellement les dossiers d’une table hiérarchique, en affichant les dossiers ayant le même état de la même manière. Les dossiers mis en surbrill plan peuvent être affichés dans une vidéo inversée, les dossiers balisés et les dossiers marqués pour suppression peuvent être affichés avec une icône significative et les dossiers masqués peuvent être masqués.
  
Les bits 16 à 31 (« 0x10000 » à « 0x80000000 ») de cette propriété peuvent être utilisés par l’application cliente IPM. Tous les autres bits sont réservés à l’utilisation par MAPI ; Celles qui ne sont pas définies dans la liste précédente doivent être initialement définies sur zéro et ne pas être modifiées.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

