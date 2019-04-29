---
title: Propriété canonique PidTagStoreUnicodeMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreUnicodeMask
api_type:
- COM
ms.assetid: a6082162-2a74-4850-a0df-4bdbc67b41d8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e15c259003ed2cb425eb181f4383f3054967b993
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437937"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a>Propriété canonique PidTagStoreUnicodeMask

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de réindicateur des indicateurs que les applications clientes doivent interroger pour déterminer les caractéristiques d'une banque de messages.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_STORE_UNICODE_MASK  <br/> |
|Identificateur :  <br/> |0x340F  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Banque de messages MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété permet de divulguer les fonctionnalités d'une banque de messages aux applications clientes qui envisagent de les envoyer à un message. Les indicateurs peuvent faciliter les décisions d'un client ou d'un autre magasin, par exemple s'il faut envoyer des **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) ou seulement **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). Un client ne doit jamais définir cette propriété. Une tentative renvoie **MAPI_E_COMPUTED**. 
  
Un ou plusieurs des indicateurs suivants peuvent être définis pour cette propriété: 
  
STORE_ANSI_OK
  
> (131072, 0x00020000) La Banque de messages prend en charge les propriétés contenant des caractères ANSI (American National Standards Institute) (8 bits).
    
STORE_ATTACH_OK 
  
> (32, 0x00000020) La Banque de messages prend en charge les pièces jointes OLE (Object Linking and Embedding) ou non-OLE pour les messages. 
    
STORE_CATEGORIZE_OK 
  
> (1024, 0x00000400) La Banque de messages prend en charge les vues classées des tables. 
    
STORE_CREATE_OK 
  
> (16, 0x00000010) La Banque de messages prend en charge la création de nouveaux messages. 
    
STORE_ENTRYID_UNIQUE 
  
> (1, 0x00000001) Les identificateurs d'entrée pour les objets dans la Banque de messages sont uniques, c'est-à-dire qu'ils ne sont jamais réutilisés pendant la durée de vie de la Banque. 
    
STORE_HTML_OK 
  
> (65536, 0x00010000) La Banque de messages prend en charge les messages HTML, stockés dans la propriété **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)). Notez que **STORE_HTML_OK** n'est pas défini dans les versions de MAPIDEFS. H inclus avec le serveur Microsoft Exchange 2000 et versions antérieures. Si votre environnement de développement utilise un MAPIDEFS. H qui n'inclut pas **STORE_HTML_OK**, utilisez la valeur «0x00010000» à la place. 
    
STORE_ITEMPROC
  
> (2097152, 0x00200000) Dans une banque de fichiers PST encapsulée, indique que lorsqu'un nouveau message arrive dans le magasin, le traitement des règles et du filtrage du courrier indésirable est effectué séparément sur le message. Le magasin appelle [IMAPISupport:: Notify](imapisupport-notify.md), en définissant **fnevNewMail** dans la structure de [notification](notification.md) qui est transmise en tant que paramètre, puis transmet les détails du nouveau message au client d'écoute. Par la suite, lorsque le client à l’écoute reçoit la notification, il ne traite pas de règles dans le message. 
    
STORE_LOCALSTORE
  
> (524288, 0x00080000) Cet indicateur est réservé et ne doit pas être utilisé.
    
STORE_MODIFY_OK 
  
> (8, 0x00000008) La Banque de messages prend en charge la modification de ses messages existants. 
    
STORE_MV_PROPS_OK 
  
> (512, 0x00000200) La Banque de messages prend en charge les propriétés à valeurs multiples, garantit la stabilité de l'ordre des valeurs dans une propriété à valeurs multiples pendant une opération d'enregistrement et prend en charge l'instanciation de propriétés à valeurs multiples dans des tableaux. 
    
STORE_NOTIFY_OK 
  
> (256, 0x00000100) La Banque de messages prend en charge les notifications. 
    
STORE_OLE_OK 
  
> (64, 0x00000040) La Banque de messages prend en charge les pièces jointes OLE. Les données OLE sont accessibles via une interface **IStorage** , telle que celle disponible via la propriété **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)). 
    
STORE_PUBLIC_FOLDERS 
  
> (16384, 0x00004000) Les dossiers de cette banque sont publics (multi-utilisateurs), et non privés (éventuellement multi-instance, pas multi-utilisateur). 
    
STORE_PUSHER_OK
  
> (8388608, 0x00800000) Le gestionnaire de protocole MAPI n'analyse pas la Banque, et la Banque est responsable de la transmission de toutes les modifications via les notifications à l'indexeur afin de disposer d'un message indexé.
    
STORE_READONLY 
  
> (2, 0x00000002) Toutes les interfaces de la Banque de messages ont un niveau d'accès en lecture seule. 
    
STORE_RESTRICTION_OK 
  
> (4096, 0x00001000) La Banque de messages prend en charge les restrictions. 
    
STORE_RTF_OK 
  
> (2048, 0x00000800) La Banque de messages prend en charge les messages RTF (Rich Text Format), généralement compressés, et la Banque elle-même conserve la synchronisation de **PR_BODY** et de **PR_RTF_COMPRESSED** . 
    
STORE_SEARCH_OK 
  
> (4, 0x00000004) La Banque de messages prend en charge les dossiers de résultats de recherche. 
    
STORE_SORT_OK 
  
> (8192, 0x00002000) La Banque de messages prend en charge les affichages de tri des tables. 
    
STORE_SUBMIT_OK 
  
> (128, 0x00000080) La Banque de messages prend en charge le marquage d'un message pour l'envoi. 
    
STORE_UNCOMPRESSED_RTF 
  
> (32768, 0x00008000) La Banque de messages prend en charge le stockage des messages au format RTF (Rich Text Format) sous forme non compressée. Un flux de contenu RTF non compressé est identifié par la valeur **dwMagicUncompressedRTF** dans l'en-tête de flux. La valeur **dwMagicUncompressedRTF** est définie dans le RTFLIB. Fichier H. 
    
STORE_UNICODE_OK
  
> (262144, 0x00040000) La Banque de messages prend en charge les propriétés contenant des caractères Unicode.
    
Une version RTF d'un message peut toujours être stockée, même si la Banque de messages n'est pas compatible avec le format RTF. Si le bit STORE_RTF_OK n'est pas défini pour un magasin particulier, un client qui gère les versions RTF doit appeler la fonction [RTFSync](rtfsync.md) pour que les versions **PR_BODY** et **PR_RTF_COMPRESSED** soient synchronisées pour le contenu de texte. Le format RTF est toujours stocké dans **PR_RTF_COMPRESSED**, qu'il soit ou non compressé. 
  
## <a name="related-resources"></a>Ressources connexes

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

