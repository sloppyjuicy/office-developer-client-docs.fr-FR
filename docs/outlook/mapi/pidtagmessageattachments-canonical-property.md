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
ms.openlocfilehash: 975f52e6ea0ca7a469a027565f845f9dc0f9c2cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342566"
---
# <a name="pidtagmessageattachments-canonical-property"></a>Propriété canonique PidTagMessageAttachments

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une table des pièces jointes d’un message. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_ATTACHMENTS  <br/> |
|Identificateur :  <br/> |0x0E13  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut être exclue dans les opérations [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluse dans les opérations [IMAPIProp::CopyProps.](imapiprop-copyprops.md) En tant que propriété de type PT_OBJECT, elle ne peut pas être récupérée avec succès par la méthode [IMAPIProp::GetProps.](imapiprop-getprops.md) Son contenu doit être accessible par la méthode [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) en demandant l’identificateur **IID_IMAPITable’interface.** Les fournisseurs de services doivent le signaler à la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) si elle est définie, mais peuvent éventuellement la signaler ou non si elle n’est pas définie. 
  
Pour récupérer le contenu de la table, une application cliente doit appeler la [méthode IMessage::GetAttachmentTable.](imessage-getattachmenttable.md) For more information, see [Tables des pi�ces jointes](attachment-tables.md). 
  
Cette propriété peut être utilisée pour la restriction de sous-objet en la spécifiant dans la structure [SSubRestriction.](ssubrestriction.md) Cela permet au client de limiter l’affichage d’un conteneur aux messages contenant des pièces jointes qui rencontrent des critères donnés. Un message peut être affiché si au moins une ligne de sa table de pièces jointes, c’est-à-dire une pièce jointe, satisfait à la restriction de sous-objet. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)
  
> Définit les structures de données de base utilisées dans les opérations distantes.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Définit les structures de données de base utilisées dans les opérations distantes.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convertit les objets RFC2445, RFC2446 et RFC2447 de l’IETF, ainsi que les objets de rendez-vous et de réunion.
    
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

