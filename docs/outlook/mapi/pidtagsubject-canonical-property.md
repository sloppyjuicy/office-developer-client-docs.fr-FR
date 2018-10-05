---
title: Propriété canonique PidTagSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubject
api_type:
- COM
ms.assetid: aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0cf9e9f8c10f8d27bd174b8b6f2bf19812dc269d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386305"
---
# <a name="pidtagsubject-canonical-property"></a>Propriété canonique PidTagSubject

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la totalité de l’objet d’un message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W  <br/> |
|Identificateur :  <br/> |0 x 0037  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont recommandées sur tous les objets de message. 
  
Ces propriétés sont toujours le texte de l’objet complet, autrement dit, la concaténation du préfixe et l’objet normalisé. S’il n’existe pas de préfixe, l’objet normalisée doit être identique à l’objet. Un message doit être stockée ou fournisseur utilise ces propriétés et les propriétés **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) pour calculer l’objet normalisée à l’aide de la règle décrite sous **PR_NORMALIZED_SUBJECT** ([ de transport PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).
  
Les propriétés de l’objet sont généralement petites chaînes de moins de 256 caractères, et un fournisseur de magasin de message n’est pas tenu prendre en charge l’interface **IStream** sur eux. Le client doit toujours tentent d’accéder par le biais de l’interface **IMAPIProp** tout d’abord et recourir aux **IStream** que si **MAPI_E_NOT_ENOUGH_MEMORY** est renvoyé. 
  
Pour un état, cette propriété contient le sujet du message d’origine précédé d’une chaîne qui indique ce qui est arrivé au message.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

