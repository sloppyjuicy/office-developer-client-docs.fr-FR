---
title: Propriété canonique PidTagStoreSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreSupportMask
api_type:
- COM
ms.assetid: ada5694a-b5b1-471f-be33-906fc052681a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8d9f6311b19ddb489885004a9e507f780d9f1ea9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786843"
---
# <a name="pidtagstoresupportmask-canonical-property"></a>Propriété canonique PidTagStoreSupportMask

  
  
**S’applique à**: Outlook 
  
Contient un masque binaire composé des indicateurs de cette requête d’applications client pour déterminer les caractéristiques d’une banque de messages. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_STORE_SUPPORT_MASK  <br/> |
|Identificateur :  <br/> |0x340D  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Divers  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété indique les fonctionnalités d’une banque de messages pour les applications clientes qui envisagent d’envoyer un message. Les indicateurs peuvent prendre en charge des décisions par un client ou un autre magasin, telles que s’il faut envoyer **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) ou uniquement **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). Un client ne doit jamais défini **PR_STORE_SUPPORT_MASK**; une tentative de définir cet indicateur renvoie MAPI_E_COMPUTED. 
  
Un ou plusieurs des indicateurs suivants peuvent être définies pour le masque de bits **PR_STORE_SUPPORT_MASK** : 
  
STORE_ANSI_OK
  
> (131072, 0 x 00020000) La banque de messages prend en charge les propriétés qui contiennent des caractères ANSI (8 bits).
    
STORE_ATTACH_OK 
  
> (32, 0 x 00000020) La banque de messages prend en charge les pièces jointes (OLE ou non OLE) pour les messages. 
    
STORE_CATEGORIZE_OK 
  
> (1024, 0 x 00000400) La banque de messages prend en charge les affichages, voir les tableaux. 
    
STORE_CREATE_OK 
  
> (16, 0 x 00000010) La banque de messages prend en charge la création de nouveaux messages. 
    
STORE_ENTRYID_UNIQUE 
  
> (1, 0 x 00000001) Identificateurs d’entrée pour les objets dans la banque de messages sont uniques, autrement dit, jamais réutilisé pendant la durée de vie de la banque. 
    
STORE_HTML_OK 
  
> (65536, 0 x 00010000) La banque de messages prend en charge des messages HTML, stockées dans la propriété **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)). Si votre environnement de développement utilise un MAPIDEFS. Fichier H qui n’inclut pas STORE_HTML_OK, utilisez plutôt la valeur 0 x 00010000. 
    
STORE_ITEMPROC
  
> (2097152, 0 x 00200000) Dans une banque de dossiers personnels encapsulée, indique que, lorsqu’un nouveau message arrive dans le magasin, le magasin effectue règles et le filtre de courrier indésirable séparément de traitement du message. Les appels de magasin [IMAPISupport::Notify](imapisupport-notify.md), le paramètre **fnevNewMail** dans la structure [NOTIFICATION](notification.md) qui est transmise en tant que paramètre, puis transmet les détails du message pour le client d’écoute. Par la suite, lorsque le client d’écoute reçoit la notification, il ne traite pas de règles dans le message. 
    
STORE_LOCALSTORE
  
> (524288, 0 x 00080000) Cet indicateur est réservé et ne doit pas être utilisé.
    
STORE_MODIFY_OK 
  
> (8, 0 x 00000008) La banque de messages prend en charge la modification de ses messages existants. 
    
STORE_MV_PROPS_OK 
  
> (512, 0 x 00000200) La banque de messages prend en charge les propriétés à valeurs multiples, garantit la stabilité d’ordre de valeur dans une propriété à valeurs multiples dans un enregistrement opération et prend en charge l’instanciation des propriétés à valeurs multiples dans les tableaux. 
    
STORE_NOTIFY_OK 
  
> (256, 0 x 00000100) La banque de messages prend en charge les notifications. 
    
STORE_OLE_OK 
  
> (64, 0 x 00000040) La banque de messages prend en charge les pièces jointes OLE. Les données OLE est accessible via une interface **IStorage** , par exemple celui disponibles par le biais de la propriété **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)). 
    
STORE_PUBLIC_FOLDERS 
  
> (16384, 0x00004000) Les dossiers de cette banque sont public (multi-utilisateur), non privée (éventuellement plusieurs instances, mais pas avec plusieurs utilisateurs). 
    
STORE_PUSHER_OK
  
> (8388608, 0 x 00800000) Le Gestionnaire de protocole MAPI ne sera pas analyser le magasin et le magasin est responsable de l’envoi des modifications via les notifications à l’indexeur que les messages indexés.
    
STORE_READONLY 
  
> (2, 0 x 00000002) Toutes les interfaces pour la banque de messages ont un niveau d’accès en lecture seule. 
    
STORE_RESTRICTION_OK 
  
> (4096, 0 x 00001000) La banque de messages prend en charge les restrictions. 
    
STORE_RTF_OK 
  
> (2048, 0x00000800) La banque de messages prend en charge les messages RTF (RICH Text Format), généralement compressés, et la banque elle-même conserve **PR_BODY** et **PR_RTF_COMPRESSED** synchronisés. 
    
STORE_RULES_OK
  
> (268435456, 0 x 10000000) Indique que les règles doivent être stockés dans cette banque de dossiers personnels, même s’il n’est pas la banque par défaut. Lorsque **STORE_RULES_OK** est utilisée conjointement avec **NON_EMS_XP_SAVE**, les règles sont en mesure de s’exécuter sur les magasins de PST encapsulé non par défaut.
    
STORE_SEARCH_OK 
  
> (4, 0 x 00000004) La banque de messages prend en charge les dossiers de résultats de recherche. 
    
STORE_SORT_OK 
  
> (8 192, 0 x 00002000) La banque de messages prend en charge le tri des vues de tables. 
    
STORE_SUBMIT_OK 
  
> (128, 0x00000080) La banque de messages prend en charge le marquage d’un message pour son envoi. 
    
STORE_UNCOMPRESSED_RTF 
  
> (32768, 0x00008000) La banque de messages prend en charge le stockage des messages au format RTF sous forme non compressée. Un flux de données au format RTF décompressé est identifié par la valeur **dwMagicUncompressedRTF** dans l’en-tête du flux. La valeur **dwMagicUncompressedRTF** est définie dans le RTFLIB. Fichier H. 
    
STORE_UNICODE_OK
  
> (262144, 0 x 00040000) Indique que la banque de messages prend en charge le stockage Unicode. Un client peut rechercher la présence de l’indicateur à décider s’il convient de demander ou d’enregistrer les informations de Unicode dans le magasin. 
    
Une version au format RTF d’un message peut être stockée toujours, même si la banque de messages est non compatibles RTF. Si le bit STORE_RTF_OK n’est pas défini pour un magasin particulier, un client de gestion des versions RTF doit lui-même appeler la fonction [RTFSync](rtfsync.md) pour conserver les versions **PR_BODY** et **PR_RTF_COMPRESSED** synchronisées pour le contenu de texte. Format RTF est toujours stocké dans **PR_RTF_COMPRESSED**, si elle est réellement compressé ou non. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXMSG]](http://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)
  
> Décrit le format des messages utilisé pour envoyer des informations relatives au partage de dossiers sur le client.
    
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

