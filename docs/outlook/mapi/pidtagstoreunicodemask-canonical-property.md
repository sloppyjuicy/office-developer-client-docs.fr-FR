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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 010b17de08ee5836a26c56f300b36822df2e981e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786846"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a>Propriété canonique PidTagStoreUnicodeMask

  
  
**S’applique à**: Outlook 
  
Contient un masque de bits d’indicateurs applications clientes doivent interroger pour déterminer les caractéristiques d’une banque de messages.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_STORE_UNICODE_MASK  <br/> |
|Identificateur :  <br/> |0x340F  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Banque de messages MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété indique les fonctionnalités d’une banque de messages vers des applications clientes envoyer un message de planification. Les indicateurs peuvent faciliter les décisions par un client ou un autre magasin, telles que s’il faut envoyer **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) ou uniquement **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). Un client ne doit jamais définir cette propriété. Une tentative renvoie **MAPI_E_COMPUTED**. 
  
Un ou plusieurs des indicateurs suivants peuvent être définie pour cette propriété : 
  
STORE_ANSI_OK
  
> (131072, 0 x 00020000) La banque de messages prend en charge les propriétés qui contiennent des caractères National Institute ANSI (American Standards) (8 bits).
    
STORE_ATTACH_OK 
  
> (32, 0 x 00000020) La banque de messages prend en charge Object Linking et Embedding (OLE) ou non-OLE pièces jointes aux messages. 
    
STORE_CATEGORIZE_OK 
  
> (1024, 0 x 00000400) La banque de messages prend en charge les affichages, voir les tableaux. 
    
STORE_CREATE_OK 
  
> (16, 0 x 00000010) La banque de messages prend en charge la création de nouveaux messages. 
    
STORE_ENTRYID_UNIQUE 
  
> (1, 0 x 00000001) Identificateurs d’entrée pour les objets dans la banque de messages sont uniques, autrement dit, jamais réutilisé pendant la durée de vie de la banque. 
    
STORE_HTML_OK 
  
> (65536, 0 x 00010000) La banque de messages prend en charge des messages HTML, stockées dans la propriété **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)). Notez que **STORE_HTML_OK** n’est pas définie dans les versions de MAPIDEFS. H qui sont inclus avec Microsoft Exchange 2000 Server et les versions antérieures. Si votre environnement de développement utilise un MAPIDEFS. Fichier H ne pas inclure **STORE_HTML_OK**, utilisez la valeur « 0 x 00010000 » à la place. 
    
STORE_ITEMPROC
  
> (2097152, 0 x 00200000) Dans une banque de dossiers personnels encapsulée, indique que lorsqu’un nouveau message arrive dans le magasin, magasin fait règles et le courrier indésirable filtrer séparément de traitement du message. Les appels de magasin [IMAPISupport::Notify](imapisupport-notify.md), le paramètre **fnevNewMail** dans la structure [NOTIFICATION](notification.md) qui est transmise en tant que paramètre, puis transmet les détails du message pour le client d’écoute. Par la suite, lorsque le client d’écoute reçoit la notification, il ne traite pas de règles dans le message. 
    
STORE_LOCALSTORE
  
> (524288, 0 x 00080000) Cet indicateur est réservé et ne doit pas être utilisé.
    
STORE_MODIFY_OK 
  
> (8, 0 x 00000008) La banque de messages prend en charge la modification de ses messages existants. 
    
STORE_MV_PROPS_OK 
  
> (512, 0 x 00000200) La banque de messages prend en charge les propriétés à valeurs multiples, garantit la stabilité d’ordre de valeur dans une propriété à valeurs multiples dans un enregistrement opération et prend en charge l’instanciation des propriétés à valeurs multiples dans les tableaux. 
    
STORE_NOTIFY_OK 
  
> (256, 0 x 00000100) La banque de messages prend en charge les notifications. 
    
STORE_OLE_OK 
  
> (64, 0 x 00000040) La banque de messages prend en charge les pièces jointes OLE. Les données OLE sont accessibles via une interface **IStorage** , telle que disponibles via la propriété **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)). 
    
STORE_PUBLIC_FOLDERS 
  
> (16384, 0x00004000) Les dossiers de cette banque sont public (multi-utilisateur), non privée (éventuellement plusieurs instances, mais pas avec plusieurs utilisateurs). 
    
STORE_PUSHER_OK
  
> (8388608, 0 x 00800000) Le Gestionnaire de protocole MAPI ne sera pas analyser le magasin et le magasin est responsable pour acheminer les modifications via les notifications à l’indexeur que les messages indexés.
    
STORE_READONLY 
  
> (2, 0 x 00000002) Toutes les interfaces pour la banque de messages ont un niveau d’accès en lecture seule. 
    
STORE_RESTRICTION_OK 
  
> (4096, 0 x 00001000) La banque de messages prend en charge les restrictions. 
    
STORE_RTF_OK 
  
> (2048, 0x00000800) La banque de messages prend en charge les messages RTF (RICH Text Format), généralement compressés, et la banque elle-même conserve **PR_BODY** et **PR_RTF_COMPRESSED** synchronisés. 
    
STORE_SEARCH_OK 
  
> (4, 0 x 00000004) La banque de messages prend en charge les dossiers de résultats de recherche. 
    
STORE_SORT_OK 
  
> (8 192, 0 x 00002000) La banque de messages prend en charge le tri des vues de tables. 
    
STORE_SUBMIT_OK 
  
> (128, 0x00000080) La banque de messages prend en charge le marquage d’un message pour son envoi. 
    
STORE_UNCOMPRESSED_RTF 
  
> (32768, 0x00008000) La banque de messages prend en charge le stockage des messages de texte (RTF) sous forme révisable sous forme non compressée. Un flux de données au format RTF décompressé est identifié par la valeur **dwMagicUncompressedRTF** dans l’en-tête du flux. La valeur **dwMagicUncompressedRTF** est définie dans le RTFLIB. Fichier H. 
    
STORE_UNICODE_OK
  
> (262144, 0 x 00040000) La banque de messages prend en charge les propriétés contenant des caractères Unicode.
    
Une version au format RTF d’un message peut être stockée toujours, même si la banque de messages est non compatibles RTF. Si le bit STORE_RTF_OK n’est pas défini pour un magasin particulier, un client de gestion des versions RTF doit lui-même appeler la fonction [RTFSync](rtfsync.md) pour conserver les versions **PR_BODY** et **PR_RTF_COMPRESSED** synchronisées pour le contenu de texte. Format RTF est toujours stocké dans **PR_RTF_COMPRESSED**, si elle est réellement compressé ou non. 
  
## <a name="related-resources"></a>Ressources connexes

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

