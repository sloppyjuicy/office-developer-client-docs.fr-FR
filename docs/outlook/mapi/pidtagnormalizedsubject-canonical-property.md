---
title: Propriété canonique PidTagNormalizedSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagNormalizedSubject
api_type:
- HeaderDef
ms.assetid: 2000e6e8-d908-4814-8093-28f8011250c8
description: Contient l’objet du message avec n’importe quel préfixe supprimé pour Outlook 2013 et Outlook 2016.
ms.openlocfilehash: abdfaab52b0b8665122e27b9a0481dd085f9241a
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63783377"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a>Propriété canonique PidTagNormalizedSubject

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’objet du message avec un préfixe supprimé.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W  <br/> |
|Identificateur :  <br/> |0x0E1D  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |E-mail  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont calculées par la boutique de messages ou les fournisseurs de transport à partir des propriétés **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) et **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) de la manière suivante.
  
- Si le **PR_SUBJECT_PREFIX** est présent et qu’il s’agit d’une sous-propriété initiale de **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** et les propriétés associées sont définies sur le contenu de **PR_SUBJECT** avec le préfixe supprimé. 
    
- Si **PR_SUBJECT_PREFIX** est présent, mais qu’il ne s’agit pas d’une sous-chaîne initiale de **PR_SUBJECT**, **PR_SUBJECT_PREFIX** est supprimé et recalculé à partir de **PR_SUBJECT** à l’aide de la règle suivante : si la chaîne contenue dans **PR_SUBJECT** commence par un à trois caractères non numériques suivis d’un signe deux-points et d’un espace, la chaîne avec le signe deux-points et le vide deviennent le préfixe. Les nombres, les espaces vides et les caractères de ponctuation ne sont pas des caractères de préfixe valides. 
    
- Si **PR_SUBJECT_PREFIX** n’est pas présent, il est calculé à partir **PR_SUBJECT** à l’aide de la règle décrite à l’étape précédente. Cette propriété est ensuite définie sur le contenu **du PR_SUBJECT avec** le préfixe supprimé. 
    
 **Remarque** Lorsque **PR_SUBJECT_PREFIX** est une chaîne vide, **PR_SUBJECT** et cette propriété sont identiques. 
  
En fin de compte, cette propriété doit être la **partie de PR_SUBJECT** suivant le préfixe. S’il n’existe aucun préfixe, cette propriété devient la **même que PR_SUBJECT**.
  
 **PR_SUBJECT_PREFIX** et cette propriété doivent être calculées dans le cadre de l’implémentation [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Une application cliente ne doit pas demander à la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) leurs valeurs tant qu’elles n’ont pas été engagés par un appel **IMAPIProp::SaveChanges** . 
  
Les propriétés de l’objet sont généralement de petites chaînes de moins de 256 caractères, et un fournisseur de magasins de messages n’est pas obligé de prendre en charge l’interface **IStream** OLE (Object Linking and Embedding) sur ces derniers. Le client doit toujours essayer d’accéder en premier via l’interface **IMAPIProp** et recourir à **IStream** uniquement si MAPI_E_NOT_ENOUGH_MEMORY est renvoyé. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour les contacts et les listes de distribution personnelles.
    
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

