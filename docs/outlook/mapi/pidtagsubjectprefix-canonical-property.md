---
title: Propriété canonique PidTagSubjectPrefix
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSubjectPrefix
api_type:
- COM
ms.assetid: 07fcb881-d873-45bf-b048-30f41d0d8d85
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2c2bece089bc985111695f5bb54098d3fc6c4f0f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624453"
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
  
Le préfixe de l’objet se compose d’un ou plusieurs caractères alphanumériques, suivis d’un deux-points et d’un espace (qui font partie du préfixe). Il ne doit pas contenir de caractères non alphanumériques avant le deux-points. L’absence de préfixe peut être représentée par une chaîne vide ou par cette propriété qui n’est pas définie. 
  
Si ces propriétés sont définies explicitement, la chaîne peut être de toute longueur et utiliser des caractères alphanumériques, mais elle doit correspondre à une sous-chaîne au début de la propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)). Si ces propriétés ne sont pas définies par l’expéditeur et doivent être calculées, leur contenu est plus restreint. La règle de calcul du  préfixe est que PR_SUBJECT doit commencer par une, deux ou trois lettres (alphabétiques uniquement) suivies d’un deux-points et d’un espace. Si une telle sous-chaîne se trouve au début de **PR_SUBJECT**, elle devient alors la chaîne de ces propriétés (et reste également au début de **PR_SUBJECT**). Dans le cas contraire, ces propriétés restent non jeun. 
  
Ces propriétés **et PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) doivent être calculées dans le cadre de l’implémentation [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Un client ne doit pas demander [à IMAPIProp::GetProps](imapiprop-getprops.md) leurs valeurs tant qu’ils n’ont pas été engagés par un appel **IMAPIProp::SaveChanges.** 
  
Les propriétés de l’objet sont généralement de petites chaînes de moins de 256 caractères, et un fournisseur de magasins de messages n’est pas obligé de prendre en charge l’interface **OLE IStream** sur ces derniers. Un client doit d’abord essayer d’accéder à l’interface **IMAPIProp** et recourir à **IStream** uniquement si MAPI_E_NOT_ENOUGH_MEMORY **est** renvoyé. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et pièce jointe.
    
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

