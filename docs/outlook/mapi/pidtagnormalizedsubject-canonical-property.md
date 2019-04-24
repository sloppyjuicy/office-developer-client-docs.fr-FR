---
title: Propriété canonique PidTagNormalizedSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNormalizedSubject
api_type:
- HeaderDef
ms.assetid: 2000e6e8-d908-4814-8093-28f8011250c8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 54a0f438dacc8a1c7838eb538ec05c5c263f1b0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329273"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a>Propriété canonique PidTagNormalizedSubject

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l'objet du message avec le préfixe supprimé.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W  <br/> |
|Identificateur :  <br/> |0x0E1D  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |E-mail  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont calculées par le magasin de messages ou les fournisseurs de transport à partir des propriétés **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) et **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) de la manière suivante.
  
- Si **PR_SUBJECT_PREFIX** est présent et qu'il s'agit d'une sous-chaîne initiale de **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** et les propriétés associées sont définies sur le contenu de **PR_SUBJECT** avec le préfixe supprimé. 
    
- Si **PR_SUBJECT_PREFIX** est présent, mais qu'il ne s'agit pas d'une sous-chaîne initiale de **PR_SUBJECT**, **PR_SUBJECT_PREFIX** est supprimé et recalculé à partir de **PR_SUBJECT** à l'aide de la règle suivante: si la chaîne contenue dans **PR_SUBJECT** commence par un à trois caractères non numériques suivi d'un signe deux-points et d'un espace, puis la chaîne avec le signe deux-points et l'espace devient le préfixe. Les nombres, les espaces et les caractères de ponctuation ne sont pas des caractères de préfixe valides. 
    
- Si **PR_SUBJECT_PREFIX** n'est pas présent, il est calculé à partir de **PR_SUBJECT** à l'aide de la règle décrite à l'étape précédente. Cette propriété est ensuite définie sur le contenu de **PR_SUBJECT** avec le préfixe supprimé. 
    
 **Note** Lorsque **PR_SUBJECT_PREFIX** est une chaîne vide, **PR_SUBJECT** et cette propriété sont les mêmes. 
  
Enfin, cette propriété doit être la partie de **PR_SUBJECT** qui suit le préfixe. S'il n'y a pas de préfixe, cette propriété devient la même que **PR_SUBJECT**.
  
 **PR_SUBJECT_PREFIX** et cette propriété doivent être calculées dans le cadre de l'implémentation de [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . Une application cliente ne doit pas demander à la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) pour leurs valeurs tant qu'elles n'ont pas été validées par un appel **IMAPIProp:: SaveChanges** . 
  
Les propriétés Subject sont généralement des petites chaînes de moins de 256 caractères et un fournisseur de banque de messages n'est pas tenu de prendre en charge l'interface OLE (Object Linking and Embedding) **IStream** . Le client doit toujours tenter d'accéder d'abord à travers l'interface **IMAPIProp** et ne recourir à **ISTREAM** que si MAPI_E_NOT_ENOUGH_MEMORY est renvoyé. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et Attachment.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelle.
    
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

