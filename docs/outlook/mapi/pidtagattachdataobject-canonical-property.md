---
title: Propriété canonique PidTagAttachDataObject
description: Décrit la propriété canonique PidTagAttachDataObject, qui contient un objet pièce jointe généralement accessible via l’interface OLE IStorage.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachDataObject
api_type:
- HeaderDef
ms.assetid: b76312c6-7682-4ded-be25-55e21b0b091b
ms.openlocfilehash: 63859815a6d7960cc7e5039f7db3f6df5658f8ac
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812508"
---
# <a name="pidtagattachdataobject-canonical-property"></a>Propriété canonique PidTagAttachDataObject

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un objet pièce jointe généralement accessible via l’interface **IStorage** OLE (Object Linking and Embedding). 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_DATA_OBJ  <br/> |
|Identificateur :  <br/> |0x3701  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient la pièce jointe lorsque la valeur de la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) est **ATTACH_EMBEDDED_MSG** ou **ATTACH_OLE**. Le type d’encodage OLE peut être déterminé à partir de **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Pour une pièce jointe associée à la valeur **ATTACH_EMBEDDED_MSG** , l’interface [IMessage:IMAPIProp](imessageimapiprop.md) peut être utilisée pour un accès plus rapide. 
  
Pour un objet OLE dynamique incorporé, la propriété **PR_ATTACH_DATA_OBJ** contient ses propres informations de rendu, et la propriété **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) doit être inexistante ou vide. 
  
Pour une pièce jointe de fichier de document OLE, le fournisseur de magasin de messages doit répondre à un appel [IMAPIProp::OpenProperty](imapiprop-openproperty.md) sur **PR_ATTACH_DATA_OBJ** et peut éventuellement répondre à un appel sur **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)). Les propriétés **PR_ATTACH_DATA_BIN** et **PR_ATTACH_DATA_OBJ** partagent le même identificateur de propriété et sont donc deux rendus de la même propriété. 
  
Pour un objet de stockage, tel qu’un fichier composé au format docfile OLE 2.0, certains fournisseurs de services permettent de l’ouvrir avec l’interface **MAPI IStreamDocfile** , une sous-classe **d’IStream** sans membre supplémentaire, conçue pour optimiser les performances. L’économie potentielle est suffisante pour justifier la tentative d’ouverture **de PR_ATTACH_DATA_OBJ** via **IStreamDocfile**. Si **MAPI_E_INTERFACE_NOT_SUPPORTED** est retourné, le client peut alors ouvrir **PR_ATTACH_DATA_BIN** avec **IStream**. 
  
Si l’application cliente ou le fournisseur de services ne peut pas ouvrir un sous-objet de pièce jointe à l’aide de **PR_ATTACH_DATA_OBJ** à l’aide de **PR_ATTACH_METHOD**, il doit utiliser **PR_ATTACH_DATA_BIN**. 
  
Pour plus d’informations sur les interfaces et formats OLE, consultez [OLE et Transfert de données](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
## <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

