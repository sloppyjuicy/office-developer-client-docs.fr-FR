---
title: Propriété canonique PidTagAttachDataObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataObject
api_type:
- HeaderDef
ms.assetid: b76312c6-7682-4ded-be25-55e21b0b091b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b3fc7690a8c9eb2ada3a34bc44217ff463721e4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785704"
---
# <a name="pidtagattachdataobject-canonical-property"></a>Propriété canonique PidTagAttachDataObject

  
  
**S’applique à**: Outlook 
  
Contient un objet attachment généralement accédé via l’interface Object Linking and Embedding (OLE) **IStorage** . 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_DATA_OBJ  <br/> |
|Identificateur :  <br/> |0x3701  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Zone :  <br/> |Pièce jointe du message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient la pièce jointe lorsque la valeur de la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) est **ATTACH_EMBEDDED_MSG** ou **ATTACH_OLE**. Le type d’encodage OLE peut être déterminée à partir de **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Pour une pièce jointe associée à la valeur **ATTACH_EMBEDDED_MSG** , l’interface de [IMessage:IMAPIProp](imessageimapiprop.md) peut être utilisée pour un accès rapide. 
  
Pour un objet OLE incorporé dynamique, la propriété **PR_ATTACH_DATA_OBJ** contient ses propres informations de rendu et la propriété **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) doit être inexistant ou vide. 
  
Pour une pièce jointe au document OLE, le fournisseur de banque de messages doit répondre à un appel [IMAPIProp::OpenProperty](imapiprop-openproperty.md) sur **PR_ATTACH_DATA_OBJ** et peut éventuellement répondre à un appel sur **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md) ). Les propriétés **PR_ATTACH_DATA_BIN** et **PR_ATTACH_DATA_OBJ** partagent le même identificateur de propriété et sont donc deux rendus de la même propriété. 
  
Pour un objet de stockage, tel qu’un fichier composé OLE 2.0 au format d’un document, certains fournisseurs de services pouvoir être ouvert avec l’interface MAPI **IStreamDocfile** , une sous-classe de **IStream** sans membres supplémentaires, conçu pour optimiser les performances. L’enregistrement potentiel est suffisant pour justifier la tentative d’ouverture de **PR_ATTACH_DATA_OBJ** via **IStreamDocfile**. Si **MAPI_E_INTERFACE_NOT_SUPPORTED** est renvoyée, le client peut ensuite ouvrir **PR_ATTACH_DATA_BIN** avec **IStream**. 
  
Si l’application cliente ou un fournisseur de services ne peuvent pas ouvrir un sous-objet de pièce jointe à l’aide de **PR_ATTACH_DATA_OBJ** à l’aide de **PR_ATTACH_METHOD**, elle doit utiliser **PR_ATTACH_DATA_BIN**. 
  
Pour plus d’informations sur les formats et les interfaces OLE, consultez [OLE et transfert de données](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
## <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

