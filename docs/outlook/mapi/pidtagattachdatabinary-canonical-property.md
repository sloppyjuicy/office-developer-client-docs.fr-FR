---
title: Propriété canonique PidTagAttachDataBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachDataBinary
api_type:
- HeaderDef
ms.assetid: 3b0a8b28-863e-4b96-a4c0-fdb8f40555b9
description: Contient des données de pièces jointes binaires généralement accessibles via l’interface IStream OLE (Object Linking and Embedding).
ms.openlocfilehash: f2d9f8512440d47d2133e4976724b8c51de2f02c
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63782565"
---
# <a name="pidtagattachdatabinary-canonical-property"></a>Propriété canonique PidTagAttachDataBinary

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des données de pièces jointes binaires généralement accessibles via l’interface **IStream** OLE (Object Linking and Embedding). 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_DATA_BIN  <br/> |
|Identificateur :  <br/> |0x3701  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient la pièce jointe lorsque la valeur de la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) est ATTACH_BY_VALUE, qui est la méthode de pièce jointe habituelle et la seule à être prise en charge. **PR_ATTACH_DATA_BIN** contient également une pièce jointe OLE 1.0 **OLESTREAM** lorsque la valeur de **PR_ATTACH_METHOD est ATTACH_OLE** . 
  
 **Les pièces jointes OLESTREAM** peuvent être copiées dans un fichier en appelant la méthode OLE **IStream::CopyTo** . Le type de codage OLE peut être déterminé à partir **PR_ATTACH_TAG propriété (**[PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Pour une pièce jointe de document OLE, le fournisseur de magasin de messages doit répondre à un appel [IMAPIProp::OpenProperty](imapiprop-openproperty.md) sur **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) et peut éventuellement répondre à un appel sur **PR_ATTACH_DATA_BIN**. Notez **que PR_ATTACH_DATA_BIN** et **PR_ATTACH_DATA_OBJ** partagent le même identificateur de propriété et sont donc deux rendus de la même propriété. 
  
Pour un objet de stockage, tel qu’un fichier composé au format docfile OLE 2.0, certains fournisseurs de services lui permettent d’être ouvert avec l’interface MAPI **IStreamDocfile** pour améliorer les performances. Un fournisseur qui prend **en charge IStreamDocfile** doit l’exposer sur **PR_ATTACH_DATA_OBJ** et peut éventuellement l’exposer **sur PR_ATTACH_DATA_BIN**. 
  
Pour plus d’informations sur les interfaces et les formats OLE, voir [OLE et Transfert de données](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
## <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

