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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393228"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a>Propriété canonique PidTagNormalizedSubject

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’objet du message avec le préfixe supprimé.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W  <br/> |
|Identificateur :  <br/> |0x0E1D  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |E-mail  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont calculées par la banque de messages ou de propriétés **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) et des fournisseurs de transport de la manière suivante.
  
- Si la **PR_SUBJECT_PREFIX** est présente et est une sous-chaîne initiale de **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** et les propriétés associées sont définies pour le contenu de **PR_SUBJECT** sans le préfixe. 
    
- Si **PR_SUBJECT_PREFIX** est présent, mais il n’est pas une sous-chaîne initiale de **PR_SUBJECT**, **PR_SUBJECT_PREFIX** est supprimé et recalculé à partir de **PR_SUBJECT** à l’aide de la règle suivante : si la chaîne contenue dans **PR_SUBJECT** commence par un à trois chiffres suivis par un signe deux-points et un espace, puis la chaîne avec le signe deux-points et blanc devient le préfixe. Numéros, les espaces et les signes de ponctuation n’est pas des caractères de préfixe valide. 
    
- Si **PR_SUBJECT_PREFIX** n’est pas présent, il est calculé à partir de **PR_SUBJECT** à l’aide de la règle décrite à l’étape précédente. Puis cette propriété est définie pour le contenu de **PR_SUBJECT** sans le préfixe. 
    
 **Remarque** Lorsque **PR_SUBJECT_PREFIX** est une chaîne vide, **PR_SUBJECT** et cette propriété sont les mêmes. 
  
Enfin, cette propriété doit être la partie de **PR_SUBJECT** suit le préfixe. S’il n’existe pas de préfixe, cette propriété est identique à **PR_SUBJECT**.
  
 **PR_SUBJECT_PREFIX** et cette propriété doivent être calculées dans le cadre de l’implémentation de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Une application cliente doit demander pas à la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour leurs valeurs jusqu'à ce qu’ils ont été validées par un appel **IMAPIProp::SaveChanges** . 
  
Les propriétés de l’objet sont généralement petites chaînes de moins de 256 caractères, et un fournisseur de magasin de message n’est pas tenu prendre en charge l’interface Object Linking and Embedding (OLE) **IStream** sur eux. Le client doit toujours tentent d’accéder par le biais de l’interface **IMAPIProp** tout d’abord et recourir aux **IStream** que si MAPI_E_NOT_ENOUGH_MEMORY est renvoyé. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.
    
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

