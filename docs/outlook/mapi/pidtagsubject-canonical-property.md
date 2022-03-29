---
title: Propriété canonique PidTagSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSubject
api_type:
- COM
ms.assetid: aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9
description: Contient l’objet complet d’un message. Ces propriétés sont recommandées sur tous les objets de message.
ms.openlocfilehash: 0f9123cbb4c34bdf37c8abd303f959a087489c90
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64454746"
---
# <a name="pidtagsubject-canonical-property"></a>Propriété canonique PidTagSubject

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’objet complet d’un message.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W  <br/> |
|Identificateur :  <br/> |0x0037  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont recommandées sur tous les objets de message. 
  
Ces propriétés sont toujours le texte de l’objet complet, c’est-à-dire la concatenation du préfixe et de l’objet normalisé. S’il n’existe aucun préfixe, l’objet normalisé doit être identique à l’objet. Une magasin de messages ou un fournisseur de transport utilise ces propriétés et les propriétés **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) pour calculer l’objet normalisé à l’aide de la règle décrite sous **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).
  
Les propriétés de l’objet sont généralement de petites chaînes de moins de 256 caractères, et un fournisseur de magasins de messages n’est pas obligé de prendre en charge l’interface **IStream** sur ces derniers. Le client doit toujours essayer d’accéder en premier via l’interface **IMAPIProp** et recourir à **IStream** uniquement si **MAPI_E_NOT_ENOUGH_MEMORY est renvoyé** . 
  
Pour un état, cette propriété contient l’objet du message d’origine précédé d’une chaîne indiquant ce qui est arrivé au message.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
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

