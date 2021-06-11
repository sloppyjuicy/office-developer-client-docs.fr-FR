---
title: Propriété canonique PidTagMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageStatus
api_type:
- HeaderDef
ms.assetid: e479e863-a8de-4f7e-9eae-3f721cd16e9a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dacd759d978394a5f4ed028915ed1c717bf6efe5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355719"
---
# <a name="pidtagmessagestatus-canonical-property"></a>Propriété canonique PidTagMessageStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de bits 32 bits d’indicateurs qui définit l’état d’un message dans une table des matières. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MSG_STATUS  <br/> |
|Identificateur :  <br/> |0x0E17  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Un message peut exister dans une table des matières et dans une ou plusieurs tables de résultats de recherche, et chaque instance du message peut avoir un état différent. Cette propriété ne doit pas être considérée comme une propriété d’un message, mais comme une colonne dans une table des matières. 
  
Une application cliente peut définir un ou plusieurs des indicateurs suivants dans cette propriété : 
  
MSGSTATUS_ANSWERED 
  
> Le message a été répondu. 
    
MSGSTATUS_DELMARKED 
  
> Le message a été marqué pour suppression ultérieure. 
    
MSGSTATUS_DRAFT 
  
> Le message est en état de brouillon de révision. 
    
MSGSTATUS_HIDDEN 
  
> Le message doit être supprimé des affichages du dossier des destinataires. 
    
MSGSTATUS_HIGHLIGHTED 
  
> Le message doit être mis en surbrillant dans les dossiers des destinataires. 
    
MSGSTATUS_REMOTE_DELETE 
  
> Le message a été marqué pour suppression dans la boutique de messages distante sans téléchargement vers le client local. 
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> Le message a été marqué pour téléchargement à partir de la boutique de messages distante vers le client local. 
    
MSGSTATUS_TAGGED 
  
> Le message a été marqué à des fins définies par le client.
    
Les **MSGSTATUS_DELMARKED,** **MSGSTATUS_HIDDEN,** **MSGSTATUS_HIGHLIGHTED** et **MSGSTATUS_TAGGED** sont définis par le client. Les fournisseurs de transport et de magasin passent ces bits sans aucune action. 
  
Les clients peuvent interpréter ces valeurs de n’importe quelle manière appropriée pour leurs applications. L’une des façons dont de nombreux clients utilisent cette propriété consiste à afficher les messages marqués pour suppression avec une icône représentative. 
  
Un client de visionneuse distante peut définir des MSGSTATUS_REMOTE_DELETE **ou** **des MSGSTATUS_REMOTE_DOWNLOAD** sur les messages dans le dossier d’en-tête qui lui est présenté par le fournisseur de transport distant. L’application cliente peut examiner chaque en-tête de message dans ce dossier pour déterminer si le message doit être téléchargé ou supprimé dans la boutique de messages distante. Il utilise ensuite la [méthode IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) pour définir l’indicateur approprié. **SetMessageStatus est** le seul moyen de définir l’un des indicateurs de cette propriété . La [méthode IMAPIProp::SetProps ne](imapiprop-setprops.md) peut pas être utilisée. Pour récupérer cette propriété, les clients appellent [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) plutôt que [IMAPIProp::GetProps](imapiprop-getprops.md).
  
Les bits 16 à 31 (0x10000 à 0x80000000) de cette propriété peuvent être utilisés par l’application cliente de message interpersonnel (IPM). Tous les autres bits sont réservés à l’utilisation par MAPI ; Celles qui ne sont pas définies dans le tableau précédent doivent être initialement définies sur zéro et ne pas être modifiées par la suite. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère la synchronisation des données d’objet de messagerie entre un serveur et un client.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[IMAPITable::QueryRows](imapitable-queryrows.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

