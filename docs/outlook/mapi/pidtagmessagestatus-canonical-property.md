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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382805"
---
# <a name="pidtagmessagestatus-canonical-property"></a>Propriété canonique PidTagMessageStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque binaire composé de 32 bits d’indicateurs qui définit l’état d’un message dans une table des matières. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MSG_STATUS  <br/> |
|Identificateur :  <br/> |0x0E17  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Un message peut exister dans une table des matières et dans une ou plusieurs tables de résultats de recherche, et chaque instance du message peut avoir un statut différent. Cette propriété n’est pas une propriété d’un message, mais une colonne dans une table des matières. 
  
Une application cliente peut définir une ou plusieurs des indicateurs suivants dans cette propriété : 
  
MSGSTATUS_ANSWERED 
  
> Le message a été répondu à. 
    
MSGSTATUS_DELMARKED 
  
> Le message a été marqué pour suppression suivante. 
    
MSGSTATUS_DRAFT 
  
> Le message est dans l’état de révision de brouillon. 
    
MSGSTATUS_HIDDEN 
  
> Le message doit être supprimé de l’affiche de dossier de destinataires. 
    
MSGSTATUS_HIGHLIGHTED 
  
> Le message doit être mis en surbrillance dans les affichages de dossier de destinataires. 
    
MSGSTATUS_REMOTE_DELETE 
  
> Le message a été marqué pour suppression au niveau de la banque de messages à distance sans télécharger sur le client local. 
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> Le message a été marqué pour téléchargement à partir de la banque de messages à distance au client local. 
    
MSGSTATUS_TAGGED 
  
> Le message a été marqué pour un usage défini par le client.
    
Les indicateurs **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**et **MSGSTATUS_TAGGED** sont définis par le client. Fournisseurs de transport et le magasin de transmettre ces bits sans aucune action. 
  
Les clients peuvent interpréter ces valeurs en aucune manière appropriée pour leurs applications. Une façon que de nombreux clients utilisent cette propriété est pour afficher les messages marqués pour la suppression d’une icône représentant. 
  
Un client distant visionneuse définir **MSGSTATUS_REMOTE_DELETE** ou **MSGSTATUS_REMOTE_DOWNLOAD** sur les messages dans le dossier en-tête présenté par le fournisseur de transport à distance. L’application cliente peut examiner chaque en-tête du message dans ce dossier pour déterminer si le message doit être téléchargé ou supprimé dans la banque de messages à distance. Il utilise ensuite la méthode [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) pour définir l’indicateur approprié. **SetMessageStatus** est la seule façon de définir des indicateurs de cette propriété ; la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) ne peut pas être utilisée. Pour récupérer cette propriété, les clients appeler [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) plutôt que [IMAPIProp::GetProps](imapiprop-getprops.md).
  
Bits 16 à 31 (0 x 10000 par le biais de 0 x 80000000) de cette propriété sont disponibles pour une utilisation par l’application cliente de message interpersonnel (IPM). Tous les autres bits sont réservés pour une utilisation par MAPI ; les paramètres non définis dans le tableau précédent doivent initialement définies sur zéro et ne sera pas modifiés par la suite. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère la synchronisation des données de l’objet messagerie entre un serveur et un client.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[IMAPITable::QueryRows](imapitable-queryrows.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

