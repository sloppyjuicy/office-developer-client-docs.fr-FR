---
title: Propriété canonique PidTagAttachDataBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataBinary
api_type:
- HeaderDef
ms.assetid: 3b0a8b28-863e-4b96-a4c0-fdb8f40555b9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1a5f8688b8ea747590cf2a2d6d5efb271aa488f8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390925"
---
# <a name="pidtagattachdatabinary-canonical-property"></a>Propriété canonique PidTagAttachDataBinary

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des données binaires de pièce jointe généralement accédées via l’interface Object Linking and Embedding (OLE) **IStream** . 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_DATA_BIN  <br/> |
|Identificateur :  <br/> |0x3701  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient la pièce jointe lorsque la valeur de la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) est ATTACH_BY_VALUE, qui est le seul doivent être pris en charge et la méthode habituelle de pièce jointe. **PR_ATTACH_DATA_BIN** contient également une pièce jointe OLE 1.0 **OLESTREAM** lorsque la valeur de **PR_ATTACH_METHOD** est ATTACH_OLE. 
  
 Pièces jointes **OLESTREAM** peuvent être copiés dans un fichier en appelant la méthode OLE **IStream::CopyTo** . Le type d’encodage OLE peut être déterminée à partir de la propriété **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Pour une pièce jointe au document OLE, le fournisseur de banque de messages doit répondre à un appel [IMAPIProp::OpenProperty](imapiprop-openproperty.md) sur **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) et peut éventuellement répondre à un appel sur **PR_ATTACH_DATA_BIN **. Notez que **PR_ATTACH_DATA_BIN** et **PR_ATTACH_DATA_OBJ** partagent le même identificateur de propriété et sont donc deux rendus de la même propriété. 
  
Pour un objet de stockage, tel qu’un fichier composé OLE 2.0 au format d’un document, certains fournisseurs de services pouvoir être ouvert avec l’interface MAPI **IStreamDocfile** pour améliorer les performances. Un fournisseur qui prend en charge **IStreamDocfile** doit exposer sur **PR_ATTACH_DATA_OBJ** et peut-être éventuellement exposer sur **PR_ATTACH_DATA_BIN**. 
  
Pour plus d’informations sur les formats et les interfaces OLE, consultez [OLE et transfert de données](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
## <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

