---
title: Tables des pièces jointes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 92a07f7b-d34c-4085-ab11-eadcd918fa1b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4aa800b504e7ffb07d94ace6d8dc30c1463ed637
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318136"
---
# <a name="attachment-tables"></a>Tables des pièces jointes

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une table Attachment contient des informations sur tous les objets Attachment associés à un message envoyé ou à un message en cours de composition. 
  
Seules les pièces jointes qui ont été enregistrées via un appel à la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) du message sont incluses dans le tableau. Les tables de pièces jointes sont implémentées par les fournisseurs de banques de messages et utilisées par les fournisseurs de transport et les applications clientes. 
  
Vous pouvez accéder à une table de pièces jointes en appelant l'une des méthodes suivantes:
  
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)
    
- [IMAPIProp:: OpenProperty](imapiprop-openproperty.md), qui demande la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).
    
Les tables de pièces jointes sont dynamiques.
  
Les fournisseurs de banques de messages ne sont pas tenus de prendre en charge le tri sur leurs tables de pièces jointes. Si le tri n'est pas pris en charge, le tableau doit être présenté dans l'ordre en fonction de la position de rendu, la propriété **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).
  
Les fournisseurs de banques de messages ne sont également pas tenus de prendre en charge les restrictions sur leurs tables de pièces jointes. Les fournisseurs qui ne prennent pas en charge les restrictions retournent MAPI_E_NO_SUPPORT à partir de leurs implémentations de [IMAPITable:: Restrict](imapitable-restrict.md) et [IMAPITable:: FindRow](imapitable-findrow.md).
  
Les tables de pièces jointes peuvent être petites; Il n'y a que quatre colonnes dans le jeu de colonnes requis:
  
- **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) 
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) 
    
- **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
    
- **PR_RENDERING_POSITION**
    
 **PR_ATTACH_NUM** n'est pas transmissible et contient une valeur permettant d'identifier de manière unique une pièce jointe dans un message. Cette propriété est souvent utilisée comme index dans les lignes du tableau. **PR_ATTACH_NUM** a une courte durée de vie; elle n'est valide que lorsque le message contenant la pièce jointe est ouvert. Sa valeur reste constante tant que la table des pièces jointes est ouverte. 
  
 **PR_INSTANCE_KEY** est requis dans presque toutes les tables. Elle est utilisée pour identifier une ligne particulière de manière unique. 
  
 **PR_RECORD_KEY** est couramment utilisé pour identifier un objet de manière unique à des fins de comparaison. Contrairement à **PR_ATTACH_NUM**, **PR_RECORD_KEY** a la même étendue qu'un identificateur d'entrée à long terme; Il reste disponible et valide même après la fermeture et la réouverture du message. Pour plus d'informations sur l'utilisation des clés d'enregistrement dans MAPI, voir [enregistrement MAPI et clés de recherche](mapi-record-and-search-keys.md).
  
 **PR_RENDERING_POSITION** indique le mode d'affichage d'une pièce jointe dans un message texte enrichi. Elle peut être définie sur un décalage en caractères, le premier caractère du contenu du message tel qu'il est stocké dans la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) étant offset 0 ou-1 (0xFFFFFFFF), indiquant que la pièce jointe ne doit pas être affichée dans le message texte du tout. Il est également possible de ne pas définir **PR_RENDERING_POSITION** . 
  
Lorsqu'une table de pièces jointes est triée en fonction de la position de rendu, le fournisseur de banque de messages la traite comme une valeur signée (PT_LONG). Par conséquent, les pièces jointes avec des positions de rendu de-1 sont triées avant les pièces jointes avec des positions de rendu qui reflètent des décalages valides. 
  
Pour plus d'informations sur le rendu d'une pièce jointe dans un message en texte brut, voir [rendu d'une pièce jointe en texte brut](rendering-an-attachment-in-plain-text.md). 
  
Pour plus d'informations sur le rendu d'une pièce jointe dans du texte mis en forme comme le format RTF, consultez la rubrique [rendu d'une pièce jointe au format RTF](rendering-an-attachment-in-rtf-text.md).
  
Certains des fournisseurs de banque de messages de propriétés incluent généralement dans un tableau de pièces jointes, car ils sont faciles à calculer ou à récupérer:
  
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

