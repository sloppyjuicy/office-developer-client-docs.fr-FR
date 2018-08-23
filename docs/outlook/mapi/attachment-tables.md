---
title: Tables des pièces jointes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 92a07f7b-d34c-4085-ab11-eadcd918fa1b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 27e489447b501b6e0d3bb7d668cecc3750be443e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564121"
---
# <a name="attachment-tables"></a>Tables des pièces jointes

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Une table de la pièce jointe contient des informations sur tous les objets attachment qui sont associés à un message envoyé ou un message dans la composition. 
  
Uniquement les pièces jointes qui ont été enregistrés via un appel à la méthode de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message sont inclus dans le tableau. Tables des pièces jointes sont implémentées par les fournisseurs de banque de messages et utilisés par les applications clientes et des fournisseurs de transport. 
  
Une table de la pièce jointe est accessible en appelant une des options suivantes :
  
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md), en demandant la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).
    
Tables des pièces jointes sont dynamiques.
  
Fournisseurs de banque de messages ne sont pas nécessaire pour prendre en charge le tri sur les tables des pièces jointes. Si le tri n’est pas pris en charge, le tableau doit être présenté en les classant par la position de rendu, la propriété **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).
  
Fournisseurs de banque de messages ne sont pas également requis pour prendre en charge des restrictions sur les tables des pièces jointes. Les fournisseurs qui ne prennent pas en charge les restrictions retourner MAPI_E_NO_SUPPORT à partir de leurs implémentations de [IMAPITable](imapitable-restrict.md) et [IMAPITable::FindRow](imapitable-findrow.md).
  
Tables des pièces jointes peuvent être petites ; Il existe quatre colonnes dans la colonne requis :
  
- **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) 
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) 
    
- **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
    
- **PR_RENDERING_POSITION**
    
 **PR_ATTACH_NUM** est nontransmittable et contient une valeur d’identification unique d’une pièce jointe dans un message. Cette propriété est souvent utilisée en tant qu’index dans les lignes de la table. **PR_ATTACH_NUM** a une courte durée de vie ; Il n’est valide que lorsque le message contenant la pièce jointe est ouvert. Sa valeur est garantie restent constantes dans la mesure où la table de la pièce jointe est ouverte. 
  
 **PR_INSTANCE_KEY** est nécessaire dans presque toutes les tables. Il est utilisé pour identifier de manière unique une ligne particulière. 
  
 **PR_RECORD_KEY** est généralement utilisé pour identifier de manière unique un objet à des fins de comparaison. Contrairement à **PR_ATTACH_NUM**, **PR_RECORD_KEY** a la même portée comme un identificateur d’entrée à long terme ; Il reste disponible et valide même une fois que le message est fermé et rouverte. Pour plus d’informations sur l’utilisation de clés d’enregistrement dans MAPI, voir [enregistrement MAPI et les clés de recherche](mapi-record-and-search-keys.md).
  
 **PR_RENDERING_POSITION** indique comment une pièce jointe doit être affichée dans un message de texte enrichi. Il peut être définie à un décalage de caractères, avec le premier caractère du contenu du message, tel que stocké dans la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) qui est décalée 0, ou -1 (0xFFFFFFFF), indiquant que la pièce jointe ne doit pas être affichée dans le message texte du tout. Ne définissez ne pas **PR_RENDERING_POSITION** est également une option. 
  
Lorsqu’une table de la pièce jointe est triée par sa position de rendu, le fournisseur de banque de message la traite comme une valeur signée (PT_LONG). Par conséquent, les pièces jointes avec les positions de rendu-1 sont triées avant les pièces jointes avec les positions de rendu qui reflètent les décalages valides. 
  
Pour plus d’informations sur le rendu d’une pièce jointe dans un message en texte brut, consultez [rendu d’une pièce jointe en texte brut](rendering-an-attachment-in-plain-text.md). 
  
Pour plus d’informations sur le rendu d’une pièce jointe dans le texte mis en forme comme texte enrichi (RTF), consultez [rendu d’une pièce jointe dans le texte RTF](rendering-an-attachment-in-rtf-text.md).
  
Les fournisseurs de banque de messages incluent couramment dans une table des pièces jointes, car ils sont faciles à calculer ou récupérer les propriétés sont les suivants :
  
|||
|:-----|:-----|
|**PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md))  <br/> |**PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md))  <br/> |
|**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md))  <br/> |**PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md))  <br/> |
|**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md))  <br/> |**PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md))  <br/> |
|**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |**PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md))  <br/> |
|**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Tables MAPI](mapi-tables.md)

