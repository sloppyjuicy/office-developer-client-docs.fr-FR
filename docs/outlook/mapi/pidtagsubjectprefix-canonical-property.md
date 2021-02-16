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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8257c3c3583072d16e96e6ea9bba4632fc78f9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339227"
---
# <a name="pidtagsubjectprefix-canonical-property"></a>Propriété canonique PidTagSubjectPrefix

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un préfixe d’objet qui indique généralement une action sur un message, telle que « FW: » pour le forwarding. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W  <br/> |
|Identificateur :  <br/> |0x003D  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont recommandées sur tous les objets de message. 
  
Le préfixe de l’objet se compose d’un ou plusieurs caractères alphanumériques, suivis d’un point deux-points et d’un espace (qui font partie du préfixe). Il ne doit pas contenir de caractères non alphanumériques avant le deux-points. L’absence de préfixe peut être représentée par une chaîne vide ou par cette propriété qui n’est pas définie. 
  
Si ces propriétés sont définies explicitement, la chaîne peut être de toute longueur et utiliser des caractères alphanumériques, mais elle doit correspondre à une sous-chaîne au début de la propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)). Si ces propriétés ne sont pas définies par l’expéditeur et doivent être calculées, leur contenu est plus restreint. La règle de calcul du  préfixe est que PR_SUBJECT doit commencer par une, deux ou trois lettres (alphabétique uniquement) suivies d’un deux-points et d’un espace. Si une telle sous-chaîne est trouvée au début de **PR_SUBJECT**, elle devient alors la chaîne de ces propriétés (et reste également au début de **PR_SUBJECT**). Dans le cas contraire, ces propriétés restent non jeun. 
  
Ces propriétés **et PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) doivent être calculées dans le cadre de l’implémentation [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Un client ne doit pas demander [à IMAPIProp::GetProps](imapiprop-getprops.md) leurs valeurs tant qu’ils n’ont pas été engagés par un appel **IMAPIProp::SaveChanges.** 
  
Les propriétés de l’objet sont généralement de petites chaînes de moins de 256 caractères, et un fournisseur de magasins de messages n’est pas obligé de prendre en charge l’interface OLE **IStream** sur ces derniers. Un client doit toujours essayer d’accéder à l’interface **IMAPIProp** en premier, et recourir à **IStream** uniquement si MAPI_E_NOT_ENOUGH_MEMORY **est** renvoyé. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server de protocole associées.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées sur les objets de message électronique.
    
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

