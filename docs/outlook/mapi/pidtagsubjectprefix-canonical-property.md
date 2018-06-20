---
title: Propriété canonique PidTagSubjectPrefix
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubjectPrefix
api_type:
- COM
ms.assetid: 07fcb881-d873-45bf-b048-30f41d0d8d85
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: be2d30f511540b2eb7aa6e55531753811aaa580d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786862"
---
# <a name="pidtagsubjectprefix-canonical-property"></a>Propriété canonique PidTagSubjectPrefix

  
  
**S’applique à**: Outlook 
  
Contient un préfixe d’objet qui indique généralement une action sur un message, tel que « TR : » pour le transfert. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W  <br/> |
|Identificateur :  <br/> |0x003D  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Zone :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont recommandées sur tous les objets de message. 
  
Le préfixe d’objet se compose d’un ou plusieurs caractères alphanumériques, suivis par un signe deux-points et un espace (qui font partie du préfixe). Ne doit pas contenir des caractères non alphanumériques avant le signe deux-points. Absence d’un préfixe peut être représentée par une chaîne vide ou par cette propriété n’est ne pas défini. 
  
Si ces propriétés sont définies de manière explicite, la chaîne peut être n’importe quelle longueur et utiliser des caractères alphanumériques, mais elle doit correspondre à une sous-chaîne au début de la propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)). Si ces propriétés ne sont pas définies par l’expéditeur et doivent être calculées, leur contenu est plus restreints. La règle pour calculer le préfixe est que **PR_SUBJECT** doit commencer par un, deux ou trois lettres (alphabétiques uniquement) suivi par un signe deux-points et un espace. Si ce une sous-chaîne est trouvée au début du **PR_SUBJECT**, il devient alors la chaîne de ces propriétés (et également reste au début du **PR_SUBJECT**). Dans le cas contraire, ces propriétés restent non définies. 
  
Ces propriétés et les **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) doivent être calculée dans le cadre de l’implémentation de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Un client ne doit pas demander [IMAPIProp::GetProps](imapiprop-getprops.md) pour leurs valeurs jusqu'à ce qu’ils ont été validées par un appel **IMAPIProp::SaveChanges** . 
  
Les propriétés de l’objet sont généralement petites chaînes de moins de 256 caractères, et un fournisseur de magasin de message n’est pas tenu prendre en charge l’interface OLE **IStream** sur eux. Un client doit toujours tentent d’accéder par le biais de l’interface **IMAPIProp** tout d’abord et recourir aux **IStream** que si **MAPI_E_NOT_ENOUGH_MEMORY** est renvoyé. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.
    
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

