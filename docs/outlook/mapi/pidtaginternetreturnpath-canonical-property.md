---
title: Propriété canonique PidTagInternetReturnPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetReturnPath
api_type:
- HeaderDef
ms.assetid: 4530dbcf-9436-4f29-b79e-1bb0f791f60b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c2d8eaf627f789c3e862a83d71e4ca2e3e55e1e0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388202"
---
# <a name="pidtaginternetreturnpath-canonical-property"></a>Propriété canonique PidTagInternetReturnPath

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur du champ d’en-tête d’un message Multipurpose Internet Mail Extensions (MIME) chemin de retour. L’adresse de messagerie de l’expéditeur du message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_INTERNET_RETURN_PATH, PR_INTERNET_RETURN_PATH_A, PR_INTERNET_RETURN_PATH_W  <br/> |
|Identificateur :  <br/> |0x1046  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Remarques

Pour récupérer la valeur de cette propriété, tout d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifiez cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur. Lors de l’appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) sur laquelle pointé le paramètre d’entrée _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid :  <br/> |PS_INTERNET_HEADERS  <br/> |
|ulKind :  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName :  <br/> |L « chemin de retour »  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

