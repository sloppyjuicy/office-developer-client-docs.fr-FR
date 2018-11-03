---
title: Propriété canonique PidTagMessageAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageAttachments
api_type:
- HeaderDef
ms.assetid: 85762771-b823-4227-9a7b-75b6ac280b2d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5f13c2825fc0127b95fbf5bc0b41d68c64556864
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384086"
---
# <a name="pidtagmessageattachments-canonical-property"></a>Propriété canonique PidTagMessageAttachments

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau des restrictions qui peuvent être appliqués à un tableau de contenu pour trouver tous les messages qui contiennent les sous-objets de pièce jointe répondant aux restrictions. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_ATTACHMENTS  <br/> |
|Identificateur :  <br/> |0x0E13  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut être exclue dans les opérations [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluse dans les opérations de [IMAPIProp::CopyProps](imapiprop-copyprops.md) . En tant que propriété de type PT_OBJECT, il ne peut pas être récupéré par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) . Son contenu doit être accessible par la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , qui demande l’identificateur d’interface **IID_IMAPITable** . Fournisseurs de services doivent signaler à la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) si elle est définie, mais peut le signaler ou pas si elle n’est pas définie. 
  
Pour récupérer le contenu du tableau, une application cliente doit appeler la méthode [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) . For more information, see [Tables des pi�ces jointes](attachment-tables.md). 
  
Cette propriété peut être utilisée pour la restriction sous-objet en le définissant dans la structure [SSubRestriction](ssubrestriction.md) . Ainsi, le client limiter l’affichage d’un conteneur pour les messages contenant des pièces jointes de réunion critère donné. Un message satisfait aux conditions requises pour l’affichage si au moins une ligne dans sa table de pièces jointes, c'est-à-dire, une pièce jointe, satisfait à la restriction sous-objet. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)
  
> Définit les structures de base de données qui sont utilisés dans les opérations à distance.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Définit les structures de base de données qui sont utilisés dans les opérations à distance.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.
    
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

