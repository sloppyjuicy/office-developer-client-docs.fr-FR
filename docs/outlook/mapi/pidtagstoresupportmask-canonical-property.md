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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 143e7f0d2cd89cd4e7956cdda05d1bd512db4027
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340970"
---
# <a name="pidtagstoresupportmask-canonical-property"></a>Propriété canonique PidTagStoreSupportMask

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de bits d’indicateurs que les applications clientes interrogent pour déterminer les caractéristiques d’une magasin de messages. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_STORE_SUPPORT_MASK  <br/> |
|Identificateur :  <br/> |0x340D  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Divers  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété révèle les fonctionnalités d’un magasin de messages aux applications clientes qui prévoient de lui envoyer un message. Les indicateurs peuvent prendre en charge les décisions prises par un client ou un autre magasin, par exemple s’il faut envoyer **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) ou uniquement **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). Un client ne doit jamais définir **PR_STORE_SUPPORT_MASK**; Une tentative de définir cet indicateur renvoie MAPI_E_COMPUTED. 
  
Un ou plusieurs des indicateurs suivants peuvent être définies pour PR_STORE_SUPPORT_MASK **masque** de bits : 
  
STORE_ANSI_OK
  
> (131072, 0x00020000) La magasin de messages prend en charge les propriétés qui contiennent des caractères ANSI (8 bits).
    
STORE_ATTACH_OK 
  
> (32, 0x00000020) La magasin de messages prend en charge les pièces jointes (OLE ou non OLE) aux messages. 
    
STORE_CATEGORIZE_OK 
  
> (1024, 0x00000400) La magasin de messages prend en charge les affichages catégorisés des tables. 
    
STORE_CREATE_OK 
  
> (16, 0x00000010) La magasin de messages prend en charge la création de nouveaux messages. 
    
STORE_ENTRYID_UNIQUE 
  
> (1, 0x00000001) Les identificateurs d’entrée pour les objets de la boutique de messages sont uniques, c’est-à-dire qu’ils ne sont jamais réutilisés pendant la durée de vie de la boutique. 
    
STORE_HTML_OK 
  
> (65536, 0x00010000) La magasin de messages prend en charge les messages HTML, stockés dans la **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)). Si votre environnement de développement utilise un MAPIDEFS. Fichier H qui n’inclut pas STORE_HTML_OK, utilisez la valeur 0x00010000 à la place. 
    
STORE_ITEMPROC
  
> (2097152, 0x00200000) Dans un magasin PST enveloppé, indique qu’à l’arrivée d’un nouveau message dans la boutique, celle-ci effectue séparément le traitement des règles et du filtrage du courrier indésirable sur le message. La boutique appelle [IMAPISupport::Notify](imapisupport-notify.md), la définition **de fnevNewMail** dans la structure [notification](notification.md) transmise en tant que paramètre, puis transmet les détails du nouveau message au client d’écoute. Par la suite, lorsque le client à l’écoute reçoit la notification, il ne traite pas de règles dans le message. 
    
STORE_LOCALSTORE
  
> (524288, 0x00080000) Cet indicateur est réservé et ne doit pas être utilisé.
    
STORE_MODIFY_OK 
  
> (8, 0x00000008) La magasin de messages prend en charge la modification de ses messages existants. 
    
STORE_MV_PROPS_OK 
  
> (512, 0x00000200) La magasin de messages prend en charge les propriétés à valeurs multiples, garantit la stabilité de l’ordre des valeurs dans une propriété à valeurs multiples tout au long d’une opération d’enregistrer et prend en charge l’ins instantiation des propriétés à valeurs multiples dans les tables. 
    
STORE_NOTIFY_OK 
  
> (256, 0x00000100) La boutique de messages prend en charge les notifications. 
    
STORE_OLE_OK 
  
> (64, 0x00000040) La magasin de messages prend en charge les pièces jointes OLE. Les données OLE sont accessibles via une interface **IStorage,** telle que celle disponible via la propriété **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)). 
    
STORE_PUBLIC_FOLDERS 
  
> (16384, 0x00004000) Les dossiers de cette banque sont publics (multi-utilisateurs), et non privés (éventuellement à instances multiples, mais pas à plusieurs utilisateurs). 
    
STORE_PUSHER_OK
  
> (8388608, 0x00800000) Le responsable du protocole MAPI n’analyse pas le magasin et est responsable de l’push des modifications par le biais de notifications à l’indexeur pour que les messages sont indexés.
    
STORE_READONLY 
  
> (2, 0x00000002) Toutes les interfaces de la magasin de messages ont un niveau d’accès en lecture seule. 
    
STORE_RESTRICTION_OK 
  
> (4096, 0x00001000) La magasin de messages prend en charge les restrictions. 
    
STORE_RTF_OK 
  
> (2048, 0x00000800) La magasin de messages prend en charge les messages au format RTF (Rich Text Format), généralement compressés, et la boutique elle-même PR_BODY **et** **PR_RTF_COMPRESSED** synchronisées. 
    
STORE_RULES_OK
  
> (268435456, 0x10000000) Indique que les règles doivent être stockées dans ce magasin PST, même s’il ne s’agit pas du magasin par défaut. Lorsque **STORE_RULES_OK** est utilisé conjointement avec **NON_EMS_XP_SAVE**, les règles peuvent s’exécuter sur des magasins wrapped PST non par défaut.
    
STORE_SEARCH_OK 
  
> (4, 0x00000004) La magasin de messages prend en charge les dossiers de résultats de recherche. 
    
STORE_SORT_OK 
  
> (8192, 0x00002000) La magasin de messages prend en charge le tri des affichages des tables. 
    
STORE_SUBMIT_OK 
  
> (128, 0x00000080) La boutique de messages prend en charge le marquage d’un message pour l’envoi. 
    
STORE_UNCOMPRESSED_RTF 
  
> (32768, 0x00008000) La magasin de messages prend en charge le stockage des messages RTF sous forme non compressée. Un flux RTF non compressé est identifié par la valeur **dwMagicUncompressedRTF** dans l’en-tête de flux. La **valeur dwMagicUncompressedRTF** est définie dans le RTFLIB. Fichier H. 
    
STORE_UNICODE_OK
  
> (262144, 0x00040000) Indique que la banque de messages prend en charge le stockage Unicode. Un client peut rechercher la présence de l’indicateur pour décider s’il doit demander des informations Unicode à la banque ou les y enregistrer. 
    
Une version RTF d’un message peut toujours être stockée, même si la boutique de messages n’est pas sensible au RTF. Si le bit STORE_RTF_OK n’est pas définie pour un magasin particulier, un client conservant des versions RTF doit lui-même appeler la fonction [RTFSync](rtfsync.md) pour que les versions **PR_BODY** et **PR_RTF_COMPRESSED** restent synchronisées pour le contenu texte. RtF est toujours stocké dans PR_RTF_COMPRESSED **,** qu’il soit en réalité compressé ou non. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXMSG]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)
  
> Décrit le format des messages utilisés pour envoyer des informations relatives au partage de dossiers sur le client.
    
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

